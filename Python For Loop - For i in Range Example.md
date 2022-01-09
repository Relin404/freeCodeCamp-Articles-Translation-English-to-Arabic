# Python For Loop - For i in Range Example

![Jeremy L Thompson](https://www.freecodecamp.org/news/content/images/size/w100/2021/02/151340_2.png)

[Jeremy L Thompson](https://www.freecodecamp.org/news/author/jeremylt/)

![Python For Loop - For i in Range Example](https://cdn-media-2.freecodecamp.org/w1280/606365729618b008528a99ae.jpg)

تُعتبر الـ Loops واحدة من هياكل التحكُّم (Control Structures) الرئيسيّة في أي لُغة برمجة، ولا تختلِف بايثون (Python) عنهم.

سنتناول في هذه المقالة بعض الأمثلة لاستخدام الـ `for` loops مع دالّة `range()` الخاصّة ببايثون.

## الـ For Loops في بايثون
تُكرّر `for` loops جُزءًا من الكود (code) لِمجموعة من القيم (values).

وكَما ذُكِر في [توثيق بايثون (Python's documentation)](https://docs.python.org/3/tutorial/controlflow.html#for-statements)، تختلف الـ `for` loops في عملِها قليلًا عن عملِها في لُغاتٍ أُخرى مِثل جافاسكربت (JavaScript) أو سي (C).

تُخزِّن الـ `for` loop كُلّ قيم القائمة (list)، المصفوفة (array)، أو السلسلة (string) المُعطاة في مُتغيِّر المُكرِّر (iterator) ثُمَّ تُكرِّر الكود الموجود في قِسم الـ `for` loop لِكُلِّ قيم مُتغيِّر المُكرِّر (iterator).

في المثالِ أدناه، يتمُّ استعمالِ الـ `for` loop لِطباعة (print) كل رقم في المصفوفة (array)
```python
# Example for loop
for i in [1, 2, 3, 4]:
    print(i, end=", ") # prints: 1, 2, 3, 4,
```
يُمكننا أيضًا إدراج منطِق (logic) أكثر تعقيدًا في قِسم الـ `for` loop. في هذا المِثال يتمُّ طِباعة ناتج عمليّة حسابيّة مُعتمِدة على قيمة مُتغيِّر المُكرِّر (iterator).

```python
# More complex example
for i in [1, 3, 5, 7, 9]:
    x = i**2 - (i-1)*(i+1)
    print(x, end=", ") # prints 1, 1, 1, 1, 1, 
```

إذا كانت قيم المصفوفة (array) مُتتابِعة (sequential)، يُمكِننا استخدام دالة `range()` الخاصة بِبايثون بدلًا مِن كِتابة مُحتوى المصفوفة (array) كاملًا.
## The Range function in Python
تُتيح دالة `range()` تتابُعًا مِن الأعداد الصحيحة (integers) بُناءً على مُدخَلات الدالة (function's arguments). يُمكِن العثور على معلومات إضافيّة عن دالة `range()` في [توثيق بايثون (Python's documentation)](https://docs.python.org/3/library/stdtypes.html#range).

```python
range(stop)
range(start, stop[, step])

```
أول قيم الفترة (range) هُوَ المُدخَل (argument) `start`. إذا تمَّ استدعاء `range()` بمُدخَل (argument) واحدٍ  فقط، ستفترض بايثون أن `start = 0`.

يُعتبر المُدخَل `stop` الحدّ الأعلى للفترة (upper bound of the range). ومِن المُهم إدراك أن الحدّ الأعلى لا تشتمِل عليه الفترة.

في المثالِ أدناه، تبدأ الفترة بقيمة افتراضيّة `0` وتتضمَّن الأعداد الصحيحة الأقل من `5`. 


```python
# Example with one argument
for i in range(5):
    print(i, end=", ") # prints: 0, 1, 2, 3, 4, 
```

في المثالِ الآتي، نُعيِّن `start = -1` ونتضمَّن الأعداد الصحيحة الأقل من `5`.

```python
# Example with two arguments
for i in range(-1, 5):
    print(i, end=", ") # prints: -1, 0, 1, 2, 3, 4, 
```

المُدخل الاختياريّ `step` يتحكَّم في مقدار التزايد بين قيمِ الفترة. بشكلٍ افتراضيّ تكون `step = 1`.

في المثالِ الأخير، تبدأ الفترة من `-1` إلى `5` وتكون قيمة الـ `step = 2`.

```python
# Example with three arguments
for i in range(-1, 5, 2):
    print(i, end=", ") # prints: -1, 1, 3, 
```

## مُلخَّص

نتناول في هذِه المقالة استخدام الـ `for` loops في بايثون ودالّة `range()`.

تُكرِّر الـ `for` loops جُزءًا من الكود لِكُلِّ قيم القائمة (list)، المصفوفة (array)، السلسلة (string)، أو الفترة `range()`.

يُمكن تبسيطًا استخدام `range()` لكتابة الـ `for` loop. يُلزَم تعيين قيمة المُدخَل `stop` لِدالّة `range()`، بل يمُكن أيضًا تعديل قيمل البداية `start`ing ومقدار التزايد `step` بين الأعداد الصحيحة في دالّة `range()`.

----------

![Jeremy L Thompson](https://www.freecodecamp.org/news/content/images/size/w100/2021/02/151340_2.png)

[Jeremy L Thompson](https://www.freecodecamp.org/news/author/jeremylt/)

I am a computational scientist, software developer, and educator. I work in C, Rust, Julia, Python, and Fortran, among other languages. I am passionate about open source software and open education.

----------

If you read this far, tweet to the author to show them you care.  Tweet a thanks

Learn to code for free. freeCodeCamp's open source curriculum has helped more than 40,000 people get jobs as developers.  [Get started](https://www.freecodecamp.org/learn/)

freeCodeCamp is a donor-supported tax-exempt 501(c)(3) nonprofit organization (United States Federal Tax Identification Number: 82-0779546)

Our mission: to help people learn to code for free. We accomplish this by creating thousands of videos, articles, and interactive coding lessons - all freely available to the public. We also have thousands of freeCodeCamp study groups around the world.

Donations to freeCodeCamp go toward our education initiatives and help pay for servers, services, and staff.

You can  [make a tax-deductible donation here](https://www.freecodecamp.org/donate/).

Trending Guides

[What is JavaScript?](https://www.freecodecamp.org/news/what-is-javascript-javascript-code-explained-in-plain-english/)[Linux List Processes](https://www.freecodecamp.org/news/linux-list-processes-how-to-check-running-processes/)[Web Page Text Editor](https://www.freecodecamp.org/news/web-page-text-editor-how-to-open-html-code-in-mac-textedit/)[What is Open Source?](https://www.freecodecamp.org/news/what-is-open-source-software-explained-in-plain-english/)[Sim Swapping Attacks](https://www.freecodecamp.org/news/protect-yourself-against-sim-swapping-attacks/)[RNG Meaning in Gaming](https://www.freecodecamp.org/news/rng-meaning-what-does-rng-stand-for-in-gaming/)[Model View Controller](https://www.freecodecamp.org/news/the-model-view-controller-pattern-mvc-architecture-and-frameworks-explained/)[Front End Development](https://www.freecodecamp.org/news/front-end-developer-what-is-front-end-development-explained-in-plain-english/)[Full Stack Developer?](https://www.freecodecamp.org/news/what-is-a-full-stack-developer-back-end-front-end-full-stack-engineer/)[JavaScript Switch Case](https://www.freecodecamp.org/news/javascript-switch-case-js-switch-statement-example/)

[Bash Sleep](https://www.freecodecamp.org/news/bash-sleep-how-to-make-a-shell-script-wait-n-seconds-example-command/)[Bash Array](https://www.freecodecamp.org/news/bash-array-how-to-declare-an-array-of-strings-in-a-bash-script/)[What is a CV?](https://www.freecodecamp.org/news/what-is-a-cv-and-how-is-it-different-from-a-resume/)[Coding Programs](https://www.freecodecamp.org/news/coding-programs-101-ways-to-learn-to-code-for-free/)[How to Exit Vim](https://www.freecodecamp.org/news/how-to-exit-vim/)[HTML Line Break](https://www.freecodecamp.org/news/html-line-break-how-to-break-a-line-with-the-html-br-tag/)[C# String to Int](https://www.freecodecamp.org/news/how-to-convert-a-string-to-an-int-in-c-tutorial-with-example-code/)[Logical fallacies](https://www.freecodecamp.org/news/logical-fallacies-definition-fallacy-examples/)[JavaScript Online](https://www.freecodecamp.org/news/javascript-online-html-css-js-code-editor-list-browser-ide-tools/)[SQL Case Statement](https://www.freecodecamp.org/news/sql-case-statement-tutorial-with-when-then-clause-example-queries/)

[JavaScript toLowerCase](https://www.freecodecamp.org/news/javascript-tolowercase-how-to-convert-a-string-to-lowercase-and-uppercase-in-js/)[Angular NgClass Example](https://www.freecodecamp.org/news/angular-ngclass-example/)[SQL Aggregate Functions](https://www.freecodecamp.org/news/sql-aggregate-functions-with-example-data-queries-for-beginners/)[What is Web Development?](https://www.freecodecamp.org/news/what-is-web-development-how-to-become-a-web-developer-career-path/)[Best Way to Learn Python](https://www.freecodecamp.org/news/the-best-way-to-learn-python-python-programming-tutorial-for-beginners/)

[Word Count in Google Docs](https://www.freecodecamp.org/news/word-count-in-google-docs-tutorial-counting-words-and-characters-in-a-google-doc-or-word-file/)[Node Environment Variables](https://www.freecodecamp.org/news/how-to-use-node-environment-variables-with-a-dotenv-file-for-node-js-and-npm/)[Event Viewer in Windows 10](https://www.freecodecamp.org/news/event-viewer-how-to-access-the-windows-10-activity-log/)[Combine 1st/Last Name Excel](https://www.freecodecamp.org/news/combine-first-last-names-excel/)[JavaScript if-else & if-then](https://www.freecodecamp.org/news/javascript-if-else-and-if-then-js-conditional-statements/)

[About](https://www.freecodecamp.org/news/about/)[Alumni Network](https://www.linkedin.com/school/free-code-camp/people/)[Open Source](https://github.com/freeCodeCamp/)[Shop](https://www.freecodecamp.org/shop/)[Support](https://www.freecodecamp.org/news/support/)[Sponsors](https://www.freecodecamp.org/news/sponsors/)[Academic Honesty](https://www.freecodecamp.org/news/academic-honesty-policy/)[Code of Conduct](https://www.freecodecamp.org/news/code-of-conduct/)[Privacy Policy](https://www.freecodecamp.org/news/privacy-policy/)[Terms of Service](https://www.freecodecamp.org/news/terms-of-service/)[Copyright Policy](https://www.freecodecamp.org/news/copyright-policy/)