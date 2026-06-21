# LaborIA Dash — Backoffice Técnico Central

Repositorio de la **Dashboard Técnica** de LaborIA: soporte global, auditoría, reportería y analítica de negocio para el equipo 4B.

## Ecosistema LaborIA

| Repo | GitHub | Descripción |
|---|---|---|
| **LaborIA_Back** | https://github.com/4Bprogramming/LaborIA_Back | API NestJS + Prisma (`/api/v1/admin/*`) |
| **LaborIA_Front** | https://github.com/4Bprogramming/LaborIA_Front | App tenant + rutas `(admin)/backoffice/*` |
| **LaborIA_Dash** | https://github.com/4Bprogramming/LaborIA_Dash | Este repo — workspace y evolución del backoffice |

## Documentación

| Doc | Contenido |
|---|---|
| [Dash-Tecnica-0000](../docs/Dash-Tecnica-0000-Infraestructura-Backoffice-Central.md) | Cimientos backoffice |
| [Dash-Tecnica-0001](../docs/Dash-Tecnica-0001-Facturacion-Monitor-Convenios.md) | Facturación SaaS + monitor CCT |

## Estado actual (v0.2.0)

Implementado:

- Modelos: `FacturaEstudio`, `TenantEstadoComercial`, auditoría crawler en `Convenio`
- Endpoints: facturación, webhook pagos, convenios-maestros + historial
- Cron billing (vencimientos) y actualización `estadoCrawler` en crawler paritario
- UI: `/backoffice/facturacion` y monitor en `/backoffice/convenios`

Cimientos v0.1.0:

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
