# VictoryCenter — Local Setup

## Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop/) installed and running

## Steps

**1. Clone the repo**
```bash
git clone --recurse-submodules https://github.com/Pichus/VictoryCenter-DevOps.git
cd VictoryCenter-DevOps
```

**2. Create your env file**
```bash
cp .env.example .env
```
No changes needed — the default values work out of the box.

**3. Start everything**
```bash
docker compose up --build
```
First run takes ~5–10 minutes (builds frontend and backend from source).

**4. Open the app**

| Service | URL |
|---------|-----|
| Frontend | http://localhost:3000 |
| Backend API | http://localhost:8080/api |

Admin login credentials are in `.env` → `INITIAL_ADMIN_EMAIL` / `INITIAL_ADMIN_PASSWORD`.

## Stopping

```bash
docker compose down
```

To also delete the database volume (full reset):
```bash
docker compose down -v
```

---

## Updating to latest code

```bash
git pull
git submodule update --remote --merge
docker compose up --build
```

## Submodules

| Folder | Repo |
|--------|------|
| `VictoryCenter-Client` | [Frontend](https://github.com/ita-social-projects/VictoryCenter-Client) |
| `VictoryCenter-Back` | [Backend](https://github.com/ita-social-projects/VictoryCenter-Back) |
