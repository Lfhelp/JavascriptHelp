# JavascriptHelp
Javascript practice and help

function alphabetPyramid(rows) {
  for (let i = 1; i <= rows; i++) {
    let line = '';
    for (let j = 0; j < i; j++) {
      line += String.fromCharCode(65 + j); // 65 is 'A'
    }
    console.log(line);
  }
}

console.log("Alphabet Pyramid:");
alphabetPyramid(5);






function reverseWords(sentence) {
  return sentence.split(' ').reverse().join(' ');
}

console.log(reverseWords("JavaScript is fun")); // "fun is JavaScript"





function countVowels(str) {
  let count = 0;
  const vowels = 'aeiouAEIOU';
  for (let char of str) {
    if (vowels.includes(char)) {
      count++;
    }
  }
  return count;
}

console.log(countVowels("Hello World")); // 3










function reverseArray(arr) {
  let reversed = [];
  for (let i = arr.length - 1; i >= 0; i--) {
    reversed.push(arr[i]);
  }
  return reversed;
}

console.log(reverseArray([1, 2, 3, 4, 5])); // [5,4,3,2,1]






<script>
  const numbers = [];

  document.getElementById('addNumber').addEventListener('click', function() {
    const input = document.getElementById('numberInput').value;
    if (input !== '') {
      numbers.push(Number(input));
      document.getElementById('output').innerText = numbers.join(', ');
      document.getElementById('numberInput').value = ''; // clear input
    }
  });

  document.getElementById('filterEven').addEventListener('click', function() {
    const evenNumbers = numbers.filter(num => num % 2 === 0);
    document.getElementById('output').innerText = evenNumbers.join(', ');
  });
</script>










<script>
  const products = [];

  document.getElementById('addProduct').addEventListener('click', function() {
    const name = document.getElementById('productName').value;
    const price = document.getElementById('productPrice').value;

    if (name && price) {
      products.push({ name: name, price: Number(price) });
      displayProducts();
      document.getElementById('productName').value = '';
      document.getElementById('productPrice').value = '';
    }
  });

  function displayProducts() {
    const productList = document.getElementById('productList');
    productList.innerHTML = '';

    products.forEach(product => {
      const li = document.createElement('li');
      li.textContent = `${product.name} - $${product.price}`;
      productList.appendChild(li);
    });
  }
</script>







<script>
  document.getElementById('applyStyle').addEventListener('click', function() {
    const text = document.getElementById('textInput').value;
    const style = document.getElementById('styleSelect').value;
    const styledText = document.getElementById('styledText');

    styledText.textContent = text || "Here is Text"; // if empty, default

    styledText.style.fontWeight = 'normal';
    styledText.style.fontStyle = 'normal';
    styledText.style.color = 'black';

    if (style === 'bold') {
      styledText.style.fontWeight = 'bold';
    } else if (style === 'italic') {
      styledText.style.fontStyle = 'italic';
    } else if (style === 'color') {
      styledText.style.color = 'red'; /
    }
  });
</script>










random 





<input type="number" id="sumInput" placeholder="Enter number">
<button id="addToSum">Add Number</button>
<button id="showSum">Show Sum</button>
<p id="sumOutput"></p>

<script>
  const sumNumbers = [];

  document.getElementById('addToSum').addEventListener('click', function() {
    const num = Number(document.getElementById('sumInput').value);
    if (!isNaN(num)) {
      sumNumbers.push(num);
      document.getElementById('sumInput').value = '';
    }
  });

  document.getElementById('showSum').addEventListener('click', function() {
    const total = sumNumbers.reduce((acc, curr) => acc + curr, 0);
    document.getElementById('sumOutput').innerText = "Sum: " + total;
  });
</script>









<input type="text" id="todoInput" placeholder="New Task">
<button id="addTodo">Add Task</button>
<ul id="todoList"></ul>

<script>
  document.getElementById('addTodo').addEventListener('click', function() {
    const task = document.getElementById('todoInput').value;
    if (task) {
      const li = document.createElement('li');
      li.textContent = task;
      document.getElementById('todoList').appendChild(li);
      document.getElementById('todoInput').value = '';
    }
  });
</script>










<input type="color" id="bgColorPicker">
<button id="changeBg">Change Background</button>

<script>
  document.getElementById('changeBg').addEventListener('click', function() {
    const color = document.getElementById('bgColorPicker').value;
    document.body.style.backgroundColor = color;
  });
</script>









<input type="number" id="num1" placeholder="First number">
<input type="number" id="num2" placeholder="Second number">
<button id="multiply">Multiply</button>
<p id="productOutput"></p>

<script>
  document.getElementById('multiply').addEventListener('click', function() {
    const a = Number(document.getElementById('num1').value);
    const b = Number(document.getElementById('num2').value);
    const product = a * b;
    document.getElementById('productOutput').innerText = "Product: " + product;
  });
</script>





















