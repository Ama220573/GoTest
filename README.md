# GoTest
# Golang 標準入力
## Case1
### input
```
A B C
```
### Code
```
var a, b, c int
fmt.Scanf("%d %d %d", &a, &b, &c)
```

## Case2
### input
```
DEF
```
### Code
```
var d, e, f int
fmt.Scanf("%1d%1d%1d", &d, &e, &f)
```

## Case3
### input
```
P1 P2 P3 ... Pn
```
### Code
```
sc := bufio.NewScanner(os.Stdin)
sc.Scan()
inputs := strings.Split(sc.Text(), " ")

var ps []int                   // Pnを格納する配列を宣言
	for _, input := range inputs { // 配列inputsの全ての要素について実行
		p, _ := strconv.Atoi(input) // string→intに型変換
		ps = append(ps, p)          // intに型変換した値を、Pnを格納する配列に追加
	}
```

## Case4
### input
```
N
U1 V1
U2 V1
...
UN VN
```
### Code
```
// 1文字ずつデータ型を指定して受け取る
var n int           // int型の変数を宣言
fmt.Scanf("%d", &n) // %dでint型を代入

sc := bufio.NewScanner(os.Stdin) // 標準入力を受け付けるスキャナ

var us []int // uの値を格納する配列を宣言
var vs []int // vの値を格納する配列を宣言

for i := 0; i < n; i++ { // 行数分繰り返す
	sc.Scan()                               // １行分の入力を取得する
	inputs := strings.Split(sc.Text(), " ") // 半角スペース区切りでstring型として配列inputsに格納
    u, _ := strconv.Atoi(inputs[0])         // string→intに型変換
	v, _ := strconv.Atoi(inputs[1])         // string→intに型変換
	us = append(us, u)                      // uの配列に追加
	vs = append(vs, v)                      // vの配列に追加
}
```
