# LaborIA Dash — Backoffice Técnico Central

Repositorio de la **Dashboard Técnica** de LaborIA: soporte global, auditoría, reportería y analítica de negocio para el equipo 4B.

## Ecosistema LaborIA

| Repo | GitHub | Descripción |
|---|---|---|
| **LaborIA_Back** | https://github.com/4Bprogramming/LaborIA_Back | API NestJS + Prisma (`/api/v1/admin/*`) |
| **LaborIA_Front** | https://github.com/4Bprogramming/LaborIA_Front | App tenant + rutas `(admin)/backoffice/*` |
| **LaborIA_Dash** | https://github.com/4Bprogramming/LaborIA_Dash | Este repo — workspace y evolución del backoffice |

## Documentación

Ver [`../docs/Dash-Tecnica-0000-Infraestructura-Backoffice-Central.md`](../docs/Dash-Tecnica-0000-Infraestructura-Backoffice-Central.md) en el monorepo local.

## Estado actual (v0.1.0)

Cimientos implementados:

- Modelos Prisma: `AdminRole`, `UsuarioAdministrador`, `LogAuditoriaTecnica`
- Endpoints admin protegidos con `AdminAuthGuard`
- UI base en Front: sidebar corporativo y rutas `/backoffice/*`

## Desarrollo local

```bash
# Backend
cd ../BACK
npm install
npx prisma migrate dev
npm run start:dev

# Frontend (incluye backoffice)
cd ../Front
npm install
npm run dev
```

Backoffice: http://localhost:3001/backoffice/login

## Licencia

Propiedad de 4B Programming — uso interno LaborIA.
