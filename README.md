# call_mspaint_by_autohotkey
快速打开画图软件 使用autohotkey


```
!p::
IfWinExist, 无标题 - 画图     ;注意这里面的标题名字就是打开程序里面写的标题,注意中间带空格.;这样写就控制了程序开关.

{
    
    WinActivate,
    return 
}
else
{
run mspaint
  WinWait, 无标题 - 画图  ;注意这行来保证下一行会执行成功, 如果不等那么直接下行就会无效,因为画图软件还没打开,执行activate会执行无效直接跳过.
    WinActivate,
return
}
```
