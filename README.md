<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/guimarbe/trillo">
    <img src="img/logo.png" alt="Logo" width="153" height="106">
  </a>
</p>

<!-- PROJECT NAME -->
# Trillo
Virtual site of a travel finder company like tripadvisor, skyscanner, booking and more. Mastering Flexbox!

<!-- TABLE OF CONTENTS -->
## Table of Contents
* [About the Project](#about-the-project)
	* [Sass](#sass)
	* [BEM Methodology](#bem-methodology)
	* [Project Structure](#project-structure)
* [Getting Started](#getting-started)
	* [Prerequisites](#prerequisites)
	* [Installing](#installing)
* [Usage](#usage)
* [Built With](#built-with)
* [Authors](#authors)
* [License](#license)
* [Contact](#contact)
* [Acknowlegments](#acknowledgements)


## About the Project
![Screenshot of the project](screenshot.png)

Trillo is a web page example developed by Jonas Schmedtmann in the Udemy course [Advanced CSS and Sass course](https://www.udemy.com/course/advanced-css-and-sass/). I wrote this code to learn the advanced techniques used nowadays to develop modern web pages. Besides, this code will help to develop other webpages as a code reference.

The focusing part of this project is the use of **flexbox**. All the project uses a flexbox layout, so if you are interested to learn how to lay a web page using flexible components, this is perfect for you!

**Notes**
>I've applied some personal changes in this project, so the final result may not be the same as the original code developed by Jonas.

Showing up next, we are going to describe the three pilars of this project: Sass, BEM methodoloy and the project architecture.

### Sass
This project is a great introductions to use Sass code. Its awesome benefits are:
* Using variables, @mixins and @extends to improve the code.
* Nesting the CSS selectors to have a visual hierarchy.
* Using different files for abstracts, components, layouts...
* Preprocessing all the SCSS code and joint in one output CSS file.

### BEM Methodology
In this project, I used the BEM (Block, Element, Modifier) methodology, wich is a component-based approach to web development. The idea behind it is to divide the user interface into independent blocks. This makes interface development easy and fast even with a complex UI, and it allows reuse of existing code without copying and pasting. For exemple:
```html
<!-- HTML code -->
<header class="header">
	<h2 class="header__heading header__heading--medium"></h2>
	<button class="btn btn--white"></button>
</header>
```
```scss
// SCSS Code
.header {
	// We are using nesting here (header__heading)
	&__heading {
		font-size: 45px;
		text-transform: uppercase;
		font-weight: 400;
		line-height: 1.6;

		// More nesting here (header__heading--medium)
		&--medium {
			color: blue;
			font-size: 20px;
		}
	}
}

.btn {
	cursor: pointer;
	border: none;
	border-radius: 50px;
	font-size: 16px;
	text-transform: uppercase;
	background-color: blue;
	color: #fff;

	// This represents btn--white.
	&--white {
		background-color: #fff;
		color: #000;
	}
}
```
As you can see,
- *header* is the **block**.
- *heading* is the **element** of the **block** *header*.
- *medium* and *white* are the **modifiers** of *header__heading* and *btn*, respectively.

This methodology is really useful in web development in general. It allows me to create a visual hierarchy to write the HTML code and it simplifies the code due to the nesting, membership and optionality that allows the BEM approach.

### Project Structure
The project has been developed taking in mind a solid architecture for web development. At first glance, it has a classic folder distribution:
* **css**: fonts, icons and compiled CSS files are located in this folder.
* **img**: background video and images, logos, pictures and favicon are hosted inside this folder.
* **sass**: our Sassy CSS files are here. I'm going to discuss more about this later.
* *index.html*: our webpage. Just HTML code.

But the most important part is the **sass** folder. Inside this, we have all the sassy code divided in multiple files and orderer in common folders to better organize the whole project. The architecture is compound by:

* **abstracts**
	* *_mixins.scss*: all the reusable CSS code is located here.
	* *_variables.scss*: all variables of the project: colors, font-sizes, paddings...
* **base**
	* *_animations.scss*: it hosts *@keyframes*, mainly.
	* *_base.scss*: html, body, root font size and typography are declared here.
* **components**
	* *A lot of components!*: all the components used in this project are located here.
* **layout**
	* *_header.scss*: header code here.
	* *_navigation.scss*: this is the code of the navbar.
* **pages**
	* *_home.scss*: this file is composed by all the <section>'s of the project.
* *main.scss*

Finally, we have the *main.scss*, that it joins all SCSS files in one using the statement *@import*.

In terms of development, is really important taking care of the folder hierarchy and how to order the elements. This kind of architecture is only possible due to the power of Sass. And it improves the workflow a lot!

<!-- GETTING STARTED -->
## Getting Started
To setting up the project locally you can download a copy of this project clicking on the *Clone or download* and then *Download ZIP*, or you can follow these simple example steps to get a copy of Trillo on your repository.

### Prerequisites
First things first, you need to install npm to use all the tools provided in the project.
1. Open the Command Promt (on Windows) or Terminal (iOS) and type:
```
$ npm install npm@latest -g
```

### Installing
2. Clone the repository:
```
$ git clone https://github.com/guimarbe/trillo.git
```

3. Inside package.json there are all the dependendies used in this project. Install all NPM packages in the project folder:
```
$ npm install
```
4. You can open the **Development Process** typing:
```
$ npm start
```
5. That's it! Trillo is running succesfully :smile:


<!-- USAGE -->
## Usage
Feel free to use this code (see more on [license](#license)).
* Watch and interact with the different elements along the webpage.
* With your web browser, you can inspect all the elements to know how was built.
* Toggle the device toolbar to see how it's responsive.

## Built with
This project is plugin free. You don't need nothing to run it!

<!-- CONTRIBUTING -->
## Contributing
Contributions are what make the open source community such an amazing place to learn, inspire and create. Any contributions you make are **greatly appreciated**.

1. Fork the project.
2. Create your Feature Branch: `git checkout -b feature/example-name`.
3. Commit your changes: `git commit -m 'Add some features'`.
4. Push to the Branch: `git push origin feature/example-name`.
5. Open a Pull Request.

<!-- AUTHORS -->
## Authors
* **Guillem Martí**: built and documentation

<!-- LICENCE -->
## License
The license of this project is from [Jonas Schmedtmann](http://codingheroes.io). The code of this project is open source to learn but not for commercial purposes.

<!-- CONTACT -->
## Contact
Guillem Martí - [@guimarbe](https://twitter.com/guimarbe)

<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [atom](https://atom.io/) - My preferred text editor
* [Emmet](https://emmet.io/)
* [Unsplash](https://unsplash.com/)
* [IcoMoon](https://www.icomoon.io/)
* [Can I use?](https://caniuse.com/)
