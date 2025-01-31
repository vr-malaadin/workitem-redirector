# <img src="https://cdn-icons-png.flaticon.com/512/7510/7510794.png" alt="WorkItem Icon" width="40" height="40"/> WorkItem Redirector
![WorkItem Redirector](https://img.shields.io/badge/status-published-brightgreen)

A simple tool to quickly navigate to specific work items in your organization's system. This web app provides a convenient interface to search for and open work items by their ID, with an optional **Embedded Mode** that displays the work item directly within the page. The app works locally for testing, with embedded mode functionality only available when running in a local environment (like `localhost` or `127.0.0.1`).

## Features

- **WorkItem ID Search:** Input a WorkItem ID to directly access the corresponding page.
- **Embedded Mode:** When running locally, you can open the work item in an embedded iframe within the page. This eliminates the need to open a new tab.
- **Error Handling:** Alerts you if a WorkItem ID is invalid or not entered.
- **Responsive Design:** The layout adapts to different screen sizes, ensuring a user-friendly experience on both desktop and mobile devices.

## Demo

You can access the live version of the app [here](https://vr-malaadin.github.io/workitem-redirector/).

## Screenshots

![image](https://github.com/user-attachments/assets/ac6934db-9e20-42f3-8fb7-828b2bf10b4d)


## Installation

### Clone the repository

```bash
git clone https://github.com/vr-malaadin/workitem-redirector.git
```

### Open in a Local Server

1. Navigate to the project folder:
   ```bash
   cd workitem-redirector
   ```

2. Open the `index.html` in your browser directly, or use a local server to test the embedded mode:
   - For **Localhost** (`http://localhost` or `http://127.0.0.1`), embedded mode will work automatically.
   - If running on any other server (including remote servers), embedded mode will be disabled, and the system will show a warning.

## Usage

### Opening a WorkItem

1. Enter a **WorkItem ID** in the input field (e.g., `12345`).
2. Click the **Open WorkItem** button to open the item in a new tab or embedded mode.
3. If you have **Embedded Mode** enabled (running locally), the WorkItem will be displayed directly within the app.

### Embedded Mode

- The **Embedded Mode** allows the work item to be displayed directly in the app using an iframe.
- This mode is only supported when the app is running locally (`localhost` or `127.0.0.1`).
- The **Embedded Mode Toggle** allows you to enable or disable this feature.

### Error Handling

If you enter an invalid WorkItem ID or leave the input empty, an error message will appear to guide you to enter a valid ID.

## Technologies Used

- **HTML5**
- **CSS3** (Custom Styling)
- **JavaScript** (DOM Manipulation, Local Environment Detection)
- **FontAwesome** for Icons

## Contributing

Feel free to fork this repository and make pull requests. Contributions are welcome!

### Issues & Bugs

If you encounter any issues or bugs, please feel free to open an issue on the GitHub repository.

## License

This project is open-source and available under the [MIT License](LICENSE).
