<template>
  <div>
    <header class="site-header">
      <nav class="nav">
        <div class="logo">
          <span class="logo-mark" aria-hidden="true"></span>
          <span class="logo-text">Octovalve</span>
        </div>
        <div class="nav-links">
          <a href="#features">Features</a>
          <a href="#providers">Targets</a>
          <a href="#download">Download</a>
        </div>
        <div class="nav-actions">
          <button class="btn ghost">GitHub</button>
          <button class="btn primary">Build from Source</button>
        </div>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div class="hero-badge">
          <span class="badge-icon" aria-hidden="true"></span>
        </div>
        <h1>Approved Remote Command Orchestration</h1>
        <p class="subtitle">
          Route model tool calls through a local MCP proxy and SSH tunnels.
          Every command is approved, policy-checked, and fully audited before it runs.
        </p>
        <div class="hero-actions">
          <button class="btn primary">Build from Source</button>
          <button class="btn secondary">See Quickstart</button>
        </div>
        <div class="preview-card">
          <img src="/hero-screenshot.png" alt="Octovalve console preview" />
        </div>
      </section>

      <section id="features" class="section">
        <div class="section-header">
          <p class="eyebrow">Core Capabilities</p>
          <h2>Everything you need for controlled remote execution</h2>
          <p class="section-subtitle">
            Keep operators in the loop while the model works across multiple targets.
          </p>
        </div>

        <div class="feature">
          <div class="feature-text">
            <h3>MCP Command Gateway</h3>
            <p>
              Expose `run_command` locally and forward requests to remote brokers without exposing SSH to the model.
            </p>
          </div>
          <div class="shot">
            <img src="/feature-chat.png" alt="Command gateway preview" />
          </div>
        </div>

        <div class="feature reverse">
          <div class="feature-text">
            <h3>Human-in-the-loop Approval</h3>
            <p>
              Review intent, command, and target in the TUI, then approve or deny with a single key.
            </p>
          </div>
          <div class="shot">
            <img src="/feature-memory.png" alt="Approval workflow preview" />
          </div>
        </div>

        <div class="feature">
          <div class="feature-text">
            <h3>Policy & Limits</h3>
            <p>
              Allow/deny lists, argument rules, timeouts, and output caps protect production hosts.
            </p>
          </div>
          <div class="shot">
            <img src="/feature-management.png" alt="Policy configuration preview" />
          </div>
        </div>

        <div class="feature reverse">
          <div class="feature-text">
            <h3>SSH Tunnel Automation</h3>
            <p>
              Built-in tunnel management keeps data and control channels stable across reconnects.
            </p>
          </div>
          <div class="shot">
            <img src="/feature-search.png" alt="Tunnel status preview" />
          </div>
        </div>

        <div class="feature">
          <div class="feature-text">
            <h3>ACP Client Integration</h3>
            <p>
              Connect to ACP-compatible agents over stdio with standardized handshake, auth, and session control.
            </p>
          </div>
          <div class="shot">
            <img src="/feature-tools.png" alt="ACP client integration preview" />
          </div>
        </div>
      </section>

      <section id="providers" class="section muted">
        <div class="section-header centered">
          <p class="eyebrow">Targets & Integrations</p>
          <h2>Connect the environments you already run</h2>
        </div>
        <div class="provider-grid">
          <div class="provider-card">Linux Servers</div>
          <div class="provider-card">macOS Hosts</div>
          <div class="provider-card">SSH</div>
          <div class="provider-card">MCP Clients</div>
          <div class="provider-card">TUI Approvals</div>
          <div class="provider-card">HTTP Control API</div>
        </div>
      </section>

      <section id="download" class="section">
        <div class="section-header centered">
          <p class="eyebrow">Download</p>
          <h2>Build the stack that matches your workflow</h2>
          <p class="section-subtitle">All components are Rust binaries and can be built locally with Cargo.</p>
        </div>
        <div class="download-grid">
          <div class="download-card">
            <h3>Local Proxy</h3>
            <p>MCP stdio server that routes `run_command` to remote brokers.</p>
            <button class="btn secondary">Build octovalve-proxy</button>
          </div>
          <div class="download-card">
            <h3>Remote Broker</h3>
            <p>TUI approval service that executes commands and writes audit logs.</p>
            <button class="btn secondary">Build remote-broker</button>
          </div>
          <div class="download-card">
            <h3>Console Control</h3>
            <p>Bootstraps brokers, aggregates targets, and exposes the control API.</p>
            <button class="btn secondary">Build console</button>
          </div>
        </div>
      </section>
    </main>

    <footer class="site-footer">
      <div class="footer-content">
        <div>
          <div class="logo">
            <span class="logo-mark" aria-hidden="true"></span>
            <span class="logo-text">Octovalve</span>
          </div>
          <p class="footer-note">Approved remote execution for modern AI workflows.</p>
        </div>
        <div class="footer-links">
          <a href="#features">Features</a>
          <a href="#providers">Targets</a>
          <a href="#download">Download</a>
          <a href="#">GitHub</a>
        </div>
      </div>
    </footer>
  </div>
</template>
