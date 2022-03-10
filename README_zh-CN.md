# fanyi.cli
一个基于百度翻译API的命令行翻译软件。

[Reading in English](README.md)

## 安装
直接下载`fanyi.cli.py`即可。

## 初次上手
### 对于Linux用户（可能还包括macOS用户）
直接运行 `./fanyi.cli.py` 即可。如果报错，请检查是否安装了python3，以及是否将python3的可执行文件或者符号链接添加到了 `/usr/bin`目录下，然后再试一次。

### 对于Windows用户
确认是否在电脑上安装了python3。然后在命令行窗口中运行 `python3 fanyi.cli.py`。

### 语言支持
本程序目前仅支持中译英和英译中。可以通过添加`-z`, `-c`或者`-e`参数以指定翻译到哪一种语言。如果不指定，程序将自动选择翻译的目标语言。

### 翻译文件
本程序目前仅支持纯文本文件的翻译（例如，`.txt`后缀的文件）。可以通过添加 `-f [FILE PATH]` 参数指定文件翻译模式。

## 示例
### 翻译文字
```
$ fanyi.cli.py
# Input text:
Speaking a foreign language is a high demand skill because of domestic cultural diversity and the number of companies doing business abroad. Foreign language skills can help you get jobs by enhancing your qualifications.
# Result:
由于国内文化的多样性和在国外做生意的公司的数量，说一门外语是一项高要求的技能。外语技能可以通过提高你的资历来帮助你找到工作。
```

### 从标准输入输出中进行翻译
```
$ fanyi.cli.py -t "Our understanding of the distribution of genetic variation in natural populations has been driven by mathematical models of the underlying biological and demographic processes. A key strength of such coalescent models is that they enable efficient simulation of data we might see under a variety of evolutionary scenarios."
# Result:
我们对自然种群中遗传变异分布的理解是由潜在生物和人口过程的数学模型驱动的。这种结合模型的一个关键优势是，它们能够有效地模拟我们在各种进化场景下可能看到的数据。
```

### 翻译文件
```
$ fanyi.cli.py --ori -f 'The Selfish Gene.txt'  # use `--ori` argument to show origin text.
# Origin:
Intelligent life on a planet comes of age when it first works out the reason for its own existence. If superior creatures from space ever visit earth, the first question they will ask, in order to assess the level of our civilization,is: 'Have they discovered evolution yet?' Living organisms had existed on earth, without ever knowing why,for over three thousand million years before the truth finally dawned on one of them. His name was Charles Darwin. To be fair,others had had inklings of the truth, but it was Darwin who first put together a coherent and tenable account of why we exist.Darwin made it possible for us to give a sensible answer to the curious child whose question heads this chapter. We no longer have to resort to superstition when faced with the deep problems: Is there a meaning to life? What are we for? What is man? After posing the last of these questions, the eminent zoologist G.G.Simpson put it thus: 'The point I want to make now is that all attempts to answer that question before 1859 are worthless and that we will be better off if we ignore them completely.'


# Result:
当行星上的智慧生命第一次找到自己存在的原因时，它就成熟了。如果来自太空的高级生物访问过地球，为了评估我们的文明水平，他们会问的第一个问题是：“他们发现进化了吗？”生命有机体在地球上已经存在了三十亿年，却不知道为什么，直到其中一个终于明白了真相。他的名字叫查尔斯·达尔文。平心而论，其他人已经对真相有所了解，但正是达尔文首先对我们存在的原因做出了一个前后一致、站得住脚的解释。达尔
文使我们有可能给这个好奇的孩子一个合理的答案，这个孩子的问题是本章的主题。当我们面临深层次的问题时，我们不再需要诉诸迷信：生命有意义吗？我们在干什么？人是什么？在提出了这些问题中的最后一个之后，著名动物学家G.G.辛普森这样说：“我现在想指出的一点是，在1859年之前回答这个问题的所有尝试都是毫无价值的，如果我们完全忽略它们，我们会过得更好。”
```

