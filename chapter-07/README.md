# Chapter 8: Refactoring #1

## Step 1: Long Parameter List

- `LongParameterList.java`

```java
public class LongParameterList {
    void print(
            String documentToPrint,
            String paperSize,
            String orientation,
            boolean grayScales,
            int pageFrom,
            int pageTo,
            int copies,
            float marginLeft,
            float marginRight,
            float marginTop,
            float marginBottom) {
    }
}
```

- Refactored `LongParameterList.java`
```java
public class LongParameterList {
    void refactoredPrint(
            PaperSize papersize,
            PrintOrientation orientation,
            ColorConfiguration color,
            PrintRange range,
            PrintMargins margins,
            int copiesCount
    ) {
    }
}

final class PaperSize {
}

final class Document {
}

final class PrintMargins {
}

final class PrintRange {
}

final class ColorConfiguration {
}

final class PrintOrientation {
}
```

## Step 2: Data Clumps
## Step 3: Code Duplication

## Read more
- [Refactoring: Improving the Design of Existing Code](https://www.amazon.com/Refactoring-Improving-Existing-Addison-Wesley-Signature-dp-0134757599/dp/0134757599)