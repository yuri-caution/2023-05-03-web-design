# 웹디자인기능사 시험 레이아웃 연습

### .gnb 구조 주의
```
<ul class="gnb">
                <li>
                    <a href="#">탑</a>
                    <ul>
                        <li><a href="#">블라우스</a></li>
                        <li><a href="#">티</a></li>
                        <li><a href="#">셔츠</a></li>
                        <li><a href="#">니트</a></li>
                    </ul>
                </li>
                <li>
                    <a href="#">아우터</a>
                    <ul>
                        <li><a href="#">자켁</a></li>
                        <li><a href="#">코트</a></li>
                        <li><a href="#">가디건</a></li>
                        <li><a href="#">머플러</a></li>
                    </ul>
                </li>
                <li>
                    <a href="#">팬츠</a>
                    <ul>
                        <li><a href="#">청바지</a></li>
                        <li><a href="#">짧은 바지</a></li>
                        <li><a href="#">긴 바지</a></li>
                        <li><a href="#">레깅스</a></li>
                    </ul>
                </li>
                <li>
                    <a href="#">악세서리</a>
                    <ul>
                        <li><a href="#">귀고리</a></li>
                        <li><a href="#">목걸이</a></li>
                        <li><a href="#">반지</a></li>
                        <li><a href="#">팔찌</a></li>
                    </ul>
                </li>
            </ul>
```

## logo 이미지 background로 넣기
```
.header h1 a{
    display: block;
    text-indent: -9999px;
    width: 200px;
    height: 40px;    
    background: url('../images/logo.png') no-repeat center;
}
```

## css에서 클래스 부를 때 gnb 마크업 구조 유의
```
.gnb {
    display: flex;
    font-size: 16px;
}

.gnb > li {
    position: relative;
}

/* 바로 아래 태그만 한정하기 위해 >(꺽쇠)사용 */
.gnb > li > a {
    display: block;
    height: 100px;   
    /* inline은 높이 안 먹히므로 display: block; 해줘야함*/
    line-height: 100px;
    padding: 0 40px;
}

.gnb > li > a:hover {
    color: tomato;
}
```

## slide 구현하기
### overflow 사용 (영역 밖의 것은 표시 안함)
### top 값을 조정해서 이미지 교체(JS로)
```
.slider {
    position: relative;
    overflow: hidden;
    height: 300px;
}

.slide {
    position: absolute;
    top: 0;
    left: 0;
}

.slide .item img {
    display: block;

}
```