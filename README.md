# ddd_note
DDDの用語集


[https://vaadin.com/learn/tutorials/ddd/strategic_domain_driven_design](https://vaadin.com/learn/tutorials/ddd/strategic_domain_driven_design)

[https://vaadin.com/learn/tutorials/ddd/tactical_domain_driven_design](https://vaadin.com/learn/tutorials/ddd/tactical_domain_driven_design)

# What is a Domain?

- Domainを構成するもの(vaadin strategic ddd)
    - activity: whatever an organization does
    - knowledge: how the organization does it.
    - environment in which the organization conducts its activities
- A core domain is what makes an organization special and different from other organizations. (vaadin strategic ddd)

## コアドメインへの集中

- A core domain is what makes an organization special and different from other organizations. An organization cannot succeed (or even exist) without being exceptionally good in their core domain. Because the core domain is so important, it should receive the highest priority, the biggest effort and the best developers. For smaller domains you may only identify a single core domain, larger domains may have more than one. You should be prepared to implement the features of the core domain from scratch.
    - 中心の領域は構成を他の組織と特別な、異なったものにするものである。組織は、コアドメインで例外的に優れていなければ、成功することはできない(あるいは存在することさえできない)。コアドメインは非常に重要であるため、最高の優先度、最大の努力、そして最高の開発者を受けるべきである。小規模なドメインの場合はコアドメインを1つしか特定できないかもしれないが、大規模なドメインの場合は複数のコアドメインがあるかもしれない。コアドメインの機能を一から実装する覚悟が必要です。(vaadin strategic ddd)
- Finally, it is worth pointing out that all subdomains are important to the overall solution regardless of the category in which they fall. They do, however, require different amounts of effort and may also have different requirements of quality and completeness.
    - 最後に、サブドメインがどのカテゴリに属するかにかかわらず、すべてのサブドメインがソリューション全体にとって重要であることを指摘しておきます。しかし、これらのサブドメインにはそれぞれ異なる労力が必要であり、また、品質と完全性に対する要求事項も異なる場合があります。(vaadin strategic ddd)

# Ubiquitous language

- To be able to create software for a domain, you need a way of describing the domain. Having a relational data model or something similar is not enough. You need to be able to describe not only things and their relations but also the dynamics such as events, processes, business invariants, how things change over time, and so on. You need to be able to discuss and reason about the domain with both your fellow developers and also the domain experts. What you need is a ubiquitous language.
    - ドメイン用のソフトウェアを作成するためには、ドメインを記述する方法が必要です。リレーショナル・データ・モデルなどを持っているだけでは十分ではありません。物事とその関係だけでなく、イベント、プロセス、ビジネスの不変性、時間の経過とともに変化していく様子などのダイナミクスも記述できる必要があります。また、仲間の開発者だけでなく、ドメインの専門家と議論したり、推論したりすることができる必要があります。必要なのはユビキタス言語です。(vaadin strategic ddd)
- The ubiquitous language is a language that is consistently used by both domain experts and developers to describe and discuss the domain. Apart from the code itself, this language is the most important deliverable of a domain-driven design process. A big part of the language is domain terminology already being used by domain experts, but you may also need to invent new concepts and processes in cooperation with the domain experts. Because of this, active participation from the domain experts is absolutely essential for domain driven design to succeed. If the customer is not interested in putting in the time and effort to teach your their domain and help you create a ubiquitous language, you should either try to convince the customer to change their mind or pick another design method.
    - ユビキタス言語とは、ドメインの専門家と開発者の両方が、ドメインを記述し、議論するために一貫して使用する言語のことです。コードそのものとは別に、この言語はドメイン駆動型設計プロセスの最も重要な成果物です。この言語の大部分は、ドメイン専門家がすでに使用しているドメイン用語ですが、ドメイン専門家と協力して新しい概念やプロセスを考案する必要がある場合もあります。このため、ドメイン駆動設計を成功させるためには、ドメインの専門家の積極的な参加が絶対的に不可欠です。もし顧客が自分のドメインを教えるために時間と労力をかけてユビキタス言語を作ることに興味がない場合は、顧客の心を変えるように説得するか、別の設計方法を選ぶようにしましょう。(vaadin strategic ddd)
- You can document the ubiquitous language in various ways. A good starting point is to create a glossary of terms. Business processes can be described graphically using e.g. swimlane diagrams and flow charts. UML can be used to describe the relationship between things and state diagrams to describe how state changes as different things move through different processes. The subdomains are also a part of the ubiquitous language, and you may even need to define different "dialects" of the language for different subdomains. This embodiment of the ubiquitous language is the domain model, and it will eventually be transformed into working code. In other words, the domain model is not the same as a data model or a UML class diagram.
    - ユビキタス言語を様々な方法で文書化することができます。良い出発点は、用語集を作成することです。ビジネス・プロセスは、スイムレーン図やフロー・チャートなどを使ってグラフィカルに記述することができます。UML は、物と物の関係を記述するために使用され、状態図は、異なる物が異なるプロセスを通って移動する際に状態がどのように変化するかを記述するために使用されます。また、サブドメインはユビキタス言語の一部であり、サブドメインごとに異なる言語の「方言」を定義する必要があってもよい。このユビキタス言語の実装がドメインモデルであり、最終的には作業コードに変換されます。言い換えれば、ドメインモデルはデータモデルやUMLのクラス図のようなものではありません。(vaadin strategic ddd)
- The ubiquitous language has a nice feature, and that is that it tells you whether you are on the right track or not. If you can easily explain a business concept or process using the language, it means you are on the right track. If you, on the other hand, find your self struggling to explain something, you are most likely missing something from the language and thereby also from your domain model. When this happens, you should grab a domain expert and go looking for the missing pieces. You may even stumble upon a revelation that turns your existing model completely upside-down and results in a far superior domain model than the one you had before.
    - ユビキタス言語には良い特徴があり、それはあなたが正しい道を歩んでいるかどうかを教えてくれるということです。もしあなたがその言語を使ってビジネスのコンセプトやプロセスを簡単に説明できれば、それはあなたが正しい道を歩んでいることを意味します。一方で、何かを説明するのに苦労しているようであれば、言語から何かが欠けている可能性が高く、それによってドメインモデルからも何かが欠けている可能性が高いです。このような場合は、ドメインの専門家を呼んで、不足している部分を探しに行く必要があります。あなたの既存のモデルを完全にひっくり返し、以前のモデルよりもはるかに優れたドメインモデルを生み出す悟りを開くかもしれません。(vaadin strategic ddd)
- モデルベースの言語が広く使われるようになり、それが自然と口から出てくるまで満足せずにいることで、完全かつ理解可能なモデルに近づくことができる。そのモデルはシンプルな要素から成り立ち、それらを組み合わせて複雑な考えを表現することができる。（中略）ドメイン専門家は、不自然な、ドメインの理解を妨げる用語や構造には異を唱えるべきである。開発者は、設計の妨げになるような曖昧さや矛盾点に注意を払う必要がある。 –Eric Evans (Fowler. [http://bliki-ja.github.io/UbiquitousLanguage/](http://bliki-ja.github.io/UbiquitousLanguage/))

# Bounded Context

- There is not necessarily a one-to-one mapping between bounded contexts and subdomains. Since a bounded context belongs to the solution space and a subdomain to the problem space, you should think about the bounded context as one alternative solution among many possible solutions. Thus a single subdomain can contain multiple bounded contexts. You may also find yourself in a situation where a single bounded context spans multiple subdomains. There is no rule against this, but it is an indication that you may need to rethink your subdomains or context boundaries.
    - 束縛されたコンテキストは解の空間に属し、サブドメインは問題の空間に属しているので、束縛されたコンテキストは、多くの可能な解の中の一つの代替解として考えるべきです。このように、1つのサブドメインに複数の境界付きコンテキストを含めることができます。また、1つの拘束されたコンテキストが複数のサブドメインにまたがっているような状況に陥ることもあるでしょう。これを禁止するルールはありませんが、サブドメインやコンテキストの境界を再考する必要があることを示しています。(vaadin strategic ddd)
- 束縛されたコンテキスト間の関係を識別する最も簡単な方法は、コンテキストを上流のコンテキストと下流のコンテキストに分類することである。コンテキストを川に隣接する都市と考えてください。上流の都市は何かを川に投棄し、それが下流の都市に届く。その中には下流の都市にとって必要不可欠なものもあり、下流の都市はそれを川から回収する。他のものは有害であり、下流の都市に直接的なダメージを与えることができる(vaadin strategic ddd)

# 戦略的DDD

- For me personally, the major takeaways from strategic domain-driven design are the following:
    - It introduces boundaries. Scope creep is a constant factor in all of my hobby projects. Eventually, they become more exhaustive than fun to work on or completely unrealistic to finish alone. When working on customer projects, I have to work hard not to cause technical scope creep by overthinking or overengineering things. Boundaries - wherever they are - help me to divide the project into smaller parts and focus on the right ones at the right time.
    - It does not require me to find a super-model that works in all cases. It recognizes that in the real world, there are often many smaller models in more or less clearly defined contexts. Instead of breaking these models, it embraces them.
    - It helps you to think about the value your system is going to bring and where you should put the most of your efforts to get the biggest value. I have personal experience from projects where properly identifying and then concentrating on the core domain would have made a huge difference. Unfortunately, I had not yet heard about strategic DDD and both time and money were wasted.
- 私個人としては、戦略的ドメイン駆動型デザインから得られる主なものは以下の通りです。
    - 境界線の導入。スコープ・クリープは、私の趣味のプロジェクトのすべてにおいて、一定の要因となっています。最終的には、作業が楽しいというよりも疲弊してしまったり、一人で完成させるには完全に非現実的なものになってしまいます。顧客のプロジェクトでは、考えすぎやオーバーエンジニアリングで技術的なスコープ・クリープを起こさないように気をつけなければなりません。境界線がどこにあっても、私はプロジェクトを小さな部分に分け、適切なタイミングで適切なものに集中するのに役立ちます。
    - それは私がすべての場合ではたらくスーパーモデルを見つけることを要求しない。現実の世界では、多かれ少なかれ明確に定義された文脈の中に、多くの小さなモデルが存在することが多いことを認識しています。これらのモデルを壊すのではなく、それらを受け入れます。
    - これは、システムがもたらす価値を考え、最大の価値を得るためにどこに最大限の努力を注ぐべきかを考えるのに役立ちます。私は個人的な経験から、コアドメインを適切に特定し、それに集中することで大きな違いが生まれたプロジェクトを経験しています。残念ながら、私はまだ戦略的DDDについて聞いたことがなく、時間とお金の両方が無駄になってしまいました。(vaadin strategic ddd)

# Value Object Advantage:

1.they bring context to the value. (vaadin tactical ddd)

2.you can add all the business operations that can be performed on values of a particular type to the value object itself.
(vaadin tactical ddd)

3.you can be sure that the value object always contains a valid value.
(vaadin tactical ddd)

an entity is an aggregate root or not?

* How is the entity going to be accessed in the application?

* If the entity will be looked up by ID or through some kind of search it is probably an aggregate root.

* Will other aggregates need to reference it?

* If the entity will be referenced from within other aggregates it is definitely an aggregate root.

* How is the entity going to be modified in the application?

* If it can be modified independently it is probably an aggregate root.

* If it cannot be modified without making changes to another entity it is probably a local entity.

# Aggregate

- aggregate is created, retrieved and stored as a whole. (vaadin tactical ddd)
- aggregate is always in a consistent state. (vaadin tactical ddd)
- aggregate is owned by an entity called the aggregate root, whose ID is used to identify the aggregate itself. (vaadin tactical ddd)
- Guidline1: Keep your Aggregates small (vaadin tactical ddd)
- Guideline2: Refer to other Aggregates by ID (vaadin tactical ddd)
- Guideline3: Change one aggregate per transaction (vaadin tactical ddd)
- Guideline4: User optimistic locking
(vaadin tactical ddd)

# Domain Event

* Domain Eventの定義: 「ドメインエキスパートが気にかける、何かの出来事」(IDDD)

* イベントを外部のサービス(別の境界づけられたコンテキスト)に通知しないといけないケースがある。(IDDD)

* こういうときはパブリッシャー、サブスクライバパターンを使うことになる。ローカルとリモートの境界づけられたコンテキストに広く影響を及ぼす。(IDDD)

* イベントを他のコンテキストに配送する際は、結果整合性を利用するのが一般的だ(IDDD)

* ドメインイベントを使うことで、バッチ処理を細かく分けてまんべんなく実行できる。(IDDD)

* 集約に対するコマンドのうち、無意味な出来事をイベントとして実装しないこともできる。イベントソーシングを使う場合や、システム間の協調の目標によっては、多くのイベントを用意することもできる。(IDDD)

- Domain Event make the system extendable.
(vaadin tactical ddd)
- In a domain-driven system, domain events are an excellent way of achieving eventual consistency.

### イベント配信手法

- Distribution through a message QUEUE
    - メリット
        - 速い
        - 既存のメッセージングソリューション使える(AMQP, JMS)
    - デメリット
        - 過去のイベントを取得できない。再送できない。
- Distribution through an event log
    - メリット
        - 過去のイベント閲覧、再送できる
    - デメリット
        - 処理済みイベント管理を実装しないといけない
        - イベント実行までに時間差が発生する

# Movable and Static Objects

- a movable object is any object of which there can be more than one instance and that can be passed around between different parts of the application. Value objects, entities and domain events are all movable objects.(vaadin tactical ddd)
- A static object, on the other hand, is a singleton (or a pooled resource) that always sits in one place and is invoked by other parts of the application but is rarely passed around (except when being injected into other static objects). Repositories, domain services, and factories are all static objects.(vaadin tactical ddd)
- movable objectはstaticオブジェクトへの参照を持ってはいけない。こうすることでmovable objectのデシリアライズ時にstatic objectをインジェクトする必要がなくなり、movable objectが使いまわししやすくなり、自己完結する。

# Other Domain Objects

- Any information from an external system (= another bounded context). The information is immutable from your point of view, but it has a global ID that is used to uniquely identify it.(vaadin tactical ddd)
- Type data that is used to describe other entities (Vaughn Vernon calls these objects standard types). These objects have global IDs and may even be mutable to some extent, but for all practical purposes of the application itself, they are immutable.(vaadin tactical ddd)
- Framework/infrastructure-level entities that are used to e.g. store audit entries or domain events in the database. They may or may not have global IDs and may or may not be mutable, depending on the use case.(vaadin tactical ddd)

# Repository

At the very least, a repository should have the following capabilities:

- Capability to save an aggregate in its entirety in some kind of data storage
- Capability to retrieve an aggregate in its entirety based on its ID
- Capability to delete an aggregate in its entirety based on its ID

(vaadin tactical ddd)

# CQRS

- Repositories always save and retrieve complete aggregates. This means that they can be pretty slow(vaadin tactical ddd)
- Repositoryだけでは、少数の属性の多数のアイテムリストを表示するときや、複数の集約の情報を一つのアイテムとしてリストを表示するときにパフォーマンスの問題が発生する。(vaadin tactical ddd)

# Domain Service

- We have already mentioned that both value objects and entities can (and should) contain business logic. However, there are scenarios where a piece of logic simply does not fit into one particular value object or one particular entity. Putting business logic in the wrong place is a bad idea so we need another solution. Enter our second static object: the domain service.(vaadin tactical ddd)
- a domain service is only responsible for making business decisions(vaadin tactical ddd)
- エンティティや値オブジェクトに責務をもたせるのが適切でないとき、その操作はDomain Serviceという独立したインターフェイスとしてモデルに追加すること。(IDDD)
- ある操作がエンティティや値オブジェクトに属さないとみなす条件(IDDD)
- 重要なビジネスロジックを実行する
- ドメインオブジェクトを、ひとつの構成から別の構成に変換する
- 複数のドメインオブジェクトからの入力にもとづいて、値を算出する

## Factory

* ファクトリはオブジェクトの生成に関わる知識がまとめられたオブジェクトです。(成瀬本)

* 生成方法が複雑なインスタンスを構築する処理をまとめるため (成瀬本)

仕様オブジェクト(成瀬本)

* 値やエンティティ(複数のこともある)を受け取り、判断結果を返すオブジェクト(成瀬本)

* リポジトリに仕様を渡してフィルタする使い方もあるが、性能問題が発生する危険がある(全件検索するため)

- As the name suggests, factories are responsible for creating new aggregates.(vaadin tactical ddd)
- A factory can be a static factory method on the aggregate root class or a separate factory class. (vaadin tactical ddd)
- The factory can interact with other factories, repositories and domain services but must never alter the state of the database (so no saving or deleting).(vaadin tactical ddd)
