# Edrys LiaScript Module

This module allows you to add interactive content and guides to an Edrys class. This includes galleries, audio, quizzes, surveys, code runners, and more. It is based on LiaScript, which allows you to specify all this functionality in simple plaintext, shared over course URLs.

## Usage

Simply use this URL to add the module to your class:

```
https://edrys-labs.github.io/module-liascript/
```

You must specify the following __General settings__. The `course` URL must be a raw LiaScript course URL, and the `content` can be used to specify the course content manually. If you specify the `course` URL, the content will be loaded from and content gets ignored.

```` yaml
classroom: false # disable or enable classroom synchronization
course: https://to your raw LiaScript course URL
# define the course content manually
content: |-
  <!--
  link:     https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.css
  script:   https://cdn.jsdelivr.net/chartist.js/latest/chartist.min.js 
  -->

  # Foo bar

  A drawing example, for demonstrating that any JavaScript library can be used,
  also for drawing.

  ```javascript
  // Initialize a Line chart in the container with the ID chart1
  new Chartist.Line('#chart1', {
    labels: [1, 2, 3, 4],
    series: [[100, 120, 180, 200]]
  });

  // Initialize a Line chart in the container with the ID chart2 new
  Chartist.Bar('#chart2', {
    labels: [1, 2, 3, 4],
    series: [[5, 2, 8, 3]]
  });
  ```
  <script>@input</script>

  <div class="ct-chart ct-golden-section" id="chart1"></div>
  <div class="ct-chart ct-golden-section" id="chart2"></div>
````

The `classroom` is optional, by default it is set to true and in the lobby there is also now classroom synchronization.
