# Bartosz Milewski's Programming Cafe

Category Theory, Haskell, Concurrency, C++

범주론, Haskell, 동시성, C++

October 28, 2014

2014년 10월 28일

## Category Theory for Programmers: The Preface

프로그래머를 위한 범주론: 서문

Posted by Bartosz Milewski under , , , ,

## Table of Contents

목차

### Part One

첫 번째 부

- Category: The Essence of Composition
- 범주론: 합성의 본질
- Types and Functions
- 타입과 함수
- Categories Great and Small
- 크고 작은 범주들
- Kleisli Categories
- Kleisli 범주
- Products and Coproducts
- 곱과 여곱
- Simple Algebraic Data Types
- 단순 대수 데이터 타입
- Functors
- 함자
- Functoriality
- 함자성
- Function Types
- 함수 타입
- Natural Transformations
- 자연 변환

### Part Two

두 번째 부

- Declarative Programming
- 선언형 프로그래밍
- Limits and Colimits
- 극한과 여극한
- Free Monoids
- 자유 모노이드
- Representable Functors
- 표현 가능한 함자
- The Yoneda Lemma
- Yoneda 보조정리
- Yoneda Embedding
- Yoneda 임베딩

### Part Three

세 번째 부

- It's All About Morphisms
- 모든 것은 사상에 관한 것이다
- Adjunctions
- 수반
- Free/Forgetful Adjunctions
- 자유/망각 수반
- Monads: Programmer's Definition
- 모나드: 프로그래머의 정의
- Monads and Effects
- 모나드와 효과
- Monads Categorically
- 범주론적 모나드
- Comonads
- 쌍대 모나드
- F-Algebras
- F-대수
- Algebras for Monads
- 모나드를 위한 대수
- Ends and Coends
- 끝과 여끝
- Kan Extensions
- Kan 확대
- Enriched Categories
- 풍부해진 범주
- Topoi
- 토포이
- Lawvere Theories
- Lawvere 이론
- Monads, Monoids, and Categories
- 모나드, 모노이드, 범주

There is a free pdf version of this book with nicer typesetting available for download. You may order a hard-cover version with color illustrations at Blurb. Or you may watch me teaching this material to a live audience.

더 나은 조판의 이 책의 무료 PDF 버전이 다운로드로 제공된다. Blurb에서 색상 삽화가 있는 하드커버 버전을 주문할 수 있다. 또는 내가 실시간 청중을 대상으로 이 자료를 가르치는 것을 볼 수 있다.

# Preface

서문

For some time now I've been floating the idea of writing a book about category theory that would be targeted at programmers. Mind you, not computer scientists but programmers — engineers rather than scientists. I know this sounds crazy and I am properly scared. I can't deny that there is a huge gap between science and engineering because I have worked on both sides of the divide. But I've always felt a very strong compulsion to explain things. I have tremendous admiration for Richard Feynman who was the master of simple explanations. I know I'm no Feynman, but I will try my best. I'm starting by publishing this preface — which is supposed to motivate the reader to learn category theory — in hopes of starting a discussion and soliciting feedback.

오랫동안 나는 프로그래머를 대상으로 범주론에 관한 책을 쓸 생각을 해왔다. 물론 컴퓨터 과학자가 아니라 프로그래머를 말하고 있으며, 과학자가 아니라 엔지니어를 말하고 있다. 이것이 미친 생각처럼 들린다는 것을 알고 있고, 정말로 두렵다. 나는 과학과 엔지니어링 사이에 엄청난 간격이 있다는 것을 부정할 수 없다. 왜냐하면 나는 양쪽 진영에서 일해봤기 때문이다. 하지만 나는 항상 무언가를 설명하고 싶은 강한 충동을 느껴왔다. 나는 단순한 설명의 대가였던 Richard Feynman을 매우 존경한다. 나는 Feynman은 아니지만, 최선을 다할 것이다. 나는 이 서문을 발행함으로써 시작하고 있으며, 이것은 독자들이 범주론을 배우도록 동기부여하기 위한 것이고, 토론을 시작하고 피드백을 구하기를 희망한다.

I will attempt, in the space of a few paragraphs, to convince you that this book is written for you, and whatever objections you might have to learning one of the most abstract branches of mathematics in your "copious spare time" are totally unfounded.

나는 몇 개의 단락에서 이 책이 당신을 위해 쓰였다는 것을 설득하려고 노력할 것이다. 그리고 당신의 "넉넉한 여유 시간"에 가장 추상적인 수학 분야 중 하나를 배우는 것에 대해 가질 수 있는 어떤 반대도 완전히 근거가 없다.

My optimism is based on several observations. First, category theory is a treasure trove of extremely useful programming ideas. Haskell programmers have been tapping this resource for a long time, and the ideas are slowly percolating into other languages, but this process is too slow. We need to speed it up.

내 낙관주의는 여러 관찰에 기반한다. 첫째, 범주론은 극도로 유용한 프로그래밍 아이디어의 보물창고이다. Haskell 프로그래머들은 오랫동안 이 자원을 활용해왔고, 아이디어들이 천천히 다른 언어들로 스며들고 있지만, 이 과정은 너무 느리다. 우리는 그것을 가속화해야 한다.

Second, there are many different kinds of math, and they appeal to different audiences. You might be allergic to calculus or algebra, but it doesn't mean you won't enjoy category theory. I would go as far as to argue that category theory is the kind of math that is particularly well suited for the minds of programmers. That's because category theory — rather than dealing with particulars — deals with structure. It deals with the kind of structure that makes programs composable.

둘째, 수학에는 여러 종류가 있으며, 각각 다른 청중을 끈다. 당신이 미적분학이나 대수학에 거부감이 있을 수 있지만, 그것이 당신이 범주론을 즐기지 않을 것이라는 의미는 아니다. 나는 범주론이 특히 프로그래머의 마음에 잘 맞는 수학의 종류라고까지 주장할 것이다. 그 이유는 범주론이 특수한 것을 다루기보다는 구조를 다루기 때문이다. 그것은 프로그램을 합성 가능하게 만드는 구조를 다룬다.

Composition is at the very root of category theory — it's part of the definition of the category itself. And I will argue strongly that composition is the essence of programming. We've been composing things forever, long before some great engineer came up with the idea of a subroutine. Some time ago the principles of structured programming revolutionized programming because they made blocks of code composable. Then came object oriented programming, which is all about composing objects. Functional programming is not only about composing functions and algebraic data structures — it makes concurrency composable — something that's virtually impossible with other programming paradigms.

합성은 범주론의 매우 근본에 있다. 그것은 범주 자체의 정의의 일부이다. 그리고 나는 합성이 프로그래밍의 본질이라고 강력하게 주장할 것이다. 우리는 위대한 엔지니어가 서브루틴이라는 개념을 생각해내기 훨씬 전부터 항상 무언가를 합성해왔다. 얼마 전 구조화된 프로그래밍의 원칙들이 프로그래밍을 혁명화했는데, 그것은 코드 블록을 합성 가능하게 만들었기 때문이다. 그 다음 객체지향 프로그래밍이 나왔는데, 그것은 모두 객체를 합성하는 것에 관한 것이다. 함수형 프로그래밍은 함수와 대수 데이터 구조를 합성하는 것만이 아니다. 그것은 동시성을 합성 가능하게 만든다. 이는 다른 프로그래밍 패러다임에서는 사실상 불가능한 것이다.

Third, I have a secret weapon, a butcher's knife, with which I will butcher math to make it more palatable to programmers. When you're a professional mathematician, you have to be very careful to get all your assumptions straight, qualify every statement properly, and construct all your proofs rigorously. This makes mathematical papers and books extremely hard to read for an outsider. I'm a physicist by training, and in physics we made amazing advances using informal reasoning. Mathematicians laughed at the Dirac delta function, which was made up on the spot by the great physicist P. A. M. Dirac to solve some differential equations. They stopped laughing when they discovered a completely new branch of calculus called distribution theory that formalized Dirac's insights.

셋째, 나는 비밀 무기, 정육점 칼을 가지고 있다. 이것으로 나는 프로그래머들이 더 쉽게 이해할 수 있도록 수학을 잘라낼 것이다. 당신이 전문 수학자일 때, 당신은 모든 가정을 정확히 정하고, 모든 진술을 적절하게 한정하고, 모든 증명을 엄밀하게 구성해야 한다. 이것은 수학 논문과 책을 외부인이 읽기 매우 어렵게 만든다. 나는 물리학자로 훈련받았고, 물리학에서 우리는 비공식적 추론을 사용하여 놀라운 진전을 이루었다. 수학자들은 위대한 물리학자 P. A. M. Dirac이 일부 미분 방정식을 풀기 위해 즉석에서 만든 Dirac 델타 함수를 웃었다. 그들이 Dirac의 통찰을 정형화하는 분포 이론이라는 미적분학의 완전히 새로운 분야를 발견했을 때 그들은 웃음을 멈췄다.

Of course when using hand-waving arguments you run the risk of saying something blatantly wrong, so I will try to make sure that there is solid mathematical theory behind informal arguments in this book. I do have a worn-out copy of Saunders Mac Lane's Category Theory for the Working Mathematician on my nightstand.

물론 손짓 논증을 사용할 때 명백히 잘못된 것을 말할 위험이 있으므로, 나는 이 책의 비공식적 논증 뒤에 견고한 수학 이론이 있음을 확인하려고 노력할 것이다. 나는 침대 옆탁자에 Saunders Mac Lane의 "Working Mathematician을 위한 범주론"의 낡은 복사본을 가지고 있다.

Since this is category theory for programmers I will illustrate all major concepts using computer code. You are probably aware that functional languages are closer to math than the more popular imperative languages. They also offer more abstracting power. So a natural temptation would be to say: You must learn Haskell before the bounty of category theory becomes available to you. But that would imply that category theory has no application outside of functional programming and that's simply not true. So I will provide a lot of C++ examples. Granted, you'll have to overcome some ugly syntax, the patterns might not stand out from the background of verbosity, and you might be forced to do some copy and paste in lieu of higher abstraction, but that's just the lot of a C++ programmer.

이것이 프로그래머를 위한 범주론이므로, 나는 모든 주요 개념을 컴퓨터 코드를 사용하여 설명할 것이다. 당신은 함수형 언어가 더 인기 있는 명령형 언어보다 수학에 더 가깝다는 것을 아마도 알고 있을 것이다. 또한 더 많은 추상화 능력을 제공한다. 그래서 자연스러운 유혹은 다음과 같이 말하는 것이다: 범주론의 풍성함이 당신에게 이용 가능해지기 전에 Haskell을 배워야 한다. 하지만 그것은 범주론이 함수형 프로그래밍 외에 응용이 없다는 것을 의미할 것이고, 그것은 단순히 사실이 아니다. 그래서 나는 많은 C++ 예제를 제공할 것이다. 인정하지만, 당신은 일부 못생긴 문법을 극복해야 하고, 패턴이 장황함의 배경에서 두드러질 수 없을 수도 있으며, 더 높은 추상화 대신 복사 붙여넣기를 하도록 강요받을 수 있지만, 그것은 C++ 프로그래머의 숙명일 뿐이다.

But you're not off the hook as far as Haskell is concerned. You don't have to become a Haskell programmer, but you need it as a language for sketching and documenting ideas to be implemented in C++. That's exactly how I got started with Haskell. I found its terse syntax and powerful type system a great help in understanding and implementing C++ templates, data structures, and algorithms. But since I can't expect the readers to already know Haskell, I will introduce it slowly and explain everything as I go.

하지만 Haskell에 관한 한 당신은 면제되지 않는다. 당신이 Haskell 프로그래머가 될 필요는 없지만, C++에서 구현할 아이디어를 스케칭하고 문서화하기 위한 언어로서 필요하다. 이것이 정확히 내가 Haskell을 시작한 방식이다. 나는 그 간결한 문법과 강력한 타입 시스템이 C++ 템플릿, 데이터 구조, 알고리즘을 이해하고 구현하는 데 매우 도움이 된다는 것을 발견했다. 하지만 독자들이 이미 Haskell을 알고 있다고 기대할 수 없으므로, 나는 천천히 소개하고 진행하면서 모든 것을 설명할 것이다.

If you're an experienced programmer, you might be asking yourself: I've been coding for so long without worrying about category theory or functional methods, so what's changed? Surely you can't help but notice that there's been a steady stream of new functional features invading imperative languages. Even Java, the bastion of object-oriented programming, let the lambdas in C++ has recently been evolving at a frantic pace — a new standard every few years — trying to catch up with the changing world. All this activity is in preparation for a disruptive change or, as we physicist call it, a phase transition. If you keep heating water, it will eventually start boiling. We are now in the position of a frog that must decide if it should continue swimming in increasingly hot water, or start looking for some alternatives.

당신이 경험 많은 프로그래머라면, 당신은 자신에게 물어볼 수 있다: 나는 범주론이나 함수형 메서드를 걱정하지 않고 오랫동안 코드를 작성해왔는데, 무엇이 변했는가? 당신은 새로운 함수형 기능이 명령형 언어로 꾸준히 침입해오고 있다는 것을 알아채지 않을 수 없다. 객체지향 프로그래밍의 보루인 Java도 람다를 허용했고, C++는 최근에 미친 속도로 진화하고 있다. 몇 년마다 새로운 표준이 변하는 세상을 따라잡으려고 노력하고 있다. 이 모든 활동은 파괴적인 변화, 또는 우리 물리학자들이 부르는 것처럼 상전이를 준비하기 위한 것이다. 계속 물을 데우면 결국 끓기 시작한다. 우리는 지금 계속 뜨거워지는 물에서 헤엄쳐야 할지, 아니면 대안을 찾아야 할지를 결정해야 하는 개구리의 위치에 있다.

One of the forces that are driving the big change is the multicore revolution. The prevailing programming paradigm, object oriented programming, doesn't buy you anything in the realm of concurrency and parallelism, and instead encourages dangerous and buggy design. Data hiding, the basic premise of object orientation, when combined with sharing and mutation, becomes a recipe for data races. The idea of combining a mutex with the data it protects is nice but, unfortunately, locks don't compose, and lock hiding makes deadlocks more likely and harder to debug.

큰 변화를 주도하는 힘 중 하나는 멀티코어 혁명이다. 현재의 프로그래밍 패러다임인 객체지향 프로그래밍은 동시성과 병렬성의 영역에서 당신에게 아무것도 제공하지 않으며, 대신 위험하고 버그가 있는 설계를 조장한다. 데이터 숨김, 객체지향의 기본 전제는 공유와 변이와 결합되면 데이터 경쟁의 레시피가 된다. mutex를 그것이 보호하는 데이터와 결합하는 생각은 좋지만, 불행하게도 락은 합성되지 않으며, 락을 숨기는 것은 교착 상태를 더 가능하게 하고 디버깅을 더 어렵게 만든다.

But even in the absence of concurrency, the growing complexity of software systems is testing the limits of scalability of the imperative paradigm. To put it simply, side effects are getting out of hand. Granted, functions that have side effects are often convenient and easy to write. Their effects can in principle be encoded in their names and in the comments. A function called SetPassword or WriteFile is obviously mutating some state and generating side effects, and we are used to dealing with that. It's only when we start composing functions that have side effects on top of other functions that have side effects, and so on, that things start getting hairy. It's not that side effects are inherently bad — it's the fact that they are hidden from view that makes them impossible to manage at larger scales. Side effects don't scale, and imperative programming is all about side effects.

하지만 동시성이 없더라도, 소프트웨어 시스템의 증가하는 복잡성은 명령형 패러다임의 확장성의 한계를 시험하고 있다. 간단히 말해서, 부작용이 통제 불능 상태가 되고 있다. 인정하지만, 부작용이 있는 함수는 종종 편리하고 쓰기 쉽다. 그들의 효과는 원칙적으로 그들의 이름과 주석에 인코딩될 수 있다. SetPassword 또는 WriteFile이라고 불리는 함수는 명백히 어떤 상태를 변이시키고 부작용을 생성하며, 우리는 그것을 다루는 데 익숙하다. 부작용이 있는 함수를 부작용이 있는 다른 함수 위에 합성하기 시작할 때, 그리고 이렇게 계속될 때, 상황이 복잡해지기 시작한다. 부작용이 본질적으로 나쁜 것이 아니다. 그것은 그들이 보이지 않는다는 사실이 더 큰 규모에서 그들을 관리하기 불가능하게 만든다. 부작용은 확장되지 않으며, 명령형 프로그래밍은 모두 부작용에 관한 것이다.

Changes in hardware and the growing complexity of software are forcing us to rethink the foundations of programming. Just like the builders of Europe's great gothic cathedrals we've been honing our craft to the limits of material and structure. There is an unfinished gothic cathedral in Beauvais, France, that stands witness to this deeply human struggle with limitations. It was intended to beat all previous records of height and lightness, but it suffered a series of collapses. Ad hoc measures like iron rods and wooden supports keep it from disintegrating, but obviously a lot of things went wrong. From a modern perspective, it's a miracle that so many gothic structures had been successfully completed without the help of modern material science, computer modelling, finite element analysis, and general math and physics. I hope future generations will be as admiring of the programming skills we've been displaying in building complex operating systems, web servers, and the internet infrastructure. And, frankly, they should, because we've done all this based on very flimsy theoretical foundations. We have to fix those foundations if we want to move forward.

하드웨어의 변화와 소프트웨어의 증가하는 복잡성은 우리가 프로그래밍의 기초를 재고하도록 강요하고 있다. 유럽의 웅대한 고딕 건축물을 지은 건축가들처럼, 우리는 우리의 기술을 재료와 구조의 한계까지 연마해왔다. 프랑스 Beauvais에는 미완성된 고딕 대성당이 있으며, 이것은 이 깊은 인간적 한계와의 투쟁을 증명한다. 그것은 높이와 가벼움의 모든 이전 기록을 깨뜨리려고 의도되었지만, 일련의 붕괴를 겪었다. 철근과 나무 지지대와 같은 임시 방편이 그것을 붕괴하는 것으로부터 유지하고 있지만, 명백히 많은 것들이 잘못되었다. 현대적 관점에서, 현대 재료 과학, 컴퓨터 모델링, 유한 요소 분석, 일반 수학 및 물리학의 도움 없이 그렇게 많은 고딕 구조가 성공적으로 완성되었다는 것은 기적이다. 나는 미래의 세대가 복잡한 운영 체제, 웹 서버, 인터넷 인프라를 구축하는 데 있어 우리가 발휘해온 프로그래밍 기술에 대해 존경할 것이기를 희망한다. 그리고 솔직히 말해서, 그들은 마땅히 그래야 한다. 왜냐하면 우리는 매우 약한 이론적 기초 위에서 이 모든 것을 해냈기 때문이다. 앞으로 나아가려면 그 기초를 수정해야 한다.

<!-- image -->

Ad hoc measures preventing the Beauvais cathedral from collapsing

Beauvais 대성당의 붕괴를 방지하는 임시 방편

Next: Category: The Essence of Composition.

다음: 범주론: 합성의 본질
