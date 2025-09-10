# HareOps 🐇

![HareOps Logo](https://dummyimage.com/600x200/000/fff\&text=HareOps+Logo)

> **Fast insight, calm RabbitMQ.**
>
> HareOps là một **GUI thế hệ mới** để quan sát và vận hành RabbitMQ. Thiết kế để nhanh, đẹp, insight-first: từ metrics, logs, traces đến DLQ explorer và flow map.

---

## ✨ Tính năng chính

* **Ops Home / Pulse**: trạng thái cluster, top hot queues, SLO error budget.
* **Flow Map (HareLens)**: trực quan hóa Exchange → Queue → Consumer với throughput, latency, redelivery.
* **Queue Health**: điểm số 0–100, prefetch tuner, backlog/unacked insight.
* **DLQ Explorer (HareBurrow)**: nhóm theo reason/routing key, xem sample, replay an toàn.
* **Tracing Bridge**: nhảy từ queue sang distributed trace.
* **Alert pack & runbooks**: cảnh báo có hướng dẫn xử lý.
* **Quorum & topology diff**: thấy leader, lag, thay đổi cấu hình.

---

## 🚀 Chạy nhanh

### Web SPA (Next.js, không SSR)

```bash
pnpm i
pnpm --filter @hareops/web dev
```

Truy cập [http://localhost:3000](http://localhost:3000).

### Desktop (Tauri + Next.js)

```bash
pnpm --filter @hareops/desktop tauri dev
```

Mở ứng dụng native cửa sổ riêng.

### Build production desktop

```bash
pnpm --filter @hareops/web build && pnpm --filter @hareops/web export
pnpm --filter @hareops/desktop tauri build
```

---

## 📦 Cấu trúc thư mục

```
hareops/
├─ apps/
│  ├─ web/         # Next.js SPA
│  └─ desktop/     # Tauri wrapper
├─ packages/
│  └─ ui/          # UI kit (shadcn/tailwind)
└─ README.md
```

---

## 🔌 Nhúng vào Backstage

* **IframeCard**: nhanh nhất.
* **Plugin frontend**: native routing/theme.
* **Backend proxy**: bảo mật, RBAC, API mediation.

Xem docs trong `docs/backstage.md`.

---

## 🛠️ Công nghệ

* **Next.js (SPA)** + Tailwind + shadcn/ui
* **Tauri** để build desktop native (macOS/Win/Linux)
* **TanStack Query** cho data layer
* **Prometheus + OpenTelemetry** integration

---

## 🧭 Roadmap

* [ ] Flow Map realtime với visx/d3
* [ ] Prefetch auto-tune loop
* [ ] Stream & federation support
* [ ] Canary publisher/consumer
* [ ] Mobile read-only app

---

## 📜 License

MIT © HareOps Team
