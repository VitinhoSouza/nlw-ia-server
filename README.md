# Welcome to **nlw-ia-server** 🤖🌎
It is a system which **uses the OpenAI API to transcribe audio into text and to generate responses according to the selected prompt (“command”)** developed during a NLW IA event. 💻

This is an API that has four endpoints. Are they:
- **List Prompts** (*GET*): 'baseUrl/prompts';
- **Create Video** (*POST*): 'baseUrl/videos', which expects a FormData in the body with a property called 'file', whose content is a '.mp3';
- **Create Transcription** (*POST*): 'baseUrl/videos/:videoId/transcription', which expects an object with a property called 'prompt', whose value is a string with words from the video subject separated by commas;
- **Create AI Completion** (*POST*): 'baseUrl/ai/complete', which expects an object with that has the following properties: {videoId (string), prompt (string) and temperature (number between 0 and 1)}.

## A preview of the application:
![NLW IA](https://github.com/VitinhoSouza/nlw-ia-server/assets/51724518/47064e56-1428-4f90-a01e-ebdb2705c263)


## Techs:
Built with **fastify** + **Node**. Also used:
- **Prisma** to assist in the database part, generating tables faster;
- **TypeScript** to better define some application data;
- **Zod** to data validation (received in requests);
- **openai** to transcribe audio and generate responses using the gpt-3.5-turbo-16k model;
- **ai** to handle sending streams.
  
## Get started:
- Open the terminal inside the project folder and do: *npm install*. When all packages are installed, do *npm run dev* to start in development mode.
