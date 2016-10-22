[How to draw diagram using by Haroopad](http://pad.haroopress.com/page.html?f=how-to-draw-diagram)

[Mermaid rendering broken](https://github.com/rhiokim/haroopad/issues/490)
Also it "works" the following, Ctrl+a, Del, and Ctrl+z



```mermaid
graph LR;
    A[Hard edge]-->|Link text|B(Round edge);
    B-->C{Decision};
    C-->|One|D[Result one];
    C-->|Two|E[Result two];
```
    
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```

```mermaid
sequenceDiagram
    Alice->Bob: Hello Bob, how are you?
    Note right of Bob: Bob thinks
    Bob-->Alice: I am good thanks!
    Bob-->John the Long: How about you John?
    Bob-->Alice: Checking with John...
    Alice->John the Long: Yes... John, how are you?
    John the Long-->Alice: Better then you!
```
