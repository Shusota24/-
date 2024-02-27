## 問１

if文が1つで済むので、よく内部ロジックで利用されているらしい。

```Java
    public static void leapYear(int year) {
        if(year % 4 == 0 && year % 100 != 0 || year % 400 == 0) {
            System.out.println("閏年です。");
            return;
        }

        System.out.println("閏年ではありません。");
        return;
    }
```

## 問2

「％が使えないなら割り算を工夫して、、」と考えて導き出す。

```Java
    List<Integer> list = new ArrayList<Integer>();

    for(int j=1;j<=1000;j++) {
        if (j/7 != (j-1)/7) {
            list.add(j);
        }
    }

    System.out.println(list);
```

## 問３
桁数の指定が無いので、ゴリ押しで判断はキツい。
正規表現(matches)でもいいが、この程度なら必要ない。

途中でreturnしない方が賢明。

```Java
    public static void misezan(int x, int y) {
        int gan;

        if(x == y) {
            gan = 1;
        } else {
            gan = (x > y) ? x : y;
        }

        if(x==6 && y==9 || x==9 && y==6) {
            gan = 11;
        }

        String xstring = String.valueOf(x);
        String ystring = String.valueOf(y);

        if(xstring.startsWith("2") && ystring.contains("5") || 
            xstring.contains("5") && ystring.startsWith("2")) {
            
            gan = 111;
        }
        
        System.out.println("眼は" + gan + "です。");
        return;
    }
```
