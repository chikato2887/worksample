>例えばコントローラー作成時は"blogs"と、モデル作成時は"blog”とそれぞれパラメーター指定させています。それに基づいて様々な変数等が自動的に作成されているようなので、"blogs"と"blog"を使い分けることに意味があるのだと思うのですが、何処にも記載が無いので未だに混乱しています。

これを理解するには、Railsの(Convention over Configuration)と言う考え方を理解するのが良いかと思います。
規約に沿った書き方をすれば多くの設定をせずに開発できると言う考え方なのですが、今回の場合は命名に関する規約を知る事ができれば混乱している箇所を解消出来るんじゃないかなと思います。

-  [モデルの命名規則](https://railsguides.jp/active_record_basics.html#%E5%91%BD%E5%90%8D%E3%83%AB%E3%83%BC%E3%83%AB)
-  [コントローラー命名規則](https://railsguides.jp/action_controller_overview.html)

上記の二つのページを参考にしてみてください。

---

> rake routes"を行ってみても、Prefixに"blog"　”new_blog"もあれば、"blogs" "confirm_blogs"もあります。何故こうなっているのか全く理解できていません。

routes.rbファイルにルーティングを記述しますが、その際の内容によってrailsがルートに対して扱いやすいような名前を付与してくれます。

[こちら](http://railsdoc.com/routes#%E3%83%AB%E3%83%BC%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0%E5%AE%9A%E7%BE%A9)にroutesを記述した時に生成されるルートのパス一覧が書かれています！確認してみてください！

なお、"confirm_blog"に関しては、routes.rbに手動で設定したルーティング名なのではないかなと思います。

ルーティングを設定するメソッドにルーティング名を手動で設定するオプションがあるので、そちらについても調べてみると良いかもしれません！

---
> 何処にも記載が無いので未だに混乱しています。

とあるのでちゃんとご自分で調べる事をしている方だと思います！
頑張っていきましょう！
