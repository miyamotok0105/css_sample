
# 本

『６ステップでマスターする　「最新標準」HTML+CSSデザイン』サポートサイト    


## ch02_base：完成形


## ch02_001：中央のテキストを作成


:root 疑似クラスは、文書を表すツリーのルート要素のこと。    
でっかい色とか決めてる。    

```
:root {
    --main-color: #5D9AB2;
    --accent-color: #BF6A7A;
    --dark-main-color: #2B5566;
}
```

htmlはsection div h1 or pの流れ。

```
section -> div -> h1
               -> p
```

cssとしてはコンテンツA（conA）の中にコンテナ（container）が入ってる。


```
<section class="conA">
    <div class="container">
        <h1>LOGGER</h1>
        <p>美味しく楽しくライフログ</p>
    </div>
</section>
```

- font-family    
前に書かれたものから優先的に適用。    

- コンテンツ    
h1とpにはちょっとマージンとかついてるだけ。    

- @media    
min-widthを指定すると後px以上の時のみ適応される。    

※ min-widthの調整が結構むずいね。    



```
.conA {
    text-align: center;
}

.conA h1 {
    /* topマージンは無し */
    margin-top: 0;
    /* bottomマージンは10px */
    margin-bottom: 10px;
    /* fontサイズ15 */
    font-size: 15vw;
}

.conA p {
    margin-top: 0;
    margin-bottom: 0;
    font-size: 18px;
}

/* ブレークポイントが768px。 */
/* 769px以下の時にはフォントサイズが変化。 */
/* 769px以上の時はフォントサイズを固定にする。 */
@media (min-width: 768px) {
    .conA h1 {
        font-size: 115px;
    }

    .conA p {
        font-size: 24px;
    }
}
```


