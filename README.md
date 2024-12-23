# Fine Tuning Mistral7b with your own Custom data

The goal of this project is to fine-tune the Mistral 7b language model using customized data prompts. 

## Technologies Used

</h3>
<br>
<p align="left">
        <img width="48" height="48" src="https://img.icons8.com/fluency/48/python.png" alt="python"/>
        <img width="48" height="48" src="https://img.icons8.com/fluency/48/jupyter.png" alt="jupyter"/>
        <img width="48" height="48" src="https://img.icons8.com/color/48/artificial-intelligence.png" alt="artificial-intelligence"/>
        <img src="https://github.com/user-attachments/assets/b5dd48a0-865b-4b31-96d8-125ebce7833e" width="70" height="48">
        <img src="https://github.com/user-attachments/assets/fcf9d268-f145-480a-86ea-19a4b106c860" width="50" height="48">
        <img src="https://github.com/user-attachments/assets/bd672ce6-0882-4840-86f5-590f99acb397" width="50" height="48">


</p>
</div>
<br>

`Python`  `Jupyter Notebook` `Artificial Intelligence`  `Mistral7b`  `Ollama`  `Open Web UI`

Here's a refined version of your project development approach:

---

## Project Development Approach

### 1. Data Cleaning
- **Exporting Data:** The project began by exporting chat data from Open Web UI. These were stored as JSON files, containing both human prompts and AI responses.
- **Dataframe Creation:** The prompts from the JSON files were structured into a dataframe with two columns: one for the input prompts (questions/human prompts) and another for the output prompts (answers/AI responses).

### 2. Train/Test Split
- **Data Splitting:** The cleaned data was then divided into training and test sets, with a 70-30 split to ensure a balanced evaluation.

### 3. Model Loading and Quantization
- **Base Model:** The Mistral 7b model was retrieved from Hugging Face.
- **Model Quantization:** To optimize performance, 4-bit quantization was applied to the model.

### 4. Initial Evaluation
- **Evaluation Prompt:** Before fine-tuning, an evaluation prompt was created to assess the baseline performance of the model.

### 5. Fine-Tuning
- **LoRA Configuration:** Low-Rank Adaptation (LoRA) was configured to prepare the model for fine-tuning.
- **Model Training:** The model was then trained on the prepared dataset.
- **Post-Training Evaluation:** The evaluation prompt was run again to measure the improvements in the model's performance after fine-tuning.

### 6. Deployment
- **Model Conversion:** The fine-tuned model was converted into a `gguf` file format.
- **Integration with Open Web UI:** The `gguf` file was then fed back into the Open Web UI server for deployment and further use.
