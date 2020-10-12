# Get screenshots from video & src


## Why 

在原有的「**quizlet x anki**」中，加入截图，便于快速回顾，对话的场景。最终的想要的东西是： 

{xxx.mp4, xxx.src} -> 程序 -> {number.png for each line}

备注：

line: 

```
20
00:00:04,040 --> 00:00:05,990
又再次所有人都不在了
No one is around. Again.
```

对于上面有一张screenshot: 20.png

## How

Run many times for the following commmand: 

* get **one** (`-frames:v`) frame **x.png** at **time** x(`-ss`) from the **video**(`-i`) with **subtitles**(`-vf subtitles=`)

```
ffmpeg -i {video_path} -ss {time} -filter:v subtitles={subtitle_path} -frames:v 1 {pic_name.png}
```

Need to know:

1. video path
1. subtitle path 
1. which point in time
1. output name


pseudocode

``` python
def get_screenshots(video, subtitle) -> None:
	frames_list = split_subtitle(subtitle) # [(str,)]
	for frame in frames_list:
		screenshot(video, subtitle, frame.time, frame.name)
```

``` python 	
def split_subtitle(subtitle) -> frames_list:
	"""
	xxx.src -> [(time, name),]
	"""
	
def screenshot(video, subtitle, time, name):
	"""
	run command above
	"""
```
 

## What

* **quizlet x anki流程**: 在{xxx.src} -> quizlet -> {卡片s}，然后翻阅卡片，遇到新的知识点，就加入anki.

