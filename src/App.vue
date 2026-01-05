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
          <a href="#providers">Providers</a>
          <a href="#download">Download</a>
          <a href="#docs">Docs</a>
          <a href="#changelog">Changelog</a>
        </div>
        <div class="nav-actions">
          <button class="btn ghost">Sign in</button>
          <button class="btn primary">Get started</button>
        </div>
      </nav>
    </header>

    <main>
      <section class="hero">
        <div class="hero-badge">
          <span class="badge-icon" aria-hidden="true"></span>
        </div>
        <h1>Elegant AI Provider Orchestration</h1>
        <p class="subtitle">
          A modern desktop console that unifies providers, tools, and memory into a clean, responsive workflow.
          Switch models instantly and keep the conversation in one place.
        </p>
        <div class="hero-actions">
          <button class="btn primary">Download for macOS</button>
          <button class="btn secondary">View documentation</button>
        </div>
        <div class="preview-card">
          <img src="/hero-screenshot.png" alt="Octovalve hero preview" />
        </div>
      </section>

      <section id="features" class="section">
        <div class="section-header">
          <p class="eyebrow">Powered Features</p>
          <h2>Everything you need to run multi-provider workflows</h2>
          <p class="section-subtitle">
            Octovalve keeps every model, tool, and context in sync so you can focus on the tasks that matter.
          </p>
        </div>

        <div class="feature">
          <div class="feature-text">
            <h3>Beautiful Chat Interface</h3>
            <p>
              A fast, focused console designed for daily use. Keep multi-step reasoning, streaming responses, and
              tool output organized in one timeline.
            </p>
          </div>
          <div class="shot">
            <img src="/feature-chat.png" alt="Chat interface preview" />
          </div>
        </div>

        <div class="feature reverse">
          <div class="feature-text">
            <h3>Intelligent Memory</h3>
            <p>
              Persist context across sessions with layered memories. Capture preferences, project details, and
              provider-specific settings without repeating yourself.
            </p>
          </div>
          <div class="shot">
            <img src="/feature-memory.png" alt="Memory preview" />
          </div>
        </div>

        <div class="feature">
          <div class="feature-text">
            <h3>Memory Management</h3>
            <p>
              Review, edit, and tune memory items before they are committed. Keep long-term context clean and
              aligned with your policies.
            </p>
          </div>
          <div class="shot">
            <img src="/feature-management.png" alt="Memory management preview" />
          </div>
        </div>

        <div class="feature reverse">
          <div class="feature-text">
            <h3>Web Search Integration</h3>
            <p>
              Gather current context without leaving the console. Pull in citations, URLs, and summaries in the
              same chat thread.
            </p>
          </div>
          <div class="shot">
            <img src="/feature-search.png" alt="Search integration preview" />
          </div>
        </div>

        <div class="feature">
          <div class="feature-text">
            <h3>Advanced Tool Use</h3>
            <p>
              Launch commands, manage approvals, and review outputs in one place. Designed for secure, auditable
              tool execution.
            </p>
          </div>
          <div class="shot">
            <img src="/feature-tools.png" alt="Tooling preview" />
          </div>
        </div>
      </section>

      <section id="providers" class="section muted">
        <div class="section-header centered">
          <p class="eyebrow">Supported Providers</p>
          <h2>Bring your preferred models and stacks</h2>
        </div>
        <div class="provider-grid">
          <div class="provider-card">OpenAI</div>
          <div class="provider-card">Anthropic</div>
          <div class="provider-card">Google</div>
          <div class="provider-card">Mistral</div>
          <div class="provider-card">Azure</div>
          <div class="provider-card">Custom</div>
        </div>
      </section>

      <section id="download" class="section">
        <div class="section-header centered">
          <p class="eyebrow">Download</p>
          <h2>Pick the build for your workstation</h2>
          <p class="section-subtitle">Replace these cards with platform-specific download links when ready.</p>
        </div>
        <div class="download-grid">
          <div class="download-card">
            <h3>macOS</h3>
            <p>Universal build for Apple Silicon and Intel.</p>
            <button class="btn secondary">Download .dmg</button>
          </div>
          <div class="download-card">
            <h3>Windows</h3>
            <p>Signed installer with automatic updates.</p>
            <button class="btn secondary">Download .exe</button>
          </div>
          <div class="download-card">
            <h3>Linux</h3>
            <p>AppImage and .deb packages available.</p>
            <button class="btn secondary">Download .AppImage</button>
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
          <p class="footer-note">Secure orchestration for modern AI workflows.</p>
        </div>
        <div class="footer-links">
          <a id="docs" href="#">Documentation</a>
          <a href="#">GitHub</a>
          <a id="changelog" href="#">Changelog</a>
          <a href="#">Privacy</a>
        </div>
      </div>
    </footer>
  </div>
</template>
