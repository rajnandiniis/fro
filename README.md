


This project is a simple email subscription form designed to collect email addresses and store them in a Google Sheet. It is built using HTML and CSS.

## Features

- Responsive design
- Simple and clean UI
- Email validation
- Stores collected email addresses in a Google Sheet



## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

Make sure you have the following installed:
- A web browser (e.g., Chrome, Firefox, Safari)

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/rajnandiniis/fro
   ```
2. Open `index.html` in your web browser to view the form.

### Usage

1. Enter your email address in the subscription form.
2. Click the "Subscribe" button.
3. The email address will be validated and stored in the connected Google Sheet.

## Google Sheets Integration

To store the email addresses in a Google Sheet, you need to set up Google Sheets API and Google Apps Script.

### Steps to set up Google Sheets integration:

1. Create a new Google Sheet and name it appropriately.
2. Click on `Extensions` > `Apps Script`.
3. Delete any code in the script editor and paste the following code:

   ```javascript
   function doPost(e) {
     var sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
     var data = JSON.parse(e.postData.contents);
     sheet.appendRow([data.email]);
     return ContentService.createTextOutput('Success').setMimeType(ContentService.MimeType.JSON);
   }
   ```
4. Save the script and deploy it as a web app.
5. Copy the URL of the deployed web app.

### Form Submission

1. Edit the `script.js` file to include the URL of your deployed web app.
   ```javascript
   const scriptURL = 'YOUR_DEPLOYED_WEB_APP_URL';
   ```
2. Open `index.html` in your browser, fill out the form, and submit. The email address will be saved in your Google Sheet.

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Contact

Your Name -rajnandini1783@gmail.com

Project Link:(https://github.com/rajnandiniis/fro)
```

Feel free to adjust the content according to your project's specifics.
