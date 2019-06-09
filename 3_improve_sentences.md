selfはインスタンスオブジェクト自身を指しています。クラスの中でインスタンスオブジェクトを呼び出す際やそのインスタンスオブジェクトを呼び出す際は、selfを使用します。

クラスとは、何かを表現するための設計図のようなものです。

インスタンスとはクラスを実体化したものです。
以下のコードを見てください
```
class Person
  attr_accessor :name

  def initialize(name)
    self.name = name
  end

  def greet
    puts "Hello! I'm #{self.name}"
  end
end

person1 = Person.new("mike")
person2 = Person.new("nancy")

person1.greet
person2.greet
```

ここのperson1とperson2はそれぞれインスタンスです。
つまり、person1, person2はPersonと言う設計図を元に作られた、基本構造は同じだけど、名前が違う別々の人間と言うことになります。
設計図(クラス)を作成する中で、インスタンスの情報を必要とする事があります。

上記の例だと、名前と言う情報はインスタンスそれぞれで固有のものです。
人間が挨拶をする時は、それぞれの人間の名前を言って欲しいです。

ですから。person1にはperson1自身のnameと言う情報を表示して欲しいし、person2にはperson2自身のnameを表示してほしいのです。

インスタンス固有の値をクラスの時点で利用するには、selfと付けることでインスタンス化した時の情報を参照できるようになります。
