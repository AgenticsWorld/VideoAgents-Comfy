# VideoAgents-Comfy 花字素材库 — VideoAgents 花字素材库(字体 + 音效)

本仓库是 VideoAgents 花字系统的远端素材源,由 `render_captions.py assets-sync` 按需拉取。

## 结构约定(不可改)
- `fonts/` — 字体文件(.ttf/.otf/.ttc),可任意子目录组织;文件名 ASCII
- `sfx/`   — 音效文件(.wav/.mp3/.m4a/.ogg/.flac),可任意子目录组织;文件名 ASCII
  (文件名单词会成为音效 tags,如 whoosh_big_01.wav → tags: whoosh, big)

## 使用
1. VideoAgents 仓库 `modules/caption_assets.json` 填 `"repo": "AgenticsWorld/VideoAgents-Comfy"`
2. `python3 code/render_captions.py assets-sync`
   → 下载到 data/fonts/remote/ 与 data/sfx/remote/(本地缓存),自动重扫 manifest
   → 本仓库删除的文件,同步时本地也会移除(远端是唯一事实源)

## 版权
只放可商用素材。当前内容:Google Fonts OFL 字体 ×5(许可证见 fonts/google-ofl/OFL-LICENSE.txt)、
Kenney CC0 音效精选(sfx/kenney/LICENSE-CC0.txt)、ffmpeg 合成音效(CC0,sfx/synth/LICENSE.txt)。
新增素材请在对应目录附许可证说明,VideoAgents 的版权终审(11-qa/copyright)会核对。
