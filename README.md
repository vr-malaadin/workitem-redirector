# <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTh8mC7f14ESDFQC0XbM6xcH6wLakU8hythSw&s" alt="Icon" width="40" height="40"> WorkItem Redirector

![WorkItem Redirector](https://img.shields.io/badge/status-published-brightgreen)

Welcome to the **WorkItem Redirector**! This tool allows users to quickly redirect to work items by entering a WorkItem ID. It's designed for efficiency and ease of use, perfect for any developer workflow.

## 📖 Overview

The WorkItem Redirector is a simple web page application that provides an easy way to navigate to specific work items in your development environment. All you need to do is enter the WorkItem ID and hit the "Go" button to be redirected automatically.

## 🚀 Live Demo

Check out the live demo [here](https://vr-malaadin.github.io/workitem-redirector/).

## 🛠️ Usage

1. Open the [WorkItem Redirector](https://vr-malaadin.github.io/workitem-redirector/) in your web browser.
2. Enter the WorkItem ID in the input field.
3. Click the "Go" button or press `Enter` to be redirected to the corresponding work item.

## 🎨 Features

- **Instant Redirection**: Quickly access work items by entering their IDs.
- **Responsive Design**: Optimized for both desktop and mobile viewing.
- **Persistent Focus**: The input field maintains focus for quicker entry.
- **Alert for Empty Input**: Alerts the user if no WorkItem ID is entered.

## 🔧 Customization

To customize the URL or style:

1. **URL Customization**:
   - Modify the `url` variable in the JavaScript section to match your development environment's URL pattern.
     ```javascript
     const url = `http://yourserver:port/tfs/web/wi.aspx?id=${number}`;
     ```

2. **Style Customization**:
   - Edit the CSS in the `<style>` section within the `<head>` tag of the HTML file.

## 📝 Code

Here's a snippet of the HTML and JavaScript code for this tool:

<details>
<summary>Click to expand the code snippet</summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WorkItem Redirector</title>
    <link rel="icon" type="image/x-icon" href="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTh8mC7f14ESDFQC0XbM6xcH6wLakU8hythSw&s">
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .container {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        input {
            font-size: 16px;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            outline-color: #1978DD;
            width: 200px;
            position: relative;
        }
        button {
            font-size: 16px;
            padding: 10px 15px;
            cursor: pointer;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            margin-left: 10px;
        }
        .input-wrapper {
            position: relative;
            display: inline-block;
        }
        .input-wrapper::before {
            content: '';
            position: absolute;
            top: -3px;
            right: -3px;
            bottom: -3px;
            left: -3px;
            background: linear-gradient(45deg, #ff00ff, #00ffff, #ff00ff);
            filter: blur(10px);
            border-radius: 8px;
            z-index: -1;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="input-wrapper">
            <input type="number" id="workitemID" placeholder="Enter a WorkItem ID" autofocus>
        </div>
        <button onclick="redirect()">Go</button>
    </div>

    <script>
        function redirect() {
            const number = document.getElementById('workitemID').value;
            if (number) {
                const url = `http://developmentvlan:8585/tfs/web/wi.aspx?id=${number}`;
                window.location.href = url;
            } else {
                alert('Please enter a WorkItem ID');
            }
        }

        const input = document.getElementById('workitemID');

        // Keep focus on the input field
        input.addEventListener('blur', function () {
            setTimeout(() => this.focus(), 0);
        });

        input.addEventListener('keyup', function (event) {
            if (event.key === 'Enter') {
                redirect();
            }
        });

        // Ensure focus on page load
        window.onload = function () {
            input.focus();
        }
    </script>
</body>
</html>
```
</details>

## 📦 Installation

No installation is necessary for this tool as it is purely a web-based application. Simply clone the repository and open `index.html` in your preferred browser.

git clone https://github.com/vr-malaadin/workitem-redirector.git


## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request for any changes or enhancements.

## 📧 Contact

For any questions or suggestions, feel free to contact the developer [here](mailto:malaadin@vanrise.com).
