```java

    List<String> sentences = Arrays.asList(
    "Hello world",
    "Java is awesome",
    "Flatmap is tricky"
);

List<String[]> wordsList = sentences.stream()
    .map(sentence -> sentence.split(" "))  // map each sentence to an array of words
    .distinct()
    .collect(Collectors.toList());  // collect the arrays into a list

List<String> uniqueWords = wordsList.stream()
    .flatMap(Arrays::stream)  // flatten the array of words into a stream of words
    .distinct()
    .collect(Collectors.toList());  // collect the distinct words into a list

System.out.println(uniqueWords);

```
