---
title: "CakeCTF 2021 振り返り"
description: ""
draft: true
math: false
tags: [""]
date: 2021-08-29T15:10:20+09:00
---

今年も[theoldmoon0602](https://twitter.com/theoremoon)と[ptr-yudai](https://twitter.com/ptrYudai)と僕の3人でCTFを開催しました。
前年度まではInterKosenCTFという名前で開催していたのですが、今年は名前を変えての開催となりました。

他の2人の記事
- theoldmoon0602: https://furutsuki.hatenablog.com/entry/2021/08/29/224254
- ptr-yudai: https://ptr-yudai.hatenablog.com/entry/2021/08/30/000015

問題リポジトリ
- https://github.com/theoremoon/cakectf-2021-public

## 作成した問題について
### [rev] Hash Browns
単純なx64elf解析問題です。
関数`f`でなにかやってますが、見る人がみると`xgcd()`に見えるのかな？と思います。わからなくても動的解析をしたり、デコンパイルしたコードを実装すればなんとかなると思います。
ハッシュが含まれる2つの配列のindexがそれぞれわかれば、ローカルでハッシュ値と合う文字を1文字づつ探索すればフラグが入手できます。
関数`f`の理解がからっきしだめでもフラグの偶数indexは復元できます。
そこから奇数indexの文字をエスパーするみたいなことができ...ないです（たぶん）。
フラグを入手された方はわかると思うんですが、フザけたフラグになってるのでエスパーは厳しいと思います。

reversingの作問は初めてだったのでreversingの問題としての面白さがわからず不安でした。
[Survey](https://ptr-yudai.hatenablog.com/entry/2021/08/30/000015#Survey%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)を見た感じそれなりに楽しんでもらえたようでほっとしています。
ちなみに問題名のHash Brownsは去年のこのCTF(旧InterKosenCTF)でボツ問になった問題名から取ってきてます。

writeup: https://hackmd.io/@ptr-yudai/rJWHh_SwO

### [crypto] Together as one
基礎的な初等整数論の知識で解ける問題です。
この問題はzer0pts CTF 2021を目標に作ってたけど、納得の行くものになったのが開催前日とかでこちらで出題しました。
当初はmediumぐらいで出してたけど、謎のパワーでlunaticになりました。
なんか毎年難易度推定バグってるけど、dynamic scoringだしまぁいっか！（おっとぼけ）という気持ちが自分の中である気がする。
よくないですね。
善処します。

問題名のTogether as one はTimmy TrumpetのDiamondsから来ています。素数が3つ集まっている感じとか、Together as one っぽくないですか（僕だけ）？

writeup: https://hackmd.io/@yoshiking/rJ5suNPXO


### [misc] Break a leg
miscのwarmup枠で出した[問題](https://furutsuki.hatenablog.com/entry/2021/08/29/224254#break-a-leg)です。
authorがtheoldmoon0602と僕になっていますが、これは僕の原案をtheoldmoon0602がいい感じにした結果がこの問題です。
ん〜、まあこれは特にコメントはないです。

## 感想
毎年大した仕事もせずに運営面をしているわけですが、今年も例にはもれずプー太郎でした :bear: 。
作問能力も運営能力も他2人の足元にも及ばないことは明らかだけど、それはそれとして今回の準備どうなのって感じだと思います。

運営中は序盤ではドタバタしながらフラグの修正したりしました。
残りの時間はブラウザで遊べるゲームをみんなでしてました。
大体負けた記憶しかないですが、めちゃくちゃ楽しかったです。
あと、最近失いかけていた関西弁が戻りました。
今はよくわからない言語を話しています。

最後に参加者の皆様ありがとうございました、お疲れ様です。
また、ポジティブな意見をくださった皆様もありがとうございます。
次回の励みになるので褒めてください :dog: 。
運営の2人もお疲れ様でした。
仕事サボってごめんなさい。
