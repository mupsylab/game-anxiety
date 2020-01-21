# act1

```
SceneSetup.act1();
```

(...300)

n: 而 这 是 人 类 的 焦 虑

n: _你_ 扮 演 焦 虑

{{if window.localStorage.continueChapter=="replay"}}
(#act1_replay)
{{/if}}

{{if window.localStorage.continueChapter!="replay"}}
(#act1_normal)
{{/if}}



# act1_replay

`hong({mouth:"0_neutral", eyes:"0_neutral"})`

h: 哦嗨！我们又回来了？

`hong({eyes:"0_neutral"})`

n: 你 的 任 务 是 从 *危 险* 中 保 护 人 类

`bb({eyes:"look", mouth:"small_lock"})`

n: 实 际 上， 重 玩 这 个 游 戏 正 让 他 们 处 于 *危 险 中*

n: 快， 警 告 他 们！

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: 人类！听着，我们碰到危险了！玩家...

[...要再次折磨我们！](#act1_replay_torture)

[...不会找到别的结局的！](#act1_replay_alternate)

[...会发现游戏内容和游戏结构相矛盾！](#act1_replay_dissonance)

# act1_replay_torture

```
window.HACK_REPLAY = JSON.parse(localStorage.act4);
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

{{if window.HACK_REPLAY.act1_ending=="fight"}}
b: 他们会让我们缩成球然后哭！
{{/if}}

{{if window.HACK_REPLAY.act1_ending=="flight"}}
b: 他们会让你恐慌发作以谋杀你的手机！
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="fight"}}
b: 他们会让我们*不*揍派对上的那个人！
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="flight"}}
b: 他们会让我们揍派对上那个混乱善良的人！
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="jump"}}
h: 额至少我们这回也许不用从屋顶上跳--
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="walkaway"}}
b: **他们会让我们从屋顶上跳下去的。**
{{/if}}

`bb({body:"fear"});`

b: **所有这些新的坏事都会发生在我们身上，然后我们就会--**

(#act1_replay_end)


#act1_replay_alternate

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: 当然了，总体来说*整个*故事还是一样的，但是每章都有两个可能的结局，再说还有那么多对话分支的选--

`bb({body:"fear"});`

b: 玩家会很失望，关掉这个页面，删掉这个程序，然后我们就会--

(#act1_replay_end)


# act1_replay_dissonance

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: 会发现- 什么玩意？

`bb({eyes:"normal"});`

b: 整个故事想阐述的就是你可以如何***选择***与你的恐惧建立健康的合作关系，

`bb({eyes:"normal_right"});`

b: 但是重玩游戏只会看到同一个故事，也就是在暗示你的***选择***压根不重要，

`bb({eyes:"narrow_eyebrow"});`

b: 也就是说游戏想传达的和游戏的结构根本就互相矛盾，

`bb({eyes:"fear"});`

b: 这个叙事宇宙的结构会开始瓦解，

`bb({body:"fear"});`

b: 然后我们就会--

(#act1_replay_end)


# act1_replay_end

`bb({body:"panic"})`

b: **死！！！！！！**

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.clearText();
```

(...1001)

```
bb({body:"laugh"});
hong({body:"laugh"});
Game.clearText();
sfx("laugh");
```

(...5001)

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({body:"0_sammich"});
```

h: 好了回到角色来吧。

```
Game.clearText();
```

n4: （ 让 _你_ _的_ 焦 虑 吧啦吧啦 选 择 和 _你_ _的_ 恐 惧 吧啦吧啦 你 知 道 怎 么 玩 的 ）

```
sfx("squeak");
hong({body:"0_squeeze"});
bb({body:"squeeze"});
```

(#act1_normal_choice)



# act1_normal

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: 哦妙啊，我的狼回来了。太————棒了。

`hong({eyes:"0_neutral"})`

n: 你 的 任 务 是 从 *危 险* 中 保 护 人 类

`bb({eyes:"look", mouth:"small_lock"})`

n: 实 际 上， 那 个 三 明 治 正 让 他 们 处 于 *危 险 中*

n: 快， 警 告 他 们！

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: 人类！听着，我们碰到危险了！危险是...

`bb({body:"squeeze"})`

n4: （ 让 _你_ _的_ 焦 虑 来 接 手 游 戏！ 选 择 和 _你_ _的_ 恐 惧 最 接 近 的 选 项 ）

(#act1_normal_choice)

# act1_normal_choice

[我们又在一个人吃午餐！](#act1a_alone) `bb({body:"squeeze_talk"})`

[我们吃东西并不能产生价值！](#act1a_productive) `bb({body:"squeeze_talk"})`

[白面包对我们有害！](#act1a_bread) `bb({body:"squeeze_talk"})`

# act1a_alone

```
bb({body:"normal", mouth:"small", eyes:"narrow"});
hong({body:"0_sammich"});
```

b: 你不知道孤独和一天抽十五根烟一样会导致过早死亡吗？

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: （Holt-Lunstad 2010，医学期刊)

`hong({eyes:"0_annoyed"})`

h: 呃，感谢你标注来源但是--

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: 也就是说如果我们*现在*没和别人待在一块儿我们就会-

`bb({body:"panic"})`

b: **死！！！！！！**

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "alone");
publish("hp_show");
```

(...2500)

`_.fifteencigs = true`

n: 你 使 用 了 *不 被 爱 的 恐 惧*

(#act1b)

# act1a_productive

```
bb({body:"normal", mouth:"small", eyes:"normal"});
hong({body:"0_sammich"});
```

b: 立马掏出你的电脑干点正事！

`hong({eyes:"0_annoyed"})`

h: 呃，我不想让面包屑掉到键--

```
bb({mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 如果我们没有在为社会做贡献我们就是社会寄生虫！

b: 就会有社会上的社会医生用药来消灭社会寄生虫然后我们就会--

```
bb({body:"panic", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: **死！！！！！！**

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "bad");
publish("hp_show");
```

(...2500)

`_.parasite = true`

n: 你 使 用 了 *成 为 坏 人 的 恐 惧*

(#act1b)

# act1a_bread

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich", eyes:"0_annoyed"});
```

h: 那些研究不是一直在证明--

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 淀粉会导致我们血糖飙升所以我们的四肢不得不被截掉然后我们就会-

`bb({body:"panic"})`

b: **死！！！！！！**

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "harm");
publish("hp_show");
```

(...2500)

`_.whitebread = true`

n: 你 使 用 了 *受 到 伤 害 的 恐 惧*

(#act1b)

# act1b

n: 效 果 显 著

`bb({mouth:"smile", eyes:"smile"});`

b: 看到了吗，人类？我是你忠诚的守卫狼！

`bb({body:"pride_talk"});`

b: 相信你的直觉！你的情感永远是合理的！

`bb({body:"pride"});`

n: 让 人 类 的 能 量 条 清 零

n: 为 了 保 护 人 类 身 体 上 + 社 会 上 + 道 德 上 的 需 求 ， 你 可 以 使 用 ：

n: *受 到 伤 害 的 恐 惧* #harm#

n: *不 被 爱 的 恐 惧* #alone#

n: 和 *成 为 坏 人 的 恐 惧* #bad#

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4: （ 重 要 提 示： 选 择 那 个 击 中 了 你 内 心 最 深 处 最 隐 秘 的 恐 惧 的 选 项！ ~）

h: ...

```
hong({body:"putaway"});
sfx("rustle");
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

(...1000)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h: 哈你猜怎么着我觉得我该看下手机了。

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: 保 护 你 的 人 类

n: 从 这 个 世 界 中。 从 其 他 人 中。 从 他 们 自 己 中。

n: 祝 你 好 运

(...500)

`Game.clearText()`

(...500)

(#act1c)

# act1c

`music('battle', {volume:0.5})`

n: 第 一 轮： *FIGHT!*

`bb({body:"normal", mouth:"normal", eyes:"normal"});`

h: 哈。脸书推送说这个周末有场派对。

`bb({eyes:"uncertain"});`

b: 那个怪胎难道不是*每个*周末都办派对吗？

`bb({eyes:"uncertain_right"});`

b: 他们内心到底是有多空虚？肯定在深处是一团糟！

`hong({eyes:"surprise"});`

h: 还有，我被邀请了？

`bb({eyes:"fear", mouth:"normal"});`

b: 那么！

[接受，否则我们会孤独到死掉！](#act1c_loner)

[拒绝，那儿全是毒品！](#act1c_drugs)

[无视，我们只会让派对变悲伤。](#act1c_sad)

# act1c_loner

{{if _.fifteencigs}}
b: 一天十五根烟，人类！十五根！
{{/if}}

{{if !_.fifteencigs}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if !_.fifteencigs}}
b: 然后我们的葬礼上会一个人都没有，他们会把我们的骨灰扬到海里，我们会被鲸鱼吃掉，
{{/if}}

{{if !_.fifteencigs}}
b: 然后我们就会成为**鲸鱼的大便**！
{{/if}}

{{if !_.fifteencigs}} `_.whalepoop = true` {{/if}}

(...500)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

{{if !_.fifteencigs}}
b: 所以我们当然要去那个派对！
{{/if}}

{{if _.parasite}}
b: 但是要带上电脑所以我们可以工作，避免当个社会寄生虫。
{{/if}}

{{if _.whitebread}}
b: 只要他们不提供**白面包**
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: **老天啊**。要是那能让你闭嘴的话，行啊。

h: 我会同意。

{{if _.whalepoop}}
b: 鲸鱼的大便啊，人类！鲸鱼的大便！
{{/if}}

`_.partyinvite="yes"`

(#act1d)

# act1c_drugs

`bb({mouth:"small", eyes:"fear"});`

{{if _.whitebread}}
b: 或者更糟... **白面包**
{{/if}}

{{if _.whitebread}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if _.whitebread}}
b: 我们吸食的冰毒和白面包会严重过量！我们肿胀的尸体都塞不进焚化炉！
{{/if}}

{{if !_.whitebread}}
b: 我们会嗑多少药！殡仪馆的人都会奇怪这具尸体怎么*已经*提前防腐过了！
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.parasite}}
b: 再说，不能去派对，我们必须工作否则就是糟糕的社会寄生虫！
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: **老天啊**。要是那能让你闭嘴的话，行啊。

h: 我会拒绝。

`_.partyinvite="no"`

(#act1d)

# act1c_sad

`bb({eyes:"uncertain_right", mouth:"normal"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.fifteencigs}}
b: 我们只会找个角落哭自己的孤独是如何像一天十五根烟一样致命。
{{/if}}

{{if _.parasite}}
b: 我们在派对上只会一直担心要怎么做才能产生价值。
{{/if}}

{{if _.whitebread}}
b: 我们只会一直担心不健康的食物选择会让我们怎么死掉。
{{/if}}

```
bb({mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"lookaway"});
```

h: 哇哦为什么呢。

`hong({eyes:"neutral"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: 所以要是我们去了我们就会让他们感觉糟糕，但如果拒绝了邀请我们也会让他们感觉糟糕！

`bb({body:"fear", eyes:"fear"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: **我们只会让别人感觉糟糕，所以我们应该感觉糟糕**

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`hong({mouth:"anger", eyes:"anger"});`

h: 呃。要是那能让你闭嘴的话，行啊。

h: 我会无视邀请。

`_.partyinvite="ignore"`

(#act1d)

# act1d

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"annoyed"});
```

h: 总之。脸书太劲了。我需要更平静，不那么容易引发焦虑的玩意。

`hong({eyes:"neutral"});`

h: 现在微博上有什么？

`bb({eyes:"look"});`

[哦不，看那个恐怖的新闻！](#act1d_news)

[哦不，那条微博是不是在暗讽我们？](#act1d_subtweet)

[嘿，一张猫喝牛奶的动图。](#act1d_milk)


# act1d_news

```
bb({eyes:"pained1"});
music(null, {fade:2});
```

b: 天啊，看着像是整个世界都烧起来了，你说是吧？

```
bb({eyes:"pained2"});
hong({mouth:"sad", eyes:"sad"});
```

b: 就好像一切都在迈向结束，所有事物都在消亡。而这都是命中注定的，我们什么都做不了。

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
bb({mouth:"shut"});
```

b: ...

`bb({mouth:"smile", eyes:"smile"});`

b: 我们把这个新闻转发吧！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.badnews=true`

```
music('battle', {volume:0.5});
hong({mouth:"anger", eyes:"anger"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 好好我会转发的所以拜托你安静！

`hong({mouth:"neutral", eyes:"annoyed"});`

h: 去他的，还是看下朋友圈吧。

(#act1e)


# act1d_subtweet

`bb({eyes:"fear"});`

b: 这是条暗讽我们的微博！一条卑鄙，狡猾的（没有艾特当事人的）嘲讽微博！

`hong({eyes:"annoyed"});`

h: 也许不是？

`bb({eyes:"narrow", mouth:"small"});`

b: 但是万一他们全都在背地里议论我们呢？

h: 他们没--

`bb({body:"fear", eyes:"fear", mouth:"normal"});`

b: **正对着我们的背后**

`hong({eyes:"sad", mouth:"sad"});`

h: 我不觉--

`bb({eyes:"narrow", mouth:"small"});`

b: 但是*万一*

h: 闭--

`bb({eyes:"narrow_eyebrow"});`

b: *万一*

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
hong({mouth:"shut"});
```

h: ...

(...1000)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.subtweet=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: 好——了，还是试下朋友圈吧。

(#act1e)

# act1d_milk

`hong({mouth:"smile", eyes:"neutral"});`

h: 哈是啊很可爱，那就转发一下吧，我觉--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: **猫消化不了牛奶我们竟然在享受对动物的虐待我们真是大烂人**

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("18p", "bad");
```

(...2500)


`_.catmilk=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: 好——了，还是看下朋友圈吧。

(#act1e)

# act1e

`hong({mouth:"neutral", eyes:"neutral"});`

h: 唔，昨晚的照片。所以*这就是*那些周末派对的样子。

{{if _.partyinvite=="yes"}} (#act1e_said_yes) {{/if}}

{{if _.partyinvite=="no"}} (#act1e_said_no) {{/if}}

{{if _.partyinvite=="ignore"}} (#act1e_said_ignore) {{/if}}

# act1e_said_yes

`hong({mouth:"sad", eyes:"annoyed"});`

h: 哎哟。好像太多人了。

h: 也许我不该同意那个邀请的？

```
hong({mouth:"neutral", eyes:"neutral"});
bb({mouth:"normal", eyes:"normal"});
```

[改变我们的决定？像个混蛋那样？！](#act1e_yes_dontchange)

[改变我们的决定！太多人了！](#act1e_yes_changetono)

{{if _.subtweet}}
[对他们绝对在偷偷议论我们。](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[等等我们还没核查事实就转发了。](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[嘿你是真的道德败坏你知道吗。](#act1e_ignore_posture)
{{/if}}

# act1e_yes_dontchange

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 他们就等着我们来结果我们却背叛他们的信任？你想注孤生吗？！

{{if _.fifteencigs}}
b: **十五。根烟。**
{{/if}}

{{if _.whalepoop}}
b: **鲸鱼。大便。**
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 闭嘴闭嘴我不改了！

(#act1f)

# act1e_yes_changetono

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 你不知道踩踏事件都是怎么来的吗？

```
bb({body:"fear", mouth:"small", eyes:"narrow"});
hong({eyes:"sad", mouth:"sad"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 2003年罗德岛的一家夜总会发生火灾，混乱中所有人都挤在了出口，于是一百个人被烧死了-，

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({mouth:"shock"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: **你想让这种事也发生在我们身上吗**-

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 2.5;
```

b: **拒绝拒绝拒绝拒绝拒绝拒绝拒绝拒**-


```
bb({body:"normal", eyes:"fear", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
hong({eyes:"anger", mouth:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 闭嘴闭嘴我改成拒绝就是了！老天啊！

(#act1f)

# act1e_said_no

`hong({mouth:"sad", eyes:"sad"});`

h: 嗯...看上去真的很有趣。

h: 也许我本来应该同意那个邀请的？

`bb({mouth:"normal", eyes:"normal"});`

[改变我们的决定？像个混蛋那样？！](#act1e_no_dontchange)

[改变我们的决定！别孤独地死掉！](#act1e_no_changetoyes)

{{if _.subtweet}}
[对他们绝对在偷偷议论我们。](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[等等我们还没核查事实就转发了。](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[嘿你是真的道德败坏你知道吗。](#act1e_ignore_posture)
{{/if}}

# act1e_no_dontchange

`bb({eyes:"anger"})`

b: 每个人都在指望我们！

b: ...让他们有一个完美的派对，没有恶心的{{if _.whitebread}}，大嚼特嚼白面包的{{/if}}讨厌鬼，比如你--


```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
bb({body:"normal", eyes:"uncertain", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 闭嘴闭嘴我不改了！

(#act1f)

# act1e_no_changetoyes

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 慢性孤独会导致产生过多的皮质醇，提高心血管疾病和中风的风险！

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.fifteencigs}}
b: **十五。根烟。**
{{/if}}

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: 闭嘴闭嘴我改成同意就是了！老天啊！

(#act1f)

# act1e_ignore_subtweet

```
bb({eyes:"fear", mouth:"small"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: All our problematic tweets have come back to roost!

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.7;
```

b: We're gonna get called out and cancelled and dragged with a rope on horseback down the information superhighway!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Why are you like this?!

(#act1f)

# act1e_ignore_factcheck

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: We're spreading disinformation! We're destroying trust in a free press!

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: We're the reason fascism will arise from the rubble of democracy!

```
bb({body:"normal", eyes:"anger"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
_.factcheck = true;
```

h: Why are you like this?!

(#act1f)

# act1e_ignore_posture

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Do you want to have a pretzel for a spine?! Stop hunching over your screen!

```
bb({body:"meta"});
```

b: That means you too.

```
bb({body:"normal", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Why are you like this?!

(#act1f)

# act1e_said_ignore

`hong({mouth:"sad", eyes:"sad"});`

h: Hm... that looks really fun.

h: Maybe I shouldn't have ignored the invite?

`bb({mouth:"normal", eyes:"normal"});`

[Keep ignoring, we're still party poopers.](#act1e_ignore_continue)

[Actually, say yes.](#act1e_ignore_changetoyes)

[Actually, say no.](#act1e_ignore_changetono)

# act1e_ignore_continue

`hong({eyes:"annoyed"});`

h: It's kinda rude to keep ignoring them though, no?

`bb({eyes:"normal_right"});`

b: Well other people always ignore *us*, so

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

b: so let's just call it even.

(#act1f)

# act1e_ignore_changetoyes

`hong({eyes:"surprise", mouth:"smile"});`

h: You're... letting me have fun?

b: Well, I mean, loneliness *can* kill us.

`hong({eyes:"neutral", mouth:"neutral"});`

(#act1e_no_changetoyes)

# act1e_ignore_changetono

`bb({eyes:"narrow"});`

b: It's too crowded. Crowds are dangerous.

(#act1e_yes_changetono)


# act1f

```
hong({mouth:"neutral", eyes:"neutral"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: Whatever. New Tinder notification.

`bb({eyes:"uncertain"})`

b: What, that hookup app?

`hong({eyes:"annoyed"})`

h: It's not a hookup app, it's just a way to meet new peopl--

`bb({eyes:"narrow"})`

b: It's a hookup app.

```
hong({eyes:"surprise", mouth:"smile"});
bb({eyes:"normal"});
```

h: Oh, I got a match! They look cute!

```
bb({eyes:"narrow_eyebrow"});
hong({eyes:"sad", mouth:"anger"})
```

h: Please don't ruin this for m--

```
bb({body:"panic"});
Game.OVERRIDE_TEXT_SPEED = 2.0;
```

b: DANGER DANGER DANGER DANGER DANGER DANGER

`bb({body:"fear", eyes:"fear", mouth:"normal"})`

[We're being *used* by other people.](#act1f_used_by_others)

[We're just *using* other people.](#act1f_using_others)

[YOUR MATCH IS A SERIAL KILLER](#act1f_killer)

# act1f_used_by_others

`bb({body:"point_crotch", eyes:"normal", mouth:"normal"})`

b: Random hookups may be able to fill the hole down there,

b: but they can never fill the hole...

`bb({body:"point_heart", eyes:"pretty", mouth:"small"})`

b: in *here*.

(...1000)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: The point is WE'RE GOING TO DIE ALONE

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.hookuphole=true`

(#act1g)

# act1f_using_others

`bb({eyes:"narrow", mouth:"small"})`

b: You think other people's genitals are Pokémon for us to collect?

```
bb({body:"sing", eyes:"pretty", mouth:"shut"});
music("pokemon");
Game.clearText();
Game.FORCE_CANT_SKIP = true;
```

```
Game.FORCE_TEXT_DURATION = 1000;
Game.FORCE_NO_VOICE = true;
```

b: ♫ (pokemon theme song)-

(...5600)

```
bb({mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2400;
```

b: ♫ I wanna be, the ^slut^ti-est-

(...500)

```
bb({eyes:"narrow", mouth:"small"});
Game.FORCE_TEXT_DURATION = 2100;
```

b: ♫ Like no one ever was-

(...1500)

```
bb({eyes:"pretty"});
Game.FORCE_TEXT_DURATION = 2300;
```

b: ♫ Thighs n' ^ass^, voluptuous breast-

(...500)

```
bb({eyes:"fear", mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2000;
```

b: ♫ with sweaty ^dick^ and balls!-

(...1000)

```
bb({eyes:"smile", mouth:"smile"});
Game.FORCE_TEXT_DURATION = 1000;
```

b: ♫ PERVY-MON! GOTTA CA-

```
Game.FORCE_CANT_SKIP = false;
Game.clearText();
music(false);
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: The point is we're a manipulative creep.

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`_.pokemon=true`

(#act1g)

# act1f_killer

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.whitebread}}
b: They'll trap you in a well and force-feed you white bread to fatten you up so they can wear your skin like a suit!
{{/if}}

{{if _.parasite}}
b: They'll bludgeon you with a pomodoro timer and say "YOU SHOULDA BEEN MORE PRODUCTIVE YOU PARASITE"
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: They'll tear your flesh to gory confetti, turn your entrails into streamers, and mix your blood into a punch bowl!
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: How's THAT for a party invite?!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.serialkiller=true`

(#act1g)

# act1g

```
bb({body:"normal", mouth:"normal", eyes:"look"});
hong({body:"2_tired"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
music(false);
```

h: ...

(...500)

h: i'm so sick of this game.

(...700)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h:
{{if _.fifteencigs}}"loneliness will kill us"... {{/if}}
{{if _.parasite}}"we're a society-parasite"... {{/if}}
{{if _.whitebread}}"don't eat that, it'll kill us"... {{/if}}
{{if _.subtweet}}"they're talking behind our back"... {{/if}}
{{if _.badnews}}"the world is burning"... {{/if}}
{{if _.hookuphole}}"we'll die alone"... {{/if}}
{{if _.serialkiller}}"they're a serial killer"... {{/if}}
{{if _.catmilk}}"cats can't digest milk"... {{/if}}
{{if _.pokemon}}a ^crappy^ parody song... {{/if}}

h: i just want to live my life.

h: i just want to be free from all this... pain.

`bb({eyes:"look_sad"});`

b: Hey... human...

`Game.OVERRIDE_TEXT_SPEED = 0.5;`

b: It'll be okay.

(...600)

`bb({body:"point_heart", eyes:"look_sad_smile", mouth:"smile"});`

b: As your loyal guard-wolf, I'll always keep an eye out for danger, and do my best to keep you safe.

`bb({body:"normal", eyes:"look_sad", mouth:"smile"});`

b: I promise.

(...600)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({body:"phone1", eyes:"neutral", mouth:"neutral"});
```

h: Last app. Instagram. What you got?

`hong({eyes:"sad"});`

h: It's... more party pictures.

`hong({mouth:"sad"});`

h: Everyone looks so happy. Free from worry. Free from anxiety.

`hong({mouth:"anger"});`

h: God, why can't I be like them? Why can't I just be *normal?*

`bb({eyes:"normal_right"});`

b: Speaking of parties, about this weekend's invite. Here's my FINAL decision:

`bb({eyes:"normal"});`

[We should go.](#act1g_go) `Game.OVERRIDE_CHOICE_LINE=true`

[We should not go.](#act1g_dont) `Game.OVERRIDE_CHOICE_LINE=true`

# act1g_go

`_.act1g = "go"`

(#act1h)

# act1g_dont

`_.act1g = "dont"`

(#act1h)

# act1h

b: We sh--

```
bb({eyes:"wat", mouth:"small"});
hong({body:"2_fuck"});
```

h: *^FUCK^.*

`hong({body:"2_you"});`

h: YOU.

(...500)

b: w

(...1500)

`bb({eyes:"wat_2"});`

b: wha?

`hong({body:"phone1", eyes:"anger", mouth:"anger"});`

h: I'm going to say YES to that party,

{{if _.act1g=="go"}}
h: NOT because you want me to, but because *I* want to.
{{/if}}

{{if _.act1g=="dont"}}
h: Precisely BECAUSE you don't want me to.
{{/if}}

```
hong({body:"putaway"});
sfx("rustle");
```

h: You're NOT in control of me.

```
sfx("rustle2");
hong({body:"0_sammich", eyes:"0_annoyed", mouth:"0_neutral"});
```

h: Now excuse me while I eat this delicious sandwich in ^goddamn^ peace.

`hong({body:"2_sammich_eat"});`

(...601)

```
sfx("sandwich");
hong({body:"2_sammich_eaten", eyes:"0_lookaway", mouth:"0_chew1"})
```

(...601)

```
bb({body:"normal", eyes:"uncertain", mouth:"shut"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
```

b: ...

```
bb({eyes:"normal_right"});
Game.OVERRIDE_TEXT_SPEED = 1;
```

b: ...

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 4;
```

b: ..................

(...500)

`bb({mouth:"normal"});`

[AHHHH WE'RE GONNA DIE](#act1h_death) `Game.OVERRIDE_CHOICE_LINE = true;`

[AHHHH EVERYONE HATES US](#act1h_loneliness) `Game.OVERRIDE_CHOICE_LINE = true;`

[AHHHH WE'RE HORRIBLE PEOPLE](#act1h_worthless) `Game.OVERRIDE_CHOICE_LINE = true;`

# act1h_death

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHH WE'RE GONNA DIE AAAAAAHHHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "harm");
```

(...2500)

(#act1i)

# act1h_loneliness

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHH EVERYONE HATES US AAAAAAHHHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "alone");
```

(...2500)

(#act1i)

# act1h_worthless

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: AHHHH WE'RE HORRIBLE PEOPLE AAAAAAHHHHHHH

```
hong({body:"3_defeated1"});
attack("100p", "bad");
```

(...2500)

(#act1i)

# act1i

```
bb({mouth:"smile_lock", eyes:"smile", body:"normal"});
music('battle', {volume:0.5});
```

n: CONGRATULATIONS

(...500)

n: YOU'VE SUCCESSFULLY PROTECTED YOUR HUMAN'S PHYSICAL + SOCIAL + MORAL NEEDS

n: WHY, LOOK HOW GRATEFUL THEY ARE!

(...500)

n: NOW THAT THEIR ENERGY IS ZERO, YOU CAN DIRECTLY CONTROL THEIR ACTIONS

`bb({mouth:"smile", eyes:"normal"});`

n: PICK YOUR ENDING MOVE

`bb({mouth:"small_lock", eyes:"fear"});`

n: *FINISH THEM*

[{FIGHT: Punish your stressful phone!}](#act1i_phone) `Game.OVERRIDE_CHOICE_LINE=true`

[{FLIGHT: Curl up in a ball and cry!}](#act1i_cry) `Game.OVERRIDE_CHOICE_LINE=true`

# act1i_phone

`bb({mouth:"normal", eyes:"narrow"})`

b: Your phone was giving you a panic attack!

`bb({eyes:"anger"})`

b: Zuckerberg and Co are hijacking your mental health for venture capitalist money!

```
bb({body:"fear", eyes:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Punish your phone! Destroy it! Kill it!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "fight";
```

b: KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL IT KILL I--

(#act1j)

# act1i_cry

`bb({eyes:"fear", mouth:"normal"})`

b: The whole world is filled with danger!

```
bb({body:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Do like the armadillo! Curl up into a ball for self-defense!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "flight";
```

b: CURL UP AND CRY CURL UP AND CRY CURL UP AND CRY CURL UP AND CRY CURL UP AND CRY CURL UP AND CR-- 

(#act1j)

# act1j

`SceneSetup.act1_outro()`
