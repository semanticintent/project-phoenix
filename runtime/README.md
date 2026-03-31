# Phoenix Runtime

The Phoenix Runtime has its own dedicated repository.

**→ https://github.com/semanticintent/phoenix-runtime**

```
npm install @semanticintent/phoenix-runtime
```

## What It Does

CLI orchestration layer for the seven-agent Phoenix pipeline.
Manages `.sil` artifact state, enforces human gates, injects
episode context, produces agent prompts ready to run in any
AI interface.

## Quick Reference

```bash
phoenix init my-project
phoenix run a-00
phoenix status
phoenix gate pass-1 --approve
phoenix episode new
phoenix run a-06
```

## Documentation

Full architecture, module design, and build sequence:
[phoenix-runtime/README.md](https://github.com/semanticintent/phoenix-runtime/blob/main/README.md)

---

*Runtime moved to dedicated repo March 2026.*
*This file is a pointer only.*
