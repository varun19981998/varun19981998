# varunprofile
A passionate full-stack  developer from India
<div id="header" align="center">
  <img src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" width="100"/>
</div>

If you visit my profile on GitHub, you’ll notice that it contains images, social network links, some GitHub statistics and links to my blogs, which makes the GitHub profile stand out. This is possible through the GitHub profile README feature. In this article, we’ll learn how to create a GitHub profile README.

We’ll cover the following:

what a GitHub profile README is
how to create a GitHub profile README
adding social badges, skills and descriptions about oneself
adding GitHub stats
creating a GitHub workflow to pull latest published blogs
To follow along with the tutorial, you’ll need to have a basic understanding of HTML and Markdown. If you’d like an introduction to Markdown, check out this Markdown introduction. Also, you should have a GitHub account. If you don’t have one yet, sign up at GitHub.

The code for this tutorial is available on GitHub.
What a GitHub Profile README Actually Is
A GitHub profile README is a feature of GitHub that allows users to use a Markdown file named README to write details about themselves such as their skills, interests, GitHub stats and showcase it to the GitHub community. It’s shown at the top of your GitHub home page, above the pinned repositories. This is a fancy way to showcase one’s skills and stats on GitHub.

Pictured below is the final look of the GitHub profile that we’ll create for this article.

GitHub profile readme GIF
We’ll divide this into multiple sections and add contents for each section incrementally. The background color will change based on the GitHub theme settings of the user.

In the next section, we’ll look at the steps for creating the README file.

Creating a GitHub Profile README
The README file resides in a GitHub repository, the name of which is the same as the username of your GitHub account. To create the repository, follow these steps:

Log in to GitHub.
Click on + icon at top right of the page and select New Repository.
GitHub Create Repository
A Create a new repository page opens. In the Repository name field, enter the username of your GitHub account. After entering the username, GitHub displays a message describing that you’re about to create a GitHub special repository.
Repository name input field
Check the Public checkbox under repository type to make the GitHub profile README visible to everyone who visits the GitHub profile page. If you don’t want users to see your GitHub profile README while it’s still in development, you can choose Private. Once you’re done with the complete development of your README, make sure to change the visibility to Public.
Check the Add a README file checkbox. This will add a README.md file where we’ll add the profile contents. The field values should look similar to thepicture below.
Create repository form fields
Click on the Create repository button. A special repository is created successfully. Go to the repository you just created and you’ll see a README.md file added to the repository.
Special repository created
In the next few sections, we’ll add contents to our README.md file. We’ll use GitHub’s file editor to write and preview the changes. You can use any other text editor you’re comfortable with.

To use the GitHub file editor, open README.md and click on the Edit this file icon (a pencil icon) on the top right of the page. You can read more about editing GitHub files at the official GitHub documentation on editing files.

Adding GIFs and Badges to Your GitHub Profile README
Here’s an image of the content that will be added in this section:

Header section
The GIF used in this section can be found here. I found this GIF on Giphy, which is full of free GIFs to use.

Go to the GIF Link and click on the Share button and then Copy GIF Link. We’ll add this copied link to an HTML img tag to display it in the Markdown file. We’re using the img tag as it’ll help us specify the width of the image.

In the GitHub file editor, replace the README.md file content with the following code:

<div id="header" align="center">
  <img src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" width="100"/>
</div>
The src attribute points to the URL we copied in the previous step. Since all the contents in this section are center-aligned, we’ve wrapped the image in an HTML div tag with the align="center" attribute.

Note: GitHub converts the README Markdown to HTML and renders it on GitHub. After conversion, the HTML is sanitized, and for security reasons, it ignores certain HTML tags and attributes such as <script>, <style>, style etc. For this reason, we’ve used an align attribute instead of CSS.

Now go to the preview tab. Pictured below is the output we get.

GIF preview
Next, we’ll add social network badges. On clicking the badge, it will redirect to the respective social networking sites. You can add social badges of various websites like Instagram, Facebook, Twitter, etc. For this tutorial, we’ll add three: Twitter, YouTube and LinkedIn.

To get the respective badges for each social network, we’ll use Shields.io, which provides various endpoints letting users create and customize social badges. We’ll use the https://img.shields.io/badge/ URL and pass additional parameters to this URL to get the respective social badges.

The first parameter we’ll pass is of the following format:

Label-Color
Label is the social network site name shown on the badge.
Color is the color of the badge.

For the three social networks, the values for this parameter will be:

LinkedIn: LinkedIn-blue
Twitter: Twitter-blue
YouTube: YouTube-red
When combined with https://img.shields.io/badge/, the following URL is created for LinkedIn:

https://img.shields.io/badge/LinkedIn-blue
After entering the above URL in the browser, we get the following output:

Linkedin badge with no styling
Note that we don’t have the icon for the badge added yet. To add it, we’ll use two query parameters in the following format:

logo={your social network icon name}
logoColor={color of the icon}
We’ll add both the parameters to the URL as below:

https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white
We’ll also add a style parameter to the above URL. There are various styling options available, the details of which you can find at Shields.io. We’ll use for-the-badge styling.

The final URL for LinkedIn will be:

https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white&style=for-the-badge
Now, when we hit this URL in the browser, we get the output pictured below.

Linkedin badge with styling
Similarly, we create URLs for other badges:

https://img.shields.io/badge/YouTube-red?style=for-the-badge&logo=youtube&logoColor=white
https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white
We’ll wrap each URL in img tag like so:

<div id="badges">
  <img src="https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
  <img src="https://img.shields.io/badge/YouTube-red?style=for-the-badge&logo=youtube&logoColor=white" alt="Youtube Badge"/>
  <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
</div>
We’ve wrapped the images in <div> tags to make sure all badges come on a single line. The above code will only display the image generated from the URL. To add hyperlinks for each of the badges, we’ll wrap each image with an <a> tag.

Build Your Own Developer Portfolio
Add the below code inside the <div> tag with id="header" and after the GIF <img> tag. Make sure to change the href attribute to point to your social profiles:

<div id="badges">
  <a href="your-linkedin-URL">
    <img src="https://img.shields.io/badge/LinkedIn-blue?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn Badge"/>
  </a>
  <a href="your-youtube-URL">
    <img src="https://img.shields.io/badge/YouTube-red?style=for-the-badge&logo=youtube&logoColor=white" alt="Youtube Badge"/>
  </a>
  <a href="your-twitter-URL">
    <img src="https://img.shields.io/badge/Twitter-blue?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter Badge"/>
  </a>
</div>
