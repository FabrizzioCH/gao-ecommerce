# e-Commerce Grupo Acero Ocotepec

Monorepo con dos proyectos independientes:

- **`backend/`** — API en Spring Boot (Java)
- **`frontend/`** — SPA en React + Vite + TypeScript

## Versiones utilizadas

### Backend

| Herramienta | Versión | Notas |
|---|---|---|
| **Java (JDK)** | **25** | Obligatorio. Un JDK menor no compila. |
| Spring Boot | 4.1.0 | Definido en `backend/pom.xml` (parent). |
| Maven | 3.9.16 | Vía wrapper (`mvnw` / `mvnw.cmd`). **No** hace falta instalar Maven. |
| Maven Wrapper | 3.3.4 | `distributionType=only-script`. |

### Frontend

| Herramienta | Versión | Notas |
|---|---|---|
| **Node.js** | **>= 20** (recomendado 24 LTS) | Los tipos apuntan a `@types/node` 24. |
| **Gestor de paquetes** | **pnpm** (lockfile v9 → pnpm 9.x) | **Usar pnpm, no npm/yarn.** Hay `pnpm-lock.yaml` commiteado. |
| React / React DOM | 19.2 | |
| Vite | 8.1 | |
| TypeScript | 6.0 | |
| ESLint | 10.x | Flat config (`eslint.config.js`). |

## Puesta en marcha

### Backend (Spring Boot)

```powershell
cd backend
.\mvnw.cmd spring-boot:run      # Windows / PowerShell
./mvnw spring-boot:run          # macOS / Linux
```

### Frontend (React + Vite)

```bash
cd frontend
pnpm install       # instalar dependencias (respeta pnpm-lock.yaml)
pnpm dev           # servidor de desarrollo con HMR
pnpm build         # type-check (tsc -b) + build de producción
pnpm lint          # ESLint
pnpm preview       # servir el build de producción
```