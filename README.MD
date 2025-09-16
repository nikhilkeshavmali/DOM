1. createElement(tagName)

👉 Ye naya HTML element banata hai (but page pe tab dikhega jab append karoge).

Use case: Agar tumhe dynamically <div>, <li>, <button> etc. banana hai.

let newDiv = document.createElement("div");
newDiv.textContent = "Hello World!";

2. appendChild(node)

👉 Ye kisi element ko parent ke andar last me daal deta hai.

Use case: List me naya item add karna, div ke andar button daalna.

document.body.appendChild(newDiv); // upar jo banaya tha wo ab body me add ho gaya

3. removeChild(node)

👉 Parent se kisi specific child element ko hata deta hai.

Use case: Todo app me “delete” button dabaya aur list item remove karna hai.

let parent = document.querySelector(".todoListsElem");
let child = document.querySelector(".todoItem");
parent.removeChild(child);

4. addEventListener(event, function)

👉 Kisi element ke saath event bind karta hai (like click, input, hover).

Use case: Button pe click hone par kuch action karna.

let btn = document.querySelector(".btn");
btn.addEventListener("click", () => {
alert("Button clicked!");
});

5. removeEventListener(event, function)

👉 Kisi element se pehle se lagaya hua event listener hata deta hai.

Use case: Agar tum temporarily ek event disable karna chahte ho.

function showMsg() {
alert("Clicked!");
}

btn.addEventListener("click", showMsg);

// Later remove karna hai
btn.removeEventListener("click", showMsg);

⚠️ Important: removeEventListener tabhi kaam karega jab tum same function reference pass karoge (arrow function ke saath direct nahi chalega).

6. setAttribute(name, value)

👉 Kisi element ke attribute ko set/update karta hai.

Use case: src lagana image ke liye, id change karna, class add karna.

let img = document.createElement("img");
img.setAttribute("src", "photo.jpg");
img.setAttribute("alt", "My Photo");
document.body.appendChild(img);

🔑 Short Summary (Hinglish):

createElement: Naya element banao.

appendChild: Parent ke andar element daalo.

removeChild: Child element hatao.

addEventListener: Event lagao.

removeEventListener: Event hatao.

setAttribute: Attribute set/update karo.
