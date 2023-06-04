---
{"dg-publish":true,"dg-home":true,"permalink":"/react-tutorial/react-quick-start/","tags":["gardenEntry"],"dgPassFrontmatter":true,"noteIcon":""}
---

# Overview
This page is the notes from [This Tutorial](https://react.dev/learn#)
- [[React Tutorial/React Quick Start#Creating and Nesting Components\|#Creating and Nesting Components]]
- [[React Tutorial/React Quick Start#Adding Markup and Styles\|#Adding Markup and Styles]]
- [[React Tutorial/React Quick Start#Displaying Data\|#Displaying Data]]
- [[React Tutorial/React Quick Start#Rendering Conditions and Lists\|#Rendering Conditions and Lists]]
- [[React Tutorial/React Quick Start#Responding to Events and Updating the Screen\|#Responding to Events and Updating the Screen]]
- [[React Tutorial/React Quick Start#Sharing Data Between Components\|#Sharing Data Between Components]]

# Creating and Nesting Components
- React Apps are made out of **Components**
	- components are a piece of UI that has it's own logic and appearance
	- A Component small like buttons or large like entire pages.
- Components are a JS function that return markup:
```jsx
function MyButton() {
	return {
		<button>I'm a button</button>
	};
}
```
- Once an Component has been ***Declared***, it can be nested into another component:
```jsx
export default function MyApp() {
	return (
		<div>
			<h1> Welcome to my App </h1>
			<MyButton />
		</div>
	)
}
```
---
 >==**Note:**==
 >	React components always begin with a capital letter, while HTML tags must be lowercase.
 >	`<MyButton /> ` ====> React
 >	`<div></div>` =====> html
---
- See below for an example of the component in action.
	- The export default keyword specify the main component in the file.
	- For more info on JavaScript syntax go to: [MDN](https://developer.mozilla.org/en-US/docs/web/javascript/reference/statements/export) or [javascript.info](https://javascript.info/import-export)
![React Quick Start First Example.png](/img/user/React%20Tutorial/Attachments/React%20Quick%20Start%20First%20Example.png)


# Adding Markup and Styles

## Writing Markup with JSX
- The Syntax seen above is called ***JSX*** which is a syntax extension to JavaScript.
	- It's Optional, but most React Projects use JSX for its convenience. 
	- JSX is Stricter than HTML.
		- All Tags **MUST** be closed like `<br />`
		- Components **CANNOT** return multiple JSX tags.
		- If Multiple Tags will be returned you must wrap them in a shared parent, like a `<div>...</div>` or empty an `<>...</>` wrapper. **See Example Below:**
```JSX
function AboutPage(){
	return(
		<>
			<h1>About</h1>
			<p>Hello there.<br />How do you do?</p>
		</>
	)
}
```

## Adding Styles
- Adding Classes in React can be done using a `className` attribute on the component.
	- This operates the way the HTML `class` attribute works.
	- Standard CSS can be then be used to target the class as normal.
```JSX
<img className="avatar" />
<style>
.avatar {
	border-radius: 50%;
}
</style>
```


# Displaying Data
- JSX lets you put Markup into JavaScript
- Using Curly Braces you can "Escape Back" to JavaScript to use JS data and variables from code.
```JSX
return ( 
	<h1> 
		{user.name} 
	</h1> 
)
```
- "Escape into JavaScript" also works for JSX attributes.
	- You have to use curly braces *instead* of quotes:
```JSX
return (
	<img className="avatar" src={user.imageURL}
	/>
)
```
- Below is an example of Displaying Data:

![React Quick Start Profile Output.png](/img/user/React%20Tutorial/Attachments/React%20Quick%20Start%20Profile%20Output.png)

---
 >==**Note:**==
>	The `style = { {} } ` is not a special syntax, it just a regular JS {} object inside of a JSX `{}`.
>	Using the style attribute allows JS Variables to define styles.
---


# Rendering Conditions and Lists
## Conditional Rendering
# Responding to Events and Updating the Screen
# Sharing Data Between Components

Tags:
#React_Tutorial