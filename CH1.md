# Functional-Light JavaScript
# 第一章：为什么是函数式编程？

总而言之函数式编程不算是一个新的概念，它几乎存在任何编程语言之中。我不知道这样说是否客观，但它确实看起来不像是一个在整个开发者世界中作为主流的概念直到最近几年。我觉得函数式编程更像是一个学术领域。

但是世界总是在变化，函数式编兴趣风潮日益高涨，不仅仅是在语言层面上甚至在一些库和框架之中，阅读这篇文章你可能会觉得很棒，因为你终于意识到了函数式编程是一个你无法继续忽视的事情，或者你可能像我一样之前尝试很多次去学习函数式编程但只是在努力去读完它所有的概念和数学符号。

无论是你出于何种原因阅读这本书，欢迎加入函数式编程的阵营。

## 自信心

我有一个很简单的前提就是我所做的一切是我在软件开发中的老师（使用Javascript）：你不能去信任那些你不懂的代码。而且，如果你不信任或者理解你的代码，无论怎么样你都会对你写的代码是否满足你的业务都会没有信心，你只能祈求好运让你的程序能够运行。

信任是什么意思？我的意思是一种你能通过阅读你的代码去较验，而不仅是通过运行，而且了解任何一块代码的将会做什么，不仅仅依赖它应该会做什么。也许我们更经常倾向于运行单元测试来检查我们程序的正确性。我的意思不是说单元测试不好。但是我觉得我们应该对我们写的代码了解的足够深入，这样在运行单元测试之前我们也有信心一定能够通过。

我相信形成函数式编程的基础技术来源于一种思维模式，即可以仅仅通过阅读我们的程序就可以拥有更多的信心，那些了解函数式编程以及经常在编程中使用的人，他们的代码是很容易阅读和检查的，通过那些他们已经证明过是正确的原则，得到他们想要的运行结果。

我希望从现在开始你将有更多的信心去编写你的代码，这里的轻量函数式编程原则将会指引你前往正确的方向。

## 交流

为什么函数式编程很重要，想回答这个问题，我们需要往后退一大步去讨论为什么编程很重要；

你听到这些也许会觉得很意外，但我不认为代码的存在主要是为了操控计算机。事实上，我觉得代码操控计算实际上只是一个幸运的意外。

我深信代码最重要的作用是作为人与人之间的一种沟通方式。

你可能有过这样的经历就是你大部分“编程”时间实际上是在阅读你写过的代码。我们之间很少有人能有特权可以倾注所有或者大部分时间用来编写新的程序而不需要去维护那些别人或者自己写过的代码。

你知道研究这个课题的研究人员说我们一天花费在代码上的时间有70%是用来读懂它吗？这令我很震憾， 70%是什么概念？难怪全球的开发者每个人一天平均只能写5行左右的代码。一天之中我们花费另外的7个小时30分钟只是用来阅读代码并找出这5行代码应该如何运行。

我觉得我们关注更多，比如我们代码的可读性等等。当然，可读性并不代表更少的字符。事实上，可读性更多来源于熟悉，（也就是我们曾经学过的）。所以，如果我们打算花费一些时间去考虑如何让代码更加容易读懂，函数式编程这一种很好用的模式将会非常有用。函数式编程原则是很完善，经过深入研究和审查，充分证明过的。

如果我们使用函数式编程的规范，我相信我们所编写的代码将会更容易理解。一旦我们理解这些规范，它们在代码里将会是熟悉和可识别的，意思是说当我们阅读代码时我们将会花更少的时间去理解它们的用意。我们的注意力将会转移到我们都很熟悉的部分，如何建立组装乐高积木，而不是乐高模块的意义。

函数式编程（至少，没有很多的专业术语让它更容易接受）是一种很高效的工具用于编写可读性很高的代码。这也是它如此重要的原因。


## Take

We're going to approach FP from the ground up, and uncover the basic foundational principles that I believe formal FPers would admit are the scaffolding for everything they do. But for the most part we'll stay arms length away from most of the intimidating terminology or mathematical notation that can so easily frustrate learners.

I believe it's less important what you call something and more important that you understand what it is and how it works. That's not to say there's no importance to shared terminology -- it undoubtedly eases communication among seasoned professionals. But for the learner, I've found it can be somewhat distracting.

So I hope this book can focus more on the base concepts and less on the fancy terminology. That's not to say there won't be terminology; there definitely will be. But don't get too wrapped up in the fancier words. Look beyond them to the ideas. That's what this book is trying to be about.

I call the less formal practice herein "Functional-Light Programming" because I think where the formalism of true FP suffers is that it can be quite overwhelming if you're not already accustomed to formal thought. I'm not just guessing; this is my own personal story. Even after teaching FP and writing this book, I can still say that the formalism of terms and notation in FP is very, very diffcult for me to process. I've tried, and tried, and I can't seem to get through much of it.

I know many FPers who believe that the formalism itself helps learning. But I think there's clearly a cliff where that only becomes true once you reach a certain comfort with the formalism. If you happen to already have a math background or even some flavors of CS experience, this may come more naturally to you. But some of us don't, and no matter how hard we try, the formalism keeps getting in the way.

So this book introduces the concepts that I believe FP is built on, but comes at it by giving you a boost to climb up the cliff wall rather than throwing you straight at it to figure out how to climb as you go.

## YAGNI

If you've been around programming for very long, chances are you've heard the phrase "YAGNI" before: "You Ain't Gonna Need It". This principle primarily comes from extreme programming, and stresses the high risk and cost of building a feature before it's needed.

Sometimes we guess we'll need a feature in the future, build it now believing it'll be easier to do as we build other stuff, then realize we guessed wrong and the feature wasn't needed, or needed to be quite different. Other times we guess right, but build a feature too early, and suck up time from the features that are genuinely needed now; we incur an opportunity cost in diluting our energy.

YAGNI challenges us to remember: even if it's counter intuitive in a situation, we often should postpone building something until it's presently needed. We tend to exaggerate our mental estimates of the future refactoring cost of adding it later when it is needed. Odds are, it won't be as hard to do later as we might assume.

As it applies to functional programming, I would give this admonition: there will be plenty of interesting and compelling patterns discussed in this text, but just because you find some pattern exciting to apply, it may not necessarily be appropriate to do so in a given part of your code.

This is where I will differ from many more formal FPers: just because you *can* FP something doesn't mean you *should* FP it. Moreover, there are many ways to slice a problem, and even though you may have learned a more sophisticated approach that is more "future-proof" to maintenance and extensibility, a simpler FP pattern might be more than sufficient in that spot.

Generally, I'd recommend to seek balance in what you code, and to be conservative in your application of FP concepts as you get the hang of things. Default to the YAGNI principle in deciding if a certain pattern or abstraction will help that part of the code be more readable or if it's just introducing more clever sophistication that isn't (yet) warranted.

> Reminder, any extensibility point that’s never used isn’t just wasted effort, it’s likely to also get in your way as well
>
> Jeremy D. Miller @jeremydmiller 2/20/15
>
> https://twitter.com/jeremydmiller/status/568797862441586688

Remember, every single line of code you write has a reader cost associated with it. That reader may be another team member, or even your future self. Neither of those readers will be impressed with overly clever unnecessary sophistication to show off your FP agility.

The best code is the code that is most readable in the future because it strikes exactly the right balance between what it can/should be (idealism) and what it must be (pragmatism).

## Resources

I have drawn on a great many different resources to be able to compose this text. I believe you too may benefit from them, so I wanted to take a moment to point them out.

### Books

Some FP/JavaScript books that you should definitely read:

* [Professor Frisbee's Mostly Adequate Guide to Functional Programming](https://drboolean.gitbooks.io/mostly-adequate-guide/content/ch1.html) by [Brian Lonsdorf](https://twitter.com/drboolean)
* [JavaScript Allongé](https://leanpub.com/javascript-allonge) by [Reg Braithwaite](https://twitter.com/raganwald)
* [Functional JavaScript](http://shop.oreilly.com/product/0636920028857.do) by [Michael Fogus](https://twitter.com/fogus)

### Blogs/Sites

Some other authors and content you should check out:

* [Fun Fun Function Videos](https://www.youtube.com/watch?v=BMUiFMZr7vk) by [Mattias P Johansson](https://twitter.com/mpjme)
* [Awesome FP JS](https://github.com/stoeffel/awesome-fp-js)
* [Kris Jenkins](http://blog.jenkster.com/2015/12/what-is-functional-programming.html)
* [Eric Elliott](https://medium.com/@_ericelliott)
* [James A Forbes](https://james-forbes.com/)
* [James Longster](https://github.com/jlongster)
* [André Staltz](http://staltz.com/)
* [Functional Programming Jargon](https://github.com/hemanth/functional-programming-jargon#functional-programming-jargon)

### Libraries

The code snippets in this book do not use libraries. Each operation that we discover, we'll derive how to implement it in standalone, plain ol' JavaScript. However, as you begin to build more of your real code with FP, you'll quickly want a library to provide optimized and highly reliable versions of these commonly accepted utilities.

By the way, you'll want to make sure you check the documentation for the library functions you use to make sure you know how they work. There will be a lot of similarities in many of them to the code we build on in this text, but there will undoubtedly be some differences, even between popular libraries.

Here are a few popular FP libraries for JavaScript that are a great place to start your exploration with:

* [Ramda](http://ramdajs.com)
* [lodash/fp](https://github.com/lodash/lodash/wiki/FP-Guide)
* [functional.js](http://functionaljs.com/)
* [Immutable.js](https://github.com/facebook/immutable-js)

Appendix C illustrates some of these libraries using various examples from the text.

## Summary

This is Functional-Light JavaScript. The goal is to learn to communicate with our code but not suffocate under mountains of notation or terminology to get there. I hope this book jumpstarts your journey!