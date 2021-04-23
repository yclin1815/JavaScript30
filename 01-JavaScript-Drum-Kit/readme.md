##筆記

[Demo](https://yclin1815.github.io/JavaScript30/01-JavaScript-Drum-Kit)

1. 使用`window.addEventListener('keydown', playSound);`監聽鍵盤動作
2. 取得`e.keyCode`對應的`div`與`audio`
3. 若無相對應的`audio`則退出
4. 將相對應的`div`class加上`playing`
5. 設定`currentTime = 0`達到連擊效果`play`播放音效
6. 取得所有`.key`為陣列並監聽，`key.addEventListener('transitionend', removeTransition));`
7. 判斷`e.propertyName`不為transform則退出，若為transform則移除`playing`