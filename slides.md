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

- repo of where we left off: https://github.com/avcoder/test-react
   - separate what we've done into its own `Lesson01.tsx` component
   - create `Lesson02.tsx` 
   - `npm i tachyons`
   - `import 'tachyons' in `Lesson02.tsx`
   - `declare module "tachyons";` in `vite-env.d.ts`
   - take tachyons html list of people and transform it into JSX
```jsx
      <div style={{ backgroundColor: "#fff", width: "90vw", height: "90vh" }}>
        <main className="pt6 mw6 center">
          {data.map((person) => (
            <FollowPerson
              key={person.username}
              avatar={person.avatar}
              name={person.name}
              username={person.username}
              isFollowing={person.isFollowing}
            />
          ))}
        </main>
      </div>
```



---
transition: slide-left
---

# Exercise: Use React DevTools to find component
10 mins

- Install React DevTools for your browser and explore it (should be similar to Vue DevTools)
- Goto: instagram.com
   - Try to find the React component for the Login button
   - why do the React components look weird/minified? (prod vs development)
   - Try to change a value of a prop in any component to see what might happen
- View your local App.tsx again in the browser
  - Just like you right-click inspect DOM element to find that particular HTML element in the DOM, you can do similar with React components
  - try changing prop values (like `label`)
  - Tip: in Chrome devtools, can use `Cmd + p` to find React filename

---
transition: slide-left
---

# useState

- re-examine the Counter button app we made in week 1
- whenever we need to keep track of dynamic values, we need to use some form of React state
- to create a state variable: `useState` function
   - this function takes a single argument: the initial value or a function
   - returns an array containing: current state, updater function
- useState is a "hook" - a special type of function that allows us to hook into React internals
- naming conventions
- by calling `setCount` the UI gets updated 
- whenever a state variable is updated, it triggers a re-render; React will call the Counter function again, creating a brand new React element
- each render is like taking a snapshot

---
transition: slide-left
---

# Exercises

1. Use `useState` to toggle a boolean value
   - ex: make the `+ Follow` button change to `- Following`
   - see https://unit06-lesson02.netlify.app/6
1. Use useState with multiple values in an array
   - ex: when button is clicked, display one more user from array
   - see https://unit06-lesson02.netlify.app/8

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

# Exercise: Lifting State Up
Parent-Child communication means having a parent component manage the state, and pass down state setters as props

- see https://unit06-lesson02.netlify.app/4
- Identify where state needs to located, and where state needs to be lifted up

---
transition: slide-left
---

# Optional: Configure imports to use absolute path

- Use ChatGPT to help you configure your tsconfig.json, tsconfig.app.json, vite.config.ts
- ❌ BEFORE: Using relative paths can be a pain point, especially when refactoring locations of files/folders
- ✅ AFTER: should now be able to use `import Component from '@/components/whatever' 




---
transition: slide-left
---

# Homework

- Finish converting to JSX [Email template layout](https://pure-css.github.io/layouts/email/) to JSX; [Github code here](https://github.com/pure-css/pure/tree/main/site/static/layouts/email)
- Begin thinking about your "Weather Forecasting App" assignment due Aug 17 midnight EST
