# poc-lab

> 近期披露的高严重性漏洞的 PoC 与复现脚本。

聚焦于**最新的、有影响力的 CVE** —— Linux 内核、Windows、macOS、容器、服务等领域。

[English](./README.md) | **中文**

## 内容说明

每个漏洞目录遵循一致的布局：

| 文件 | 用途 |
|------|------|
| `exploit.py` / `exploit.sh` | PoC 脚本 |
| `README.md` | CVE 信息、受影响版本、复现步骤、参考资料 |

## 目录结构

```
poc-lab/
├── CVE-2026-XXXXX/       # 每个 CVE 一个目录
│   ├── exploit
│   ├── build
│   └── README.md
├── VULN-NAME/            # 如无 CVE 编号，使用漏洞名称
│   ├── exploit.sh
│   └── README.md
└── ...
```

目录按 **CVE 编号** 组织（如 `CVE-2026-31431/`）。若漏洞暂无 CVE 编号，则使用公开名称（如 `RedSun/`、`YellowKey/`）。

浏览仓库根目录即可查看所有可用 PoC —— 随着新漏洞的披露与复现，列表会持续增长。

## 快速开始

```bash
# 克隆仓库
git clone https://github.com/Unclecheng-li/poc-lab.git
cd poc-lab

# 选择一个漏洞目录
cd <CVE-or-NAME>

# 先阅读复现指南
cat README.md

# 运行 PoC
python3 exploit.py   # 或：bash exploit.sh
```

## 贡献

欢迎贡献新的 PoC。添加新漏洞的步骤：

1. 创建以 CVE 编号或漏洞名称命名的目录
2. 包含 PoC 脚本（`exploit.py` / `exploit.sh`）以及 `README.md`，其中应包括：
   - CVE 编号与漏洞名称
   - 受影响版本 / 组件
   - 逐步复现指南
   - 参考资料（安全公告链接、补丁提交、致谢）
3. 提交 Pull Request

## 免责声明

本仓库仅用于**安全研究与教育目的**。

- 请勿在未获授权的情况下对非你所有的系统使用这些 PoC。
- 作者对滥用行为不承担任何责任。
- 请始终遵循负责任的披露规范。

## 相关链接

- [VulnClaw](https://github.com/Unclecheng-li/VulnClaw) —— AI 驱动的渗透测试框架

## 许可证

MIT
