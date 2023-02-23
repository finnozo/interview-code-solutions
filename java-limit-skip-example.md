```java

  public void test() {
        List<Integer> myList = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 12, 14, 11, 23, 54, 32, 111);

        myList.stream()
                .skip(2)
                .limit(5)
                .forEach(System.out::println);

    }

```
