## About

This is a codebase that will allow energy.gov users to quickly get started developing new graphics and maps. By cloning this repo, you can immidiately begin coding. 

If you're working with [Foundation](http://foundation.zurb.com/) responsive framework, pull down [the App_Frame_Foundation repository](https://github.com/energyapps/app-frame-foundation). Note: Its a big work in progress, and a lot of the CSS will interfere with energy.gov's default css. So don't use it right now.

## Dependencies
- Git (obviously)
- Download and install [Jekyll](http://jekyllrb.com/)

## Setup

- Clone the repo:

`git clone https://github.com/energyapps/app_frame.git`

- Rename the folder to your project name

`mv app_frame/ new_directory_name/`

- On the [EnergyApps Github group](https://github.com/energyapps) create and name a new project repo.
- cd into that folder in terminal and change remote URL to new repo:

`git remote -v` List all remote urls

`git remote set-url origin https://github.com/energyapps/NEW-REPO-NAME.git` -changes the remote url to your new URL

- Push to this new repo

`git push -u origin master`

- Branch out the gh-pages branch

`git branch gh-pages`
`git checkout gh-pages`
`git push origin gh-pages`

- Begin work in the `index.html` file.
- Build the Jekyll `_site/` folder by running `jekyll build` in your directory. I recommend running `jekyll build --watch`, which automatically rebuilds your `_site` folder whenever you change something in the directory.
- Run the jekyll server by running `jekyll serve`. You can now see your page at [](http://localhost:4000/)
- Push changes to github, see website running remotely at energyapps.github.io/NEW-REPO-NAME/index.html
- Recommended: Update Readme to reflect your current project.

## Contents

1. 	root directory
	* README.md 
		- You are here.
	* index.html 
		- Merges in the markup from the post (see below) and contains the styles from the energy.gov/maps section.
	* article.html
		- Merges in the markup from the post (see below) and contains the styles from the energy.gov/articles section.
2.	_posts/
	* Contains the markup that you are creating. This goes beneath header info. It will be merged into the index and article above.
3.	_layout/
	* The _layouts/ folder is the Jekyll folder that contains layouts for any type of page within a jekyll site. 
	* default.html
		- This is a very rough cannibalization of the DOM elements in energy.gov/maps element.
		- Markup, CSS, and JS are merged here automatically by Jekyll
		- Contains links to JS, CSS in other folders (see below), as well as links to external energy.gov css files.
4.	_site/
	* This is the folder that is generated by Jekyll and holds the merged static webpages.
5. js/
	* data.js
		- Data for the map in json objects. This would be added to the maps content type.
	* script.js
		- script that executes all commands on graphic. This would be added to the maps content type.
6. css/
	* style.css
		- custom css to be added to map. CSS that would be added to the maps content type.
	* master_style.css
		- A static copy of the above as a fallback when the energy.gov links break.
	* fonts.css
		- a collection of some commonly used energy.gov fonts

## Needs/Ideal Work flow

	- You will create your content in index.html, data.js, script.js, and style.css.
	- These files will then be merged into the default.html using Jekyll pages.
	- When you create your map on cms.doe.gov or stage.cms.doe.gov you will have to copy your js, css, and html over. Or, if you use the upload option, you will have to make sure that your index.html has the jekyll code removed.
	
## Notes

Public Domain
