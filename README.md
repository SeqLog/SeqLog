# SeqLog — a native macOS outliner that keeps your notes as plain Markdown files

**[seqlog.com](https://seqlog.com)** · [Download for Mac](https://seqlog.com/dl/latest/SeqLog.dmg) ·
[Release notes](https://github.com/SeqLog/SeqLog/releases/latest) ·
[vs Logseq](https://seqlog.com/vs/logseq) · [vs Obsidian](https://seqlog.com/vs/obsidian)

SeqLog is a **local-first outliner and note-taking app for macOS**: a daily journal, wikilinks,
backlinks, instant full-text search and built-in Git, editing the plain `.md` files already on
your disk with nothing in between. Written in SwiftUI, not Electron. No account, no cloud,
no database, no lock-in.

> A native alternative to **Logseq**, **Obsidian** and **Roam Research** for people who want
> their notes to stay ordinary Markdown files on their own Mac.

**Free forever on macOS.** No account, no trial, no upsell.

![SeqLog journal view](https://seqlog.com/press/journal.png)

## Why plain files

Your vault is a folder of ordinary `.md` files, and that folder is the *only* storage — no
database, no index, no proprietary layer sitting on top. Everything you already own keeps
working on it: `grep`, `git`, `rsync`, Finder, your editor, and coding agents like Claude Code
or Codex pointed straight at the directory. Notes you can only reach through one app are notes
you have lent to that app.

## What it does

- **Files are the truth** — CommonMark plus `[[wikilinks]]`, one file per page, journals by
  date. Open the same vault in any editor, diff it in any tool, sync it any way you like.
- **Search without an index** — full text, backlinks, unlinked references and page names,
  through a Rust ripgrep FFI that greps the files on every query. Nothing to rebuild,
  nothing to go stale, nothing to corrupt.
- **Git is the sync layer** — embedded libgit2: auto-commit on save, push and pull to any
  remote, branch switching, conflict resolution, commit history with inline diffs, and
  per-file revert. Your note history is a real repository, not a proprietary version store.
- **An outliner, keyboard first** — indent, collapse, multi-select and drag to reorder across
  pages. Every edit has a symmetric inverse, so undo and redo never drift.
- **⌘K and ⌘F** — one command palette for pages, slash commands, favorites and recents. One
  find bar that reaches across every journal day, loaded or not.
- **Full frame rate on any vault** — recycled rows drawn directly with CoreText, absolute-frame
  layout, no per-frame SwiftUI solve. A five-thousand-page journal flings like an empty one.
- **Four languages** — English, 简体中文, Español and Français, following your system setting.

Also in the box: daily journal, tabs, drag & paste images, image lightbox, code fences,
unlinked references, favorites & recents, external-edit watching, GitHub sign-in, and
signed automatic updates.

## Screenshots

| Backlinks | Git history |
|---|---|
| ![Page with backlinks](https://seqlog.com/press/page-backlinks.png) | ![Commit history with inline diff](https://seqlog.com/press/git-history.png) |

| Command palette | Find across the journal |
|---|---|
| ![Command palette](https://seqlog.com/press/command-palette.png) | ![Find bar](https://seqlog.com/press/find.png) |

## Requirements

macOS 15 or later. Apple Silicon, or [an Intel build](https://seqlog.com/dl/latest/SeqLog-x86_64.dmg).
Signed and notarized; updates ship through Sparkle.

## Pricing

macOS is **free forever** — not a trial, not a reduced tier, not ad-supported. An iOS version
is in progress; it will be a **one-time purchase, never a subscription**, and it will not make
the Mac app any less free.

## Privacy

No account, no analytics, no telemetry. Your notes never leave your Mac. The app reaches the
network for exactly three things: the update feed, GitHub sign-in if you ask for it, and the
Git remote you configured yourself. [Full policy](https://seqlog.com/privacy).

## FAQ

**Is SeqLog open source?** No. It is free on macOS but the application source is not published.
One developer, no VC, no ads, and nothing held back from a "free tier" — closed source is what
makes that arithmetic work. If open source is non-negotiable for you, Logseq and Obsidian are
good answers and we would rather say so than pretend.

**Can I open my existing Logseq vault?** Yes. SeqLog uses the same `pages/` and `journals/`
layout, and normalizes Logseq's `YYYY_MM_DD` journal filenames. See
[SeqLog vs Logseq](https://seqlog.com/vs/logseq).

**How is it different from Obsidian?** Obsidian is also file-based; the differences are blocks
versus documents, native versus Electron, built-in Git versus a plugin, and free for commercial
use versus a per-seat commercial licence. See [SeqLog vs Obsidian](https://seqlog.com/vs/obsidian).

**Does it need a server or a subscription to sync?** No. Sync is Git, to any remote you already
have — GitHub, a self-hosted forge, or a folder on a drive.

## About this repository

This repo is SeqLog's **release home, update feed and issue tracker**. The application source
is not published here.

- **Found a bug or want a feature?** [Open an issue](https://github.com/SeqLog/SeqLog/issues).
- **Looking for downloads?** [Releases](https://github.com/SeqLog/SeqLog/releases), or
  [seqlog.com](https://seqlog.com) for the always-current build.
- `appcast.xml` / `appcast-x86_64.xml` are the Sparkle update feeds. They are generated by the
  release pipeline; don't edit them by hand.

---

## 中文简介

**SeqLog 是一款原生 macOS 大纲笔记应用**，用 SwiftUI 写成，直接编辑你磁盘上的 Markdown 文件。
日记、双向链接、全文搜索与内置 Git，全都建在普通 `.md` 文件之上——没有数据库，没有索引，
没有私有格式，也不需要账号和云端。**macOS 版永久免费。**

> 适合正在找 **Logseq 替代品 / Obsidian 替代品 / Roam Research 替代品**，
> 又希望笔记始终是自己 Mac 上一堆普通 Markdown 文件的人。

- **文件就是唯一真相**：CommonMark + `[[双链]]`，一页一个文件，日记按日期命名。
  同一个 vault 可以用任何编辑器打开、任何工具 diff，也能让 Claude Code、Codex
  这类 coding agent 直接改——笔记只能从一个 app 进去，就等于把它借给了那个 app。
- **不建索引的搜索**：全文、反链、未链引用与页名，走 Rust ripgrep FFI 每次直接 grep 文件。
  不用重建，不会陈旧，也不会损坏。
- **Git 就是同步层**：内嵌 libgit2，保存自动提交，推拉任意远程，切分支、解冲突、
  看带行内 diff 的提交历史、按文件回滚。
- **大纲编辑，键盘优先**：缩进、折叠、多选、跨页拖拽重排。每个编辑操作都有对称的逆操作，
  撤销与重做不会漂移。
- **⌘K 与 ⌘F**：一个命令面板管页面、斜杠命令、收藏与最近；一条查找栏横跨所有日记天，
  没加载的也搜得到。
- **满帧滚动**：行视图复用 + CoreText 直接绘制 + 绝对坐标布局，五千页的日记和空库一样跟手。
- **四种语言**：English / 简体中文 / Español / Français，跟随系统。

适用场景：个人知识库、卡片盒笔记法（Zettelkasten）、每日日志与工作记录。

**下载**：[seqlog.com](https://seqlog.com) · macOS 15 及以上，已签名并公证，通过 Sparkle 自动更新。
**隐私**：无账号、无统计、无遥测，笔记不出本机（[隐私政策](https://seqlog.com/privacy)）。
**关于开源**：macOS 永久免费，iOS 版将来收费且是一次性买断、非订阅。一个人做，没有 VC，
没有广告，也不会在免费版里留一手——闭源是让这笔账算得通的原因。如果开源对你是硬性要求，
Logseq 和 Obsidian 是更合适的选择。

本仓库是 SeqLog 的**发布源、更新源与 issue 跟踪处**，不包含应用源码。
