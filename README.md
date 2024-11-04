# My GitHub Page

이 페이지는 GitHub Pages를 통해 생성된 웹사이트 예제입니다. 아래 탭을 클릭하여 다양한 섹션을 확인해 보세요.

<!-- HTML과 CSS를 혼용하여 탭 스타일을 추가합니다 -->

<style>
/* Tab container style */
.tab-container {
    display: flex;
    flex-direction: column;
    max-width: 600px;
    margin: 20px auto;
    font-family: Arial, sans-serif;
}

/* Tab button styles */
.tab-buttons {
    display: flex;
    cursor: pointer;
}

.tab-buttons div {
    flex: 1;
    padding: 10px;
    text-align: center;
    background: #f0f0f0;
    border: 1px solid #ddd;
    border-bottom: none;
}

.tab-buttons div:hover {
    background: #e0e0e0;
}

.tab-buttons .active {
    background: #ffffff;
    font-weight: bold;
}

/* Tab content styles */
.tab-content {
    border: 1px solid #ddd;
    padding: 20px;
    display: none;
}

.tab-content.active {
    display: block;
}
</style>

<div class="tab-container">
    <!-- Tab buttons -->
    <div class="tab-buttons">
        <div class="tab-button active" onclick="openTab(event, 'introduction')">Introduction</div>
        <div class="tab-button" onclick="openTab(event, 'method')">Method</div>
        <div class="tab-button" onclick="openTab(event, 'example')">Example</div>
    </div>

    <!-- Tab contents -->
    <div id="introduction" class="tab-content active">
        <h2>Introduction</h2>
        <p>This page is a simple website created with GitHub Pages. Here, you can find information about the project, the method used, examples, and license details.</p>
    </div>

    <div id="method" class="tab-content">
        <h2>Method</h2>
        <p>The process for creating a website using GitHub Pages is as follows:</p>
        <ol>
            <li>Create a GitHub repository</li>
            <li>Add and write the <code>index.html</code> file</li>
            <li>Configure GitHub Pages</li>
            <li>Visit the site URL to check your website</li>
        </ol>
    </div>

    <div id="example" class="tab-content">
        <h2>Example</h2>
        <p>Here is an example of a basic HTML structure:</p>
        <pre>
            <code>
                <!DOCTYPE html>
                <html lang="en">
                <head>
                    <meta charset="UTF-8">
                    <title>Example Page</title>
                </head>
                <body>
                    <h1>Example Title</h1>
                    <p>This is an example paragraph for demonstration purposes.</p>
                </body>
                </html>
            </code>
        </pre>
    </div>
</div>

<script>
/* JavaScript function for tab functionality */
function openTab(event, tabId) {
    var i, tabcontent, tabbuttons;
    
    // Hide all tab contents
    tabcontent = document.getElementsByClassName("tab-content");
    for (i = 0; i < tabcontent.length; i++) {
        tabcontent[i].style.display = "none";
    }

    // Remove active class from all tab buttons
    tabbuttons = document.getElementsByClassName("tab-button");
    for (i = 0; i < tabbuttons.length; i++) {
        tabbuttons[i].className = tabbuttons[i].className.replace(" active", "");
    }

    // Show the current tab and add active class to the button
    document.getElementById(tabId).style.display = "block";
    event.currentTarget.className += " active";
}
</script>
