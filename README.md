# ALICE-Motion SaaS

Procedural motion control — trajectory equation API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-Motion |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/plan` | 軌道計画 |
| `POST /api/v1/execute` | モーション実行 |
| `GET  /api/v1/profiles` | モーションプロファイル一覧 |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
