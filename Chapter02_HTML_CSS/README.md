# HTML გამოყენების საფუძვლები
<hr>
HTML არის სტანდარტული მარკაპ ენა რომელიც გამოიყენება ვებ გვერდების შესქმნელად

## შესავალი [HTML Introduction](https://www.w3schools.com/html/html_intro.asp)
HTML არის მარკირების ენა რომელიც გამოიყენება ვებ გვერდების შესაქმნელად.

HTML ტიპის ფაილებს აქვთ `.html` გაფართოება. გაფართოება მიანიშნებს ტექსტურ ედიტორს
ან ვებ ბრაუზერს მიხვდეს თუ რა ტიპის ფაილთან აქვს ურთიერთობა. ახალი html
ფაილის შექმნისას ის უნდა შევინახოთ შესაბამის ფორმატში.

მაგალითად: `main.html`

ამ ფაილის გახსნისას ბრაუზერს ეცოდინება როგორ გამოიტანოს მასში მოთავსებული html კოდი.
## სტრუქტურა

### საწყისი შაბლონი

თანამედროვე ინტეგრირებული გარემოების (IDLE) უმრავლესობას, როგორიც არის PyCharm, WebStorm, Atom და ა.შ. აქვს ჩაშენებული საწყისი HTML-ის შაბლონი.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <p>Hello world</p>
  </body>
</html>
```

## HTML ელემენტების ანატომია
HTML-ის ელემენტი მოთავსებულია შესაბამის ელემენტის ტიპის განმსაზღვრელ tag-ებში. მაგ: 
![html თეგები](Projects/images/anatomy.png)
_[მსგავსება HTML-სა და Markdown ფორმატ შორის და ასევე უამრავი საჭირო თეგი თავისი მაგალითებით შეგიძლიათ ანხოთ ამ მისამართზე](https://www.markdownguide.org/basic-syntax/)_

ფუნქციურად მსგავსი ელემენტების თეგებს ვაერთიანებთ კომპონენტებში, კომპონენტის განმსაზღვრელ თეგებს შორის.

HTML დოკუმენტის სტრუქტურა მოიცავს ორ ძირითად კომპონენტს `<head> </head>` და `<body> </body>`.


- head კომპონენტში გაერთიანებული ელემენტები გამოიყენება html დოკუმენტის აღწერისთვის და კონფიგურაციისთვის. იგი ვებგვერდზე არ ჩანს ვიზუალურად და ინახავს meta ინფორმაციას, დაკავშირებულ ფაილებს, ენკოდინგის ტიპს და ა.შ. მაგ: `<title> Title </title>`

- body კომპონენტში გაერთიანებული ელემენტები გამოიყენება ვიზუალური მხარის შესაქმნელად. მაგ: `<p> Hello world </p>`


## კომენტარი
კომენტარი დოკუმენტის ის ნაწილია რომელსაც ბრაუზერი უგუნვებელყოფს გვერდის დამუშავებისას და ის მხოლოდ ადამიანისთვის არის განკუთვნილი.

მაგალითად:

```html
<!--    აქ რაც არ უნდა დაწერო ყველაფერი ქარი შევა კომენტარში   -->
```
ინფორმაცია `<!-- და -->` თეგებს შორის აღიქმება კომენტარად, მრავალხაზიანი კომენტარის შემთხვევაშიც:

```html
<!--    
გრძელი სიტყვა მოკლედ ითქმის
და სასურველია ნაკლებ ხაზში ჩაატიო
-->
```
## ტექსტი, პარაგრაფი, ფორმატირება

### სათაურები

```html
<h1>პირველი დონის სათაური</h1>
...
<h6>მეექვსე დონის სათაური</h6>
```

| თეგი   | ელემენტი             |
| ------ | -------------------- |
| **h1** | მაღალი დონის სათაური |
| **h6** | დაბალი დონის სათაური |

### პარაგრაფები

```html
<p>
  პარაგრაფი.<br />
  ახალი ხაზი.
</p>
<p>ახალი პარაგრაფი.</p>
<hr />
<p>ნახეთ ხაზი ზემოთ.</p>
```

| თეგი   | ელემენტი           |
| ------ | ------------------ |
| **p**  | პარაგრაფი          |
| **br** | ახალი ხაზი         |
| **hr** | ჰორიზონტალური ხაზი |

### ტექსტის ფორმატირება

```html
<em>Formatting</em> is <strong>important</strong> ! (a+b)
<sup
  >2<sup> = a<sup>2</sup>+ b<sup>2</sup> + 2ab</sup></sup
>
```

| თეგი       | ელემენტი    |
| ---------- | ----------- |
| **sub**    | subscript   |
| **sup**    | superscript |
| **em**     | emphasize   |
| **strong** | important   |
| **mark**   | highlighted |
| **small**  | small       |
| **i**      | italic      |
| **b**      | bold        |

## Div და Span

Div და Span გვეხმარება html კოდის პორციებად დაყოფაში. როდესაც დავიწყებთ ელემენტებისთვის სტილის მინიჭებას, ხშირად გვექნება შემთხვევა როდესაც გარკვეული სტილის
გამოყენება მხოლოდ კონკრეტული ელემენტების სეგმენტზე გვჭირდება. ასეთი შემთხვევებისთვის გამოიყენება ეს თეგები.
 
### სინტაქსი:

```html
...

<div class="container">
  <h1>სათაური</h1>
  <p>პარაგრაფი</p>
</div>
<p>პარაგრაფი div-ის გარეთ რომელიც <span>span თეგს შორის</span> მოვათავსეთ</p>

...
```

## ატრიბუტები

ზოგ HTML ელემენტს გააჩნია ატრიბუტები, ატრიბუტები განსაზღვრავენ ელემენტის რაობას.
შესაბამისი ატრიბუტების გამოყენებით შეგვიძლია ელემენტს მივანიჭოთ სტილი, ბმული, სახელი და ა.შ

### ბმულები

```html
<a href="url">გახსენი ბმული იმავე ფანჯარაში</a>
<a href="url" target="_blank">გახსენი ბმული ახალ ფანჯარაში</a>

<a href="#comments">ბმული ელემენტზე id-ით კომენტარი</a>
<h2 id="comments">კომენტარი</h2>
```

| ატრიბუტი | აღწერა           |
| -------- | ---------------- |
| **href** | ბმულის მისამართი |

### სურათები
<img src="https://www.flixist.com/wp-content/uploads/ul/226276-midnightgospel1.jpg" alt="description" width="300" height="200" />

```html
<img
  src="https://www.flixist.com/wp-content/uploads/ul/226276-midnightgospel1.jpg"
  alt="description"
  width="300"
  height="200"
/>
```

| თეგი    | ელემენტი |
| ------- | -------- |
| **img** | image    |

| ატრიბუტი      | აღწერა          |
| ------------- | --------------- |
| src           | მისამართი       |
| alt           | ტექსტი          |
| width; height | სიგანე; სიმაღლე |

## ხშირად გამოყენებადი თეგები

### დაუნომრავი სია

```html
<ul>
  <li>item</li>
  <li>item</li>
  <li>item</li>
</ul>
```

| თეგი   | ელემენტი       |
| ------ | -------------- |
| **ul** | unordered list |
| **li** | list item      |

### დანომრილი სია (დალაგებული)

```html
<ol>
  <li>first</li>
  <li>second</li>
  <li>third</li>
</ol>
```

| თეგი   | ელემენტი     |
| ------ | ------------ |
| **ol** | ordered list |
| **li** | list item    |

### სტანდარტული ცხრილი

```html
<table>
  <tr>
    <th>სათაური 1</th>
    <th>სათაური 2</th>
  </tr>
  <tr>
    <td>მწკრივი 1, სვეტი 1</td>
    <td>მწკრივი 1, სვეტი 2</td>
  </tr>
  <tr>
    <td>მწკრივი 2, სვეტი 1</td>
    <td>მწკრივი 2, სვეტი 2</td>
  </tr>
</table>
```

| თეგი      | ელემენტი           |
| --------- | ------------------ |
| **table** | ცხრილი             |
| **tr**    | ცხრილის მწკრივი    |
| **th**    | ცხრილის დასახელება |
| **td**    | ცხრილის უჯრა       |

## [ფორმები](https://www.w3schools.com/html/html_forms.asp)

ვებ გვერდის ერთ-ერთი უმნიშვნელოვანეს ფუნქციონალია მომხმარებლისგან ინფორმაციის აღება. ინფორმაციის
ვებ გვერდის ინტერფეისიდან ამოღება ხდება html ფორმების გამოყენებით. ფორმის ასაწყობად ვიყენებთ
html თეგს `<form>`, რომელშიც შეგვიძლია მოვათავსოთ `<input>` ელემენტი.

ფორმის დასასრულს ვამატებთ **submit** ტიპის input-ს, რაც ავტომატურად ამაგრებს ღილაკს შევსებული ფორმის შესასრულებლად.

```html
<form>
  <fieldset>
    <legend>რეგისტრაცია</legend>
    <label for="signIn">სახელი :</label>
    <input type="text" id="signIn" name="login" />
    <br />
    <label for="pswd">პაროლი :</label>
    <input type="password" name="password" id="pswd" />

    <br />
    <label>სქესი:</label>
    <br />
    <input type="radio" name="sex" value="male" />მამრობითი<br />
    <input type="radio" name="sex" value="female" />მდედრობითი<br />
    <br />

    <label>საყვარელი პოკემონი : </label>
    <select name="color">
      <option>Charizard</option>
      <option>Gengar</option>
      <option>Greninja</option>
    </select>
    <br />

    <br />
    <input type="checkbox" name="" id="robot" />
    <label for="robot">არ ვარ რობოტი</label>
    <br />
    <input type="checkbox" name="" id="rules" />
    <label for="rules">ვეთანხმები ვებგვერდის წესებს</label>
    <br />

    <br />
    <textarea
      name=""
      id=""
      cols="30"
      rows="10"
      placeholder="კომენტარის სივრცე"
    ></textarea>

    <br />
    <input type="submit" value="რეგისტრაცია" />
  </fieldset>
</form>
```

| თეგი                        | ელემენტი                      |
| --------------------------- | ----------------------------- |
| **form**                    | form                          |
| **label**                   | label for input               |
| **fieldset**                | group inputs together         |
| **legend** for=""           | legend for fieldset           |
| **input** type="_text_"     | text input                    |
| **input** type="_password_" | password input                |
| **input** type="_radio_"    | radio button                  |
| **input** type="_checkbox_" | checkbox                      |
| **input** type="_submit_"   | send form                     |
| **select**                  | drop-down list                |
| **option**                  | drop-down list item           |
| **optgroup**                | group of drop-down list items |
| **datalist**                | autocompletion list           |
| **textarea**                | large text input              |
## დამატებითი რესურსები
1. [HTML-ის სრული ვებ კურსი დეველოპერთათვის Mozilla-სგან](https://developer.mozilla.org/en-US/docs/Web/HTML)
2. [gendx | HTML Cheat Sheet](https://github.com/gendx/html-cheat-sheet#minimal-page)

---

# CSS

**cascading style sheets** ( CSS ) აღწერს თუ როგორ გამოჩნდება HTML ელემენტები ვებ გვერდზე.
CSS შეუძლია რამოდენიმე სხვადასხვა გვერდზე განლაგებულ ელემენტებზე იქონიოს გავლენა. სტილის დაწერა შეგვიძლია თვითონ html
დოკუმენტში, კონკრეტულ html ელემენტზე და დაკავშირებულ ფაილში, მაგ.: `style.css`

## ტერმინოლოგია და ანატომია

![ანატომია](https://mdn.mozillademos.org/files/9461/css-declaration-small.png)

 დასახელება     | გამოყენება      
----------------|-----------------
 Selector       | ტეგის სელექტორი 
 Property       | პარამეტრი       
 Property Value | მნიშვნელობა     
 Declaration    | გაწერა (სტილის) 

### მაგალითი:

```css
p {
    background-color: lightblue;
    color: white;
    text-align: center;
    font-family: serif;
    font-size: 20px;
}
```

## სტილის უპირატესობის იერარქია

- inline style - გულისხმობს კონკრეტულ html ელემენტზე გაწერილ სტილს. ამისთვის გამოიყენება style ატრიბუტი. ამგვარი სტილი
  უპირატესია ყველა სხვა ფორმით გაწერილ სტილზე.

```html
<p style="color: red">This is a paragraph.</p>
```

- internal style - გულისხმობს html დოკუმენტში გაწერილ სტილს. ამისთვის `<head> </head>` ბლოკში
  გამოიყენება `<style> </style>`. ამგვარი სტილი არაა უპირატესი inline სტილზე.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Document</title>

    <style>
        h1 {
            color: blue;
        }
    </style>
</head>

<body>
<h1>This is a heading</h1>
</body>
</html>
```

- external style - გულისხმობს დამოუკიდებელ css დოკუმენტში გაწერილ სტილს. ამისთვის html დოკუმენტს `<head> </head>` ბლოკში
  უნდა დავუკავშიროთ css დოკუმენტი. ამგვარი სტილი არაა უპირატესი inline სტილზე.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <link rel="stylesheet" href="./style.css"/>
    <title>Document</title>
</head>

<body>
<h1>This is a heading</h1>
</body>
</html>
```

ატრიბუტი `rel` აღნიშნავს ბმული ფაილის ტიპს/როლს _html_ ფაილისთვის, ხოლო
`href`-ში თავსდება იმ ფაილის მისამართი სადაც სტაილშიტია მოთავსებული.

## class და id

ყოველ HTML ელემენტს აქვს შესაძლებლობა მიენიჭოს class ან id ატრიბუტი. ამ ატრიბუტების დახმარებით შეგვიძლია მივწვდეთ
სასურველ ელემენტებს.

**class**-ის გამოყენებით შეგვიძლია გავაერთიანოთ სხვადასხვა (თუნდაც არაერთგვაროვანი ტიპის) html
ელემენტი და მივანიჭოთ მათ საერთო მახასიათებელი.

**id**-ის მეშვეობით შეგვიძლია ინდივიდუალურად ავირჩიოთ html ელემენტი რომელზეც გვსურს რეაგირება.
შესაბამისად ყოველ ელემენტს უნდა ჰქონდეს უნიკალური ინდივიდუალური id მნიშვნელობა.

## css სინტაქსი:

`#` - გამოიყენება id-ის გამოსაძახებლად
`.` - გამოიყენება class-ის გამოსაძახებლად

მაგალითად:

```css
.class {
    background: maroon;
}

#id {
    background: green;
}
```

## ხშირად გამოყენებული პარამეტრები

| პარამეტრი                                                         | აღწერა                                    | მაგალითი                                           |
|-------------------------------------------------------------------|-------------------------------------------|----------------------------------------------------|
| color                                                             | ტექსტის ფერი                              | color: red; color: ff0000                          |
| background-color                                                  | უკანა ფონის ფერი                          | background-color; white, background-color: #ffffff |
| border                                                            | ჩარჩო                                     | border: 1px solid black                            |                          
| border-radius                                                     | ჩარჩოს მომრგვალება                        | border-radius: 12px                                |
| padding, padding-top, padding-bottom, padding-right, padding-left | შვილობილი ელემენტის მშობლისგან დაშორება   | padding: 16px                                      |
| margin, margin-top, margin-bottom, margin-right, margin-left      | ორი HTML ელემენტის ერთმანეთისგან დაცილება | margin-top: 12px                                   |
| font-size                                                         | ფონტის ზომა                               | font-size: 16px                                    |
| cursor                                                            | მაუსის გადატარებისას იკონის შეცვლა        | cursor: pointer                                    |
| width                                                             | სისქე                                     | width: 32px                                        |
| height                                                            | სიმაღლე                                   | height: 64 px                                      |
| transition                                                        | ერთი ვიზუალიდან მეორეზე გადასვლის სიჩქარე | transition: 0.5s                                   |

### ჩარჩოს შექმნის მაგალითი

```css
div {
    background: maroon;
    border: orange;
    border-width: thick;
    border-style: dotted;
}
```

ან

```css
div {
    background: maroon;
    border: royalblue 2px dashed;
}
```

### ფონტი

#### ჩაშენებული ფონტების გამოყენება

```css
p {
    font-family: verdana;
    font-size: 20px;
    font-weight: bold;
    text-align: center;
}
```