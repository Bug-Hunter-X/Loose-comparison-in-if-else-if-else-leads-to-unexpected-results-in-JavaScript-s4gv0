# Loose Comparison in JavaScript if/else if/else

This example demonstrates a potential pitfall in JavaScript's loose comparison (`==`) within `if/else if/else` statements.  The issue arises when comparing against `null` using loose comparison, which may result in unexpected behavior when 0 or other 'falsy' values are encountered.

## Problem:
The `foo` function demonstrates the issue. The intention is to handle `null`, negative numbers, and positive numbers differently. However, loose comparison can lead to unexpected results because `0` and empty string ("") will also be evaluated as falsy, causing the second condition to trigger unexpectedly. 

## Solution:
The solution uses strict equality (`===`) to avoid this problem. Strict equality only returns true when the operands have the same type and value, making comparison more predictable.

This example highlights the importance of using strict equality (`===`) in JavaScript whenever you need to ensure accurate comparison and avoid subtle bugs related to loose comparison.