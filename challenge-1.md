# Introduction to DOM - Exercises

1. Answer the following questions:

   - How would you select from JavaScript an element `p` that has the class `text` and also the class `important`?
   **const element = document.querySelector("p.text.important");**

   - How would you select from JavaScript a `button` element with class `button` and that is disabled?
   **const buttonElement = document.querySelector("button.button[disabled]");**

   - How would you select from JavaScript all the `li` elements that are direct children of an `ul` element 3 with class `list`?
   **const ulElement = document.querySelector('ul.list > li');**

   - How would you select from JavaScript all the `input` elements that are descendants of a `form` element with class `form-new-item`, and that have a `type` attribute with a value `text`?

   **const formElement = document.querySelector('form.form-new-item');**
   **const textInputElements = formElement.querySelectorAll('input[type="text"]');**



2. From the following HTML structure, create a script that selects the header "The MEAN stack". Next, change the text to "The MERN stack" and remove the "subtitle" class.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Modificar Texto y Clase</title>
</head>
<body>
    <main class="main-content">
        <h1 class="app-title">Bootcamp technologies</h1>
        <section class="info">
            <h2 class="subtitle">The MEAN stack</h2>
            <p class="text">
                The MEAN stack is the set of technologies used in the bootcamp by
                FullStack Web Development.
            </p>
        </section>
    </main>
    <script>
        const subtitleElement = document.querySelector('.subtitle');
        if (subtitleElement) {
            subtitleElement.textContent = 'The MERN stack';
            subtitleElement.classList.remove('subtitle');
        }
    </script>
</body>
</html>


3. Here you have an HTML without data:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fill Student Information</title>
</head>
<body>
    <article class="student">
        <h2 class="student-name"></h2>
        <span class="student-age"></span> years
        <img class="student-photo" src="" alt="" />
    </article>
    <script>
        const studentData = {
            name: "Arnau Gallego",
            age: 19,
            photoUrl: "https://escolapiamataro.com/fp/daw2/arnau-gallego.jpg"
        };
        const name = document.querySelector('.student-name');
        const age = document.querySelector('.student-age');
        const photo = document.querySelector('.student-photo');
        if (name) {
            name.textContent = studentData.name;
        }
        if (age) {
            age.textContent = studentData.age;
        }
        if (photo) {
            photo.src = studentData.photoUrl;
            photo.alt = " foto de " + studentData.name;
        }
    </script>
</body>
</html>

Create a script where you declare a variable with a student's data
(name, age and photo URL). Next, get the elements from the HTML
and fill them in with the student's information.
