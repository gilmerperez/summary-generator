# Summary Generator

## Description

The Summary Generator is a REST API that processes text content and returns a summarized version in bullet points. This project utilizes the OpenAI API to generate concise summaries, making it easier to extract key information from lengthy text inputs.

## Table of Contents

- [Usage](#usage)
- [Instructions](#instructions)
- [Key Features](#key-features)
- [Sample Input](#sample-input)
- [Sample Output](#sample-output)
- [Technology Stack](#technology-stack)
- [Additional Resources](#additional-resources)

## Usage 

To start the application, run the following commands:

```bash
npm install # Install dependencies
npm start   # Start the API server
```

## Instructions

1. Clone the repository and navigate to the project directory.

2. Install dependencies using npm install.

3. Create a .env file using .env.EXAMPLE as a reference and add your OpenAI API key.

4. Start the server with npm start.

5. Use Insomnia or a similar API testing tool to send a POST request to:

```bash
POST /api/summarize
```

with the following JSON payload:

```bash
{
    "text": "Your long text content here"
}
```

6. The API will return a summary in bullet points.

## Key Features

* Accepts text content via a POST request.

* Calls the OpenAI API to generate a summarized response.

* Returns bullet-pointed key takeaways from the input text.

* Can be tested using Insomnia or similar API testing tools.

## Sample Input

```json
{
    "text": "Johannes Gutenberg (1398 – 1468) was a German goldsmith and publisher who introduced printing to Europe. His introduction of mechanical movable type printing to Europe started the Printing Revolution and is widely regarded as the most important event of the modern period. It played a key role in the scientific revolution and laid the basis for the modern knowledge-based economy and the spread of learning to the masses.\nGutenberg many contributions to printing are: the invention of a process for mass-producing movable type, the use of oil-based ink for printing books, adjustable molds, and the use of a wooden printing press. His truly epochal invention was the combination of these elements into a practical system that allowed the mass production of printed books and was economically viable for printers and readers alike.\nIn Renaissance Europe, the arrival of mechanical movable type printing introduced the era of mass communication which permanently altered the structure of society. The relatively unrestricted circulation of information—including revolutionary ideas—transcended borders, and captured the masses in the Reformation. The sharp increase in literacy broke the monopoly of the literate elite on education and learning and bolstered the emerging middle class."
}
```

## Sample Output

```json
{
    "result": "- Johannes Gutenberg introduced printing to Europe, starting the Printing Revolution\n- His contributions to printing include mass-producing movable type, using oil-based ink, adjustable molds, and a wooden printing press\n- Gutenberg's invention allowed for the mass production of printed books, leading to the spread of knowledge to the masses\n- Mechanical movable type printing in Renaissance Europe altered society by allowing for mass communication and increasing literacy\n- The circulation of information led to the spread of revolutionary ideas and broke the monopoly of the literate elite on education"
}
```

## Technology Stack

* **Node.js & Express:** Backend framework for handling API requests.

* **TypeScript:** Provides type safety and enhances development.

* **OpenAI API:** Generates text summaries from input content.

* **dotenv:** Manages environment variables securely.

* **Insomnia/Postman:** Used for API testing and verification.

## Additional Resources

Learn more about Express.js: [Express Documentation](https://expressjs.com/)

OpenAI API documentation: [OpenAI API](https://platform.openai.com/docs/overview)

Environment variables in Node.js: [dotenv GitHub](https://github.com/motdotla/dotenv)
