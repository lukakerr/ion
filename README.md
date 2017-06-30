# Mos 
###### (mac operating system)

A lightweight (11kb minified, 13kb un-minified) CSS framework that brings MacOS styled elements to Electron.

### About

Mos was developed with the aim of bringing native MacOS elements and components, such as buttons, sidebars, search inputs, tables, icons, and toolbars, to HTML and CSS. 

Mos is designed to be used specifically within an [Electron](https://github.com/electron/electron) application, but can be used just fine in a normal HTML page.

### Getting Started

- Run `git clone https://github.com/LukaKerr/mos.git` to get the source code


### Folder Structure

```
mos/
├── README.md
├── index.html
├── css/
│   ├── mos.css
│   └── mos.min.css
├── fonts/
│   └── mos.ttf
└── img/
    ├── search.png
    └── sidebar/
        └── ...png
```

### Screenshot

<div style="text-align:center">
	<img src ="https://i.imgur.com/tUBrODR.png" alt="mos">
</div>

### Documentation

#### Title Bar

A title bar can either be normal or tall. Remove the `tall` class below to get a normal title bar. The title bar is used to drag the application.

Inside the `bar` div, there are 4 other main elements:

- The `buttons` div which is the red, yellow and green buttons in every application
- The `title` div, which is just the title of your application shown in the title bar
- The `bar-buttons` div, which lets you add as many buttons as you want to the title bar. These buttons must have the `btn` class, as well as another class to show an icon. Note: the `left-open-big` and `right-open-big` are meant to go next to each other, as back and forward buttons
- The `search` element, which is simply a search input

The `bar-buttons` div also has `active` and `disabled` classes which make a button active or disabled.

```
<div class="bar tall">
	<div class="buttons">
		<button></button>
		<button></button>
		<button></button>
	</div>
	<div class="title">mos</div>

	<div class="bar-buttons">
		<button class="btn left-open-big"></button>
		<button class="btn right-open-big"></button>
		<button class="btn cog"></button>
		<button class="btn folder disabled"></button>
		<button class="btn info"></button>
		<button class="btn space"></button>
		<button class="btn reply active"></button>
		<button class="btn download"></button>
		<button class="btn login"></button>
		<button class="btn home"></button>
	</div>

	<input class="search" placeholder="Search">
</div>
```

#### Sidebar

The `sidebar` div gets shown on the left side of the window. This is used to display a list of elements, similar to the Finder

A `heading` div will put a heading above a bunch of items

Each `item` div inside the `items` div, must have the class `item`, as well as another class that determines what icon is shown next to it. Below are all the possible items you can use (this includes coloured tags)

```
<div class="sidebar">
	<div class="heading">
		Favourites
	</div>
	<div class="items">
		<div class="item allmyfiles">
			All My Files
		</div>
		<div class="item icloud">
			iCloud Drive
		</div>
		<div class="item airdrop">
			AirDrop
		</div>
		<div class="item applications">
			Applications
		</div>
		<div class="item desktop">
			Desktop
		</div>
		<div class="item documents">
			Documents
		</div>
		<div class="item downloads">
			Downloads
		</div>
		<div class="item movies">
			Movies
		</div>
		<div class="item music">
			Music
		</div>
		<div class="item pictures">
			Pictures
		</div>
		<div class="item home">
			Luka
		</div>
		<div class="item laptop">
			Luka
		</div>
	</div>
	
	<div class="heading">
		Files
	</div>
	<div class="items">
		<div class="item folder">
			Folder
		</div>
		<div class="item file">
			File
		</div>
	</div>

	<div class="heading">
		Tags
	</div>
	<div class="items">
		<div class="item red">
			Red
		</div>
		<div class="item orange">
			Orange
		</div>
		<div class="item yellow">
			Yellow
		</div>
		<div class="item green">
			Green
		</div>
		<div class="item blue">
			Blue
		</div>
		<div class="item purple">
			Purple
		</div>
		<div class="item gray">
			Gray
		</div>
	</div>
</div>
```

#### Table

A table can be displayed by using the HTML `table` element with the class `table`. If you want each row to have alternating background colours, add the `alt` class as shown below

```
<table class="table alt">
	<tr>
		<th>Name</th>
		<th>Date Modified</th>
		<th>Size</th>
		<th>Kind</th>
	</tr>
	<tr>
		<td>mos.css</td>
		<td>Today 3:33 pm</td>
		<td>100 KB</td>
		<td>CSS</td>
	</tr>
	<tr class="disabled">
		<td>Controllers</td>
		<td>8 April 2017, 8:45 am</td>
		<td>--</td>
		<td>Folder</td>
	</tr>
	<tr class="active">
		<td>Holiday.png</td>
		<td>23 June 2017, 6:50 pm</td>
		<td>2 GB</td>
		<td>PNG Image</td>
	</tr>
	<tr>
		<td>user.rb</td>
		<td>Today 1:44 pm</td>
		<td>5.1 MB</td>
		<td>Ruby Source</td>
	</tr>
</table>
```