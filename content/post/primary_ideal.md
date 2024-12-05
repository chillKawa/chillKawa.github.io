+++
title = '準素イデアルについて'
date = 2024-05-02T13:39:48+09:00
draft = false
description = "A はネーター環として"
image = "/images/prime_fil.PNG"
imageBig = "/images/prime_fil.PNG"
categories = ["math","環論"]
authors = ["脳brain"]
avatar = "/images/ava.png"
+++

準素イデアルの定義ってどんなものを採用してますか?

私は $\mathrm{Ass}_A(A/\mathfrak{q}) =\lbrace\mathfrak{p}\rbrace$ となるものを $\mathfrak{p}$-準素イデアルと定義してます.

なんか良くあるのは片方が入ってなかったら$n$乗が入るみたいな定義で, それで証明を読んでもよくわからない感があるので個人的にきついです.

所で Ass とかも松村とかの定義はあんまり好みじゃなくて.

$M\in\mathrm{mod}A$とする. この時, $M$の**Associated prime**を;
$$\mathrm{Ass}_AM=\lbrace\mathfrak{p}\in\mathrm{Spec}A\mid\exists\varphi\in\mathrm{Hom}_A(A/\mathfrak{p},M):\text{inj.}\rbrace$$

とした方が好きです.　こうすると加群の埋め込みで統一出来て simple みたいに扱えるので気分がいいです. 例えば $N\subset M$ に対して $\mathrm{Ass}N\subset\mathrm{Ass}M$とかが直感で分かります. 一応ちゃんと見ると, $\mathfrak{p}\in\mathrm{Ass}N$ に対して $A/\mathfrak{p}\to N$ っていう inj.が取れて合成;
$$A/\mathfrak{p}\to N\hookrightarrow M$$
を考えたらいいですね.

# 良い証明

![description of the image](/images/prime_fil.PNG)

ってのがあって, これを見ると$0$次元ネーターがアルティンってのは明らかです. 実際, $0$次元なので filtration に出てくる prime は極大で加群的に見たら$A/\mathfrak{p}_i$は simple だから組成列になってて分かります. 逆も $A/\mathrm{rad}A$ が semisimple なので良いです(ちゃんというと radical は冪零なので $A\supset\mathrm{rad}A\supset\dots\supset\mathrm{rad}^nA=0$ でこの組成因子は semisimple になるから(semisimple 上の加群なので)).

準素イデアル分解の 1st uni. thm.も加群レベルですぐ見れて;

$N=\bigcap N_i$を irredundant(無駄のない準素分解)とすると (但し$\mathrm{Ass}(M/N_i)=\lbrace \mathfrak{p}_i\rbrace$), inj. $M/N \to \bigoplus_i M/N_i$があるので$\mathrm{Ass}(M/N)\subset\lbrace \mathfrak{p}_1,\dots\mathfrak{p}_n\rbrace$.

irredundant だから $0\neq\bigcap_{i\neq j}N_j/N\to M/N$ が inj.で $ \mathfrak{p}\_i \in\mathrm{Ass}\bigcap\_{i\neq j}N_i/N \subset \mathrm{Ass}M/N$だから, $\mathrm{Ass}M/N=\lbrace \mathfrak{p}_1,\dots\mathfrak{p}_n\rbrace$.

一応置いておく(これは元を取っている;;)
![description of the image](/images/lemma_primary.PNG)

あと短完全列で Ass が Supp みたいに振舞うのも pull back 取ったらすぐわかります.
