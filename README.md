# Hi there, I'm Aniket! 👋

<p id="typing-animation"></p>

<script>
const texts = [
  "I'm a front-end developer.",
  "Future full-stack developer.",
  "2+ years of learning coding."
];

let count = 0;
let index = 0;
let currentText = '';
let letter = '';
let direction = true;

(function type() {
  if (count === texts.length) {
    count = 0;
  }
  currentText = texts[count];

  if (direction) {
    letter = currentText.slice(0, ++index);
  } else {
    letter = currentText.slice(0, --index);
  }

  document.getElementById('typing-animation').innerHTML = letter;

  if (letter.length === currentText.length) {
    direction = false;
    setTimeout(type, 1000);
  } else if (index === 0) {
    direction = true;
    count++;
    setTimeout(type, 100);
  } else {
    setTimeout(type, 100);
  }
}());
</script>
