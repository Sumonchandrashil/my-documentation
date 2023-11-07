Unparenthesized `a ? b : c ? d : e` is deprecated. 
Use either `(a ? b : c) ? d : e` or `a ? b : (c ? d : e)`


The error message you're encountering is because you have an unparenthesized ternary expression, and the PHP interpreter is warning you about potential ambiguity. To resolve this issue and make your code more explicit, you can follow the suggestions provided in the error message.

You can use either of the following alternatives:

1. Parenthesize the first ternary expression:

   ```php
   ($a ? $b : $c) ? $d : $e
   ```

   This means that if `$a` is true, it will first evaluate `$b` or `$c`, and then evaluate the second ternary expression.

2. Parenthesize the second ternary expression:

   ```php
   $a ? $b : ($c ? $d : $e)
   ```

   This means that if `$a` is true, it will evaluate `$b`. If `$a` is false, it will check the second ternary expression with `$c`, `$d`, and `$e`.

Choose the one that matches your intended logic for the conditional expression.