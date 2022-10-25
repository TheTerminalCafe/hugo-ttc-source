# Welcome to The Terminal Café !

This repository contains the source code of the ttc website, how we add stuff in it, technologies used and rules for contribution. 

# Technologies used
While making our website we are leveraging the Hugo framework to generate static webpages and Bootstrap 5 to create the template websites along side that we have also included mermaid for markdown interpretation.
|       Name     |           Link                                 |       Version               |
|----------------|------------------------------------------------|-----------------------------|
|Hugo			 |[Hugo](http://gohugo.io/)                       |v0.93.3+extended             |
|Bootstrap 5     |[Bootstrap](https://getbootstrap.com/)          |v5.0.2                       |
|Mermaid         |[Mermaid](https://mermaid-js.github.io/mermaid/)|v8.8.0                       |

 
## What is TTC website ?

TTC short for The Terminal Cafe is a welcoming discord server for everything related to technology with other fun things sprinkled on top of it. We started on 2019 as CTT and quickly became a melting-pot for tech minded from people all around the world later we rebranded our self as The Terminal Cafe. The website is just another attempt from us to make technology more accessible to everyone anywhere around the world .

### How pages are generated ??

All files and folders are presented as a tree in the project. We have created some predefined templates which gets used while generating the webpages. First the user uploads the folder containing a markdown file with the content , a thumbnail icon and an article banner. If it gets accepted after our internal review we pull that folder in our main source and that page becomes a part of our website.

# Contributions 

Yes, anyone can contribute to this project be it via code or via articles just fork this project , make changes in your repo and create a PR, if approved it will become the part of the website. Please make sure you don't add any personal information or closed source code into the project to avoid legal troubles.

Please join our server and contact the admin team for more information.

## Adding Code to the repository 

So you want to contribute code to the project !! that's wonderful. Create a repo under your profile make changes and create a pull request detailing what you have changed inside it. Once its accepted it will get added to next build of the website 

### Formatting
While contributing to the code please follow the general naming convention of [Hugo](https://github.com/spech66/hugo-best-practices) and standard web practices.
Additionally we require the contributors to add  comments in the code for rest of the team. One example given below
```
<div  class="container my-2">
	<!-- Carousel for the homepage -->
	<!-- 3 pages with diffrent topics will be placed here -->
	<div  id="carouselExampleCaptions"  class="carousel slide"  data-bs-ride="carousel">
		<div  class="carousel-indicators">
		<button  type="button"  data-bs-target="#carouselExampleCaptions"  data-bs-slide-to="0"  class="active"
			aria-current="true"  aria-label="Slide 1"></button>
		<button  type="button"  data-bs-target="#carouselExampleCaptions"  data-bs-slide-to="1"
			aria-label="Slide 2"></button>
		<button  type="button"  data-bs-target="#carouselExampleCaptions"  data-bs-slide-to="2"
			aria-label="Slide 3"></button>
	</div>
	<!-- Carousel End -->
</div>
```
Similarly while submitting a pull request kindly elaborate what you are contributing ( feature or bug ) and then submit it. 

![prsample](https://cdn.discordapp.com/attachments/608335535915663370/1034045466851168306/unknown.png "PR Sample")

## Adding articles to the repository 

You can add articles to the website just like how we add code to the project but in-case of articles you need to add bit more things and you have to follow the predefined format. (_read Formatting_)

Our website is divided in  4 categories 
1. News articles
2. Coding Tutorials
3. Non tech stuff 
4. Admin pages

We use tags and paths to determine how the page will be placed.If you want to add an article after creating your own fork, create a folder in the category you want to create an article for with the naming conversion `[yourpostwithourspaces]` , inside that folder create a markdown file which will hold the main content and metadata for that particular article. While creating the file follow the naming conversion

Congratulations you have created the blank article now you will have to add 2 images for the same. One a thumbnail and two a banner , add both of them in the same folder as the markdown file. These file should also follow the standard naming convention 
##### Naming Convention
1. Folder name --> `[yourpostwithourspaces-yyyymmdd]`.
2. Markdown file --> `[yourpostwithourspaces-yyyymmdd.md]`.
3. Icon --> `[yourpostwithourspaces-icn-yyyymmdd.md]`.
4. Banner --> `[yourpostwithourspaces-banner-yyyymmdd.md]`.

After you are done now write your article and verify for any mistakes. When you are done create a PR we will verify the request and if its ok we will add that to our repo. Please contact the admin team for more info or any questions.

Example file structure 
```
root
	|__content
	| |__news
	|	|__ pos-20221101
	|		|__ pos-20221101.md
	|		|__ pos-icn-20221101.md
	|		|__ pos-banner-20221101.md
	|__ Other files [DO NOT MODIFY]		
```
### Formatting
When you are adding any new article we need some meta data based on that we will create the site. Below are the flags that you can to add in your file. 

**1. title:**
As the name suggest this is the title of your post. Using this is mandatory
Usage: `title: "Demo Name"` 

**2. date:**
This tag handles the date this is actually the publish date, based on it we will place it on the website lists. Use the current date as the value here. Using this is mandatory
 Usage: `date: 2021-09-03T17:27:59`
 
**3. author:**
Author tag is responsible for denoting who wrote this article. Please write the exact author name that you have been given from the admin team as this is case sensitive and your user icon depends on this value. Using this is mandatory
  Usage: `author: Nyn`
  
**4. tags:**
 Tags allows us to categories the based on specific types. You can put more than one value here as with [].  Using this is not mandatory but highly recommended. 
  Usage: `tags: [gaming,cloud,news]`
  
**5. featured:**
This handles if a post is featured in the front page. ***DO NOT TOUCH THIS VALUE***. This will be assigned by the admin team who will review your article.
	Usage: `featured: "true"`
	
**6. type:**
Type tells the website what kind of website it is. While creating a normal webpage use the value `posts` so that it can be indexed properly.Using this is mandatory
	Usage: `type: "posts"`
	
**7.thumbnail:**
As you can see this value suggests what will be the thumbnail or icon for your post. Thumbnails should be placed on the same folder and same level as the main markdown file and should follow the naming convention. To use your thumbnail paste the relative path so that we can pick and place in the website. Using this is mandatory
	Usage: `thumbnail: /news/pos-20221101/pos-icn-20221101.png`
	
**8.articleImage:**
 Just like the last one articleImage or banner states the image that we will use as your article's banner. ArticleImage should be placed on the same folder and same level as the main markdown file and should follow the naming convention. To use your articleImage paste the relative path so that we can pick and place in the website. Using this is mandatory
  Usage: ``articleImage: /news/pos-20221101/pos-banner-20221101.png``

**9.draft:**
 Draft tag makes the post draft means this will not show the page anywhere default value is true. If you want to post but dont show them make it true.
  Usage: ``draft: "true"``

  
 **Example**
 ```
 ---
title: "I am a demo"
date: 2022-09-03T17:27:59
author: Nyn
tags: [demo,code,news]
featured: "false"
type: "posts"
thumbnail: /news/pos-20221101/pos-icn-20221001.png
articleImage: /news/pos-20221101/pos-banner-20221001.png

---
```

**_Note: Always use three dashes `---` before and after putting your mata data in the markdown file_**

After the meta data and 3 dashes `---` you can write your article as standard markdown document.
 
# Copying

Our project is licensed under GPL license so its completely opensource and free to use . If you ended up using our project don't forget to credit us along side the original repository link. Please don't use the same name as it will make further complications.

# How to Run

To run this project you must have hugo installed in your system. Please refer to your OS instructions on how to install hugo. 

**Example**
```
#Fedora linux#
sudo dnf install hugo
```

After Hugo is isntalled download the repo go inside the folder and run `hugo serve` to see the webpage. By default hugo will start it on port 1313 so the page will be on `http://localhost:1313/`.Read the terminal output for more info. Press CTRL and C to kill the server and exit.

```
git clone https://github.com/TheTerminalCafe/hugo-ttc-source.git
cd hugo-ttc-source
hugo serve
```

# Current Contributers

|       Name     |           Link                                 |
|----------------|------------------------------------------------|
|Ereshkigal		 |[Profile](https://github.com/Ereshkigal01)      |


<center>
	<h3>
		Made with Code and 💛
	</h3>
</center>

