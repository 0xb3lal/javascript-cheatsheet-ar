
## Number Methods

**tostring( )**
دي بتحول اي رقم ل string
```js
console.log(100.tostrig())

//Output

"100" //string
```

**tofixed( )**
دي لو فيه رقم float بتخليك تتحكم في عدد الارقام اللي ممكن يرجع بعد العلامة وخلي بالك بردو ان
ال ( )tofixed بترجع ديما string 
```js
console.log(100.777777.tofixed(2))

//Output

"100.77" //strig
```

**parseInt( )**
دي بتحلل البيانات وترجعلك منها الرقم بس 
```js
console.log(parseInt("100 Belal"))

//Output

100 //integer
```
لكن هي مش بالذكاء الكافي عشان لوقبل الرقم كلام ترجعلك بردو الرقم لا هي بس لو الرقم في بداية الكلام بترجعه 

**parseFloat( )**
دي شبه اللي فوق بالظبط بس كلك نظر دي فكرتها ان لو الرقم float بترجعهولك كامل float
```js
console.log(parseFloat("100.500"))

//Output

100.5 //float
```

**isInteger( )**
دي زي ما انت شايف بتسال سوال شرطي هل ده رقم وبترجع true, false 
```js
console.log(Number.isInteger(100))

//Output

true 
```

**isNan( )**
دي بتسال هل الحاجة دي not a number وبترجع بردو true, false

### Math Object

لو هنستخدم اي حاجة من ال methods اللي جاية لازم قبل ما تستخدمها تحط قبلها `Math`
**round( )**
دي بتقرب الكسر سواء لفوق او لتحت لكن بشروط زي لو الرقم اقل من النص (0.5) هينزل لاقرب رقم تحت ولو اكبر من النص هيرفعه لاقرب رقم فوق
```js
console.log(Math.round(0.5))

//Output
0

console.log(Math.round(0.6))

//Output
1
```

**ceil( )**
دي معناها سقف وبتعمل نفس الوظيفة الميثود اللي فوق دي لكن دي ديما هترفع الكسر لاقرب رقم فوق بغض النظر الكسر ده اصغر او اكبر من النص
```js
console.log(Math.ceil(0.1))

//Output
1
```

**floor( )**
دي معناها ارضية ونفس الفكرة بردو لكن دي هتنزل الكسر ديما لاقرب رقم تحت بغض النظر عن الكسر قيمته ايه 
```js
console.log(Math.floor(0,7))

//Output
0
```

**abs( )**
دي بترجع القيمة المطلقة من العنصر يعني لو سالب يكون موجب 

**min( )**
دي من اسمها واضح انك لو اديتها شوية ارقام هترجع اصغر رقم فيهم 

**max( )**
دي لو اديتها شوية ارقم هترجع اكبر رقم فيهم

**pow( )**
دي اللي هي الاس بتديله رقم والاس بتاعه 
```js
console.log(Math.pow(2, 4))

//Output
8
```

**random( )**
دي بترجعلك رقم عشوائي مش محتاجة كلام كتير

**trunc( )**
دي ديما لو مديها رقم float مثلا هترجع بس الرقم الصحيح اللي فيه 
```js
console.log(Math.trunc(99.5))

//Output
99

```


## String Methods

**charAt( )**
دي بتجبلك قيمة ال Index ده ايه بمعني 
```js
let name = "Belal"
console.log(name.charAt(1));

//Output
e //عشان اللغة بتبدا من الصفر 
```

**trim( )**
دي بتشيل المسافات اللي ممكن تكون موجودة في النص من الاول او من الاخر

**indexOf( )**
بيبحث من عن الكلمة اللي انت هتحددها في ال string 

**lastIndexOf( )**
نفس الكلام هيبحث عن الكلمة اللي انت هتحددها لكن من الاخر للاول

**slice( )**
دي بتقطعلك النص بتاعك حتة انت اللي تحددها سواء ممكن تحددله مكان يقطع من لحد الاخر او تحددله مكان يبتدي منه ونهاية يقف عنده وخلي بالك انت لو قلتله اقطعلي مثلا من 2 لحد 6
خلي بالك ال index 6 مش هيكون معاه `not including the end`
حاجة كمان لوعاوز يعد من الاخر للاول هتستخدم `negative value`
```js
let name="Belal Ammar"
console.log(name.slice(2))

//Output
"lal Ammar"

console.log(name.slice(2, 6))

//Output
"lal "
```

**repeat( )**
دي بتكرر الحاجة مش محتاجة شرح كتير لكن انا كاتبها للتذكير 

**split( )**
دي ببساطة بتقطع العنصر بتاعك وبتاخد حاجتين لكن الحاجتين optional وبترجع الحاجة بتاعتك او يعن الناتج في array

**substring( )**
دي شبه ال `()slice`لكن في شوية اختلافات زي انها مش بتدعم القيم السالبة اللي كانت ال slice بتدعمها عشان تجيب من الاخر للاول وكمان لو خليت ال value بتاعة البداية اكبر من النهاية هيبدلهم تلقائي وكمان لو اديته اي value سالب هيخليها كانك بتقوله ابدا من الصفر
```js
let a="Belal Ammar"
console.log(a.substring(2,6))
//Output
"lal "

console.log(a.substring(6,2))
//Output
"lal "

console.log(a.substring(-10,6))
//Output
"Belal "
```

**substr( )**
دي بردو تقريبا زيهم لكن دي مش بتتعامل بال index لا بتتعامل ب length يعني بدل ما بتقول عاوز من فين لحد فين لا بتقوله عاوز ال Length الفلاني ولو حددتله length اكبر من حجم ال string اللي عندك هيرجع string فاضي ودي عادي بياخد قيمة سالبه و اه بيجيب من الاخر عادي
```js
let a="Belal"
console.log(a.substr(0,5))
//Output
"Belal"

console.log(a.substr(-3, 2))
//Output
"la"
```

**includes( )**
دي من الحاجات اللي بترجع true, false ومن اسمها باين هي بتعمل ايه هي بتشوف هل ال string بيحتوي علي الكلمة اللي انت محددهالها ولا لا وخلي بالك هنا ممكن تحددله index يبدا يدور من عنده لكن هو optional 

**startwith( )**
دي بردو بتشوف هل ال string بيبدا بالكلمة اللي انت عاوزها ولا لا

**endwith( )**
نفس الكلام بيشوف هل ال string بينتهي بالكلمة اللي انت عاوز ها ولا لا

## Comparison Operators

**== Equal
!= Not Equal
=== Identical
!== Not Identical**

```js
console.log(10 == "10"); // Compare Value Only
//Output
true

console.log(10 != "10"); // Compare Value Only
//Output
false

console.log(10 === "10"); // Compare Value + Type
//Output
false

console.log(10 !== "10"); // Compare Value + Type
//Output
true

```


**! Not
&& And
|| Or**


### NUllish Coalescing Operator

**Logical Or ||**
وده لو عندك لاي سبب قيمة رحعت null , undefined, any falsy value هيكون واخد زي بديل يرجعه لو حاجة من دول رجعت 

**NUllish Coalecing Operator ??**
ده نفس الفكرة لكن ده بيرجع بس البديل لو قيمة  كانت Null , undefined

## Array Methods

**unshift( )**
دي بتاخد منك عدد العناصر اللي انت عاوزها تضيفها في `بداية` ال Array 

**push( )**
نفس اللي فوق لكن دي بتضيف العناصر اللي عاوزها في `نهاية` ال Array

**shift( )**
دي بتمسح `اول` عنصر في ال Array بس خد بالك انه بيعمل للعنصر return يعني تقدر تخزنه في variable وتستخدمه تاني عادي جدا

**pop( )**
دي بتمسح `اخر` عنصر في ال Array بس خد بالك انه بيعمل للعنصر return يعني تقدر تخزنه في variable وتستخدمه تاني عادي جدا

**indexOf( )**
دي بتبحث عن العنصر اللي انت بتحدده داخل ال Array وبترجعلك رقم ال index بتاعه كام وممكن كمان تحددلها تبدا منين وتنتهي فين لكن لومحددتش هيبدا يبحث من ال index صفر وبردو خلي بالك ده بيجيب اول قيمة بس انت باحث عنها لو عندك كذا value متشابهة هيجيب اول واحدة تقابله

**lastIndexOf( )**
ده شبه اللي فوق لكن ده بيبحث من الاخر وبردو بيرجع رقم ال Index و لو اديته قيمة سالبة بعد هيبدا يبجث من عندها بردو من الاخر للاول

**includes( )**
دي زي شرط كدا بتشوف ال value اللي انت اديتهالها موجودة فعلا في ال Array وبترجعلك يا true , false

**sort( )**
دي بترتب ال values اللي في ال Array g و ابقي ابحث عنها لانها شغالة بطريقة غريبة لانها مش بترتب علي حسب ال value دي اكبر من دي ولا لا .
دي برتب حسب بداية ال value يعني لو بتبدا ب 2 حتي هي 2000 و بعدها 10000 هترتب ال 10000 قبل ال 2000 فا ابحث عنها بردو عشان الدنيا توضح 

**reverse( )**
دي بتعكس الدنيا خالص اللي في الاخر ييجي في الاول والعكس صحيح 

**slice( )**
دي من اسمها بتطع ال Array يعني بتاخد حتة منه وتجعهالك عادي جدا وبتاخد منك ال start , end
لكن الاتنين optional يعني لو مديتهاش حاجة خالص `هترجعك ال Array كاملة (Array.length)`

**splice( )**
دي بتستخدم في انها تضيف تعدل تحذف عناصر حسب ما تحددلها لكن خلي بالك انها بتعدل علي ال Array الاصلية مهم تعرف دي لان معظم الميثودز تقريبا بتنشئ array جديدة بالتعديل اللي هي بتعمله 

**join( )**
دي بتستخدم عشان تفصل بين عناصر ال array اللي وممكن متستخدمش معاها حاجة وممكن تستخدم معاها separator 

**concat( )**
دي بتجمع اتنين array مع بعض يعن عندنا اتنين array بتضيف عناصرهم علي بعض في array جديدة


## Ternary Operator

دي طريقة كدا من طرق انك تعمل condition في js كدا كدا قريبة من ال if لكن الحكاية هنا انك ممكن تعملها في سطر واحد حاجة اختصار يعني لكن في حاجة دي بنستخدمها لو الشرط اللي هتعمله صغير يعني حاجة بسيطة اما لو الشرط كبير وهيكون في logic الافضل تستخدم if عشان الكود بتاعك يكون friendly, readable
```js
/*
Formt:

Condtion ? true : false

*/
// ده شكل الكود العادي 

let age = 20;

if (age >= 18) {
  console.log("adult");
} 
else {
console.log("minor");
}
//Output 
"adult"

// ternary operator

let age = 20;
console.log(age >= 18 ? "adult" : "minor");

```

## Functions Notes

لو عندي function بتاخد parameter ونا مش هكون عارف عدد ال parameters اللي المفروض هتاخدها بنستخدم `...` قبل البارميتر اللي هنديه للفانكشن وده ساعتها هيحول ال parameter ده ل `Array`وساعتها هتقدر تلووب علي ال values اللي فيه اللي هتكون في حاالتنا قيم ال parameter اللي انا already معرفش عددها كام 
```js
function calc (...numbers){
	let result = 0;
	for(let i = 0; i<numbers.length; i++){
		console.log(numbers[i])
		result += numbers[i] // result = result + numbers[i]
	}
	return result
}
console.log(calc(10, 20, 30, 40))

//Output
100
```

### Anonymous function

دي عبارة عن function مش بيكون ليها اسم وبتكون متخزنة جوة variable وبنادي عليها باسم ال variable ده لكن في شوية حاجات لازم تخلي بالك منها ان ال function عشان هي بتكون متخزنة في variable فمش هينفع تنادي عليها تنادي عليها قبل ما تكون عامل declare لل variable ده وده اول فرق بينها وبين ال function العادية لان ال function العادية ممكن تنادي عليها عادي قبل ما تعملها declare بمعني انك مثلا هتكون منادي عليها في السطر الاول في الكود بتاعك وانت مثلا معرفها او يعني عاملها في السطر التاسع مثلا في ال function العادية ده عادي لان اصل الفانكشن بتكون في معمولة في ال run time فمفيش اي error هنا 
لكن ال anonymous func عشان هي بتتخزن في variable وجيت تعمل نفس الكلام اللي فوق عشان مكسل اكتبه هيحصل error انه انت ناديت عليها من قبل ما تعملها declare

طب بنستخدمها امته ال anonymous func دي بنستخدمها لحاجة مثلا انا هستخدمها لمرة واحدة وخلاص فملهاش لازمة ان اعمل function عادية واديها اسم مخصوص وقصة وليلة لا دي بس function هتعمل حاجة وخلاص مش هستخدمها تاني هنا ال anonymous func مناسبة جدا

```js
let calculator = function (n1, n2){ // no name this is anonymous func
return n1 + n2 ;
}
console.log(calculator(4, 6));
//Output
10
```

مثال كمان بس عشان اوريك ايه لازمة ال anonymous func 
```js
setTimeout(function(){
	console.log("i'am anonymous func");
}, 2000)
```
بس دي عبارة عن function فكرتها ان بعد ثانيتن هتطبع الكلام ده في ال console بالله عليك هنا انا محتاج اسمي ال function دي اسم؟ جدع قولت لا ! يبقي خلاص هنا نستخدم ال anonymous func.


### Nested function

دي من اسمها انها بتعمل functions جوا بعض بنستخدمها في حالة ان عندنا function بتعمل process كبيرة 
ونا عاوز اخلي ال process دي وهي بتتعمل تكون الدنيا more simple فبنستخدم الطريقة دي عشان نعمل كدا وبنعمل في الاخر عادي خالص في اخر ال function الاصلية (الأم) return عادي جدا لل result الاخيرة الي انت محتاجها 
```js
function sayHello(fname, lname){ // main function
	let message = "Hello"
	
	//nested functions
	
	function concatMsg(){
	
		function getFullName(){
		
			return `${fname} ${lname}`
			
		}
	return `$message ${getFullName()}`
	}

return concatMsg

}

console.log(sayHello("Belal", "Ammar"))
```

### Arrow function

دي عبارة عن function لكن الفكرة إنها طريقة مختصرة لكتابة الـ function في JavaScript.  
وهي ممكن تقبل parameters عادي وممكن برضو تكتبها في سطر واحد في حالة إنها بترجع أو بتنفذ statement واحدة بس وبنستبدل كلمة `function` في تعريفها بالرمز: `=>`
عشان نعرف إنها Arrow Function أما لو فيه أكتر من statement هيتنفذوا، فلازم نستخدم `{}`
ونكتب `return` عادي لو عايزين نرجّع قيمة وممكن برضو لو فيه parameter واحد بس نشيل الأقواس `()` ونكتب الـ parameter مباشرة
```js
let print = () => 10;
console.log(print());
//Output
10
```

## Scopes in JS

الـ **global scope** ده الاسكوب العام بتاع البرنامج، بمعنى إنك لما تعرف variables فيه فـ المتغيرات دي ممكن أي جزء في البرنامج يعمل access عليها عادي زي مثلًا function أو loop أو أي block تاني في الكود

أما الـ **local scope** فبيكون خاص بالمكان اللي المتغير اتعمل فيه، يعني ال variables دي مينفعش نعمل access عليها من بره المكان ده وبتبقى متاحة بس جوه الـ function أو الـ block اللي اتعرفت فيه

وديما يعني ب ده by default طبعا انه ديما بيكون الاولوية ل local scope يعني مثلا انت عندك function عرفت فيه variable معين وليكن مثلا a هو اول حاجة بيدور جوة ال function دي (local scope)
هل عندنا variable بالاسم ده ؟؟ ايوة يبقي خلاص مش هنطلع برة طب لا يبقي نروح ندور
برة (Global scope) 
نستفاد ايه بقي من الكلام ده انا مثلا ال functions او اي حاجة عادي ليها accessعادي جدا علي
ال global scope لكن خلي بالك محدش ليه access علي حاجة local ركززز اوي في الحتة دي

### Block Scope
الـ **block scope** بيكون الاسكوب الخاص بأي كود مكتوب جوا `{ }`
يعني لو عرفت variables جوا block زي `if` أو `for` أو أي `{ }` فالـ variables دي بتبقى متاحة جوا الـ block ده بس ومينفعش نعمل access عليها من بره لكن الكلام ده بيحصل لما المتغير يتعرف
باستخدام `let أو const`لأن دول بيشتغلوا بنظام `block scope`
أما لو variable اتعرف باستخدام `var` فهو مش بيحترم الـ block scope وبيبقى متاح بره الـ block عادي.

### Lexical Scope

محتاجين بس كدا نعرف كام معلومة حلوة عن ازاي ال scope بيشتغل فال js وبعض المعلومات الاخري 

الـ **execution context** ده البيئة اللي JavaScript بتنفذ فيها الكود يعني لما الكود يشتغل ال JavaScript بتعمل context مخصوص عشان تعرف ال variables موجودة فين ال functions فين الكود هيتنفذ إزاي

بمعنى أبسط:  
هو المكان اللي الكود بيتفهم ويتنفذ جواه وكل مرة function
بتتنده JavaScript بتعمل **execution context جديد** ليها
```js
function sayHi() {
  let name = "Belal";
  console.log(name);
}

sayHi();
```
لما `sayHi()` تتنادي JavaScript بتعمل **execution context** خاص بال function دي عشان تشغل الكود اللي جواها

الـ **lexical environment** هو المكان اللي JavaScript بتخزن فيه ال variables, functions مع معرفة المكان اللي اتعرفوا فيه في الكود
كلمة **lexical** معناها إن JavaScript بتحدد الاسكوب حسب مكان الكود في الكتابة **مش حسب وقت التنفيذ**.
```js
let x = 10;

function test() {
  console.log(x);
}

test();
```
ال function هنا قدرت توصل لـ `x` لأن JavaScript بتبص على مكان تعريف ال function في الكود وتبدأ تدور في **ال scopes اللي فوقها**

علاقتهم ببعض ان كل **execution context** بيكون جواه حاجة اسمها **lexical environment**

في حاجة كمان مهم انك تعرفها عشان تفهم ال logic ال js كويس او يعني عشان تقدر تتخيل وهي 
الـ **scope chain** في JavaScript عبارة عن الطريقة اللي JavaScript بتدور بيها على ال **variables** لما الكود يحاول يعمل access عليهم بمعنى لما JavaScript تحتاج variable بتبدأ تدور عليه في الاسكوب الحالي ولو ملقتهوش تبدأ تطلع للاسكوب اللي **فوقه**، وتفضل تطلع لحد ما توصل للـ **global scope**
```js
let a = 10;

function first() {
  let b = 20;

  function second() {
    let c = 30;
    console.log(a);
  }

  second();
}

first();
```

هنا مثال مثلا عشان نشوف ال js وهي بتحاول توصل ل variable ال a
تدور في ال scope بتاع **second** مش موجود تدور في scope بتاع **first** مش موجود تدور في **global scope**
وزي ما انت شايف كده هتلاقي `a` في **global scope** يعني بيدور **من تحت لفوق** وليس العكس 

## Higher Order Function

الـ **higher order function** في JavaScript هي function بتتعامل مع functions تانية
يعني ممكن تعمل حاجتين تستقبل function **كـ parameter** او ممكن بردو**ترجع** function

```js
function greet(name) {
  return "Hello " + name;
}

function processUser(callback) {
  return callback("Belal");
}

console.log(processUser(greet));

```

هنا ال`processUser` تعتبر **higher order function** لأنها استقبلت `greet` كـ parameter

### map ( )

دي عبارة عن  method موجودة في **arrays** في JavaScript ووظيفتها انها  بتلف على كل عنصر في الـ array وتطبق عليه function وترجع **array جديدة** حاجة شبه كانك عامل loop علي array عشان ترجع منه العناصر بتاعته

```js
const numbers = [1,2,3,4];

const result = numbers.map(num => num * 2);

console.log(result);

//Output: [2, 4, 6, 8]

let result = numbers.map(function(ele){
return num * 2
})

//Output: [2, 4, 6, 8]

```

اللي حصل هنا ان ال map لفت علي كل عنصر في ال array كل عنصر اتبعت لل func ال func ضربته في 2 رجعت array جديدة بالنتيجة وعملتها بالشكلين العادي وال arrow عشان تعرف انه عادي بتقبل النوعين 
احنا بنعتبر ان ال map هي higher order function لان زي ما انت شوفت انها بتاخد function as a parameter

### filter( )

الـ **filter** في JavaScript هي method موجودة على الـ arrays وظيفتها انها تمشي علي كل عنصر في ال array و  تختار بس العناصر اللي بتحقق شرط معين وترجعلك array جديدة لكن من غير العناصر اللي محققتش الشرط ده 
```js
let numbers = [1, 2, 3, 4, 5, 6];

// نختار الأرقام الزوجية بس
let evenNumbers = numbers.filter(function(num){
    return num % 2 === 0;
});

console.log(evenNumbers);
//Output: [2, 4, 6]

let evenNumbers = numbers.filter(num => num % 2 === 0);
//Output: [2, 4, 6]
```

### reduce( )
الـ **`reduce()`** في JavaScript هي method على الـ arrays بتستخدمها لما تكون عايز تحول كل عناصر الـ array لقيمة واحدة يعني بدل ما ترجع array زي map او filter لا ال reduce بترجع عنصر واحد فقط وهي ال result,ممكن نستخدمها في جمع و ضرب الأرقام دمج النصوص حساب مجموع قيم معينة
```js

let numbers = [1, 2, 3, 4, 5, 6];
let result = numbers.reduce(function(accumulator, currentValue){
  return accumulator + currentValue
}, initialValue)

console.log(result)
// Output: 21

/*
accumulator: القيمة الل بتتجمع فيها النتيجة
currentValue: Array القيمة الحالية في ال
initialValue: القيمة اللي عاوز تبدا بيها ودي بتكون اختيارية
*/

```

### forEach( )

الـ **`forEach()`** في JavaScript هي method خاصة بالـ arrays بتستخدمها عشان تمشي على كل عنصر في الـ array وتنفذ عليه كود معين لكن الفرق بينها وبين ال filter, map انها مش بتنشئ Array جديدة لانها كمان مش بترجع حاجة بترجع `undefind` هي بس بتنفذ function معينة علي كل عنصر وخلاص
```js
// Main format

array.forEach(function(element, index, array) {
   return
});
```

## Object

الـ **Object** ده طريقة لتخزين الداتا في شكل (key : value) وممكن تعمل جوا ال object ده methods , properties 

ال **properties** دي بالعامية كدا هي المعلومات اللي عاوزين نعرفها في ال object 
ال **methods** دي هي ال functions اللي بتنفذ حاجة معينة لكن بنستدعيها من داخل ال object
property

```js
//Ex to creta object 

let user = {
  name: "Belal",         //property
  country: "Egypt",      //property
  
  sayHello: function() { //method 
	return ("Hello");  
}
};

console.log(user.name);
console.log(user.country);
console.log(user.sayHello());

/*
Output

Belal
Egypt
Hello
*/
```

### Bracket Notation
عندنا حاجة بقي او يعني طريقة استخدام كدا اسمها `Bracket Notation` دي طريقة بنستخدمها واحنا بنادي مثلا علي property او method من داخل object بنستخدمها مثلا في حالة اننا عرفنا مثلا property او method بطريقة متمشيش مع rules بتاعة تعريف ال identifiers زي ما انت عارف انك مثلا مينفعش ال identifiers اللي بتعرفه يبدا برقم او يكون جواه space او - فلو مثلا انت عرفت property ب `country of` فدي تسميتة غلط فطبيعي لازم 
تحطها في دبل كوتس `"country of"` طب وانت بتنادي عليها مش هينفع تنادي عليها بالطريقة العادية اللي هي `user.country of` كدا غلط عشان تنادي عليها صح لازم تحطها جوا `[]` او لو مثلا حط اسم property عندك جوا variables وعاوز تنادي باسم ال variables ده بدل اسم ال property بردو وانت بتنادي عليه لازم تستخدم `[]`  وخلي بالك احنا لما بنستعمل
ال `Bracket Notation` مش بنحط ال `.` بعد اسم ال object
```js
let myVar = "contry"

let user = {
  name: "Belal",         //property
  country: "Egypt",      //property
  "country of": "Usa"
}
};

console.log(user.name);
console.log(user[myVar]);
console.log(user["country of"]);


/*
Output

Belal
Egypt
Usa
*/
```

### Create Object With New Keyword

دي طريقة ممكن ت create بيها object بدل الطريقة العادية اللي انت شفتها فوق وهي انك ممكن تنشئ object باستخدام ال `()new Object` دي طريقة اسمها **New Keyword**
```js
let user = new Object({
  name: "Belal",         //property
  country: "Egypt",      //property
}) ;

console.log(user.name);
console.log(user.country);
/*
Output

Belal
Egypt
*/

// object وممكن تستخدم الطريقة دي بردو في انك تضيف من برة باستخدام اسم ال  
let user = new Object({
}) ;
user.name: "Belal",         //property
user.country: "Egypt",      //property
console.log(user.name);
console.log(user.country);
/*
Output

Belal
Egypt
*/

```

وطبعا لو حطيت جوه جو مثلا property واديتها قيمة وجيت برة عملتها تاني بقيمة جديدة مش محتاج اقولك انه هيعمل over write علي القيمة القديمة

### this

ال`this` هي مش method ولا object هي Reference (إشارة) للـ Object اللي بيشغّل الكود بمعني اخر `this` بتشير لــ مين اللي نادى الفنكشن او يعني الفانكشن دي مملوكة لمين ركز ديما في الحتة دي عشان بتلخبط

```js
let user = {
    name: "Belal",
    sayHello: function() {
        console.log(this.name);
    }
};

user.sayHello();

/*Output: Belal 
becouse: this === user
*/
```

اسال نفسك سوال مين هنا اللي مالك ال name ؟؟  بالظبط زي ما انت جاوبت هو ال object اللي اسمه user بص بقي قيس علي كدا 

**مشكلة `this` مع Arrow Functions**

```js
let user = {
    name: "Belal",
    show: () => {
        console.log(this.name);
    }
};

user.show();
//Output: undefined
```
ليه؟

لأن arrow functions مبيكونش ليها this خاص بيها  
بتاخد `this` من المكان اللي اتعملت فيه

**ملحوظة:**
لو ال function اللي انت حطيت فيها ال this دي normal function اذا 
```txt
this = object اللي نادى الفنكشن
```
لو هي كانت arrow function اذا 
```txt
this = Global Scope ال
```


### Create Object With Create Method

ال`Object.create(proto)` بتعمل object جديد وبتخلي الـ prototype بتاعه هو `proto`
ده معناه إن الـ object الجديد يورث الخصائص والـ methods من الـ object اللي إنت حطيته ك prototype
```js
let newObject = Object.create(proto, [propertiesObject]);
```
ال`proto` ده ال object اللي الـ newObject هيورث منه

ال`propertiesObject` ده اختياري، تقدر تعرف خصائص مباشرة مع تعريف الـ object الجديد
```js
let person = {
    greet: function() {
        console.log("Hello, " + this.name);
    }
};

let user1 = Object.create(person);
user1.name = "Belal";

user1.greet(); 
//Outpu: Hello, Belal

```

احنا هنا استخدمنا this عشان يشاور علي ال object اللي هيديه الميثود زي ما انت شايف ال Object اللي اسمه Person مفيهوش property اسمها name فلو كنا حطينا person مكان this 
كان الناتج هيكون `Hell, undefind` انما استخدمنا هنا this عشان هنا هتعود علي ال property اللي في ال user1 عشان هو اللي عنده اسم ال property دي وزي ما انت فهمت ان ال user1 هيورث كل حاجة من ال Person لانه user1 واخد ال Person ك `proto` 
### Create Object With Assign Method

ده بيعمل object ممكن ياخد properties بتاعة object واحد او اكتر بالاضافة انك طبعا ممكن تضيف كمان انت Properties جديدة عادي جدا وبياخد قيمتين هما ال `source` , `target`

ال `target` هو ال object اللي هيتضافله ال properties اللي انت عاوزها
ال `source` دول ال object أو ال objects اللي هتاخد منها ال properties المطلوبة 
```js
let user = { name: "Belal" };
let info = { age: 22, gender: "male" };

Object.assign(user, info);

console.log(user);
//Output: { name: "Belal", age: 22, job: "Bug Hunter" }
```
هنا زي ما شوفت ال output ال Properties من `info` اتضافت على `user`

```js
let obj1 = { a: 1 };
let obj2 = { b: 2 };
let obj3 = { c: 3 };

let merged = Object.assign({}, obj1, obj2, obj3);

console.log(merged);
//Output: { a: 1, b: 2, c: 3 }
```
هنا استخدمنا `{}` كـ target عشان نعمل object جديد بدل ما نغير أي object موجود

## Dom

ال**DOM** اختصار Document Object Model  
وهو  الطريقة اللي JavaScript بتشوف بيها صفحة الـ HTML يعني ال browser بيحول صفحة HTML ل (Objects) تقدر JavaScript تتعامل معاها.
و دول بعض الحاجات اللي ممكن تتعامل بيها مع ال dom لكن هما كتير جدا 

### Get Elements

**getElementById**

دي بتجيب عنصر واحد باستخدام ال **id** و  الـ id لازم يكون `unique` يعني عنصر واحد بس في الصفحة
```html
<h1 id="main">Hello</h1>
<script>
let element = document.getElementById("main");

console.log(element);
//Output: Hello
</script>
```

**getElementsByTagName**

بتجيب العناصر حسب **اسم ال Tag**
```html
<p>text1</p>
<p>text2</p>
<p>text3</p>
<script>
let paragraphs = document.getElementsByTagName("p");

console.log(paragraphs);
/*
Output: 
<p>text1</p>
<p>text2</p>
<p>text3</p>
*/
</script>
```
زي ما انت شايف مرجعة Html collection وعشان توصل لعنصر منهم بتستخدم index
```js
console.log(paragraphs[0]);
console.log(paragraphs[1]);
```

**getElementsByClassName**

بتجيب العناصر اللي عندها **class معين**
```html
<div class="box">1</div>
<div class="box">2</div>
<div class="box">3</div>
<script>
let boxes = document.getElementsByClassName("box");

console.log(boxes);

/*
Output: 
<div class="box">1</div>
<div class="box">2</div>
<div class="box">3</div>
*/
</script>
```
زي ما انت شايف مرجعة Html collection وعشان توصل لعنصر منهم بتستخدم index
```js
boxes[0]
boxes[1]
```

**CSS Selectors**
ال JavaScript تقدر تستخدم نفس `CSS selectors` لكن في طريقتين:

ال `querySelector`
دي بيرجع أول عنصر فقط
```js
document.querySelector(".box")
document.querySelector("#main")
document.querySelector("p")

let el = document.querySelector(".box");
console.log(el);
```

ال `querySelectorAll`
بيرجع كل العناصر
```js
elements[0]
elements[1]
```

### Documents

**document.title**
بيجيب أو يغير `title` الصفحة
```js
console.log(document.title);
```
**document.body**

ده بيمثل كل `body` الصفحة وتقدر تغير او تعدل فيه عادي
```js
console.log(document.body);
```

**document.images**

بيجيب كل الصور في الصفحة وممكن تغير بيها عادي جدا 
```html
<img src="1.jpg">
<img src="2.jpg">

<script>
let imgs = document.images;

console.log(imgs);

/* 
index ممكن توصل لصورة معينة باستخدام ال 

imgs[0]
imgs[1]

*/
</script>
```

**document.forms**

بيجيب كل ال `forms` في الصفحة وممكن توصل لفورم معين بردو باستخدام ال index او بالاسم 
```html
<form id="login">
<input type="text">
</form>
<script>
let forms = document.forms;

console.log(forms);
</script>
```

**document.links**

بتقدر تجيب وتعدل كل الروابط `<a>` اللي فيها `href` وممكن توصل ل لينك معين باستخدام ال Index
```html
<a href="google.com">Google</a>
<a href="facebook.com">Facebook</a>
<script>
let links = document.links;

console.log(links);
</script>
```

### Get, Set Elements
 
 **innerHTML**

ده بتقدر تيجيب و تغير محتوي العنصر  بس لو المحتوي ده في html فهو هينفذه ك html عادي جدا
```html
<div id="box">
  <p>Hello</p>
</div>
<script>
let el = document.getElementById("box");

console.log(el.innerHTML);
//Output: <p>Hello</p>
</script>
```

**textContent**

دي بقي شبه ال `innerHTML` بس دي بتجيب محتوي العنصر ولو جواه html هتطبعه زي ما هو مش ك نص مش هتنفذه
```html
<div id="box">
  <h1>Hello</h1>
</div>
<script>
let el = document.getElementById("box");

console.log(el.textContent);
//Outpu: Hello
</script>
```

**innerText**

ال`innerText` شبه `textContent` لكنه بيتعامل مع النص الظاهر بس
```html
<div id="box">
  Hello
  <span style="display:none">Secret</span>
</div>
<script>

let el = document.getElementById("box");

console.log(el.innerText);
//Output: Hello 
</script>
```
طب مجبش كلمة secret ليه عشان هي مخفية و ال innerText مش بيجيب غير الظاهر بس

**getAttribute**
بتجيب قيمة attribute معين
```html
<img id="img" src="photo.jpg" alt="image">
<script>
let img = document.getElementById("img");

console.log(img.getAttribute("src"));
//Output: photo.jpg
</script>
```

**setAttribute**

بتغير أو تضيف attribute

```html
<script>
img.setAttribute("src", "newphoto.jpg");
</script>

<!--Output-->
<img src="newphoto.jpg" title="My Image">
```

### Check Attributes

**attributes**

ده بيرجعلك كل الـ attributes الخاصة بالـ HTML element في صورة `NamedNodeMap`عشان تقدر توصل لأي attribute موجود في العنصر
```html
<input type="text" id="username" class="form-control" placeholder="name">
<script>
let el = document.getElementById("username");
console.log(el.attributes);
</script>

<!--
Output:

NamedNodeMap {  
0: type="text"  
1: id="username"  
2: class="form-control"  
3: placeholder="name"  
}
-->
```

**hasAttribute**

دي من اسمها بتشوف اذا كان ال HTML element فعلا في ال attribute الفلاني ولا لا وطبعا بتاخد منك ال اسم ال attribute اللي بتدور عليه وبترجعلك true , false

**removeAttribute**

دي بتمسح ال attribute اللي بتحدده لكن خلي بالك هي بتمسحه خالص مش بتخلي ال value بتاعته فاضية 

**hasAttributes**

دي نفس القصة بردو هترجعلك true , false لكن مش بتاخد منك حاجة هي بت check بس هل في attributes ولا لا

### Create Element

**createElement( )**
بيعمل عنصر HTML جديد في الصفحة 
```js
let div = document.createElement("div")
```

**createTextNode( )**
بيعمل text node (نص عادي جوه عنصر)
```js
let text = document.createTextNode("Hello World");
```

**createComment( )**
بيعمل comment جوه الـ DOM
```js
let comment = document.createComment("This is a comment");
```

**appendChild( )**
بيضيف عنصر جوه عنصر تاني.

### Dom Events

ال events احنا بسنتخدمها عشان ننفذ حاجة معينة بناء علي ال event ده بيعمل اي و ممكن نستخدمها جوا ال html, js 
**onclick( )**
ده بيشتغل لما الuser يضغط كليك شمال على العنصر
```html
<button onclick="alert('Clicked!')">Click me</button>
```

**oncontextmenu( )**
ده بيشتغل لما تعمل كليك يمين واحينا او في الغالب يستخدم عشان ميخلكش تقدر تفتح ال menu
بتاعة ال browser اللي بيكون فيها ال inspect 
```html
<div oncontextmenu="alert('Right click detected')">
  Right click here
</div>
```

**onmouseenter( )**
بيشتغل أول ما الماوس يدخل جوه العنصر لكن الفرق بينه وبين `mouseover` إن mouseenter مش بيكرر ال event لو دخلت عناصر فرعية
```html
<div onmouseenter="console.log('Mouse entered')">
  Hover here
</div>
```

**onload( )**
بيشتغل لما ال page تعمل load

**onscroll( )**
بيشتغل لما تعمل Scroll.

**onresize( )**
بيشتغل لما حجم ال page يتغير

**onfocus( )**
بيشتغل لما العنصر ياخد فوكس زي input لما تدوس عليه

**onblur( )**
بيشتغل لما العنصر يتشال من عليه ال focus غالبًا بيتستخدم عشان تعمل validate لل inputs اللي ال user حطها في form معين

**preventDefault( )**

دي طريقة في ال event object بتمنع السلوك او الوظيفة الطبيعية لل element انها تشتغل 
مثلا لو عندك لينك في ال Page هيوديك علي جوجل دي ممكن تمنع القصة دي .

### Class List

**classList( )**

هي خاصية لكل عنصر في DOM وبتديك access لكل الـ classes اللي على العنصر ك DOMTokenList
```html
<div id="myDiv" class="box red"></div>
<script>
let el = document.getElementById("myDiv");
console.log(el.classList);  // DOMTokenList ["box", "red"]
</script>
```

**length( )**
ده بيجيب عدد ال classes اللي موجودة علي ال element

**contains( )**
بتشيك إذا كان العنصر عنده class معين ولا لأ وطبعا بترجع `true, false`
```html
<div id="myDiv" class="box red"></div>
<script>
console.log(el.classList.contains("red"));  // true
console.log(el.classList.contains("blue")); // false
</script>
```

**item(index)**
ترجع اسم الـ class في الـ index اللي انت محدده
```js
console.log(el.classList.item(0)); // "box"
console.log(el.classList.item(1)); // "red"
```

**add( )**

دي بتضيف class معين
**remove( )**
دي بتحذف class معين

**toggle( )**
دي بقي لو ال class اللي انت اديتهولها مش موجود هتضيفه ولو موجود هتمسحه
```js
el.classList.toggle("active");  // يضيف "active" لو مش موجود
el.classList.toggle("active");  // يمسح "active" لو موجود
```
ممكن تمرر `true/false` ك second argument لتحديد إذا عايز تضيف أو تمسح:
```js
el.classList.toggle("active", true);  // دايمًا يضيف
el.classList.toggle("active", false); // دايمًا يمسح
```

### Deal With Elements

**append( )**

دي بتضيف عنصر جوه العنصر الحالي لكن في الآخر يعني لو عندك عنصر فيه محتوى، وعايز تضيف حاجة آخره
```html
<ul id="list">
  <li>Item 1</li>
</ul>

<script>
// create new element
const li = document.createElement("li");
li.textContent = "Item 2";

// add it to the end of ul
document.getElementById("list").append(li);
</script>
<!--
Output:

<ul id="list">
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
-->
```

**prepend()**

دي عكس append بتضيف العنصر جوه العنصر لكن في الأول

**before( )**
دي بتحط ال element قبل element معين 

```html
<p id="second">Second paragraph</p>
<script>
const p = document.createElement("p");
p.textContent = "First paragraph";

document.getElementById("second").before(p);
</script>
<!--
Output:
<p>First paragraph</p>
<p id="second">Second paragraph</p>
-->
```

**after( )**
دي العكس بتحط ال element بعد ال element مباشرة

**remove( )**
دي ببساطة بتحذف ال element من الصفحة

### DOM Traversing

معناه انك تتنقل بين ال elements بتاع الصفحة بدل ما كل تفضل تجيب كل element بال Id بتاعه لا ده بيخليك تقدر تتنقل بين العناصر يمين شمال فوق تحت جاي معاك في حتة 

الفكرة بتاعته : تخيل يعم ان ال html دي شجرة 
```html
<div>
  <p>First</p>
  <p id="target">Second</p>
  <p>Third</p>
</div>
```
العنصر `Second` ليه: عنصر قبله و عنصر بعده و عنصر أب (parent) وال  DOM methods اللي هنذكرها دي بتخلينا نتحرك بينهم بسهولة

**nextSibling( )**

دي بتجيب العنصر أو النود اللي بعده مباشرة لكن خلي بالك هي كمان ممكن ترجع ال text node h اللي هي يعني زي المسافات و ال new lines

**previousSibling( )**

نفس الفكرة لكن دي العكس ال element اللي قبله وبرضو ممكن ترجع text node

**nextElementSibling( )**

دي بقي بتجيب  HTML Element اللي بعده مباشرة وتتجاهل ال text node ودي هي الي في الغالب بنستخدمها
```js
const el = document.getElementById("target");
console.log(el.nextElementSibling);

//Output:<p>Third</p>
```

**previousElementSibling( )**

دي العكس بتجيب العنصر اللي قبله مباشرة
**parentElement( )**

دي بتطلع لفوق في الشجرة وتجيب العنصر الأب اللي بيحتوي علي كل ال elements اللي انت بتتحرك بينها دي
```js
const el = document.getElementById("target");
console.log(el.parentElement);
/*
Output:

<div>
  <p>First</p>
  <p id="target">Second</p>
  <p>Third</p>
</div>
*/
```
### AddEventListener

هي method بتخليك تسمع event معين على element معين زي click  وبعدين تعمل action لما ال event ده يحصل زي انك هتنفذ function معينة اي حاجة بقي

صيغته بتكون كالتالي : 
```js
element.addEventListener(event, callback, options);
```
ال event  نوع الحدث زي `"click"` أو `"mouseenter"`
ال callback هي  function هتتنفذ لما ال event يحصل
ال options  دي بتكون object اختياري، فيه حاجات زي `{ once: true }`

```html
<button id="btn">Click me</button>

<script>
const btn = document.getElementById("btn");

btn.addEventListener("click", () => {
  alert("Button clicked!");
});
</script>
```

## Bom

ال **BOM** اختصار لـ Browser Object Model
ببساطة هو كل الحاجات اللي الbrowser بيوفرها لك في JavaScript علشان تتحكم في ال browser نفسه مش الصفحة بس اشهر object في ال bom هو `window` وده بالبلدي كدا هو الاب لكل حاجة تقريبا يعني هو بيحتوي علي ال document , console وكل ال objects دي لكن احنا لما بنيجي نكتب اي object منهم بنستسهل ونكتب اسم ال object علي طول 
```js
console.log("good")
//same: 
window.console.log("good")
```

تعالي نشوف ايه اشهر ال methods اللي تابعة ل window object في ال Bom

**alert( )**

بتظهر رسالة للuser بس ال user ملوش غير إنه يضغط OK لكن هي مش بتستخدم كتير لانها بتوقف الكود موقتا لحد ما اليوزر يضغط ok 
**confirm( )**

دي ببساطة بتسال ال user سؤال وبيكون عنده اجابتين `ok, cancel` وطبعا بيرجع `true, false` uعشان تقدر تهندل اي اللي هيحصل في اي حالة
**Prompt( )**

دي بنستخدمها لو عاوزين ناخد Input من ال user لو اديته value وضغطت ok هيرجعلك ال value انما لو ضغطت cancel هيرجعلك null
```js
prompt("What is your name?")
```

**ملحوظة**: التلاتة methods دول `blocking` يعني ال js code بيقف لحد لما الوزر يجاوب
**setTimeout( )**

دي بتنفذ كود او function بعد وقت معين انت بتحدده
```js
setTimeout(function() {

}, delay)
//delay: X milliseconds

//ex:
console.log("Start")

setTimeout(function () {
  console.log("Hello after 2 seconds")
}, 2000)

console.log("End")
```
هنا هيطبع في الكونسول `Start` وبعد ثانيتين هيطبع `Hello after 2 seconds` ثم ال `End`

في حاجة كمان في ال setTimeout لو انت مديها function بتاخد arguments ال arguments دي بتتحط بعد قيمة ال delay وده الشكل العام بتاعها
```js
setTimeout(function, delay, arg1, arg2, arg3)
```

```js
function sayhello(user) {
  console.log(`Hello ${user}`)
}
setTimeout(sayhello, 2000, "belal")
```

**ملحوظة:** لو انت حطيت ال setTimeout في Variable هيرجعلك ال id بتاع ال timer طب هستفاد ايه من ال id اللي هيرجع ده هتستخدمه لو عاوز توقف ال setTimeout عن طريق function اسمها  `( )clearTimeout`
ودي بقي هي بيكون قيمتها بتكون ال id 

**clearTimeout( )**

دي بتلغي ال setTimeout باستخدام ال id اللي ال setTimeout بترجعه 
```js
let timer = setTimeout(function () {
  console.log("good")
}, 5000)

clearTimeout(timer)
```
الكود ده مش هيتنفذ اصلا لاننا ببساطة وقفنال ال function بتاعة ال setTimeout عن طريق ال id اللي setTimeout رجعه واللي متخزن في ال timer
وده مثال عملي: 
```js
let message = setTimeout(function () {
  alert("Session Expired")
}, 10000)

// cancel after 5 seconds
setTimeout(function () {
  clearTimeout(message)
}, 5000)
```
الكود ده المفروض انه هيطلع alert بعد 10 ثواني فانا ضيفت clearTimeout عند الثانية ال 5 فمش هيظهر alert خلاص

**setInterval( )**

دي شبه `setTimeout` في كل شي  لكن الفرق الأساسي ان ال setTimeout بتنفذ الكود مرة واحدة بس بعد الوقت
اما ال `setInterval` بتنفذ الكود كل فترة زمنية بشكل متكرر وده الشكل العام بتاعها مع مثال
```js
setInterval(function, delay)

//ex:

setInterval(function () {
  console.log("Hello")
}, 2000)
```
ده هيفضل يطبع كل ثانيتين كلمة `Hello` طب ازاي بنوقفه بنوقفه بحاجة اسمها `clearInterval` وبتاخد بردو ال id اللي بترجعه ال `setInterval` اه بردو بترجع id شبه ال setTimeout 


**clearInterval( )**

بنستخدمها عشان نوقف ال setInterval بعد وقت معين باستخدام ال id اللي بيرجعه ال setInterval

مثال لاستخدام ال setInterval, clearInterval مع بعض
```js
let num = 5;

function countdown(){
    num -= 1;
    console.log(num);
    
    if (num === 0){
        console.log("Boom....")
        clearInterval(count)
    }
}
let count = setInterval(countdown, 1000);
```
ده هفضل يعد من 5 الي 1 ولما يوصل لل 0 هيقف طبعا عشان في clearInterval وهيطبع `Boom`

### Location

ده ال object  المسؤل او اللي بيمثل ال URL الحالي لل page ده بيخليك تقدر تقرا منه معلومات عن ال page او تغيرها ال page اللي انت فيها او حتي تعدل في ال url نفسه و اه هو زي هو بردو object من ضمن ال objects الخاصة بال window
```js
console.log(location)
//same:
console.log(window.location)
```
ده هيوريك كل حاجة تخص اللينك بتاع ال page اللي انت فيها

**location.href( )**

ده اللينك  الكامل لل page اللي انت فيها وتقدر منه تغير لينك الصفحة وخلي بالك ان بيحفظ ال entry point بتاعتك في ال history يعني تقدر ترجع لل entry point تاني عشان هنشوف حاجت مش بتحفظ ال entry point 
```js
location.href = "https://google.com"
```
ده هيغير لينك ال page ل google لو هتستخدمه في redirect

**location.host( )**

ده هيرجعلك ال domain + port ولو مفيش port متحدد هيرجعلك ال domain بس

**location.protocol( )**

ده هيرجعلك نوع ال protocol سواء بقي http او https

**location.assign( )**

دي بتعمل redirect ل page جديدة لكن ال page الحالية بتتسجل في history يعني تقدر تعمل back عادي 

**location.replace( )**

ده برضو بيعمل redirect لكن الفرق انه يا معلم مش هيحفظها في الhistory يعني مش هتقدر ترجع لل entry point بال back

**location.reload( )**

ده بيعمل reload لل page مفيهوش حاجة 
```js
location.reload(true)
```
ده بيخليك تعمل reload لل page لكن من ال server لكن للامانة يعني معظم كل ال browsers دلوقتي بقت تتجاهلها


### Localstorage

هي جزء من الـ Web Storage API وبتخليك تخزن data في الbrowser بشكل مستمر حتى لو قفلت ال page او ال browser البيانات بتكون مخزنة على شكل Key و Value وبتكون على شكل strings

**setItem(key, value )**
دي بنستخدمها عشان نخزن value جديدة في ال Localstorage ولازم ال value تكون string ولو مش string هتتحول auto ل string
```js
localStorage.setItem("username", "belal");
// same
window.localStorage.setItem("username", "belal");
```

**getItem(key)**

دي بتجيب ال value المتخزنة لل key أللي انت محدده او طالبه ولو ال Key مش موجود هترجع `null`
```js
let user = localStorage.getItem("username");
console.log(user); // belal
```

**removeItem(key)**

بتحذف العنصر اللي عنده ال key اللي انت طالبه 
```js
localStorage.removeItem("username");
```

**clear( )**
دي بتحذف كل ال data اللي في ال Localstorage
```js
localStorage.clear();
```

**key(index)**

دي بترجع اسم ال Key اللي عنده `index` معين في ال Localstorage وطبعا ال index بيبدا من 0
```js
localStorage.setItem("name", "belal");
localStorage.setItem("age", "22");

console.log(localStorage.key(0)); // name
console.log(localStorage.key(1)); // age
```

### SessionStorage

شبه ال Localstorage برضو بتخليك تخزن data في الbrowser علي شكل key , value وبردو بتكون string لكن الفرق الوحيد ان ال data دي بتروح اول لما ال session تخلص او لما تقفي ال browser

**setItem(key, value )**
دي بنستخدمها عشان نخزن value جديدة في ال sessionstorage ولازم ال value تكون string ولو مش string هتتحول auto ل string
```js
sessionstorage.setItem("username", "belal");
// same
window.sessionstorage.setItem("username", "belal");
```

**getItem(key)**

دي بتجيب ال value المتخزنة لل key أللي انت محدده او طالبه ولو ال Key مش موجود هترجع `null`
```js
let user = sessionstorage.getItem("username");
console.log(user); // belal
```

**removeItem(key)**

بتحذف العنصر اللي عنده ال key اللي انت طالبه 
```js
sessionstorage.removeItem("username");
```

**clear( )**
دي بتحذف كل ال data اللي في ال sessionstorage
```js
sessionstorage.clear();
```

**key(index)**

دي بترجع اسم ال Key اللي عنده `index` معين في ال sessionstorage وطبعا ال index بيبدا من 0
```js
sessionstorage.setItem("name", "belal");
sessionstorage.setItem("age", "22");

console.log(sessionstorage.key(0)); // name
console.log(sessionstorage.key(1)); // age
```

## Destructuring

### Destructuring Arrays
دي طريقة بنستخدمها عشان لو عندنا array بدل ما تجيب العناصر منه واحد واحد لا الطريقة دي بتخليك تعمل extract للعناصر اللي في ال array وتطهم في variables بسهولة
```js
let arr = ["belal", 22, "Egypt"];

let [name, age, country] = arr;

console.log(name);    // belal
console.log(age);     // 22
console.log(country); // Egypt
```
هنا كل عنصر في ال array اتحط في variable حسب ترتيبه

**skip element**
بردو بتخليك عندك حرية انك تعمل skip لعناصر معينة 
```js
let arr = ["belal", 22, "Egypt"];

let [name, , country] = arr;

console.log(name);    // belal
console.log(country); // Egypt
```
هنا احنا عملنا skip لل age

**Default Values**

بردو لو عندك element وملوش قيمة في ال array ممكن تعمله default value بدون اي مشكلة 
```js
let arr = ["belal"];

let [name, age = 18] = arr;

console.log(age); // 18
```
عملنا default value لل age 

**Swap Values**

الطريقة دي بتوفرهالك عملية ال Destructuring عشان تقدر تعمل swap بين قيمة variable , قيمة variable تاني
بص تعالي نشوف الطريقة العادية لل swap وبعدين نشوف الطريقة بتاعة Destructuring
```js
let book = "Video";
let video = "Book";
```
عشان تعمل swap وترجع لكل variable قيمته المنطقية بالطريقة العادية محتاج variable تالت تخزن فيه قيمة variable منهم 
```js
let book = "Video";
let video = "Book";
// save book value in stach
let stach = book; //Video
// change book value
book = video //Book
// change video value
video = stach // Video
```
دي الطريقة العادية طويلة اوي وبنحتاج variable تالت وقصة وليلة 

دي بقي طريقة ال Destructuring 
```js
let book = "Video";
let video = "Book";

[book, video] = [video, book]
```
بس كدا احنا عملنا swap بين قيمة الاتنين variable بكل سهولة

**Nested Arrays**

دي بتسمحلك تعمل extract ل array جوا array 
```js
let arr = ["belal", [22, "Egypt"]];

let [name, [age, country]] = arr;

console.log(age); // 22
```

### Destructuring Objects

زي الـ arrays، بس الترتيب هنا بيعتمد على اسم الـ key يعني بتسحب القيم من الـ object وتحطها في variables بسهولة باستخدام اسم ال key بس
```js
let user = {
    name: "belal",
    age: 22,
    country: "Egypt"
};

let {name, age, country} = user;

console.log(name);    // belal
console.log(age);     // 22
```
خلي بالك في ال Destructuring objects لازم اسم المتغير = اسم الـ key ده ال main different بين دي وبين ال  array

**Alias**

دي ميرة في ال Destructuring objects وهي انها بتسمحلك تغير اسم ال variable الي بتنادي بيها علي اسم ال key
```js
let user = {
    name: "belal",
    age: 22
};

let {name: username, age: userAge} = user;

console.log(username); // belal
console.log(userAge);  // 22
```

**Default Values**
نفس الكلام اللي كان في ال array بيسمحلك تحط default value 
```js
let user = {
    name: "belal"
};

let {name, age = 18} = user;

console.log(age); // 18
```

**Nested Object**
بتسمحلك تعمل extract ل object جواه object 
```js
let user = {
    name: "belal",
    info: {
        age: 22,
        country: "Egypt"
    }
};

let {
    name,
    info: {age, country}
} = user;

console.log(age); // 22
```

### Destructuring Function Parameters

دي طريقة عشان بدل ما تاخد object أو array كامل جوه function وتطلع القيم جوه، تقدر تفك القيم مباشرة في parameters بحيث الكود يبقى أقصر وأسهل للقراءة
```js
let user = {
    name: "belal",
    age: 22
};

function printUser({name, age}) {
    console.log(`Name: ${name}, Age: ${age}`);
}

let user = {name: "belal", age: 22};
printUser(user); // Name: belal, Age: 22
```
هنا احنا عملنا extract لل obj ك variable في ال function parameter 

## Set Data Types

### Set( )

ال set هو عبارة عن data structure بيخزن unique values  فقط مفيش تكرار وطبعا ده بيخزن جميع انواع ال data لان في حاجة اسمها WeakSet دي مش بتخزن غير objects بس  
```js
let mySet = new Set([1, 2, 3, 3]);
console.log(mySet); // Set(3) {1, 2, 3}
```

طبعا ليه properties و methods هنتكلم عليها دلوقتي 

**size**

ده عبارة عن property خاصة بال set وهي من اسمها بتجيبلك عدد ال elements اللي جوا ال set
```js
let mySet = new Set([1, 2, 3]);

console.log(mySet.size); // 3
```

**add( )**

دي عبارة عن Method بتضيف element جديد وخلي بالك لو العنصر ده كان موجود فهو مش هيتضاف (unique values only)
```js
let mySet = new Set();

mySet.add(1);
mySet.add(2);
mySet.add(2);

console.log(mySet); // {1, 2}
```

هنا طبعال 2 التانية منطبعتش عشان هرجع اقول تاني ال set بتسيب ال unique value only'

**delete( )**
دي عبارة عن Method بتحذف عنصر معين بترجع `true` لو اتحذف، `false` لو مش موجود
```js
let mySet = new Set([1, 2, 3]);

mySet.delete(2);

console.log(mySet); // {1, 3}
```

**has( )**

دي عبارة عن Method بتتأكد هل العنصر موجود ولا لأ بترجع `true` أو `false`  برضو هي شبه **()includes**  لكن خاصة ب ال set
```js
let mySet = new Set([1, 2, 3]);

console.log(mySet.has(2)); // true
console.log(mySet.has(5)); // false
```

**clear( )**
دي عبارة عن Method بتحذف كل عناصر ال set
```js
let mySet = new Set([1, 2, 3]);

mySet.clear();

console.log(mySet); // {}
```

### WeakSet( )

دي بردو عبارة عن data structure لكن دي بتخزن بس ال objects مش شبه ال set اللي بتخزن كل انواع ال data
```js
let weakSet = new WeakSet();

let obj = {name: "belal"};
weakSet.add(obj);

// weakSet.add(1); ❌ error
```
ليه error لانك اديته data هو مش بيقدر يخزنها هو بس مش بيخزن غير ال objects

### Garbage Collector (GC)

ده نظام جوه JavaScript بيشيل من الذاكرة أي حاجة **ملهاش reference** طب اي علاقته بال set , WeakSet 

`ال set` بيفضل ماسك الحاجة حتي لو ملهاش reference هيفضل ماسكها وخلاص وده بعض الاحيان غلط لانه ممكن يسبب data leaks لان انا المفروض خلاص الحاجة دي مش عاوزها او ملهاش صاحب فانت ليه ماسكها ومحتفظ بيها في ال memory 

`ال WeakSet` بقي مختلف تماما لان لو الحاجة ملهاش reference قوية هيسمح لل Garbage Collector انه يمسحها او يعني هو مش هيسمح هو اصلا Garbage Collector هيمسحها تلقائيا وده بيكون مهم جدا عشان مش هيعمل data leaks وهنا ال weakset هيكون مناسب جدا للحاجت الموقتة زي ال caching, tracking obj 

وده مثال لشرح المفهوم من منظور عملي لكن مرة باستخدام ال set ومرة weakset

تخيل عندنا مثلا object معين في الموقع عاوز اعرف هل في user زاره ولا لا 

**باستخدام ال Set**
```js
// Using Set

let visited = new Set();

function track(user) {
    visited.add(user);
}

// Create object

let user1 = {name: "belal"};

track(user1);

console.log(visited.has(user1)); // true

// Delete reference

user1 = null;

```

هنا بقي المشكلة المفروض انا دلوقتي لما خليت قيمة ال user1 بتساوي null المفروض انا بقوله انا خلاص مش عاوزه مش محتاجه الطبيعي جدا انه يتشال من ال memory بس عشان احنا مستخدمين set هيفضل محتفظ بيه في ال memory ومش هيمسحه 

**باستخدام ال WeakSet**
```js
// Using WeakSet

let visited = new WeakSet();

function track(user) {
    visited.add(user);
}

let user1 = {name: "belal"};

track(user1);

console.log(visited.has(user1)); // true

user1 = null;

```
نفس المثال اهو لكن ايه اللي هيحصل هنا انا يا معلم لما قولت ان user1 بيساوي null يعني انا مش عاوزه 
ايه اللي حصل ال `GC` مسحه تلقائي خلاص لان ده خلاص ملهوش reference 

*وبكدا في الحالة دي او الحالات المشابهة المفروض استخدم ال weakset لانه هو الصح 

### Map( )

هو عبارة عن data structure بيخزن الداتا علي شكل key, value شبه ال object لكن ال Map اقوي ومرن اكتر من ال object 
```js
let myMap = new Map([
    ["name", "belal"],
    ["age", 22]
]);
```

**size**
دي عبارة عن Property بتجيب عدد العناصر
```js
console.log(myMap.size); 
```

اهم ال Methods 
**set(key, value)**

دي بتضيف element جديد
```js
myMap.set("name", "belal");
myMap.set(1, "number");
```

**get(key)**

دي بتجيب ال value الخاصة با key اللي انت مديهولها
```js
console.log(myMap.get("name")); // belal
```

**has(key)**

دي بسال هل ال key ده موجود وبترجع `true`, `false`
```js
console.log(myMap.has("name")); // true
```

**delete(key)**

دي بتحذف element
```js
myMap.delete("name");
```

**clear( )**
دي بتحذف كل ال elements

**مميزات ال Map عن object**

- تقدر تعمل key باي data type انت عاوزه عاوز تعمله string, number, obj , function دي حاجة مستحيلة في ال Obj
- ممكن تعمل loop في ال Map بسهولة اكتر من ال object

باستخدام `for...of`
```js
for (let [key, value] of myMap) {
    console.log(key, value);
}
```

باستخدام `forEach`
```js
myMap.forEach((value, key) => {
    console.log(key, value);
});
```

- خلي بالك انك في ال object مفيش طريقة او property مباشرة انك تجيب ال size بتاع ال object لكن في ال Map لا عندك property اسمها size بتجيب ال size بتاع ال Map
- حاجة كمان ان ال Map هي افضل واسرع من ال object

### WeakMap( )

بص هي نفس فكرة ال set , WeakSet بالظبط  ال Map بتقبل اي  data type زي ما قولنا قبل كدا لكن ال WeakMap مش بتقبل غير ال objects  بس ونفس بردو المميزات ان ال map هتفضل ماسكة ال value حتي لو ملهاش reference لكن ال WeakMap او لما ال data ملهاش reference ال `GC` هيمسحها تلقائيا من ال Memory  

### Array.from( )

دي method بتحول أي حاجة شبه الـ array (أو iterable) إلى Array حقيقي وده الشكل العام ليها 
احنا ببساطة بنستخدمها لو عاوزين نحول اي شي ل array سواء كانت الحاجة دي string, set, map, NodeList


```js
Array.from(iterable, mapFunction, thisArg)
```

ده مثال هنحول string كامل علي بعضه ل array نقدر ننفذ علي ال elements بتاعته اي حاجة 
```js
let str = "belal";

let arr = Array.from(str);

console.log(arr); // ["b", "e", "l", "a", "l"]
```

انت ممكن تستخدمها مع اي ,حاجة لكن زي ال set, map ,function
ده مثال في استخدامها مع ال function 
```js
let numbers = [1, 2, 3];

let result = Array.from(numbers, x => x * 2);

console.log(result); // [2, 4, 6]
```
ايه اللي حصل عندنا array راح ممررها ل Array.from عشان يفككها ل elements اقدر انفذ عليها operations 
عدي العناصر دي علي arrow function بتاخد كل عنصر من ال array اللي طلعت وتضربه في `2`

### Array.copyWithin( )

دي method بتنسخ جزء من ال array وتنسخه في مكان اخر داخل نفس ال array لكن بدون ما تاثر علي حجم ال array وده الشكل العام ليها وخلي بالك كمان انها `mutable` يعني مش بيعمل array جديدة في الناتج لا بيعدل علي ال array الاصلية
```js
array.copyWithin(target, start, end)
```
- ال  `target`  هو المكان اللي هتحط في النسخة داخل ال array 
- ال  `start`  ده المكان اللي هتبد تنسخ من عنده وهو optional يعني لو محددتوش هيبدأ من `index 0 `
- ال  `end` ده المكان الي هينتهي عنده النسخ داخل ال array وخلي بالك في ملحوظة قديمة
ان ال end not included فخد بالك وبردو هي optional لان لو مححدتش هيكمل نسخ للنهاية لحد (اخر index)
- وفي حاجة كمان ان لو ال start او ال end بدأو ب `-` سالب كدا هيشتغل من اليمين للشمال من ورا لقدام 
يعني اخر index هو هيكون البداية 

```js
let arr = [1, 2, 3, 4, 5];

arr.copyWithin(0, 3);

console.log(arr); // [4, 5, 3, 4, 5]
```
المثال ده هيعمل ايه زي ما انت شايف ال target هنا 0 و ال start 3 يعني ابدا نسخ من بداية ال index 3 لحد اخر index عندك وانسخهم في ال Index 0 هي ممكن تكون بتلغبط لكنها تافهة والله

مثال باستخدام negative index
```js
let arr = [1, 2, 3, 4, 5];

arr.copyWithin(-2, 0);

console.log(arr); // [1, 2, 3, 1, 2]
```
هنا عندك التارجت -2 يعني هيبدا من اخر عنصرين يعني ممكن تقول ال index 3 هو التارجت وينسخ الجزء من ال index 0 لاخر Index

### Array.some( )

هي method وظيفتها تلف علي ال array تشوف هل في عنصر واحد علي الاقل بيحقق شرط معين ولا لا 
وطبعا بترجع true, false وده الشكل العام 
```js
array.some(callback(element, index, array), thisArg)
```

مثال: 
```js
let numbers = [1, 2, 3, 4];

let result = numbers.some(num => num > 3);

console.log(result); // true
```
هنا هو لف علي كل الارقام اللي في ال array وحاول يشوف هل في حاجة اكبر 3 وده الشرط المطلوب ولقي ال 4 اذن `true`

*ملحوظة مهمة خلي بالك ان ال some بتقف او لما بتلاقي الشرط اتحقق يعني لو لقت عنصر حققق الشرط هتقف وتطلع `true` يعني هي مش بتكمل للاخر

### Array.every( )

هي method وظيفتها تلف علي ال array تشوف هل كل العناصر اللي جواه بتحقق شرط معين لو كلهم بحققو الشرط هترجع `true` لو حاجة فيهم مش بتحقق هيرجع `false` وده الشكل العام 
```js
array.every(callback(element, index, array), thisArg)
```

مثال:
```js
let numbers = [2, 4, 6];

let result = numbers.every(num => num % 2 === 0);

console.log(result); // true
```
رجع true ليه ؟ عشان كل الارقام بتحقق الشرط (even)

### Spread ...

ده عبارة عن operator بيعمل expand للعناصر بيحول اي حاجة لمجموعة عناصر منفصلة 

امثلة :

**Array concatenation**

```js
let arr1 = [1, 2];
let arr2 = [3, 4];

let result = [...arr1, ...arr2];

console.log(result); // [1, 2, 3, 4]
```

**Array (copy)**

```js
let arr = [1, 2, 3];

let copy = [...arr];

console.log(copy); // [1, 2, 3]
```

**Add elements**

```js
let arr = [2, 3];

let newArr = [1, ...arr, 4];

console.log(newArr); // [1, 2, 3, 4]
```

**Object (copy)**

```js
let user = {name: "belal"};
let copy = {...user};

console.log(copy) // { name: 'belal' }
```

ممكن نستخدمها مع كل حاجة تقريبا وليها امثلة واستخدامات كتيرة جدا 

## Regular Expression(RegEx)

ال `regex` لو انت متعرفوش ده عبارة عن نمط او pattern بنستخدمه عشان نبحث او نحدد او نعدل علي strings معينة او مطابقة لل pattern اللي انا حاطتها دي .
### Flags

**ignore case ( i )**

ده لما بتستخدمه انت بتقوله كدا هات الكلمة او الحروف المطابقة لل pattern الل نا حاطه سواء كانت `capital or small` 
```js
let str = "Belal";

console.log(/belal/i.test(str)); // true
```
الكلمة اللي انت قايله يدور عليها هي `belal` يعني small بس استخدمت `i` فكدا هيجبها سواء كدا او كدا 

**global ( g )**

ده معناه انه هيجيب كل المطابق لل pattern مش اول كلمة تقابله بس وهيحطها في array بالترتيب اللي لقاهم بيه لان مثلا ال `i` بيرجعلك بس اول حاجة مطابقة لل pattern
```js
let str = "hi hi hi";

console.log(str.match(/hi/g)); // ["hi", "hi", "hi"]
```

**multiline ( m )**

بالبلدي كدا يعني هيمشي علي سطر سطر ويطبق ال pattern اللي انا مديهوله
```js
let str = `start
end`;

console.log(/^end/m.test(str)); // true
```

### Ranges ( [ - ] )

ده معاناه اختار اللي موجود في ال `range` ده فقط طب لو حطيت ال range ده جوا `()` ده معناه group وده بنستخدمه كتير لو في pattern معقد او مركب

**char range [a-z]**
```js
let regex = /[a-z]/;
```
ده معناه انه هيدور علي اي حروف `small` بس 
**number range  [0-9]**

```js
let regex = /[0-9]/;
```
يعني اي رقم بين `0, 9` 

**combine ranges**

يعني اي حرف واي رقم
```js
let regex = /[a-zA-Z0-9]/;
```

**Negation ( ^ )**

دي بالبلدي كدا `ماعدا` كذا بمعني هات اللي مثلا اي حاجة ما عدا الحروف ال small 

```js
let regex = /[^a-z]/;
```

**OR operator ( | )**

```js
let regex = /dog|cat/;
```
معناه هات ال dog او  cat 

### Character Classes

دي بتكون عبارة عن  shortcuts جاهزة بدل ما تكتب ranges زي `[0-9]` أو `[a-z]` لا ال shortcuts دي بتسهل عليك الدنيا وبتخلي الموضوع او كتابة ال pattern اسهل اوضح 


**Any Character ( . )**

النقطة `.`معناها اي حاجة حتي ال space ما عدا ال `newline`
```js
let regex = /c.t/;
```
ده معناه انه لو لقي cat هيقبلها عادي لقي cut هيقبلها عادي لقي cot تمام
طب لو لقي `ca\nt` لا مش هيقبلها لا `n\`معناها newline و ال `.` مش بتقبل ال newline 

**\d  digits**
أي رقم من 0 لـ 9
```js
let regex = /\d/;
console.log("hello123".match(/\d/g)); // ["1","2","3"]
```

**\D  NOT digits**

كل حاجة ما عدا الارقام
```js
let regex = /\D/g;

console.log("a1b2".match(regex)); // ["a","b"]
```

**/w word character**

ده هيجيب كل دول 
- من a-z
- من A-Z
- من 0-9
- ال underscore `_`
```js
let regex = /\w/g;

console.log("a1_!".match(regex)); // ["a","1","_"]
```
مجابش  `!` عشان هي طبعا مش included في ال `w/` بتجيبها  

**\W  NOT word character**

اي حاجة غير دول 
- من a-z
- من A-Z
- من 0-9
- ال underscore `_`
```js
let regex = /\W/g;

console.log("a1_!".match(regex)); // ["!"]
```

**\s  whitespace**

اي whitespace زي `tap, space, newline` 
```js
let regex = /\s/g;

console.log("a b\tc".match(regex)); // [" ", "\t"]
```

**\S  NOT whitespace**
أي حاجة مش space
```js
let regex = /\S/g;

console.log("a b".match(regex)); // ["a","b"]
```

**/b Word Boundary**

دي بالمعني الحرفي معناها حدود الكلمة يعني هي بتشوف هل الكلمة بتبدا او بتنتهي بالكلمة دي 
```js
let text = "hello world";

console.log(/\bworld/.test(text)); // true
```
ليه هتكون true لان فعلا في كلمة في الجملة اللي انت باعتها بتبدا بكلمة world عشان انت مستخدم b/ اللي بتست علي word boundary

**/B NOT Word Boundary**

دي العكس يعني مش عند بداية او نهاية الكلمة بمعني لو كلمة في نص الكلام هيجبها لانها عكس `b/` 
```js
let text = "category";

console.log(/\Bcat/.test(text)); // true
```
ليه true عشان انا مستخدم `B/`  وبقوله دور علي cat فلاقها في وسط كلمة تانية خلاص اذن true

**test( )**

دي method من ال RegEx Object بتشوف هل ال pattern بيتحقق او يعني في تطابق
ولا لا وبترجع `true, false` 
```js
let regex = /hello/;

console.log(regex.test("hello world")); // true
```

ملاحظة لازم تخلي بالك منها لو استخدمت `g` flag ممكن يسبب behavior غريب
```js
let regex = /a/g;

console.log(regex.test("a")); // true
console.log(regex.test("a")); // false 
```
ليه؟

لان `g` بيخلي regex يحتفظ بالمكان `lastindex` طبعا منتش فاهم حاجة تعالي اقولك

لما عملت test اول مرة راح مرجعلك true ليه لان بدا عادي جدا من ال` Index 0 `فلقي ال a فراح مرجع `true `وحرك نفسه ل `index 1 `فلما انت عملت test تاني بعدها رجع `false` عشان هو بدا من `اخر Index` وقف عنده اللي هو Index 1 واللي هو مش موجود فراح مرجع `false`

### Quantifiers

دي ببساطة بتحدد كام مرة ال element هيتكرر 

**+ one or more**

ده بيقول انه لازم يحصل مرة واحدة على الأقل أو أكتر
```js
let regex = /a+/;

console.log("a".match(regex));     // ["a"]
console.log("aaa".match(regex));   // ["aaa"]
```

لو مفيش حروف
```js
console.log("b".match(/a+/)); // null
```


`* zero or more` 

ممكن متحصلش او تحصل مرة او اكتر 
```js
console.log("a".match(/a*/));   // ["a"]
console.log("".match(/a*/));    // [""]  
```
هنا هو رجع ال `a` عشان هي valid ورجعها مرة فاضية عشان `*` بترجع zero او لا فبنسباله بردو valid

**?  zero or one**
ده مرة واحدة او مفيش 
```js
console.log("a".match(/a?/)); // ["a"]
console.log("".match(/a?/));  // [""]
```
ده بردو valid لان بردو `?`  بتجبللك فهو لقاها مرة ولما ملقهاش بردو بالنسباله valid


**number of n{x}**

يعني انا بقوله لازم يكون اتكرر عدد معين من المرات لا اكتر ولا اقل 
```js
let regex = /a{3}/;
console.log(regex.test("aaa"))   // true
console.log(regex.test("aa"))    // false
console.log(regex.test("aaaa"))  // true 
```
ليه الاخيرة true يعم دي 4 مرات هي اه 4 لكن جواه `3a` فكدا تكون match مع اللي انا عاوزه

**range n{x, y}**

دي معناها range من x الي y من المرات يعني زي اقولك بالبلدي مثلا من 2 ال 4 مرات 
```js
let regex = /a{2,4}/;
console.log(regex.test("aa"))     // true
console.log(regex.test("aaa"))    // true
console.log(regex.test("aaaa"))   // true
console.log(regex.test("a"))      // false
console.log(regex.test("aaaaa"))  // true 
```
الاخيرة true ليه منتا خلاص فهمت بقي هما اه 5 لكن جواهم 4a فخلاص match

**at least {x, }**

يعني علي الاقل كذا مرة أو يعني مرة او اكثر
```js
let regex = /a{2,}/;
console.log(regex.test("aa"))     // true
console.log(regex.test("aaa"))    // true
console.log(regex.test("aaaaaa")) // true
console.log(regex.test("a"))      // false
```

**start with something ^**

بيدور علي اي حاجة بتبدا الحاجة الي انت مديهاله
```js
let regex = /^a/;
console.log(regex.test("apple"))   // true
console.log(regex.test("banana"))  // false
```
هنا بقوله هل في حاجة من دول بتدا بحرف ال `a` 

**end with something $**

بيدور علي اي حاجة بتنتهي بالحاجة اللي انت مديهاله 
```js
let regex = /a$/;
console.log(regex.test("coda"))   // true
console.log(regex.test("apple"))  // false
```
هنا بيشوف اي حاجة بتنتهي بحرف ال `a`

**Positive Lookahead ?=**

دي معناها ان لازم يكون في pttern معين بعد الحاجة اللي بدور عليها بس من غير ما يدخل في ال match
بالبلدي بقوله هات حاجة بشرط يكون بعدها حاجة معين
```js
let regex = /a(?=b)/;
console.log(regex.test("ab"))   // true
console.log(regex.test("ac"))   // false
```
هنا بقوله هات `a` بس بشرط يكون بعدها `b`

**Negative Lookahead ?!**

دي معناها هات حاجة بشرط ميكونش بعدها pattern معين 
```js
let regex = /a(?!b)/;
console.log(regex.test("ac"))   // true
console.log(regex.test("ab"))   // false
```

#### replace, replaceAll with  regular expression

**replace( )**

كانت بدور علي اول match في النص وتبدله بالحاجة اللي انت عاوزها

```js
let text = "I love cats and cats";

let result = text.replace("cats", "dogs");

console.log(result); // I love dogs and cats
```

بس لما بنستخدمها في ال regex هتكون fixable اكتر  
```js
let text = "I love cats and cats";

let result = text.replace(/cats/, "dogs");

console.log(result); // I love dogs and cats
```

طب لو عاوزين نغير كله مش اول match بس هنستخد flag ال `g`  
```js
let result = text.replace(/cats/g, "dogs"); // I love dogs and dogs
```

**replaceAll( )**

نفس الكلام لكن كانت بتبدل كل ال matches مرة واحدة مباشرة بدون flag ال `g`
```js
let text = "I love cats and cats";

let result = text.replaceAll("cats", "dogs");

console.log(result); // I love dogs and dogs
```

مع ال regex 
```js
let result = text.replaceAll(/cats/g, "dogs");
```
لازم لو هنستخدمها مع ال regex نحط ال `g` انما وضعها الطبيعي من غير regex مش هنحط ال flag

## OOP

### Constructor Function

**Old Syntax**


هي function بتستخدمها علشان تعمل objects كتير بنفس الشكل (template) يعني بدل ما كنت بتكتب objects يدوي ولو عاوز تعدل علي حاجة في كل واحد لازم تعدل لكل واحد لوحده
```js
let user1 = {
  name: "Belal",
  age: 23
};

let user2 = {
  name: "Ahmed",
  age: 25
};
```

هنا بقي ال constructor function حل المشكلة دي بالشكل اللي انت شايفه ده
```js
function User(name, age) {
  this.name = name;
  this.age = age;
}
let user1 = new User("Belal", 23);
let user2 = new User("Ahmed", 25);

console.log(user1);
console.log(user2);
```

- خلي بالك لازم اسم ال constructor يبد ب capital
- ال `this` هنا بتمثل ال object الجديد 
- بنستخدم new خلي بالك بردو

لكن ال syntax ده بيعمل مشكلة صغيرة كدا وهي ان كل object بياخد نسخة من ال function فبيكون فيه waste في ال memory ف بنضطر نستخدم حاجة اسمها prototype عشان نخلي كل
ال objects تشترك في نفس ال function 
```js
function Product(title, price) {
  this.title = title;
  this.price = price;
}

Product.prototype.show = function () {
  console.log(this.title + " - " + this.price);
};

let p1 = new Product("Phone", 5000);
let p2 = new Product("Laptop", 15000);

p1.show();
p2.show();
```


**New Syntax**
دي بقي ال syntax  الجديدة لل constructor function 
```js
class User {
  constructor(name, role) {
    this.name = name;
    this.role = role;
  }

  showRole() {
    console.log(this.name + " is " + this.role);
  }
}

let user1 = new User("Belal", "Admin");

user1.showRole();
```
هو نفس الشكل القديم لكن ده شكل ال syntax افضل هنا ال prototype بيحصل automatic ولازم نستخدم ال `new` 

### Properties And Methods

ال `Properties` دي بتكون عبارة عن خصائص او data زي كدا
```js
this.name
this.age
```

ال `Methods` دي بتكون عبارة عن functions بتنفذ حاجة معينة 

```js
class User {
  constructor(name, age) {
    this.name = name; // property
    this.age = age;   // property
  }

  sayHello() {        // method
    console.log("Hello " + this.name);
  }
}
```

خلي بالك عشان نقدر نستخدم ال property في قلب ال methods
لازم بنستخدم `this` + اسم ال property زي ما في المثال كدا

*ملحوظة: لو عملت methods جوا ال `constructor` في الحالة دي كل object هياخد نسخة 

لكن الصح ان لو هتعمل methods تكون بعد ال constructor لان ساعتها ال methods هتكون shred بين كل ال objects

### Update Properties And Built In Constructors

**Update Properties**
يعني إزاي تغيّر قيمة property جوه object
```js
class User {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  updateAge(newAge) {
    this.age = newAge;
  }
}

let user1 = new User("Belal", 23);

user1.updateAge(35);

console.log(user1.age); // 35
```
دي الطريقة الصح المستخدمة 

**Built-in Constructors**
دي constructors جاهزة في اللغة اشهرهم `String,er, Array, Date, Object`

مثال عام لاستخدام ال constructor 
```js
class Product {
  constructor(title, price) {
    this.title = title;
    this.price = price;
    this.createdAt = new Date();
  }

  updatePrice(newPrice) {
    if (newPrice > 0) {
      this.price = newPrice;
    }
  }
}

let p1 = new Product("Phone", 5000);

p1.updatePrice(4500);

console.log(p1);

/*
Output:

Product {
  title: 'Phone',
  price: 4500,
  createdAt: 2026-04-07T17:56:30.012Z
}
*/
```
### Class static properties, methods

ال `static` يعني حاجة تبع ال `class` نفسه مش تبع ال object بنستخدمه عشان ننفذ function او اي حاجة لكن علي مستوي ال `class` 
```js
class Product {
  static total = 0;

  constructor(title) {
    this.title = title;
    Product.total++;
  }

  static showCount() {
    console.log("Total: " + Product.total);
  }
}

let p1 = new Product("Phone");
let p2 = new Product("Laptop");

Product.showCount(); // Total: 2
```
المثال ده بيوضح بشكل عملي ميرزة ال `static methods`  لان هو هنا بيعمل ايه هو بجبلك عدد ال products اللي اتعملت في ال class ده 

*ملحوظة: ال this داخل ال static method ساعتها بتشاور علي ال class
بتكون كدا `this  ===  class` 
```js
class Test {
  static hello() {
    console.log(this);
  }
}

Test.hello(); // Test class
```

### Class Inheritance

معناها ان class هيورث او يعني هياخد methods , properties من class اخر بنستخدم المبدأ ده عشان نقلل التكرار في الكود يكون منظم اكتر 

ده الشكل الاساسي لنظام ال Inheritance  
```js
class Parent {
  
}

class Child extends Parent {

}
```

مثال يوضح الفكرة من المبدأ ده
```js
// Parent
class User {
  constructor(name) {
    this.name = name;
  }

  sayHello() {
    console.log("Hello " + this.name);
  }
}
// Child
class Admin extends User {
  constructor(name, role) {
    super(name); // from parent
    this.role = role;
  }
}

let admin1 = new Admin("Belal", "Super Admin");

console.log(admin1.name); // Belal
console.log(admin1.role); // Super Admin
```
خلي بالك  لما تضيف constructor في ال child لازم تستخدم `()super` ولازم super تكون قبل `this`

### Class Encapsulation

دي طريقة بتخلي ال properties محمية او يعني private ومتقدرش تعدل عليها او تقراها بشكل مباشر لكن ممكن تعمل ده من خلال ال methods بنستخدم المبدأ ده عشان نحمي البيانات من التعديل الغلط و نتحكم في ال values اللي اسمه ال validation

لو عاوزين نطبق بقي مبد ال encapsulation ده في ال class علي property معينة بنحط قدام ال property دي رمز ال `#` 
```js
class User {
  #salary;

  constructor(name, salary) {
    this.name = name;
    this.#salary = salary;
  }

  getSalary() {
    return this.#salary;
  }

  setSalary(value) {
    if (value > 0) {
      this.#salary = value;
    }
  }
}

let user1 = new User("Belal", 5000);
console.log(user1.getSalary()); // 5000
user1.setSalary(7000);
console.log(user1.getSalary()); // 7000
```

### Prototype

كل object في JavaScript عنده حاجة اسمها `prototype` بيستخدمها علشان يورث منها properties و methods وهو مهم عشان هو بيوفر في ال memory عشان يخلي كل ال objects تشارك نفس ال methods بدل ما كل Object يعمل نسخة لنفسه في ال memory 

مثال يوضح الفكرة دي
```js
function User(name) {
  this.name = name;

  this.sayHello = function () {
    console.log("Hello " + this.name);
  };
}
```
هنا كل object بياخد نسخة من `sayHello` فهنا في استهلاك لل memory علي الفاضي 

```js
function User(name) {
  this.name = name;
}

User.prototype.sayHello = function () {
  console.log("Hello " + this.name);
};
```
الحل بقي هو ال `prototype` لانه هيخلي كل ال object تشترك في نفس ال method او ال function يعني وكدا نكون وفرنا في ال memory

**Add To Prototype Chain**

دي معناها انك بتضيف methods أو properties للـ prototype علشان كل الـ objects تشوفها

مثال:
```js
function User(name) {
  this.name = name;
}

User.prototype.sayHello = function () {
  console.log("Hello " + this.name);
};
let u1 = new User("Belal");
let u2 = new User("Ahmed");

u1.sayHello();
u2.sayHello();
```
هنا انا ضفت function اسمها sayHello بس بال prototype كدا بقي اللي هيحصل ان كل ال object تقدر تتعامل عادي مع ال function دي من غير ما كل object كان يعمل نسخة لنفسه

**Add methods**

```js
Admin.prototype.showRole = function () {
  console.log(this.name + " is " + this.role);
};

let a1 = new Admin("Belal", "Admin");

a1.sayHello(); // from User
a1.showRole(); // from Admin
```
اللي حصل هنا كالتالي :
```txt
a1 → Admin.prototype → User.prototype → Object.prototype
```
ودي هنا بتكون  `Prototype Chain` كاملة

### Property Descriptor

 كل property في object ليها إعدادات مخفية (meta data) بتتحكم في سلوكها

مثال :
```js
let user = {
  name: "Belal"
};
```
الـ `name` دي ليها properties مخفية زي:

- ال writable
- ال enumerable
- ال configurable

ده ال Descriptor بتاع ال property
```js
console.log(Object.getOwnPropertyDescriptor(user, "name"));

/*
{
  value: "Belal",
  writable: true,
  enumerable: true,
  configurable: true
}
*/
```

طب معناهم ايه:
ال **writable** يعني هل نقدر نغير ال value الموجودة ب value تانية
```js
user.name = "Ahmed";
```
لو انت مخلي قيمة ال `writable = true` ال value هتتغير عادي

ال **enumerable** يعني لو عملت loop علي ال قيم ال object ده هتظهر ولا لا
```js
for (let key in user) {
  console.log(key);
}
```
لو ال `enumerable = true` فهتظهر عادي لو عملت looping علي ال object

ال **configurable** يعني هل اقدر امسح ال property دي او اغير ال descriptor بتاع ال property دي 

مثال علي تعديل ال descriptor
```js
let user = {
  name: "Belal"
};

Object.defineProperty(user, "name", {
  writable: false,
  enumerable: false,
  configurable: false
});
```
الشكل ده كدا مش هيخليك لا تعدل علي ال value بتاعة ال Property ولا تظهر في ال looping و لا تقدر تمسحها 

## Date And Time

ال `Date` في js هو عبارة عن Object او constructor بنتعامل بيه مع الوقت الحالي و التاريخ وما شابه يعني خلي بالك ال date في computer science من يوم `1/1/1970` لو عاوز تعرف القصة ابحث عنها  

```js
let now = new Date();
let date = new Date();

console.log(now); //Mon Apr 13 2026 16:00:00 GMT+0200
console.log(date.getTime()); // timestamp (milliseconds from 1970)
```
ده هيجبلك الوقت الحالي زي ما واضح كدا 

### Get Date and Time

**getFullYear( )**

ده هيجبلك السنة اللي انت فيها
```js
date.getFullYear() // 2026
```

**getMonth( )**

ده هيجبلك رقم الشهر لكن خد بالك هو هيرجعلك رقم الشهر بس بال index بتاعه يعني هيكون رقم من `( 0 - 11 )` 
```js
date.getMonth() // 3 = April
```

**getDate( )**

ده هيجبلك رقم اليوم في الشهر احنا النهاردة 13 في الشهر هيجيب 13
```js
date.getDate() // 13
```

**getDay( )**

ده هيجبلك رقم اليوم في الاسبوع
```js
date.getDay() // 0 = Sunday
```

**getHours( )**

ده هيجيب الساعة كام حاليا طبعا هتكون بنظام 24 ساعة وتقدر تجيب الدقايق والثواني وحتي ال milliseconds وكل حاجة منهم ليها ال method الخاص بيها 
```js

date = new Date();
console.log(date.getHours()) // 16
console.log(date.getMinutes()) // 47
console.log(date.getSeconds()) // 33
```

**getUTCFullYear ( )**

بص نفس الكلام اللي فوق لكن ده بالتوقيت العالمي يعني ده هيجبلك السنة بالتوقيت العالمي

**getUTCMonth( )**

ده بردو هيجبلك الشهر بالتوقيت العاليمي وقيس بقي علي كدا عشان في method كتيرة لكل حاجة حرفيا

### Set Date and Time

**setFullYear( )**

ده من خلاله هتقدر تغير السنة الحالية 
```js
date.setFullYear(2030)
```

**setMonth( )**

ده هتغير بيه الشهر لكن ب ال Index بتاع الشهر زي ما اتفقنا `( 0 - 11 )`
```js
date.setMonth(0) // January
```

**setDate( )**

بنغير بيه اليوم لكن في بالنسبة للشهر 
```js
date.setDate(15)
```

**setHours( )**

هنغير بيه الساعة 
```js
date.setHours(10)
```

وبنفس النظام بقي مع باقي ال set methods 

في بس method مهمة اللي هي 
**setTime( )**

نغير بيها  الوقت كله باستخدام `timestamp`
```js
date.setTime(0) // يرجع ل 1970
```

### Formatting Date And Time 

**toDateString( )**

بتجيب التاريخ بس (بدون وقت)
```js
let date = new Date();

console.log(date.toDateString()); // Mon Apr 13 2026
```

**toTimeString( )**

بتجيب الوقت بس 
```js
console.log(date.toTimeString());
```

**toLocaleString( )**

بيرجع تاريخ و وقت لكن حسب لغة الجهاز بتاعك
```js
console.log(date.toLocaleString()); // 13/4/2026, 4:30:25 PM
```

**toLocaleDateString( )**

نفس الكلام لكن التاريخ بس بردو علي حسب لغة الجهاز
```js
console.log(date.toLocaleDateString());
```

**toLocaleTimeString( )**

نفس الكلام لكن الوقت بس 
```js
console.log(date.toLocaleTimeString());
```

مثال هيرجع تاريخ اليوم لكن بالعربي
```js
let now = new Date();
console.log(date.toLocaleDateString("ar-EG")); // ١٣‏/٤‏/٢٠٢٦
```

**toISOString( )**

ده بيجيب التاريخ لكن بصيغة ثابتة 
```js
console.log(date.toISOString()); // 2026-04-13T14:30:25.000Z
```

### Tracking Operations Time

معناها هنقيس الكود بياخد وقت قد ايه عشان ينفذ المطلوب في طريقتين واحدة قديمة ودي مش دقيقة اوي لكن شغالة تمام وفي طريقة جديدة ودي بتكون دقيقة جدا 

الطريقة القديمة :
```js
let start = Date.now();

// operation
for (let i = 0; i < 1000000; i++) {}

let end = Date.now();

console.log(end - start); // 3 milliseconds
```
الطريقة دي مش ادق حاجة

الطريقة الجديدة :
**performance.now( )**

دي بتكون دقيقة جدا لانها بترجع الوقت ب (microseconds)
```js
let start = performance.now();

for (let i = 0; i < 1000000; i++) {}

let end = performance.now();

console.log(end - start); // 2.478100000000005
```

**performance.mark( )**

ببساطة فكرتها انها هتحط علامة او يعني mark عند وقت معين 
```js
performance.mark("start");

for (let i = 0; i < 1000000; i++) {}

performance.mark("end");

performance.measure("loopTime", "start", "end");

let result = performance.getEntriesByName("loopTime");

console.log(result[0].duration); // 2.530299999999997
```
الطريقتين مهمين لكن كل حاجة بيكون ليه استخدام علي حسب السيناريو المستخدم فيها

## Generator Function

دي فكرتها عبارة عن function بتقدر تقف وتكمل نفس وقت ما انت عاوز 
```js
function* myGenerator() {
	yield
}
```
ال `*` هنا مهمة جدا 
اما ال `yield` دي زي ال return كدا في لكن هي هنا بتوقف ال function مش بتنهيها 

مثال:
```js
function* gen() {
  yield 1;
  yield 2;
  yield 3;
}
let g = gen();

console.log(g.next()); // { value: 1, done: false }
console.log(g.next()); // { value: 2, done: false }
console.log(g.next()); // { value: 3, done: false }
console.log(g.next()); // { value: undefined, done: true }
```
ايه هو ال 
**next( )**
ده وظيفته ان يشغل ال function لحد او yield
```js
function* test() {
  console.log("Start");
  yield 1;
  console.log("Middle");
  yield 2;
  console.log("End");
}

let t = test();

t.next();
// Start

t.next();
// Middle

t.next();
// End
```
ال `()next` هنا بينفذ بس لحد اخر حاجة وقف عندها yield وكل مرة بتعمل `()next` بيجيب بينفذ لحد ال yield أللي بعده وهكذا

بنستخدم ال generator function في اننا نوفر في ال memory لان مش بيخزن كل ال values مرة واحدة تاني حاجة في حاجة اسمها ال lazy execution لان بيشتغل step by step مش مرة واحدة فهنا هتكون ال generator function مناسبة جدا

### Delegate Generator Function

ال delegate معناه ان نائب بنفس المعني ده ان هيكون في generator بينوب عن generator تاني او يعني بيسلم التنفيذ ل generator او iterable تاني وده بيكون عن طريق ان بتضيف `*yield` 

مثال:
```js
function* gen1() {
  yield 1;
  yield 2;
}

function* gen2() {
  yield* gen1();
  yield 3;
}

let g = gen2();

console.log(g.next()); // 1
console.log(g.next()); // 2
console.log(g.next()); // 3
```
احنا هنا ايه اللي حصل انت عملت ال generator الاول `gen1` تمام مفيش اي مشاكل وبردو عملت ال `gen2` لكن في ال generator التاني انت خليته ينوب في الشغل عن ال `gen1` لاننا استخدمنا `()yield* gen1` كدا اللي هيحصل انه ههحبلك القيم ال في ال `gen1` ويكمل الباقي لو في قيم في ال `gen2` لكن خلي بالك لما محطتش `*`بعد ال yield هيرجعلك اسم ال generator 

### Generate Infinite Numbers

ده فكرته انك هتعمل generator يطلع ارقام لا نهائية عن طريق انك هتعمل loop لكن زي ما نت عرفت ان ال generator مش هينفذ ال loop مرة واحدة لا هو مش هينفذ او يعني مش هيجيب ال value أللي عليها الدور غير لما تطلب yield اللي بعدها 
```js
function* numbers() {
  let i = 0;

  while (true) {
    yield i++;
  }
}
let gen = numbers();

console.log(gen.next().value); // 0
console.log(gen.next().value); // 1
console.log(gen.next().value); // 2
console.log(gen.next().value); // 3
```
هنا احنا عملنا infinite loop بس الفكرة ان ده generator زي ماقولنا فال yield هيوقف التنفيذ كل مرة وال `()next` هو اللي بخليه يكمل 

ده مثال عملي عشان تفهم فكرة ال `generate infinite loop` :
```js
// generate IDs

function* idGenerator() {
  let id = 1;

  while (true) {
    yield id++;
  }
}

let ids = idGenerator();

console.log(ids.next().value); // 1
console.log(ids.next().value); // 2
```


## JSON

هو format بيستخدم عشان ينقل ال data بين ال `server` لل `(JavaScript)client` 
ده شكله 
```js
{
  "name": "Belal",
  "age": 21
}
```
لازم ال keys تكون داخل `" "` وده الفرق بين ال json , js object لان ال js object مش لازم الkeys تكون داخل `" "` وخلي بالك بردو ان ال json ال type بتاعه هو `STRING` 

**JSON.parse( )**

دي بتحول ال json  الي JavaScript object 
```js
let data = '{"name":"Belal","age":23}';

let obj = JSON.parse(data);

console.log(obj.name); // Belal
```

**JSON.stringify( )**

دي بتعمل العكس يعني هتحول من JavaScript object الي json String 
```js
let obj = {
  name: "Belal",
  age: 23
};

let json = JSON.stringify(obj);

console.log(json); // {"name":"Belal","age":23}
```

*ملحوظة : وانت بتستخدم stringify وكان موجود في ال object اللي هتحوله key وال key ده ال value بتاعته هي function ف stringify هتتجاهلها لان json عبارة عن `data` فقط مفيش logic 
ولو عندك حاجة `undefined` فهمي بردو هتتشال 

## Synchronous & Asynchronous

**Synchronous**

ال Synchronous معناه متزامن يعني الكود هيشتغل line by line يعني لما ال line الاول يخلص يدخل علي ال line اللي بعده مينفعش يدخل علي ال line التاني والاول لسه مخلصش
```js
console.log("1");
console.log("2");
console.log("3"); 
/*
1
2
3
*/
```
عادي جدا ال output انما بقي مثال شبه اللي جي ده 

```js
console.log("Start");

for (let i = 0; i < 1e9; i++) {}

console.log("End");
``` 
هو هنا هيطبع start ويستني ال Loop تخلص عشان يطبع end 

**Asynchronous**

ده معناه غير متزامن يعني مش لازم ال line  الاول يخلص عشان ال line التاني يتنفذ لا الاتنين هيشتغلو مع بعض بشكل pararel مع بعض من غير اي مشاكل 
```js
console.log("Start");

setTimeout(() => {
  console.log("Async");
}, 2000);

console.log("End");
```
هنا هيطبع start وبعدين هيطبع end عادي ولما الثايتين يعدو هيطبع async وده  تعريف ال `Asynchronous`

**Event Loop And Callback Queue**

هنا موضوع هيكون انك تفهم ال js بيشتغل ازي مش كتبابة كود الفكرة ببساطة ان ال `event loop` بيراقب ال `call stack` لو فاضي بيجيب ال task اللي عليها الدور من ال `callback queue` وينفذها الفكرة كلها من النظام ده انه بيخلي ال JavaScript كأنها لغة `multi-tasks` او `multi-threads` بس ركز اللغة اصلا هي single threads يعني الكود بتاعها بيتنفذ داخل thread واحد

ال `call stack` ده المكان اللي بيتنفذ فيه الكود (line by line) 
ال `callback queue` ده المكان اللي tasks بتقف فيه مستنية دورها عشان تتنفذ
ال `event loop` ده زي متقول كدا المدير اللي بينظم الدنيا كلها بيعمل ايه بيشوف لو ال `call stack` فاضي يجيب ال task اللي عليها الدور من ال `callback queue` وينفذها بس هي دي وظيفته

مثال: 
```js
console.log("A");

setTimeout(() => {
  console.log("B");
}, 0);

console.log("C");
/*

A
C
B

*/
```
طب اي الل حصل هنا ليه الترتيب طلع بالشكل ده لان ال `setTimeout` هي function خاصة بال webApi فبتروح الاول لل webApi وبستتني في ال queue لحد ما ييجي دورها وتتنفذ لو مش فاهم خلي اي Ai يفهمك الحتة دي بس الموضوع بسيط اعتقد

## AJAX (Asynchronous JavaScript And XML

هو وظيفته العملية يعني باختصار تبعت request للسيرفر وتاخد data من غير ما تعمل refresh للصفحة بنستخدمه في ال search live او عشان نجيب data من ال api 

ليه طريقتين:
الطريقة القديمة:
**XMLHttpRequest( )**

```js
let xhr = new XMLHttpRequest();

xhr.open("GET", "https://jsonplaceholder.typicode.com/users");

xhr.send();

xhr.onreadystatechange = function () {
  if (xhr.readyState === 4 && xhr.status === 200) {
    console.log(JSON.parse(xhr.responseText));
  }
};
```
ده الشكل القديم مشاكله في ال verbose , معقد صعب في القراءة 

الطريقة الحديثة:
**fetch( )**

```js
fetch("https://jsonplaceholder.typicode.com/users")
  .then(res => res.json())
  .then(data => {
    console.log(data);
  });
```
الطريقة دي سهلة لان بتبعت request بيرجع response تحوله ل json تستخدم ال data

## Promise

هو عبارة عن object بيمثل عملية async هتنجح او هتفشل بعد شوية يعني لو ال promise اتحقق ده ساعتها بنسميه `resolved` ولو ال promise فشل ومتحققش ساعتها بنسميه `rejected`

**ال promise ليه 3 حالات :**

1. الحالة الاولي  `pending` ودي معناه لسه ال promise في حالة انتظار او Pending يعني
2. الحالة التانية `fulfilled` ودي معناها ان الحمد الله نجح 
3. الحالة التالتة  `rejected` ودي معناه ان ال promise فشل او منفعش

وده بيكون شكل ال promise :
```js
let myPromise = new Promise((resolve, reject) => {

});
```
وهو بيكون عبارة عن constructor بياخد function فيها `resolve, rejsect` 

مثال :

```js
let myPromise = new Promise((resolve, reject) => {
  let success = true;

  if (success) {
    resolve("Success");
  } else {
    reject("Failed");
  }
});

myPromise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  });
```

الجزء اللي في الاول ده احنا عملنا ال promise وهيعمل ايه يعني ده الجزء اللي فيه ال Logic وبنسميه `Promise Executor` وده بيكون فيه ال process ال async و القرار هل ال process نجحت او فشلت

اما الجزء التاني ده بيتعامل مع ال result النهائية والجزء ده بنسميه `Promise Handlers`
وبنستخدم `then` في حالة ال state بتاع ال Promise كانت `fulfilled / resolved`
و `catch` لو  ال state بتاع ال Promise  كانت `rejected`

عشان تكون فاهم بردو او يعني يكون ابسط قيمة ال `reslove` اللي في ال logic فوق دي بتتخزن في `then`
وال `reject` اللي موجودة في ال else ودي بتكون في حالة انت ال promise فشل بتتخزن في `catch`

في حاجة كمان او يعني method كمان بنستخدمها مع ال promises وهي ال `finally` ودي وظيفتها ان سواء في حالة ال fulfilled او rejected هتنفذ حاجة معينة 

#### Promise Methods

**Promise.all( )**

دي فكرته ببساطة ان بيستني كل ال promises تنجح (resolved) ويرجعلك كل ال values  في `Array` لكن لو في promise واحدة فشلت(rejected) ساعتها هيكون بالنسباله كله فشل
```js
let p1 = Promise.resolve("One");
let p2 = Promise.resolve("Two");
let p3 = Promise.resolve("Three");

Promise.all([p1, p2, p3])
  .then((data) => {
    console.log(data);
  });
// ["One", "Two", "Three"]  
```

طبعا هنا كل ال promises نجحت فعلا فرجعلك ال result كلها في `Array` لكن لو واحدة منهم كانت فشلت كان هيرجعلك `Error`

**Promise.allSettled( )**

ده هيرجعلك نتيجة كل  ال promises سواء نجحت او فشلت 
```js
let p1 = Promise.resolve("One");
let p2 = Promise.reject("Error");
let p3 = Promise.resolve("Three");

Promise.allSettled([p1, p2, p3])
  .then((data) => {
    console.log(data);
  });
  
/*

[
  { status: "fulfilled", value: "One" },

  { status: "rejected", reason: "Error" },

  { status: "fulfilled", value: "Three" }
]

*/
```

**Promise.race( )**

دي فكرتها ببساطة ان ا`ول Promise تخلص هي دي اللي هترجع` سواء بردو نجحت او فشلت 

```js
let p1 = new Promise((resolve) => {
  setTimeout(() => {
    resolve("First");
  }, 1000);
});

let p2 = new Promise((resolve) => {
  setTimeout(() => {
    resolve("Second");
  }, 2000);
});

Promise.race([p1, p2])
  .then((data) => {
    console.log(data);
  });
  
// First
```

هنا هو رجع `First`عشان هي هترجع بعد ثانية واحدة فدي اول Promise هينجح وحتي لو كان في Promise فهيم فشل اول واحد فهو ده بردو اللي هيرجع وخلي ال value اللي هترجع مش هترجع في ال `Array` 
## Fetch Api

هي عبارة عن function بتبعت http request لل server وبترجع `Promise` وعشان كدا بنقدر نستخدم معاه الmethod الخاصة بال promise الليه `then, catch, async, await`
وده بيكون شكل ال fetch
```js
fetch("https://jsonplaceholder.typicode.com/users")
  .then((response) => {
    return response.json();
  })
  .then((data) => {
    console.log(data);
  });
```
ال response ده بيكون object في معلومات عن ال request
زي: `status, headrs, body` 

لكن ال body مش بيكون جاهز لازم الاول نحوله ل `JSON` الاول فبنستخدم `()response.json` لكن خلي بالك بردو انت حتي بعد لما حولته ل `json`  مش هيكون data مباشرة كدا لا ده هيكون `promise` عشان كدا استخدمنا `()thne` كمان لان دي بقي اللي هيكون متخزن فيها ال data اللي عاوزينها

## Async, Await

**async**

هي عبارة عن `keyword` بنحطها قبل ال function وبترجعلك `Promise` 
```js
async function test() {
  return "Belal";
}
console.log(test()); // Promise { "Belal" }
```

طبعا هنا رجعت `Promise` وطالما رجعت promise يبقي هنستخدم `then` 
```js
async function test() {
  return "Belal";
}

test().then((data) => {
  console.log(data);
}); // Belal
```

**await**

دي وظيفتها ان تخلي الكود كل يقف لحد لما ال `Promise` تخلص وساعتها تكمل السطور اللي بعده وخلي بالك ان await لازم تبقى جوه async 
```js
async function test() {
  let promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve("Belal");
    }, 3000);
  });

  let result = await promise;

  console.log(result);
}

test();
```
اللي بيحصل هنا باختصار ان ال promise بدا تمام ال await هتوقف تنفيذ باقي الكود لحد لما ال promise يخلص بعد 3 ثواني `resolve("Belal")` والقيمة تتحط في ال `result` ال output يكون `Belal` لو اخدت بالك هنا محتجناش `then` ليه لان ال `await` وظيفتها انها تفك ال promise اللي هيجيلها بتقوم بنفس وظيفة ال `then`

*ملحوظة : ال await مش بتوقف الكود كله لا هي بس بتوقف ال async function  

مثال يوضح الملحوظة دي 
```js
async function test() {
  await new Promise((resolve) => {
    setTimeout(resolve, 3000);
  });

  console.log("Inside");
}

console.log("Start");

test();

console.log("End");

/*
Start
End
Inside
*/
```
لاحظ هنا ان البرنامج كمل عادي وبعد ال 3 ثواني طبع ال `Inside` انما بقي لو فعلا ال await بتوقف البرنامج فالمفروض كان ال `Inside` هي اللي تطلع الاول

*ال await مع ال reject لو promise فشل هترمي `throw error` عشان كدا بنستخدم `try, catch` 

## Try, Catch

بنستخدمهم عشان نمسك ال Error بدل ما الكود يوقف ويكسر ال APP 
```js
try {
  let x = y + 10; 
  console.log(x);
} catch (error) {
  console.log("Error happened:", error.message);
} // Error happened: y is not defined
``` 

هنا هو رمي error افضل ما البرنامج يوقف وينهار كمان هو ساعدك تتعامل مع ال errors بشكل نضيف

**مثال مع ال finally**

```js
try {
  console.log("Trying...");
} catch (error) {
  console.log("Error");
} finally {
  console.log("This always runs");
}
```
ال finally هتتنفذ كدا كدا سواء حصل error او محصلش 