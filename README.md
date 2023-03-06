# مقدمة إلى جافاسكريبت

# سوف نتعلم في هذا الدرس :
* المتغيرات في لغة الجافاسكريبت
* التعامل مع الثوابت في لغة الجافاسكريب
* كيفية كتابة التعليقات
* أنواع البيانات Data Types 
## مقدمة
تعد جافاسكريبت (JavaScript) لغة برمجة قوية وشائعة تستخدم في تطوير تطبيقات الويب والتفاعلية وتطبيقات الجوال.   
تم إنشاء جافاسكريبت للعمل بشكل مثالي مع صفحات الويب المتصفح، حيث يمكن استخدامها لتحسين الوظائف وتجعل تفاعل المستخدم أكثر تفاعلية.

يتم تشغيل جافاسكريبت في المتصفح، ويتم كتابة الأوامر باللغة الإنجليزية. على الرغم من أنها تعتبر لغة متطورة، إلا أنه يمكن للمبتدئين التعلم منها بسهولة.
## أنواع البيانات والمتغيرات (Data Types and Variables) :

تعد أنواع البيانات والمتغيرات أحد المفاهيم الأساسية في جافاسكريبت. يمكن استخدام المتغيرات لتخزين البيانات في الذاكرة، والتعامل مع هذه البيانات باستخدام أنواع البيانات.


### المتغيرات  (Variables) :


تعد المتغيرات عبارة عن وسيلة لتخزين القيم في جافاسكريبت، ويمكن تعريفها باستخدام الكلمة المفتاحية  var و let , const  مع اسم المتغير. على سبيل المثال:
```js 
let age = 25;
const name = "Ali";
var isStudent = true;
```
في هذا المثال، تم تعريف المتغيرات age و name و isStudent لتخزين قيم العمر والاسم والحالة الدراسية على التوالي .
ويكون الفرق بينهم :
 ### ـvar
 في السابق كان يتم استخدام var  لتعريف المتغيرات، ولكن في الوقت الحالي، ينصح باستخدام let و const بدلاً من var لأسباب عديدة، بما في ذلك:

- استخدام  var يمكن أن يؤدي إلى مشاكل في نطاق المتغيرات، حيث يمكن الوصول إلى المتغيرات من خلال أي جزء من الكود، حتى خارج الدالة التي تم تعريف المتغير فيها.
- من الممكن في var ان يتم إعادة تعريف المتغير دون قصد، مما يؤدي إلى تغيير قيمة المتغير بشكل غير متوقع.
- في var لا يتم الإعلان عنها محلياً في `block`، وهذا يعني أن المتغير سيكون متاحًا في أي مكان داخل الدالة.

### ـlet
يمكن ان let يستخدم لتعريف المتغيرات المحددة داخل نطاق معين، ويمكن الوصول إليها فقط داخل النطاق الذي تم تعريفها فيه، مثل `blokcs`، أو الدوال، أو الأجزاء المحددة من الكود. ومن بين المزايا التي يوفرها let على var:

- تستخدم let لتعريف المتغيرات في نطاق الكتلة (block scope)، وهو النطاق الذي يحصره الأقواس  {}. هذا يعني أنها لا يمكن الوصول إليها خارج هذا النطاق .
- في let لا يمكن إعادة تعريفها في النطاق ذاته، مما يضمن عدم تغيير قيمة المتغير بشكل غير متوقع.

### ـconst 
- تستخدم const لتعريف المتغيرات في نطاق الكتلة ولكن بقيمة ثابتة، وهي القيمة التي يتم تعيينها للمتغير عند تعريفه.
- لا يمكن تغيير قيمة المتغير المعرف بواسطة const.
- تساعد const في تجنب الأخطاء التي يمكن أن تحدث بسبب تعديل قيمة المتغير بطريق الخطأ.

مثال :
```js
// var example
var x = 5;
if (true) {
  var x = 10;
}
console.log(x); // Output: 10

// let example
let y = 5;
if (true) {
  let y = 10;
}
console.log(y); // Output: 5

// const example
const z = 5;
// z = 10; // Error: Assignment to constant variable.
console.log(z); // Output: 5
```
عندما تقوم بتعريف متغير باستخدام var ، يتم تخزينه في نطاق الدالة. إذا تم تعريف المتغير داخل دالة ، فلن يكون متاحًا خارج الدالة.

على سبيل المقارنة ، عند استخدام let أو const ، يتم تخزين المتغير في النطاق الذي يتم فيه تعريفه. إذا تم تعريف المتغير داخل كتلة مثل if أو for ، فلن يكون متاحًا خارج block.

# تسمية المتغيرات 
يمكن تسمية المتغيرات في جافاسكريبت باستخدام أي مجموعة من الأحرف الصغيرة والكبيرة والأرقام والشرطة السفلية (_) ولكن هناك بعض القواعد التي يجب اتباعها عند تسمية المتغيرات:

* يجب أن يبدأ اسم المتغير بحرف أو شرطة سفلية (_).
* يمكن استخدام الأحرف الصغيرة والكبيرة والأرقام والشرطة السفلية (_).
* الأسماء حساسة لحالة الأحرف، يعني أن المتغير myVar و myvar و MyVar ليست متساوية.
* يجب تجنب استخدام الأسماء المحجوزة في جافاسكريبت مثل var و let و const و function وغيرها.
مثال على تسمية المتغيرات:
```js
let firstName = "John"; // باستخدام الحروف الصغيرة والكبيرة
const LAST_NAME = "Doe"; // باستخدام الشرطة السفلية والحروف الكبيرة
var age = 25; // باستخدام حرف صغير
let _address = "123 Main St"; // باستخدام الشرطة السفلية

```

في هذا المثال، تم استخدام الأحرف الصغيرة والكبيرة والشرطة السفلية في تسمية المتغيرات، كما تم تجنب استخدام الأسماء المحجوزة في جافاسكريبت.

#  التعليقات Comments

في حالات معينة أثناء كتابة الكود، قد يحتاج المبرمج إلى وضع بعض الملاحظات أو التعليقات. فمثلاً، قد يحتاج إلى وضع ملاحظة لتذكيره بتعديل code معين، فيقوم المبرمج حينها بكتابة بعض الملاحظات بجانب ذلك الكود للعودة إليه فيما بعد. وفي حالات أخرى، قد يعمل على الملف البرمجي أو المشروع البرمجي أكثر من شخص، وقد يحتاج أحد المبرمجين إلى أن يضع بعض الملاحظات لأعضاء الفريق، وهكذا. توفر التعليقات طريقة تُساعد المبرمج على كتابة ما يود من ملاحظات في البرنامج، وبالنسبة للغة JavaScript فإنها ستتجاهل تلك التعليقات، ولن تنظر إليها على أنها تعليمات تقوم بتنفيذها.

## تعليق السطر الواحد Single Line Comment

عند رغبتنا في وضع تعليق في سطر واحد أو ما يُسمى بـ single-line comment، والذي سينتهي بنهاية السطر، سنستخدم // كعلامة لبداية التعليق. يوضح السطر التالي هذه الفكرة.


    // This is a comment.

ليس بالضرورة أن يبدأ التعليق من بداية السطر، فقد يكون التعليق هو جزء من سطر برمجي. لتوضيح الفكرة، لاحظ معي المثال التالي:


    let age = 25; // This is my age.
## تعليق  متعدد الأسطر Multi-line Comments

في بعض الحالات، قد نحتاج إلى كتابة تعليق طويل، يمتد على أكثر من سطر. في هذه الحالة، يمكننا استخدام أسلوب التعليق متعدد الأسطر Multi-line Comment. ونقوم بذلك عن طريق كتابة الملاحظات بين /* */ .   لتوضيح الفكرة لاحظ معي المثال التالي.


    /* Write your
       comments here..
    */

قد يستخدم البعض أسلوب التعليق متعدد الأسطر كتعليق سطر واحد. لتوضيح الفكرة، لاحظ معي المثال التالي:


    /* Write your comment here.. */

وبنفس الأسلوب، يمكنك استخدامها عند وجود سطر برمجي. لتوضيح الفكرة، لاحظ المثال التالي:


    let age = 25; /*This is my age.*/

تعلمنا في هذا الدرس اهمية استخدام التعليقات لوضع الملاحظات و التنبيهات في الكود و لشرح بعض الأوامر البرمجية التي قمت بكتابتها لأعضاء الفريق الذين يعملون معك في نفس المشروع، و تعلمنا طريقتان لكتابة التعليقات: Single Line Comment و Multi-line Comments

### أنواع البيانات (Data Types) :

#### الأعداد (Numbers): وتشمل الأعداد الصحيحة والعشرية.
```js 
let a = 10;
let b = 5;
let c = a + b; 
console.log(c); // النتيجة: 15

```

#### السلاسل النصية (Strings): وتشمل مجموعة من الأحرف والأرقام والرموز المحيطة بعلامات التنصيص الأحادية أو الزوجية.
```js
let greeting = "Hello, world!";
console.log(greeting); // النتيجة: Hello, world!

```

```js
let greeting = 'أكاديمية طويق ';
console.log(greeting); // النتيجة: أكاديمية طويق

```

#####  خاصية length في النصوص :

يعتبر حساب عدد الأحرف في نص معين من العمليات التي يتم استخدامها في كثير من البرامج لخدمة أغراض مُختلفة. فمثلاً، قد تحتاج إلى التحقق من طول كلمة السر أثناء تسجيل مستخدم جديد في برنامجك، وهنا قد تساعدك خاصية length لهذا الغرض. في هذا الدرس سوف نتطرق للحديث عن خاصية length وكيفية كتابتها واستخدامها.

##### استخدام length لمعرفة عدد الأحرف

يمكن حساب عدد الأحرف في نص معين عن طريق استخدام خاصية length ولتوضيح الفكرة، لاحظ معي المثال التالي:

```js
    let name = 'Ali';
    console.log(name.length);
```
في السطر الأول قمنا بتعريف متغير باسم name وقيمته Ali، وفي السطر الثاني قمنا بحساب عدد الأحرف لقيمة المتغير name من خلال استخدام خاصية length، ومن ثم قمنا بطباعة النتيجة وفي هذه الحالة ستكون المخرجات على النحو التالي:

```
    3
```
لاحظ أن النتيجة 3 تمثل عدد أحرف قيمة المتغير name، أي القيمة Ali ، وهذا باختصار هو دور خاصية length.
في حال كان لدينا نص فارغ وقمنا باستخدام خاصية length فإن النتيجة ستكون صفر.

##### استخدام length مع النص بشكل مباشر

يمكن استخدام خاصية length بشكل مباشر مع نص معين، ولتوضيح الفكرة لاحظ معي المثال التالي:


    console.log('Saudi'.length);

لاحظ أننا قمنا باستخدام خاصية length مباشرة مع النص Saudi وستكون المخرجات على النحو التالي:

    5

كما تلاحظ حصلنا على النتيجة 5 وهذا لأن كلمة Saudi تحتوي على 5 أحرف.
للتنبيه، يتم احتساب المسافات والرموز في حساب طول النص.

##### مثال على استخدام length

من الاستخدامات الشائعة لخاصية length استخدامها في برنامج يقوم  بحساب طول كلمة السر لمستخدم جديد في حال اشتراط طول معين لقبول كلمة السر ولتوضيح الفكرة لاحظ معي المثال التالي:

```js
    let password = '12345678';
    if(password.length >= 8){
       console.log('The password is accepted') ;
    }
```
كما تلاحظ، في السطر الأول قمنا بحفظ كلمة السر داخل المتغير password. بعد ذلك قمنا بوضع الشرط الخاص لقبول كلمة السر،  وهو أن يتم قبولها في حال كانت تساوي 8 أحرف أو أكثر، ويتم طباعة الجملة The password is accepted في حال تحقق الشرط، وعليه، ستكون المخرجات على النحو الت:

```
     The password is accepted
```
لاحظ انه تم  تحقق الشرط وطباعة الجملة The password is accepted وذلك لأن طول كلمة السر يساوي 8.
تستخدم if للتحقق من صحة شرط معين، لذلك قمنا باستخدامها للتحقق من عدد حروف كلمة المرور، وسنتعلم المزيد عن جملة if في الدروس القادمة بإذن الله تعالى.

 تعلمنا في هذا الدرس كيفية معرفة عدد الأحرف في نص معين من خلال استخدام الخاصية length والطرق المختلفة لكتابتها واستخدامها.
 
 
##### الوصول إلى العناصر بإستخدام Bracket Notation

تتيح لك لغة JavaScript امكانية الوصول إلى عنصر أو حرف معين داخل النص. سنتطرق في هذا الدرس إلى كيفية الوصول إلى حرف معين داخل النص من خلال استخدام الأقواس المربعة [] أو ما يُسمى بمفهوم Bracket Notation.

##### كيفية الوصول إلى عنصر معين داخل النص

يمكن الوصول إلى عنصر معين داخل النص عن طريق استخدام الأقواس المربعة [] أو Bracket Notation وكتابة رقم خانة العنصر المطلوب بينهما، ولتوضيح ذلك لاحظ معي المثال التالي:

```js
    let language = 'JavaScript';
    console.log(language[2]);
```
قمنا في السطر الثاني من المثال السابق بتعريف متغير language يحتوي على القيمة JavaScript وبما أن الحروف في نص يتم ترقيمها من اليسار إلى اليمين بحيث يبدأ تعداد أول حرف من صفر، أي أن أول حرف J تكون قيمة خانته هي صفر ورقم خانة ثاني حرف a هي 1 وهكذا، وعند طباعة الخانة رقم ٢ للمتغير language ستكون المخرجات على النحو التالي:

```
    v
```
لاحظ أن النتيجة هي v وذلك لأن قيمة الخانة 2 في المتغير language هي الحرف v.
يُعرف رقم الخانة والذي نضعه بين الأقواس المربعة بمفهوم Index.

##### عدم إمكانية تحديث عنصر داخل النص

يعتبر مفهوم bracket notation بمفهوم يستخدم للقراءة فقط، أي لا يمكنك تحديث قيمة عنصر معين داخل النص بإستخدام Bracket Notation، ولتوضيح هذه الفكرة لاحظ معي المثال التالي:


    let name = 'Saleh';
    name[0] = 'R';
    console.log(name);

في المثال السابق قمنا بتعريف متغير باسم name وقيمته Saleh، وفي السطر الثاني قمنا بمحاولة لتعديل الخانة الأولى للمتغير name إلى الحرف R، وعند طباعة المتغير name ستكون المخرجات على النحو التالي:


    ```
    Saleh
    ```

لاحظ أن قيمة الخانة رقم 0 للمتغير name لم تتغير إلى R بل بقيت كما هي على قيمتها الأساسية، أي S .

تعرفنا في هذا الدرس على كيفية الوصول إلى عنصر معين داخل النص وتنفيذ عمليات مُختلفة عليه مثل الطباعة بالإضافة إلى أننا وضحنا عدم امكانية تحديث عنصر  معين داخل النص من خلال استخدام Bracket Notation.


#### القيم الثابتة (Booleans): وتستخدم لتمثيل القيم المنطقية مثل true و false.
```js
let isSunny = true;
let isRaining = false;

```
#### القيم الفارغة (Null): وهي تمثل عدم وجود أي قيمة، وتستخدم عادة لإعادة تعيين قيمة متغير معين.
```js
let myVariable = null;

```
#### القيم المُنشئة (Undefined): وهي تمثل عدم تعريف قيمة معينة، وتستخدم عادة عند تعريف متغير جديد.
```js
let myVariable;
console.log(myVariable); // logs "undefined"

```
المشغلات والتعبيرات (Operators and Expressions) :
يمكن استخدام Operators and Expressions في جافاسكريبت للقيام بالعديد من العمليات الرياضية والمنطقية. يمكن استخدام Operators  لإجراء عمليات الجمع والطرح والضرب والقسمة وغيرها، بينما يمكن استخدام Expressions للتحقق من الشروط وإجراء العمليات المنطقية.

Operators
يمكن تصنيف Operators في جافاسكريبت إلى عدة أنواع، بما في ذلك:

المشغلات الرياضية: وتشمل` + و - و * و / و %`.
```js
let x = 10;
let y = 5;
console.log(x + y); // Output: 15
console.log(x - y); // Output: 5
console.log(x * y); // Output: 50
console.log(x / y); // Output: 2
console.log(x % y); // Output: 0
```
المشغلات المنطقية: وتشمل `&& و || و ! و == و != و > و < و >= و <=`.
```js
let x = 10;
let y = 5;
console.log(x == y); // Output: false
console.log(x === "10"); // Output: false
console.log(x != y); // Output: true
console.log(x !== "10"); // Output: true
console.log(x > y); // Output: true
console.log(x >= y); // Output: true
console.log(x < y); // Output: false
console.log(x <= y); // Output: false

```
```js let x = 10;
let y = 5;
let z = 3;

console.log(x > y && y > z); // Output: true
console.log(x < y || y < z); // Output: false
console.log(!(x > y)); // Output: false
```

