
# 升级贺卡

## {开场 @showdialog}

你已经做了一张贺卡，现在让它变得更惊艳！  
![传递爱心](/static/skillmap/story/story-activity-2.gif "热带鱼为什么喜欢咸水？")

---

## {步骤 2}

工作区里已经有一张简单贺卡的代码。  
**换个背景，打造一张全新贺卡**  
⭐⭐⭐

- :paint brush: 点击 ``||scene:将背景图设为 [ ] ||`` 积木里的灰色方块，  
  在弹窗顶部切换到 **"图库"** 标签页，挑一张新背景。  
  _💡 也可以留在 **编辑器** 自己画一张。_

- :mouse pointer: 完成后点击 **下一步** 继续。

```blocks
//@highlight
scene.setBackgroundImage(img`
`)
effects.confetti.startScreenEffect()
music.playMelody("G B A G C5 B A B", 120)
```

---

## {步骤 3}

**换首音乐吧**  
🎹🎹🎹

- :mouse pointer: 想换旋律？点击 ``||music:播放旋律 [ ]以速度 120 (拍速)||``  里的音符，  
  在编辑器或图库里挑一首。

```blocks
scene.setBackgroundImage(img`
`)
effects.confetti.startScreenEffect()
//@highlight
music.playMelody("G B A G C5 B A B ", 120)
```

---

## {步骤 4}

按 **Ⓐ** 键就能循环显示你的祝福语——让贺卡更有心意！

- :game: 从 ``||controller: 控制器||`` 拖一个 ``||controller:当按键A按下 ||`` 容器到工作区。  
- :circle: 从 ``||game:游戏||`` 拖  ``||game:显示文本 [""]对话框位于底部||`` 积木，  
  放进 **当 A 按钮被按下** 容器里。  
- :mouse pointer: 在文本框里写下你的第一条祝福语。

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    game.showLongText("地球日快乐！", DialogLayout.Bottom)
})
```

---

## {步骤 5}

把游戏画面切出来看看，  
别忘了按 **Ⓐ** 键测试你的第一条消息！

---

## {步骤 6}

**再加一句暖心话**  

- :mouse pointer: 右键  ``||game:显示文本 [""]对话框位于底部||`` → **复制**，  
  把复制出来的积木拖到 **当 A 按钮被按下** 容器底部。  
- :mouse pointer: 在新积木里输入第二条祝福语。

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    game.showLongText("地球日快乐！", DialogLayout.Bottom)
    game.showLongText("送给最棒的地球", DialogLayout.Bottom)
})
```

---

## {步骤 7}

**🎨 让对话框更出彩 🎨**

- :mouse pointer: 从 ``||game:游戏||`` 拖  ``||game:显示文本[""]对话框位于底部||`` 积木  
  到 **当 A 按钮被按下** 容器最上方。  
- :mouse pointer: 点击灰色方块 → 图库，挑一个好看的边框。

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    game.setDialogFrame(img`
        `)
    game.showLongText("地球日快乐！", DialogLayout.Bottom)
    game.showLongText("送给最棒的地球", DialogLayout.Bottom)
})
```

---

## {步骤 8}

再按 **Ⓐ** 键，看看循环消息和边框效果。  
😍 😍 😍

---

## {步骤 9}

**🎀 最后的小心思 🎀**

- :circle: 从 ``||game:游戏||`` 拖  ``||game:设置对话框文本颜色为[]||``积木  
  放到 **当 A 按钮被按下** 顶部。  
- :mouse pointer: 选一种既好看又易读的字体颜色。

```blocks
controller.A.onEvent(ControllerButtonEvent.Pressed, function () {
    game.setDialogTextColor(1)
    game.setDialogFrame(img`
        `)
    game.showLongText("地球日快乐！", DialogLayout.Bottom)
    game.showLongText("送给最棒的地球", DialogLayout.Bottom)
})
```

---

## {恭喜 @showdialog}

🥳 完成啦！🥳  
在点击 **完成** 前，再按几下 **Ⓐ** 键，看看贺卡效果！

---

## {终章}

**🎊 祝贺你 🎊**  
现在你有了一张任何朋友都会惊喜的贺卡！  
点击 **完成** 返回主页，把它分享给家人和朋友吧！

```template
{
scene.setBackgroundImage(img`
.
`)
effects.confetti.startScreenEffect()
music.playMelody("- - - - - - - - ", 120)
}
```

```ghost
scene.setBackgroundColor(0)
scene.setBackgroundImage(img`
    .
    `, SpriteKind.Player)
mySprite.setPosition(0, 0)
forever(function () {
    for (let index = 0; index < 4; index++) {
    }
})
```