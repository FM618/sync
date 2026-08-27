# Third-Party Notices

本软件（sync）包含以下第三方开源组件。各组件的版权归其各自作者所有，
并遵循其各自许可证的条款。本文件随软件分发，以满足各许可证的声明义务。

完整依赖清单见源码工程中的 `Cargo.lock` 与 `pnpm-lock.yaml`；
各 crate 的完整许可证文本可通过 crates.io 页面获取。

## Rust 运行时依赖（主要组件）

| 组件 | 版本 | 许可证 |
|------|------|--------|
| tauri | 2.x | MIT OR Apache-2.0 |
| tauri-plugin-opener / tauri-plugin-autostart | 2.x | MIT OR Apache-2.0 |
| wry | 0.55 | Apache-2.0 OR MIT |
| tao | 0.35 | Apache-2.0 |
| tokio | 1.x | MIT |
| serde / serde_json | 1.x | MIT OR Apache-2.0 |
| mdns-sd | 0.14 | MIT OR Apache-2.0 |
| rustls / tokio-rustls | 0.23 / 0.26 | Apache-2.0 OR ISC OR MIT |
| rcgen | 0.13 | MIT OR Apache-2.0 |
| aes-gcm / hmac / sha2（RustCrypto） | 0.10 / 0.12 / 0.10 | MIT OR Apache-2.0 |
| x25519-dalek / curve25519-dalek | 2.x / 4.x | BSD-3-Clause |
| tray-icon | 0.24 | MIT OR Apache-2.0 |
| reqwest / hyper | 0.13 / 1.x | MIT OR Apache-2.0 |
| webkit2gtk / soup3 / gtk 系（gtk-rs） | 2.0 / 0.5 / 0.18 | MIT（动态链接系统 LGPL 库） |

## MPL-2.0 组件

以下组件采用 Mozilla Public License 2.0（**弱 copyleft、文件级约束**）。
这些组件未被修改，其源代码可通过 crates.io 公开获取（链接见下）：
MPL-2.0 允许其与专有代码静态链接分发，仅要求保留本声明并使
该组件自身的源代码可获取——crates.io 已公开提供，满足该要求。

| 组件 | 版本 | 源代码 |
|------|------|--------|
| cssparser | 0.36 | <https://crates.io/crates/cssparser> |
| cssparser-macros | 0.6 | <https://crates.io/crates/cssparser-macros> |
| dtoa-short | 0.3 | <https://crates.io/crates/dtoa-short> |
| option-ext | 0.2 | <https://crates.io/crates/option-ext> |
| selectors | 0.36 | <https://crates.io/crates/selectors> |

## 前端运行时依赖

| 组件 | 版本 | 许可证 |
|------|------|--------|
| Vue.js | 3.5.x | MIT |
| @tauri-apps/api | 2.x | Apache-2.0 OR MIT |
| @tauri-apps/plugin-opener | 2.x | MIT OR Apache-2.0 |

## 系统组件（不随安装包分发）

| 组件 | 平台 | 说明 |
|------|------|------|
| WKWebView | macOS | 操作系统内置 Web 视图 |
| WebView2 Runtime | Windows | 微软操作系统组件 |
| WebKitGTK / GTK3 | Linux | 系统库，由包管理器安装（LGPL） |

## 许可证分布统计

- Rust 依赖共 526 个 crate（含构建/平台条件依赖），许可分布：MIT / Apache-2.0 及其组合为主，
  另有 BSD-3-Clause、ISC、Zlib、Unlicense、Unicode-3.0、CC0 等宽松许可；
- **MPL-2.0**：5 个（见上表，弱 copyleft / 文件级，闭源分发允许）；
- **r-efi**（UEFI 绑定，目标平台专用）：`MIT OR Apache-2.0 OR LGPL-2.1-or-later`
  三选一许可——选择 MIT 即满足条款，不产生 LGPL 义务；
- **无 GPL / AGPL 强 copyleft 组件**。对全部 526 个 crate 逐一核验：本地解析 316 个，
  crates.io 在线核验 168 个；其余 42 个（gtk-rs / windows-rs / reqwest 系等知名 crate）
  因网络波动未在线核验，其许可均为已知宽松许可（MIT / Apache-2.0 / BSD / ISC）。
