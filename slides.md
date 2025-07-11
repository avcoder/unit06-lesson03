---
# You can also start simply with 'default'
theme: default
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: /assets/intro.jpg
# some information about your slides (markdown enabled)
title: Software Development | Foundations
info: |
  ## Software Development | Foundations
# apply unocss classes to the current slide
class: text-left
drawings:
  persist: false
transition: slide-left
mdc: true
---

# React: useState 
Frontend Development: Unit 06 - Lesson 03

- [ ] useState
- [ ] 
- [ ] 

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
-->

---
transition: slide-left
---

# Recap

- reminder: Algorithm and Data Structure Assignment due Jul. 20 
- repo of where we left off: https://github.com/avcoder/test-react


---
layout: image-right
transition: slide-left
image: /assets/dodds.png
backgroundSize: 400px 270px
class: text-left
---

# 10 minute break

🍦 Cool Tips, Trends and Resources:

- ⌨️ [React Cheat Sheet](https://zerotomastery.io/cheatsheets/react-cheat-sheet/)
- 🧊 [Importing React Through the Ages](https://www.epicreact.dev/importing-react-through-the-ages)
- ⋈ [Should I useState or useReducer](https://kentcdodds.com/blog/should-i-usestate-or-usereducer)



<br>
<hr>
<br>

- 🧪 [Enter anonymous lab questions](https://docs.google.com/forms/d/e/1FAIpQLSevvGARdHQikso-uLqFCO481MABKE5HofuSrlzEPMNQ2ZLykw/viewform?usp=dialog)
- ℹ️ [Course feedback survey](https://circuitstream.typeform.com/to/ZoyYk7px#course_id=SoftwareAN&instructor=9514)

---
transition: slide-left
---

# Conditionals

- in JSX, with the curly braces, we can't use JS statements, only expressions
  - why do you think we can't use JS statements?  (think what is being passed to `React.createElement()`? )
- use of `&&` 
  - ex: `{ isOnline && <div className="green" /> }`
  - why does the above work?  what's happening?
  - ex: `{ numOfItems > 0 && <ShoppingList items={shoppingList} /> }`
  - ex: `{ !!numOfItems && <ShoppingList items={shoppingList} /> }`
- use of ternary operators
  ```jsx
  return (
    <>
      { isLoggedIn ? <AdminDashboard /> : <p>Please login first</p> }
    </>
  )
  ```

---
transition: slide-left
---

# Exercise: Use conditional for a prop
5 mins. Continuing with your first iteration of this component from an earlier slide...

- Modify your `<Button />` component such that if it is given the `disabled` prop, it will actually make the button disabled
   - reminder: can disable an HTML button tag via `<button disabled>Submit</button>`
`<Button label="Submit" disabled />`

---
transition: slide-left
---

# Exercise: Use conditional for text
5 mins. Continuing with your first iteration of this component from an earlier slide...

<img src="/assets/inbox.png" style="width: 400px" />

- make it so that if variable `isFollowing` is true, then the button text will say `- Following`
   - otherwise if `isFollowing`is false, then button text will say `+ Follow`


---
transition: slide-left
---

# Exercise: Create simple React website
remainder of time.  Choose one appropriate to your comfort level so far with React

Level 1
- Convert your first HTML/CSS assignment back from Unit 1 into React/JSX

Level 2
- Convert this entire [Email template layout](https://pure-css.github.io/layouts/email/) to React/JSX; [Github code here](https://github.com/pure-css/pure/tree/main/site/static/layouts/email)
- We will use this later to keep learning about React

Level 3
- Conver this entire [Dashboard](https://assets.justinmind.com/wp-content/uploads/2020/02/dashboard-design-example-hcare.png) to React/JSX

---
transition: slide-left
---

# Homework

- Finish converting to JSX [Email template layout](https://pure-css.github.io/layouts/email/) to JSX; [Github code here](https://github.com/pure-css/pure/tree/main/site/static/layouts/email)
- Begin thinking about your "Weather Forecasting App" assignment due Aug 17 midnight EST