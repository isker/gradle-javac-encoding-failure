```
λ ./gradlew assemble

> Task :compileJava
/private/tmp/encoding-test/src/main/java/encoding/test/Library.java:7: error: unmappable character (0xD0) for encoding US-ASCII
    private final String foo = "????";
                                ^
/private/tmp/encoding-test/src/main/java/encoding/test/Library.java:7: error: unmappable character (0xB4) for encoding US-ASCII
    private final String foo = "????";
                                 ^
/private/tmp/encoding-test/src/main/java/encoding/test/Library.java:7: error: unmappable character (0xD0) for encoding US-ASCII
    private final String foo = "????";
                                  ^
/private/tmp/encoding-test/src/main/java/encoding/test/Library.java:7: error: unmappable character (0xB0) for encoding US-ASCII
    private final String foo = "????";
                                   ^

> Task :processResources NO-SOURCE
> Task :classes
> Task :jar
> Task :assemble

BUILD SUCCESSFUL in 635ms
2 actionable tasks: 2 executed
/tmp/encoding-test λ javac -encoding ASCII src/main/java/encoding/test/Library.java
src/main/java/encoding/test/Library.java:7: error: unmappable character (0xD0) for encoding ASCII
    private final String foo = "����";
                                ^
src/main/java/encoding/test/Library.java:7: error: unmappable character (0xB4) for encoding ASCII
    private final String foo = "����";
                                 ^
src/main/java/encoding/test/Library.java:7: error: unmappable character (0xD0) for encoding ASCII
    private final String foo = "����";
                                  ^
src/main/java/encoding/test/Library.java:7: error: unmappable character (0xB0) for encoding ASCII
    private final String foo = "����";
                                   ^
4 errors
/tmp/encoding-test λ echo $?
1
```
