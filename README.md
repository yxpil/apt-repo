# BIT APT 源（Debian / Ubuntu / 麒麟等）

自托管 APT 仓库，由 CI 从 [BIT Releases](https://github.com/yxpil/bit/releases) 自动同步。

```bash
echo "deb [trusted=yes] https://yxpil.github.io/apt-repo stable main" | sudo tee /etc/apt/sources.list.d/bit.list
sudo apt update && sudo apt install bit
```

- Suite/Codename: `stable`，组件: `main`
- 架构: amd64 / arm64 / riscv64 / loongarch64
- Release 文件未签名（客户端需 `[trusted=yes]`）

---

<div align="center">

<a href="https://github.com/yxpil/apt-repo">
  <img width="100%" src="https://alittlecatgirlpanel.yxp.hk/card?repo=yxpil/apt-repo" alt="gh-card · yxpil/apt-repo" />
</a>

<sub>Powered by <a href="https://alittlecatgirlpanel.yxp.hk"><b>gh-card</b></a> · 粉色手写体 README 仓库名片</sub>

</div>
