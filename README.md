# Instructions: Working with HTML and CSS

1. **Note:** The page design shall be organised into the following areas:
    - header
    - main section
    - project section

2. Start by organising your page with the following comments after the comment ` <!-- Set up your page structure here --> `

    ```HTML
        <!-- Set up your page structure here -->

        <!-- Start of header -->

        <!-- End of header -->


        <!-- Start of mainsection -->

        <!-- End of mainsection -->


        <!-- Start of project section, uses grids -->
    
        <!-- End of project section -->
    ```

3. Refer to `header` to add the following for a navigation bar:

    ```HTML
        <a name="top"><!-- This is an anchor tag, equivalent of a bookmark --></a>  
        <div class="header">
            <div class="logo"><!-- Un-comment the line here to add a logo --></div>
            <nav>
                <ul>
                    <li><a href="#top">Home.</a></li>
                    <li><a href="#projects">Projects.</a></li>
                    <li><a href="#contact">Let's talk.</a></li>
                </ul>
            </nav>
        </div>
    ```

4. Next, for the `mainsection`, add the following to represent the page cover (welcome):

    ```HTML
        <section id="mainsection">

            <div class="left-div">
                <div class="profilecontainer">
                    <img src="img/alex.png" alt="alex" class="rounded-image">
                    <p>
                        <span class="strong">&lt;Your Name Here&gt;</span>
                        <span>Full-stack Developer</span>
                    </p>
                </div>

                <div class="profiledetails">
                    <span class="subheader">Codes in:</span>
                    <ul>
                        <li>HTML . CSS . JavaScript</li>
                        <li>Java</li>
                        <li>SQL</li>
                    </ul>
                    <span class = "subheader">Works with:</span>
                    <ul>
                        <li>React</li>
                        <li>Springboot</li>
                        <li>jUnit + Mockito (Unit Tests)</li>
                    </ul>
                    <span class="subheader">Builds using:</span>
                    <ul>
                        <li>GitHub</li>
                        <li>IntelliJ IDEA</li>
                        <li>MySQL WorkBench</li>
                        <li>Visual Studio Code</li>
                    </ul>
                </div>
            </div>

            <div class="right-div">
                <div class="text">
                    <h1>Hi! <span class="typing"></span></h1>
                    <p>Good day, visitor. Use this starter template as your start your portfolio development journey.</p>
                    <div class="linkcontainer">
                        <a href="#projects">View projects below.</a>
                    </div>
                </div>
            </div>
        </section>
    ```

5. Refer to the `projectsection` where we need to the following placeholder and container to display the cards:

    ```HTML
        <a name="projects"></a>    
        <section id="projectsection">

            <div class="sectiontitle">Projects</div>
            <div class="showcasecontainer">

                <!-- Project Cards go here -->

            </div>

        </section>
    ```

6. Refer to the `projectsection` where we need to add cards for the projects on our page:

    ```HTML
        <!-- Project card #1 -->
        <div class="projectcard">
            <a href="#">
                <img src="img/web-design.jpg" alt="Add a description here">
                <!-- Project name -->
                <h4>Community Web Portal Design</h4>
                <p class="scope">Web Page Design</p>
                <p><span>UI/UX</span><span>HTML</span><span>CSS</span></p>
            </a>
        </div>

        <!-- Project card #2 -->
        <div class="projectcard">
            <a href="#">
                <img src="img/mobile-app.jpg" alt="Add a description here">
                <!-- Project name -->
                <h4>Expense Calculator Web App</h4>
                <p class="scope">JavaScript Development</p>
                <p><span>User Interaction</span><span>Application Logic</span></p>
            </a>
        </div>

        <!-- Project card #3 -->
        <div class="projectcard">
            <a href="#">
                <img src="img/data-tracking.jpg" alt="Add a description here">
                <!-- Project name -->
                <h4>Enrollment Tracker</h4>
                <p class="scope">Database Design</p>
                <p><span>SQL</span><span>Data Analysis</span></p>
            </a>
        </div>

        <!-- Project card #4 -->
        <div class="projectcard">
            <a href="#">
                <img src="img/chess.jpg" alt="Add a description here">
                <!-- Project name -->
                <h4>Chess Game</h4>
                <p class="scope">Java</p>
                <p><span>Game Development</span></p>
            </a>
        </div>

        <!-- Project card #5 -->
        <div class="projectcard">
            <a href="#">
                <img src="img/fitness-tracking.jpg" alt="Add a description here">
                <!-- Project name -->
                <h4>Fitness Tracker</h4>
                <p class="scope">App Development</p>
                <p><span>SwiftUI</span><span>Swift Programming</span></p>
            </a>
        </div>

        <!-- Project card #6 -->
        <div class="projectcard">
            <a href="#">
                <img src="img/photography.jpg" alt="Add a description here">
                <!-- Project name -->
                <h4>SG Arts Award</h4>
                <p class="scope">Photography</p>
                <p><span>Creative</span><span>Competition</span></p>
            </a>
        </div>
    ```

7. Update the styles to apply the changes for ***projectsection***

    Add the following styles for projectsection.

    ```CSS
        /* Start of styling projectsection */
        /* ******************************* */

        /* Set projectsection's style*/
        #projectsection {
            width: 80%;
            margin: auto;
            height: 100dvh;
        }

        /* Set the showcasecontainer to list the projects, repeated in equal columns of 3s per fractional unit */
        .showcasecontainer {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            grid-gap: 24px;
        }

        /* Set the card background to white */
        .projectcard {
            font-size: small;
            background-color: white;
            border-bottom-left-radius: 10px;
            border-bottom-right-radius: 10px;
            padding-bottom: 24px;
        }

        /* Set the project card p tag with a left padding of 24px */
        .projectcard h4, .projectcard p {
            padding-left: 16px;
        }

        /* Set the image in the project card */
        .projectcard img {
            display: block;
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
            margin-bottom: 10px;
            width: 100%;
            height: 180px;
            background-size: cover;
            background-position-x: center; 
            background-position-y: center;
            background-repeat: no-repeat;  
            background-image: url("img/imgplaceholder.png");
            text-indent: -9999px; /* remove or comment out text indent if all images are available */
        }

        /* Set the projectcard's title style (se the text to upper case) */
        .projectcard .scope {
            text-transform: uppercase;
            padding-top: 8px;
            padding-bottom: 8px;
        }

        /* Set mouseover effect for project card */
        .projectcard:hover {
            transition: 0.45s ease-out;
            transform: scale(1.05);
        }

        /* Set the link colour for the project card */
        .projectcard a {
            text-decoration: none;
            color: gray;
            transform: scale(1.0);
        }

        /* Set some tag layout for the <span> tag */
        .projectcard span {
            display: inline-block;
            font-size: x-small;
            align-content: space-between;
            border-radius: 6px;
            margin: 4px;
            background-color: lightseagreen;
            padding: 5px 10px;
            color: #FFFFFF;
            white-space: nowrap;
        }

        /* ***************************** */
        /* End of styling projectsection */
    ```

8. Add within `projectsection` the below markup for users to visit the top of the page:

    ```HTML
        <div class="top">
            <a href="#top">&#x25B2; Back to Top</a>
        </div>
    ```

9. To style the contents for **Back to Top**, include the following styles:

    ```CSS
        /* Start of styling miscellaneous elements */
        /* *************************************** */

        .top{
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .top a{
            margin-top: 20px;
            text-decoration: none;
            color: lightseagreen;
            font-size: small;
        }

        /* ************************************* */
        /* End of styling miscellaneous elements */
    ```
