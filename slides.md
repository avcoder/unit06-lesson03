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

- [ ] Props
- [ ] useState
- [ ] Covering gotchas

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
transition: slide-left
---

# Common Gotchas
Try the following common errors to see what errors look like in React.  Find solutions for each.

- Forgetting to `return` JSX
- Confusing camelCase for HTML attributes `onclick vs onClick`
- Using `class` instead of `className`
- if using inline styles, using hyphenated names instead of camelCase 
  - ex: `background-color vs backgroundColor`
- Multiple top-level elements without a wrapper/fragment
- DON'T use if statements directly inside JSX like `return ( if (isLoggedIn) { <p>Welcome</p> });`
- Not using `key` in lists
- JSX requires properly closed tags, even for void elements. ex: `<input /> <br />`
- what happens if props are undefined? ex: `return (<div className={someUndefinedClass}>Hi</div>)`
- if `numOfItems` is 0, this will render 0 `{numOfItems && <ShoppingList items={shoppingList} />}`
- examine if there are any more red squiggly lines in VSCode? 


---
transition: slide-left
---

# Optional: Configure imports to use absolute path

- Use ChatGPT to help you configure your tsconfig.json, tsconfig.app.json, vite.config.ts
- ❌ BEFORE: Using relative paths can be a pain point, especially when refactoring locations of files/folders
- ✅ AFTER: should now be able to use `import Component from '@/components/whatever' 


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

# Homework

- Finish converting to JSX [Email template layout](https://pure-css.github.io/layouts/email/) to JSX; [Github code here](https://github.com/pure-css/pure/tree/main/site/static/layouts/email)
- Begin thinking about your "Weather Forecasting App" assignment due Aug 17 midnight EST
