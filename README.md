**I turn business problems into production software.**

Head of Development at a telecom and smart-home operator, founder of [84softworks](https://84softworks.com).
Business goals become products through architecture, team and process – a team of six under my lead,
eleven products in production, most of them still carrying load today.

### Building now

**[ThunderVox](https://github.com/beiroun/thundervox)** – a SIP endpoint platform for devices standing at
physical points: intercom panels, elevators, gates, SOS posts. Kamailio for signaling, rtpengine for media,
push-wait at the core.

The hard part was never the PBX. Asterisk, FreeSWITCH and Kamailio are raw material – free, worn smooth,
and none of them solve the one thing this niche is built on: a call from a panel has to reach a phone that
is asleep. Park the transaction, wake the device with a push, resume it on REGISTER, keep two-way audio and
panel video alive with both legs behind NAT – and speak the private SIP dialect of every hardware vendor
along the way. That layer is the product; everyone else writes it themselves and burns out on it.

Designed against a live field of 5,000 panels over a directory of 500,000 numbers, where an offline
subscriber is a row in a table rather than a registration.

### Shipped

- **AI call analytics** – transcription, diarization, sentiment, 24 marketing signals, a RAG assistant and
  automatic ticketing. 250K+ calls and 18K+ chats processed. The whole model stack fits on two consumer
  GPUs (RTX 3080 + 4080 Super, under $2,700 of hardware): a Spring router fanning work out to parallel
  Python workers.
- **Consumer app for intercoms, cameras and access control** – 500K+ users, 200K MAU, native Android and
  iOS, Wear and watchOS, voice assistants. The platform behind it covers ~5,000 intercoms and ~20,000 cameras.
- **Field service platform** – rewritten from scratch; remote billing databases separated from operational
  ones with scheduled batch replication, so screens that used to crawl now answer instantly.
  1.5M+ service requests, 14M+ payment records.
- **In-house messenger** – operator and client applications, attachments, surveys, real-time delivery.
- **The infrastructure under all of it** – bare-metal Kubernetes (kubeadm, Longhorn, Flannel), a monolith
  split into microservices behind a custom API gateway and auth service, Kafka as the single concurrency
  mechanism, self-hosted GitLab, CI, tracker and chat, automated TLS and backups.

### Stack

```
Backend     Kotlin · Spring Boot · PHP/Symfony · PostgreSQL · MS SQL · Redis · Kafka · Flyway
Mobile      Android (Kotlin/Java) · iOS (Swift, Objective-C++) · React Native · Wear · watchOS
AI          Qwen3 · LLaMA 3.1 · BERT · embeddings · RAG · transcription · diarization, self-hosted
Telephony   Kamailio · rtpengine · Asterisk/FreePBX · SIP · RTP · RTSP · VoIP push
Infra       Kubernetes on bare metal · Docker · GitLab CI · Linux · networking
```

### Background

M.Sc. with honours, artificial intelligence in power engineering (2025) – the thesis became the call
analytics platform above and went into production. B.Sc. with honours in software engineering.
Commercial work since the first year of university; a development team under me since 23.

### Why this profile is quiet

Most of what is listed here belongs to the company that paid for it: it runs, it holds load, and it is not
mine to publish. What is public is my own, starting with ThunderVox.

### Elsewhere

- [84softworks.com](https://84softworks.com) – the company, the flagship, the numbers
- [x.com/beiroun_stderr](https://x.com/beiroun_stderr) – build log, English
- [t.me/beiroun_stderr](https://t.me/beiroun_stderr) – build log, Russian
- [LinkedIn](https://www.linkedin.com/in/andrei-baranov-173993419)
- 84softworks@gmail.com

*Logs, not lectures.*
