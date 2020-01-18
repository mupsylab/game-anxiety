# intro

`SceneSetup.intro();`

# intro-play-button

(...51)

[开始游戏！](#intro-start) `publish("intro-to-game-1"); Game.OVERRIDE_CHOICE_LINE=true;`

# intro-start

(...500)

`clearText()`

n3: 所以在我们开始之前，*你*有什么阅读偏好？

`publish("show_options_bottom")`

# intro-start-2

n3: 好，让我们的故事开始吧...

```
publish("hide_tabs");
clearText();
```

(...1000)

`publish("intro-to-game-2")`

n2: 这 是 一 个 人 类

(...600)

`clearText()`

(...300)

`publish("intro-to-game-3")`

# act1

```
SceneSetup.act1();
publish("hide_tabs");
music('battle', {volume:0.5});
```

(...300)

n: 而 这 是 人 类 的 焦 虑

n: _你_ 来 扮 演 焦 虑

(#act1_normal)


# act1_normal

```
hong({body:"putaway"});
sfx("rustle");
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 不。不，没有，没在听。我得看下手机。

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: 你 的 任 务 是 从 *危 险* 中 保 护 人 类

`bb({eyes:"look", mouth:"small_lock", body:"fear"})`

b: 妈耶！你又开始把生命和微博一起刷走了！

```
bb({eyes:"normal", mouth:"normal", body:"normal"});
hong({eyes:"annoyed"});
```

h: 是啊我在想为什么我不多坐着然后听我的内心发言。

`hong({eyes:"neutral"});`

n: 快，警告他们面临的*危险*！

```
bb({eyes:"look"});
```

[哦不，看那个恐怖的新闻！](#act1d_news)

[哦不，那条微博是不是在暗讽*我们*？](#act1d_subtweet)

[嘿，一张猫喝牛奶的动图。](#act1d_milk)

# act1d_milk

`hong({mouth:"smile", eyes:"surprise"});`

h: 哈是啊很可爱，我--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: **猫消化不了牛奶我们竟然在享受对动物的虐待我们真是大烂人**

(...200)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("20p", "bad");
publish("hp_show");
```



