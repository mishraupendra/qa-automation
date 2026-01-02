
# QA Automation — Playwright (Web), Appium (Mobile), REST Assured (API) + GitHub Actions

This repository demonstrates:
- **Web E2E**: Playwright (TypeScript)
- **Mobile E2E**: Appium (Android via WebdriverIO, CI emulator runner)
- **API tests**: REST Assured (Java)
- **CI/CD**: GitHub Actions with browser/device matrix, parallel shards, artifacts, and a **quality gate** for failures/flakiness

## Quick start (local)
```bash
npm ci
npx playwright install --with-deps
npm run test:web        # run Playwright
npm run test:web:report # open Playwright HTML report

# API tests (REST Assured, Java)
# Set base URL of target app
export BASE_URL=https://example.com
mvn -q -f api-tests/pom.xml test

# Appium (Android)
# Requires an emulator/device and Appium server (local or cloud)
npx appium &
npm run test:appium:android
