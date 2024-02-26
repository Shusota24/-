## 問１

if文が1つで済むので、よく内部ロジックで利用されているらしい。

```Java
    public static void leapYear(int year) {
        if(year % 4 == 0 && year % 100 != 0) {
            System.out.println("閏年です。");
            return;
        }

        System.out.println("閏年ではありません。");
        return;
    }
```

## 問2

ちと難しいですが、「％が使えないなら割り算を工夫して、、」と考えて導き出す。

```Java
    List<Integer> list = new ArrayList<Integer>();

    for(int j=1;j<=1000;j++) {
        if ( (j+1)/7 == j/7 && j/7 - (j-1)/7 == 1 ) {
            list.add(j);
        }
    }

    System.out.println(list);
```

## 問３
