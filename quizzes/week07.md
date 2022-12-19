# Advanced Front-End Frameworks


**1.** Describe the two ways to bind Data in Vue?
<!-- enter you answer in the space below -->
```
The v-model directive makes two-way binding between a form input and app state very easy to implement. One can bind a form input element and make it change the Vue data property when the content of the field changes.

```

**2.** The `SPA` acronym stands for what?
<!-- enter you answer in the space below -->
```
Single
Page
Application

You kind of have one Home Page, and mix out different models and components; rather than fully navigating to a bunch of different pages.
```
**3.** What are some of the advantages/uses of a `SPA` over a traditional one?
<!-- enter you answer in the space below -->
```
They're more efficient in processing. They cost less. And it takes less time from developers, because we can reuse components and such.
```
**4.** What does the `onMounted` method in Vue do?
<!-- enter you answer in the space below -->
```
onMounted makes functions run or activate when a component is mounted. So for instance, when you first load a page, the components on that page that require onMounted will run. Or if a new component is activated and drawn to the page, it's onMounted actions will occur.
```
**5.** What is the `v-model` attribute in Vue for, and when might you use it?
<!-- enter you answer in the space below -->
```
A v-model binds an input value (from a form for instance) to data saved and accessed within the AppState and/or database. You might use it in a comment box for a review or social site, or a form to fill out a user profile. Or search bar.
```
**6.** The `v:on` (`@`) directive can be used for what?
<!-- enter you answer in the space below -->
```
The @ or 'v:on' directive is an event listener on an element. For instance, it can be used to stop, prevent, and capture something. You might use it to direct navigation to a new page on a click. Or filter content via button. Or prevent a page from reloading on a form submit.
```
**7.** Which Vue attributes(directives) could you use to conditionally render elements on a page?
<!-- enter you answer in the space below -->
```
v-show to show something only if
v-if to do something only if
v-else-if    if it's not v-if
v-else to do something if the v-if isn't fulfilled

```
**8.** What is the purpose of the `key` attribute when using `v-for` on an element?
<!-- enter you answer in the space below -->

```
The key attribute tells you what a letter stands for in a template; from a parent to a child component.
It tells you that 't' is for telephoneNumber.

```
**9.** What is the `<slot>` element and what is it used for?
<!-- enter you answer in the space below -->
```
<slot> is used to switch components out of a model.
A better way to put it, is it is a placeholder. 
You can set up a component and within that leave a <slot> and the inject other component markups inside of it. It helps you reuse code, and keep a thing uniform.

```