# How to Batch Rename Filesname


#How to batch rename filesname

```bash
ls *.mp4| awk -F" 【中文 www.zhongwen.zw 】" '{print "mv \""$0"\" \""$1$2"\""}'  | bash:
```
