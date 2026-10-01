# Component 4 — Quality Inspection & Non-Conformance Management
**Student:** Anoja
**Your primary ownership:** Quality inspections, inspection items, non-conformances, QualityRiskAnalysisAgent

## What you submit
- ackend/BuildWise.Api/Controllers/QualityInspectionsController.cs — your main controller
- ackend/agent_service/quality_agent.py — your Python AI agent (port 8004, most complex)
- ackend/BuildWise.Api.Tests/QualityInspectionServiceTests.cs — your unit tests
- web/buildwise-web/src/pages/QualityInspectionsPage.jsx + NonConformancesPage.jsx
- web/buildwise-web/src/Features/quality/ — all quality React components
- mobile/.../features/quality/ — your Flutter screens
- docs/reports/IT24XXXXX-Anoja-ai-usage-log.md — your AI usage log

## Run & verify
```powershell
powershell -File scripts/start-dev.ps1
powershell -File scripts/verify-component4.ps1
```

## Test your component
```powershell
dotnet test backend/BuildWise.Api.Tests/BuildWise.Api.Tests.csproj --filter "Quality"
cd backend/agent_service && pytest test_quality_agent.py -v
cd web/buildwise-web && npm test -- --run --reporter verbose
```

## Install APK on Android phone
1. Enable "Install unknown apps" on your phone
2. Transfer mobile/.../flutter-apk/app-release.apk and install
3. API at http://10.110.168.34:5078 (PC must be on same WiFi)
