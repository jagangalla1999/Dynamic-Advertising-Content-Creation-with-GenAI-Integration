# Ad Generator

This project is a Streamlit application designed to generate advertisements based on user input. It utilizes the OpenAI GPT-3 model for text generation and DALL-E for image generation.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [File Overview](#file-overview)
- [Contributing](#contributing)

## Features
- **Generate Ads**: Create ad text based on brand name, tagline, and product description.
- **Customize Output**: Control the number of generations, length of the output, and creativity level.
- **Image Generation**: Generate and display images related to the ad text.
- **Save Functionality**: Save generated ads and images.

## Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/yourusername/ad-generator.git
    cd ad-generator
    ```

2. **Install dependencies**:
    Ensure you have Python 3.8+ and install the required packages.
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up OpenAI API Key**:
    Make sure to set your OpenAI API key in your environment variables:
    ```bash
    export OPENAI_API_KEY='your_openai_api_key'
    ```

## Usage

1. **Run the application**:
    ```bash
    streamlit run app.py
    ```

2. **Interact with the UI**:
    - Enter the brand name, tagline, and product description in the provided text areas.
    - Adjust the parameters in the sidebar:
        - **Number of Generations**: Select how many ads to generate.
        - **Output Length**: Choose between Short, Medium, and Long ad text.
        - **Creativity**: Adjust the creativity level of the generated text.
        - **Show Images**: Option to display images generated by DALL-E.
    - Click **Generate** to create the ads.
    - Click **Save Ads & Images** to save your generated content.

## Configuration

The main configuration is handled via the Streamlit UI. However, you can customize the appearance and behavior of the app by modifying `app.py`.

## File Overview

### `app.py`
The main Streamlit application file that:
- Defines the UI components and layout.
- Collects user inputs for the brand name, tagline, and product description.
- Provides options to customize the number of ad generations, output length, and creativity level.
- Calls the ad generation logic from `fine_tuned.py`.
- Optionally calls the image generation function from `dalle.py`.

### `fine_tuned.py`
Contains the logic for generating ad text using the OpenAI API:
- Defines the `AdGenerator_logic` function that takes user inputs and generates ad text based on a fine-tuned GPT-3 model.
- Uses the OpenAI API to create text completions.

### `dalle.py`
Handles image generation using the DALL-E API:
- Defines the `create_and_show_images` function that generates and displays images based on the ad text.
- Uses the OpenAI API to create images.

## Contributing

1. **Fork the repository**.
2. **Create a new branch**:
    ```bash
    git checkout -b feature/your-feature-name
    ```
3. **Commit your changes**:
    ```bash
    git commit -m 'Add some feature'
    ```
4. **Push to the branch**:
    ```bash
    git push origin feature/your-feature-name
    ```
5. **Open a pull request**.
