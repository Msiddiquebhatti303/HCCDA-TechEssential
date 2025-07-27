Directory Structure

my-enterprise/
├── index.html
├── web.md
├── styles.css
└── README.md


index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Enterprise</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="markdown-content"></div>
    <script src="https://cdn.jsdelivr.net/npm/showdown@2.1.0/dist/showdown.min.js"></script>
    <script>
        fetch('web.md')
            .then(response => response.text())
            .then(markdown => {
                const converter = new showdown.Converter();
                const html = converter.makeHtml(markdown);
                document.getElementById('markdown-content').innerHTML = html;
            });
    </script>
</body>
</html>


web.md

# My Enterprise

## Overview
My Enterprise is a cutting-edge solution for businesses.

## Features
* Feature 1
* Feature 2
* Feature 3

## Usage
1. Step 1
2. Step 2
3. Step 3


styles.css

body {
    font-family: Arial, sans-serif;
    margin: 20px;
}

#markdown-content {
    max-width: 800px;
    margin: 0 auto;
}


README.md

# My Enterprise

My Enterprise is a comprehensive solution for businesses.

