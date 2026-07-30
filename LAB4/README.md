              ┌───────────────────────┐
              │      Developer        │
              │  Code + Git Commit    │
              └──────────┬────────────┘
                         │
                         ▼
              ┌───────────────────────┐
              │     GitHub Repository │
              │ Push / Pull Request   │
              └──────────┬────────────┘
                         │
                         ▼
              ╔════════════════════════════════════╗
              ║         GitHub Actions (CI)        ║
              ╠════════════════════════════════════╣
              ║ ✓ Checkout Repository              ║
              ║ ✓ Setup Python Environment         ║
              ║ ✓ Install Dependencies             ║
              ║ ✓ Run Linting (Code Quality)       ║
              ║ ✓ Execute Unit Tests               ║
              ║ ✓ Build Application                ║
              ║ ✓ Generate Build Artifact          ║
              ╚════════════════════════════════════╝
                         │
                         ▼
              ╔════════════════════════════════════╗
              ║          Continuous Delivery       ║
              ╠════════════════════════════════════╣
              ║ Deploy → Development Environment   ║
              ║            │                       ║
              ║            ▼                       ║
              ║ Execute Integration Tests          ║
              ║            │                       ║
              ║            ▼                       ║
              ║ Deploy → Testing Environment       ║
              ║            │                       ║
              ║            ▼                       ║
              ║ Manual Approval (Optional)         ║
              ║            │                       ║
              ║            ▼                       ║
              ║ Deploy → Production                ║
              ╚════════════════════════════════════╝
                         │
                         ▼
              ┌───────────────────────┐
              │  Monitoring & Logs    │
              │ Alerts • Health Check │
              └───────────────────────┘
