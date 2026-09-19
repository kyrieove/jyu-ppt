# jyu-ppt

把一篇论文 PDF 一键做成于韦斯屈莱大学（JYU）学术风格的英文 PPT，带演讲备注，中途不需要确认。

One-shot: research paper PDF → English JYU-style academic PPTX with speaker notes.

## 安装 / Install

**Codex**：在 Codex 里发这一句（中英二选一）：

```
用 skill-installer 安装 https://github.com/kyrieove/jyu-ppt/tree/main/jyu-ppt
```
```
Use skill-installer to install https://github.com/kyrieove/jyu-ppt/tree/main/jyu-ppt
```

装好后，开一个新对话就能用了。

**Claude Code / Antigravity / ZCode**：在终端里运行下面对应的命令，然后重启工具。

```bash
git clone https://github.com/kyrieove/jyu-ppt.git %TEMP%\jyu-ppt && xcopy /E /I %TEMP%\jyu-ppt\jyu-ppt %USERPROFILE%\.claude\skills\jyu-ppt
```

Antigravity 把目标目录换成 `%USERPROFILE%\.gemini\antigravity\skills\jyu-ppt`；ZCode 换成 `%USERPROFILE%\.zcode\skills\jyu-ppt`。

## 使用 / Use

**Codex**：

```
$jyu-ppt C:\path\to\paper.pdf
```

也可以直接说：「用 jyu-ppt 把 C:\path\to\paper.pdf 做成 PPT」。

**Claude Code / Antigravity / ZCode**：直接说「用 jyu-ppt skill 把 C:\path\to\paper.pdf 做成 PPT」。

**第一次运行**会问你三件事：封面上的姓名、单位、要不要放 InterLearn logo。回答会存进 skill 目录下的 `profile.md`，以后不再问。想改就直接编辑这个文件。第一次运行还会自动安装 Python 依赖，需要 Python 3.10 以上。

做完后，PPTX 在项目文件夹的 `exports\` 里。

## 里面有什么

- **品牌** `hulei_jyu`：JYU 的颜色、Aleo 和 Lato 字体、logo。
- **4 页框架** `hulei_jyu_frame`：封面、章节页、内容页的页眉页脚、结尾页。
- **视觉风格** `jyu-academic`，附 23 页占位范例。页数和版式都按论文本身来，默认用开放版式，卡片只在需要并列比较时用。
- 内置 [ppt-master](https://github.com/hugohe3/ppt-master)（作者 Hugo He，MIT 许可）。

JYU 和 InterLearn 的 logo 归各自机构所有，仅供其成员做学术报告使用。
