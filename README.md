# CAPTCHA Challenge Demo

This project provides a simple, single-file responsive web application designed to demonstrate a user interface for solving CAPTCHAs. It fetches CAPTCHA images either from a URL specified in the query parameters or defaults to a local sample image.

## Features

*   **Responsive Design:** Built with Tailwind CSS for a seamless experience across various devices.
*   **Dynamic Image Loading:** Displays CAPTCHA images from a `?url=` query parameter or defaults to `sample.png`.
*   **User Input and Validation:** Provides an input field for users to enter the CAPTCHA text and performs client-side validation for the default `sample.png` image.
*   **Clear Feedback:** Displays messages indicating correct/incorrect answers or submission status for external CAPTCHAs.

## How It Works

The application loads an image to serve as a CAPTCHA. Users are prompted to enter the text they see in the image into an input field. Upon submission, the application provides feedback.

**Important Note on "Solver" Functionality:**
This application focuses on the *user interface* for a CAPTCHA challenge. For the default `sample.png` image, it includes client-side validation against a known correct answer ("ADUR3"). For images loaded from external URLs (via the `?url=` parameter), the application will accept user input but cannot perform real-time, automated validation (like OCR) without a backend service. It will acknowledge the submission but indicate that actual solving for dynamic images requires a server-side component.

## Usage

1.  **Open `index.html`:** Simply open the `index.html` file in your web browser. It will load with the `sample.png` image by default.
2.  **Solve the Default CAPTCHA:** For `sample.png`, type "ADUR3" (case-insensitive) into the input field and click "Verify".
3.  **Use a Custom CAPTCHA URL:** To load a custom image, append a `?url=` query parameter to the `index.html` path.
    *   Example: `file:///path/to/your/project/index.html?url=https://example.com/some-captcha-image.png`
    *   Replace `https://example.com/some-captcha-image.png` with the actual URL of your desired CAPTCHA image.

## Project Structure

*   `index.html`: The main, single-file web application.
*   `sample.png`: The default CAPTCHA image used when no `url` parameter is provided.
*   `README.md`: This file.
*   `LICENSE`: The MIT License for this project.

## Technologies Used

*   HTML5
*   Tailwind CSS (via CDN)
*   JavaScript

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
