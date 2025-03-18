# Dataset Documentation

## 1. Data Description
The dataset used in this study consists of two types of text: human-written content and AI-generated content. The data was collected from publicly available sources and synthetic generation techniques. The human-written content was collected from Wikipedia, and the AI-generated content was created using the Llama3.2 model.  

The dataset is balanced, containing 193 entries of human-written content and 193 entries of AI-generated content, ensuring that both classes have equal representation.

## 2. Data Collection Process
The data collection process began by retrieving relevant topics from the "Artificial Intelligence" category on Wikipedia using the Wikipedia API. Each topic title was extracted, removing special characters, and stored in a JSON file to serve as the basis for both human-written and AI-generated content.  

For **human-written content**, the Wikipedia API was used to fetch the introductory section of each article corresponding to the selected topics. These introductions were extracted as plain text, cleaned by removing extra spaces, and saved as individual TXT files in a designated `human` folder.  

For **AI-generated content**, the same set of topics was used as prompts for the Llama3.2 model. The model was deployed locally using the Ollama framework, and each topic was provided as input with an instruction to generate a formal and objective introduction in the style of a Wikipedia article. The generated text was then cleaned and stored in TXT files within an `ai` folder, ensuring a consistent structure with the human-written data.  

Once both types of text were collected, they were combined into a structured dataset. Each entry in the dataset included a text sample and a label (`human` or `ai`). The final dataset was saved as a CSV file named `dataset.csv`, which contained two columns:

- `text`: The text sample
- `label`: The classification (human or ai)

This structure ensures equal representation of human-written and AI-generated content.

## 3. Example Topic: Perusall
### Human-Written Text Example
> *Perusall is a social web annotation tool intended for use by students at schools and universities. It allows users to annotate the margins of a text in a virtual group setting that is similar to social media—with upvoting, emojis, chat functionality, and notification. It also includes automatic AI grading.*

### AI-Generated Text Example
> *Perusall is an online annotation and discussion platform designed to facilitate collaborative learning and academic engagement. Developed by Perusall LLC, a US-based company, this platform allows students, educators, and researchers to annotate and discuss educational materials, such as e-books, articles, and multimedia content, in real-time.*

