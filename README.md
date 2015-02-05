# APEL Git-page

---

## How to add pages

### 1. Add a Folder

Intially add a folder into the base directory of the site. The folder should be called the lowercase name of the page you wish to create.


---

### 2. Add 'index.md' page.

The next step is to add a 'index.md' page inside of that directory. The layout of the page should be as follows:

    ---
    layout: default <- Change if needed
    title: APEL 
    subheading: APEL client and server source code
    project-url: https://github.com/apel/apel
    ---

    Page Content

The actual layout of the page is handled by html pages in the _layout folder. If you find yourself having to need a new -specific- layout, feel free to copy the 'default' layout:

    {% include head.html %} - Don't Touch

    <div class="wrapper">
        <header>
            <h1>{{site.name}}</h1>
            <p>{{page.subheading}}</p>
            &nbsp;
            {% include nav.html %}
        </header>
        <section>
            <h1> {{page.title}}</h1>

            {{content}}

        </section>
    </div>

    {% include foot.html %} - Don't Touch


---

### 3. If Directory, add page to navbar_links.yml

If the new page is a page you wish to be added to the nav bar, you will need to add it to the navbar_links.yml file inside of the _data folder.

To add the page use the following format and reorganise as you see fit:

-   name: "Example"
    url: "/example/"