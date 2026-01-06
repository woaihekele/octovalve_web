# Octovalve 文案草案 / Messaging Draft

## 一句话定位 / One-liner
面向大模型工具调用的远程命令代理：模型只连本地 MCP stdio，经 SSH 隧道转发到远端审批执行并回传结果。  
A remote command broker for LLM tooling: models connect only to local MCP stdio, requests are tunneled to a
remote broker for human approval and execution.

## 价值主张 / Value
- 更安全：先审批，再执行；策略与限制可控。  
  Safer by design: approve before execution, with enforceable policies and limits.
- 更可审计：完整请求、输出与审计日志留痕。  
  Auditable by default: every request, output, and audit log is persisted.
- 更易扩展：多目标统一接入，控制面可聚合状态。  
  Scales to multiple targets with a consolidated control plane.

## 核心能力 / Core Capabilities
- 本地 MCP 代理：`octovalve-proxy` 提供 `run_command`/`list_targets`，标准化工具入口。  
  Local MCP proxy: `octovalve-proxy` exposes `run_command`/`list_targets` as a unified tool entry.
- 远端审批执行：`remote-broker` 在 TUI 中人工确认后执行命令并返回结果。  
  Remote approval & execution: `remote-broker` requires manual approval in TUI before running commands.
- 控制与同步：`console` 自动同步/启动远端 broker，聚合多目标状态并提供 HTTP API。  
  Control & sync: `console` bootstraps remote brokers, aggregates target status, and serves an HTTP API.
- 内置隧道管理：代理与控制服务自动维护 SSH 隧道。  
  Built-in tunnels: SSH tunnels are maintained automatically by proxy and console.
- 策略与限制：白名单/黑名单、参数规则、超时与输出大小限制，支持 `argv`/`shell` 模式。  
  Policy & limits: allow/deny lists, argument rules, timeouts, output caps, `argv`/`shell` modes.
- 审计留痕：请求/结果与 stdout/stderr 落盘，审计日志可追溯。  
  Audit trail: request/result plus stdout/stderr are persisted with audit logs.

## 工作流程 / Workflow
1) MCP 客户端调用本地 `octovalve-proxy` 的 `run_command`。  
2) 代理通过 SSH 隧道转发给远端 `remote-broker`。  
3) 远端审批后执行并回传结果。  

1) MCP client calls `run_command` on local `octovalve-proxy`.  
2) The proxy forwards via SSH tunnel to `remote-broker`.  
3) The broker approves, executes, and returns results.

## 安全与审计 / Security & Audit
- 远端默认监听 `127.0.0.1`，仅通过 SSH 隧道访问。  
- `intent` 字段用于记录执行意图，结合审计日志形成链路。  
- 可只开放只读白名单，降低风险。  

- Brokers bind to `127.0.0.1` by default and are accessed via SSH tunnels.  
- The `intent` field records execution intent and supports audit trails.  
- Read-only allowlists can be enforced for safer operation.

## 适用场景 / Use Cases
- 需要“可审批、可追溯”的远程命令执行。  
- 多机/多环境统一审批与执行入口。  
- 对输出与历史记录有合规要求的自动化流程。  

- Remote command execution with approval and traceability.  
- Unified approval/execution across multiple machines.  
- Automation workflows with compliance-grade logging.
