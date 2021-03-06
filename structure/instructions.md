<h1>Building the BBIS Documentation</h1>

<h2>Getting Started + Developer Guides</h2>

<h2>Technical Reference</h2>

<h3>BBNCExtensions</h3>
<ol>
  <li>
    Check out the following projects from TFS:
    <ul>
      <li>$\Documentation\Technical_Training\Sandcastle</li>
      <li>$\Documentation\Technical_Training\DocumentationUtilities\SandcastleToJekyll</li>
      <li>$\Infinity\DEV\CRM_Integration\ClassicCMS\Web\Content</li>
    </ul>
  </li>
  <li>In the Sandcastle folder, open BBNCExtensions.shfbproj.  You'll notice that the three referenced files are pointing to the ClassCMS checkout, which if you'er following standard UserEd folder structures, should be C:\Team_Projects\Inifinty\DEV..</li>
  <li>You shouldn't need to adjust any of the settings, and instead can simply build the output by pressing CTRL-SHIFT-B.  This command builds the HTML version in the BBNCExtensionsOutput directory of the Sandcastle folder.</li>
  <li>Open the SandcastleToJekyll Visual Studio solution.</li>
  <li></li>
</ol>

<h3>REST API</h3>
<ol>
  <li>
    Check out the following projects from TFS:
    <ul>
      <li>$\Documentation\Technical_Training\DocumentationUtilities\WebApiToJekyll</li>
    </ul>
  </li>
</ol>

<h3>JavaScript SDK</h3>
<ol>
  <li>
    Check out the following projects from TFS:
    <ul>
      <li>$\Documentation\Technical_Training\DocumentationUtilities\JsDocToJekyll</li>
    </ul>
  </li>
</ol>

<h1>Locally Testing Jekyll</h1>

<p>When committed to the gh-pages branch of the bbis repo, GitHub pages automatically processes the files, including building the site using Jekyll.  This works great for production, but for real-time development, it's not practical.  To solve this, I "serve" the the site locally using Jekyll.  This process is <a href="http://jekyll-windows.juthilo.com" target="_blank">possible on a Windows Machine</a>, but it's <strong>a lot</strong> simpler to install Jekyll on OSX/Linux.</p>

<p>Below is an outline of steps necessary to build/serve the site locally:</p>

<ol>
  <li>
    Install Jekyll
    <ul>
      <li><a href="http://jekyll-windows.juthilo.com" target="_blank">Windows</a></li>
      <li><a href="http://jekyllrb.com/docs/installation/" target="_blank">OSX / Linux</a></li>
    </ul>
  </li>
  <li>Open Terminal/Command Prompt and CD into the directory where you've cloned the BBIS repo.</li>
  <li>Because Sandcastle produces so many individual files for the BBNCExtensions Technical Reference, building/serving the files locally takes several minutes.  To speed up this process, I created the _environment.sh file, which accepts one argument - "prod" or "dev" - and moves a large portion of the files to a temporary folder on my desktop.  In order for someone else to use this shortcut, you would need to update the script for their environment.  It runs like so: <code>sh _environment.sh prod</code> or <code>sh _environment.sh dev</code></li>
  <li>Run the following:<code>jekyll serve --baseurl ''</code></li>
</ol>

<p>Below are a list of links regarding Jekyll deployment:</p>

<ul>
  <li><a href="https://help.github.com/articles/using-jekyll-plugins-with-github-pages/" target="_blank">Using Jekyll Plugins with GitHub Pages</a></li>
  <li><a href="https://pages.github.com/versions/" target="_blank">GitHub Pages Version Dependency</a></li>
</ul>

