# phoenix Realtime 変換入力
## 目的
PCによる日本語入力にスマートフォンの様な操作感を取り入れ、日本語入力による疲労を軽減し作業を快適なものにします。

## 背景
現在、PCで日本語入力をする際に最も多く使われているのはqwertyローマ字かな漢字変換です。これは今から30年以上も前の昭和時代に開発されたものであるため、当時としては最適なものであったとは思われるのですが、現在一般に使用されているスマートフォンの日本語入力と比較すると複雑で過酷な操作体系であると感じざるを得ません。

文書作成において同一の単語は一連の文書の中で何度も何度も出てきます。しかし、正確に同じ単語を何度も何度も延々と打ちこまなければならないのはかなり辛く間違いを起こしやすいです。

Google-IMEではこの様な問題を解決する為の機能として補完機能(Realtime 変換機能)を実装しました。しかしながら、この補完機能もqwertyローマ字かな等と組み合わせて使用した場合にはTabキーを頻繁に打鍵する事を要求され小指の腱鞘炎を引き起こしてしまう危険性を孕み、又ホームポジションからの頻繁な往復は疲労を蓄積させ、作業効率の改善という意味では十分であるとは言えません。

この様な問題を解決する為、補完機能の操作に要する手や指の運動量を最小にし、文書作成を快適にするphoenix Realtime 変換入力を作ってみました。

また、MS-IMEにも予測入力という名前で補完機能が実装されたのでphoenix Realtime 変換入力を使って頂ける人の数が増えました。

## 実現方法
phoenixかな配列はキーボードの上段と中段のキーだけを使用してかなを入力する行段系のかな配列です。

下段のキーを使用して補完機能によって提示される候補を一打鍵で選択及び入力する事で快適な日本語入力を実現します。

phoenixかな配列は同時打鍵の配列ではありませんので、打鍵と打鍵の間の時間を気にする必要はありません。

phoenixかな配列は基本的に100%交互打鍵で入力する事を想定していますが、打鍵順序が入れ替わっても意図した文字を入力できるように定義してありますので、打鍵順序の入れ替わりを気にせずにリラックスして入力をする事ができます。


## インストール方法
- AutoHotKeyをインストールします。

### Google-IMEの場合
- phoenix_rt.txtを使用してGoogle-IMEのローマ字定義をphoenixかな配列に変更します。

- Google-IMEの設定画面で補完機能を有効にします。

### MS-IMEの場合

- MS-IMEを以前のバージョンに戻します。
[以前のバージョンに戻す](https://support.microsoft.com/ja-jp/windows/%E4%BB%A5%E5%89%8D%E3%81%AE%E3%83%90%E3%83%BC%E3%82%B8%E3%83%A7%E3%83%B3%E3%81%AE-ime-%E5%85%A5%E5%8A%9B%E6%96%B9%E5%BC%8F%E3%82%A8%E3%83%87%E3%82%A3%E3%82%BF%E3%83%BC-%E3%81%AB%E6%88%BB%E3%81%99-adcc9caa-17cb-44d8-b46e-f5b473b4dd77#:~:text=%5B%E8%A8%AD%E5%AE%9A%5D%20%E5%86%85%E3%81%AE%E6%A4%9C%E7%B4%A2%E3%83%9C%E3%83%83%E3%82%AF%E3%82%B9,%E4%BD%BF%E3%81%86%5D%20%E3%82%92%E3%82%AA%E3%83%B3%E3%81%AB%E3%81%97%E3%81%BE%E3%81%99%E3%80%82)

- phoenix10.regをダブルクリックしてMS-IMEのローマ字定義にphoenixを追加します。

- MS-IMEの設定画面でローマ字定義をphoenixに変更します。

- MS-IMEの設定画面で予測入力を有効にします。

## 操作方法

- phoenix_rt.ahkのスクリプトを実行します。

- かな文字を入力していくと補完機能の候補リストがカーソルの下に表示されます。

- 候補リストの先頭の項目を選択し入力するにはzをキーインします。

- 同様に候補リストの2番目はx、3番目はc、4番目はv、5番目はb、6番目はn、7番目はmをキーインします。

- phoenixかな配列を使用した日本語入力の方法は下記のサイトを参照してください。

http://phoenixrt.kachoufuugetu.net


