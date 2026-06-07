### 로컬 세션은 wayland 로 하고, xrdp 세션은 X11 기반 세션으로 하기 

```
2026.06.02
```



#### 1) 로그인 선택 
```
1) 로그인 창(패스워드 입력단계) 우측 아래 톱니 아이콘에서 wayland 로 선택한다.
```


#### 2) 창 이동시 끊어짐이 있을 경우
``` 

gsettings set org.gnome.mutter experimental-features "['x11-randr-fractional-scaling', 'kms-modifiers']"

**********@**********:~$ 
**********@**********:~$ gsettings set org.gnome.mutter experimental-features "['x11-randr-fractional-scaling', 'kms-modifiers']"
**********@**********:~$ 
**********@**********:~$ cat /sys/module/nvidia_drm/parameters/modeset
cat: /sys/module/nvidia_drm/parameters/modeset: 허가 거부
**********@**********:~$ 
**********@**********:~$ sudo bash
[sudo] ********** 암호: 
root@**********:/home/**********# 
root@**********:/home/**********# cat /sys/module/nvidia_drm/parameters/modeset
Y
root@**********:/home/**********# 
```
