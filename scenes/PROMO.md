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

n2: **这 是 一 个 人 类**

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

n: **而 这 是 人 类 的 焦 虑**

n: **_你_ 来 扮 演 焦 虑**

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

n: **你 的 任 务 是 从 *危 险* 中 保 护 人 类**

`bb({eyes:"look", mouth:"small_lock", body:"fear"})`

b: Gasp! You're scrolling your life away on Twitter! Again!

```
bb({eyes:"normal", mouth:"normal", body:"normal"});
hong({eyes:"annoyed"});
```

h: Yeah I wonder why I don't just sit and listen to my thoughts more often.

`hong({eyes:"neutral"});`

n: QUICK, WARN THEM ABOUT A *DANGER!*

```
bb({eyes:"look"});
```

[Oh no, look at that horrible news story!](#act1d_news)

[Oh no, is that tweet secretly about *us?*](#act1d_subtweet)

[Hey, a GIF of a cat drinking milk](#act1d_milk)

# act1d_milk

`hong({mouth:"smile", eyes:"surprise"});`

h: Heh ya that's cute, I--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: CATS CAN'T DIGEST MILK AND WE'RE TERRIBLE PEOPLE FOR ENJOYING ANIMAL ABUSE

(...200)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("20p", "bad");
publish("hp_show");
```



