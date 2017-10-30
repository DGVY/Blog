---
title: NSIS-调试技巧
date: 2017-10-27 17:10:27
categories:
- NSIS
---

# txt输出法

{% codeblock lang:nsis %}
    GetTempFileName $R0
    FileOpen $R1 $R0 w
    # Your Code
    FileWrite $R1 "文件标志 = $TempFileFlag$\r$\n"
    FileWrite $R1 "文件名   = $TempFileName$\r$\n"
    FileWrite $R1 "临时路径 = $TempFilePath$\r$\n"
    FileWrite $R1 "目标路径 = $TargFilePath$\r$\n$\r$\n"
    # Your Code
    FileClose $R1
    Exec '"notepad.exe" "$R0"'
{% endcodeblock %}


#消息框弹出法

{% codeblock lang:nsis %}
    MessageBox MB_OK "messagebox_text" 
{% endcodeblock %}