# APT 软件源（BIT）

Debian / Ubuntu / UOS / 麒麟 / Loongnix 等可直接添加本源安装 BIT。

```bash
# 添加软件源（4 架构：amd64 / arm64 / riscv64 / loongarch64）
echo "deb [trusted=yes] https://yxpil.github.io/apt-repo stable main" | sudo tee /etc/apt/sources.list.d/bit.list
sudo apt update
sudo apt install bit
```

> 说明：本源未做 GPG 签名，`[trusted=yes]` 用于跳过签名校验；安装包本身与 GitHub Release 的 .deb 完全一致（SHA256 相同），下载时由 HTTPS 传输保证完整性。

支持的架构：

| 架构 | 芯片 |
|---|---|
| amd64 | Intel / AMD / 兆芯 / 海光 |
| arm64 | 飞腾 / 鲲鹏 / 麒麟 / 树莓派等 |
| riscv64 | VisionFive 2 等 RISC-V 设备 |
| loongarch64 | 龙芯 3A5000 / 3A6000 |

升级：`sudo apt update && sudo apt install --only-upgrade bit`

卸载：`sudo apt remove bit`

各架构安装包也可从 [Releases](https://github.com/yxpil/bit/releases) 直接下载。
