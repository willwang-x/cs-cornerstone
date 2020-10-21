<h1 align="center">
<br>
  <img src="https://i.imgur.com/ssBehdB.png" alt="practice exmaple from modern family" width=200">
  <br><br>
  Practice: 如何通过视频学习英语？  
  <br><br>
</h1>


## Why

* 理解视觉化的学习材料
* 作为听力的测试，因为表达的第一步是听懂

## How 

### Ideal

* 产生疑问：**无字幕**观看视频
* 解答疑问：{xxx.mp4, xxx.src} → 程序 → {notes.md}
* 复习解答：将知识点加入Anki复习。

### Reality

> watching -> {**processing**...} -> review points in anki

* 产生疑问：无字幕观看视频
* 解答疑问：
	* 1）利用[Word Discoverer](https://chrome.google.com/webstore/detail/word-discoverer-expand-yo/noncaeikjgpbdeoocblijjgegnobogib) 对字幕扫描。 
	* <del> 2）分解知识点 by quizlet </del> (因为还是慢)
	* 3) {video.mp4, xxx.srt} -> ffmpeg -> {screenshots}
		* **遍历**截图，同时**删除**不包含知识点的截图
		* {xxx.srt, [screenshot.png]} -> anki小程序 -> {anki card: 文字，截图}
		* 在Anki中遍历，使用cloze工具
* 复习解答：加入Anki by [ODH](https://github.com/ninja33/ODH) or 手动


## What

* **processing**: 一个将看完的**视频**变成Anki中**知识点**的**流程**。
* **视频**：生活需求 x 内容简短 x 难度合适，如 职场 x 20mins x 90%听懂 = 摩登家庭。视频来源：电影，TED，youtube。最好有中英字幕，便于对答案。
* **notes.md**: 词汇概括 + 截图 + 知识点
* **知识点**：定义为[lexical_item](https://www.wikiwand.com/en/Lexical_item)，可理解为「可学习单元」，如发音，习语，句型。
* **quizlet**: {xxx.src} → quizlet →  {card, ... , card} e.g. [Modern.Family](https://quizlet.com/535264808/modernfamilys11e01-flash-cards/?new)
* **小程序**: {xxx.mp4, xxx.src} -> 小程序 -> {screenshot.png for each line}
* [getsub](https://github.com/gyh1621/GetSubtitles): 一步下载字幕
	* `getsub {path} -q -s` 
* **词库过滤器**：{xxx.src, new.txt} -> 词库过滤器 -> {all-point.src}

## Todo

1. 收集关于语块的数据库，如[英语句型手册](https://wenku.baidu.com/view/3024cbbf172ded630a1cb63d.html#)。
* 清理语块资料，得到可被应用的知识点数据库。
* 理解[Word Discoverer](https://chrome.google.com/webstore/detail/word-discoverer-expand-yo/noncaeikjgpbdeoocblijjgegnobogib)，加入以上的知识点数据库，作为暂时使用工具。
* 写一个程序：{xxx.mp4, xxx.src, lexical_item.txt} → 程序 → {notes.md}
* 优化notes.md的外观。


## Q&A 

**How to batch import text with images into Anki?**

* **Tools**: python, imgur, [Anki Markdown Notes](https://ankiweb.net/shared/info/2141874715#:~:text=Starting%20from%20scratch%20Create%20a,Markdown%20files%20is%20shown%20below.)
* **Goal**: {xxx.srt, images} -> **tools** ->  {xxx.md} 
* **Ideas**: to upload image to imgur and get url link
* hwo to make it a cloze card?

```
3
- 你得去周旋\N- 周旋?
- You should mingle.\N- Mingle?
- https://i.imgur.com/eMuVMka.png
```

