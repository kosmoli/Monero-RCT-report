# Zero to Monero 中文翻译

基于 [UkoeHB/Monero-RCT-report](https://github.com/UkoeHB/Monero-RCT-report) 的中文翻译。

## 翻译约定

- **技术术语保留英文**：RingCT、MLSAG、Bulletproofs、Schnorr、Ed25519、Pedersen commitment、stealth address、key image 等
- **章节标题**：中文翻译后附英文原文，如 `第 1 章 引言 (Introduction)`
- **数学公式**：完整保留，不做任何修改
- **LaTeX 命令/宏/标签/引用**：完整保留
- **编译环境**：需要 XeLaTeX + xeCJK（原版使用 pdfLaTeX）

## 文件结构

与上游 `content/` 完全对应：

```
translations/zh/
├── main.tex                    # 主文件（已适配 XeLaTeX + xeCJK）
├── content/
│   ├── introduction.tex        # 第 1 章 引言
│   ├── basicConcepts.tex       # 第 2 章 基本概念
│   ├── advancedSchnorr.tex     # 第 3 章 高级 Schnorr 签名
│   ├── addresses.tex           # 第 4 章 地址
│   ├── commitments.tex         # 第 5 章 承诺方案
│   ├── transactions.tex        # 第 6 章 交易
│   ├── blockchain.tex          # 第 7 章 区块链
│   ├── txKnowledgeProofs.tex   # 第 8 章 交易知识证明
│   ├── multisig.tex            # 第 9 章 多重签名
│   ├── escrowedMarket.tex      # 第 10 章 托管市场
│   ├── txTangle.tex            # 第 11 章 TxTangle
│   ├── appendix.tex            # 附录
│   └── bulletproofs.tex        # Bulletproofs 补充
├── front/                      # 封面、摘要（已翻译标题）
├── back/                       # 参考文献（保留原文）
└── README.md                   # 本文件
```

## 编译

```bash
# Ubuntu/Debian:
apt install texlive-xetex texlive-lang-chinese fonts-noto-cjk

# 编译：
cd translations/zh
xelatex main.tex
biber main
xelatex main.tex
xelatex main.tex
```

## 同步上游更新

```bash
cd /path/to/Monero-RCT-report
git remote add upstream https://github.com/UkoeHB/Monero-RCT-report.git
git fetch upstream
git merge upstream/main
# 检查 content/ 中哪些文件有变更，更新 translations/zh/content/ 中的对应翻译
```

## 翻译进度

- [x] 第 1 章 引言 (Introduction)
- [x] 第 2 章 基本概念 (Basic Concepts)
- [x] 第 3 章 高级 Schnorr 签名 (Advanced Schnorr)
- [x] 第 4 章 地址 (Addresses)
- [x] 第 5 章 承诺方案 (Commitments)
- [x] 第 6 章 交易 (Transactions)
- [x] 第 7 章 区块链 (Blockchain)
- [x] 第 8 章 交易知识证明 (Transaction Knowledge Proofs)
- [x] 第 9 章 多重签名 (Multisig)
- [x] 第 10 章 托管市场 (Escrowed Market)
- [x] 第 11 章 TxTangle
- [x] 附录 (Appendix)

---
*翻译始于 2026-06-26，Kosmo & Kleo*
