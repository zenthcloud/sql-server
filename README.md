# Zenth SQL Server (ZQL)

**Zenth SQL Server (ZQL)** is a high-performance, secure, and cloud-native relational database engine, forked from [PostgreSQL](https://www.postgresql.org/). Developed by the Zenth Cloud team, ZQL is designed to power our next-generation European cloud infrastructure with full sovereignty, performance optimization, and seamless integration with our ecosystem.

> ✨ ZQL is the SQL backbone of **Zenth Cloud**, enabling secure, isolated, and scalable data storage for our clients and internal services.

---

## 🔍 What is ZQL?

ZQL is a customized fork of PostgreSQL, tailored for:

- **Cloud-native deployments** with tight integration into the [Zenth Cloud Panel](https://panel.zenthcloud.com)
- **Multi-tenant architectures**, where each enterprise/customer has its own isolated database environment
- **Enhanced monitoring**, backup, and failover tools natively embedded
- **Custom authentication** (linked to Zenth Cloud accounts and IAM policies)
- **Simplified provisioning** for hosted services such as web apps, mail servers, and internal systems

---

## 🚀 Key Features

- 🛡️ **Security-First**: Hardened by default, with modern TLS, internal-only binding options, and strict user management.
- 📈 **Performance-Tuned**: Optimized for running on Zenth Cloud Proxmox-based nodes with smart caching and I/O.
- 🔄 **Built-in Replication**: Future-ready for native HA and Geo-replication (ZQL Cluster Edition).
- 🧩 **Plugin-Ready**: Still compatible with many PostgreSQL extensions (with some verification).
- 🔧 **Panel Integration**: Fully manageable through Zenth Panel for admin-free experience.

---

## 🧪 Status

| Component           | Status       |
|---------------------|--------------|
| Fork & Rename Base  | ✅ Completed |
| Build System        | ✅ Stable    |
| Initial ZQL Release | ✅ v1.0.0    |
| Zenth Panel Support | 🛠️ In Progress |
| HA Clustering       | 🔜 Planned   |

---

## 📦 Installation

ZQL is distributed as a standalone binary (`zql`), container image (`zenth/zql`), or Debian package (`zql-server`).

### Docker (Preview)

```bash
docker run -d \
  --name zql \
  -e POSTGRES_USER=admin \
  -e POSTGRES_PASSWORD=yourpassword \
  -p 5432:5432 \
  zenthcloud/zql:latest
````

### Native Build (Linux)

```bash
git clone https://github.com/zenthcloud/sql-server.git
cd sql-server
make
sudo make install
```

> Note: You can run ZQL side-by-side with PostgreSQL (binary name is `zql`).

---

## 🤝 Compatibility

* **PostgreSQL 16.x based**
* Compatible with most standard PostgreSQL drivers (psycopg, pgAdmin, JDBC, etc.)
* Migration from PostgreSQL → ZQL is seamless (via pg\_dump/restore)

---

## 📚 Documentation

ZQL documentation is coming soon. Until then, refer to the PostgreSQL 16 documentation for most behavior.

---

## 👥 Contributors

ZQL is maintained by the [Zenth Cloud](https://zenthcloud.com) core infrastructure team, part of **Sky Genesis Enterprise**.

---

## 🌐 Learn More

* 🔗 Website: [https://zenthcloud.com](https://zenthcloud.com)
* 💬 Community: Coming soon
* 🛠️ Zenth Cloud Panel: Web interface for managing databases, services & infrastructure

---

## 📌 Vision

ZQL is part of our mission to build a **fully sovereign, European, cloud-native platform** that empowers individuals, startups, and enterprises with privacy, performance, and freedom of deployment.

## 🛡️ License

ZQL is released under the **PostgreSQL License**, following the terms of the upstream project.

---