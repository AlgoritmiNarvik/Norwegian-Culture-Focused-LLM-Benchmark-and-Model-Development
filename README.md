### [DRAFT, project plan]
## Norwegian Culture-Focused LLM Benchmark and Model Development

### Introduction:
This project focuses on developing a benchmark for Norwegian language models and subsequently tuning a Large Language Model (LLM) to better understand and generate content specific to Norwegian culture. The project takes inspiration from the Vikhr project for Russian described in [Vikhr: The Family of Open-Source Instruction-Tuned Large Language Models for Russian](https://doi.org/10.48550/arXiv.2405.13929) by Nikolich et al., adapting its approach to suit the Norwegian linguistic and cultural context. The project will be carried out over a month by a small team of 2-3 members.

### Project Objectives:
- **Phase 1:** Develop a comprehensive benchmark specifically for Norwegian LLMs, focusing on culturally and linguistically relevant tasks.
- **Phase 2:** Tune and evaluate Norwegian language models using the benchmark developed in Phase 1.
- **Outcome:** Create a instruction-following Norwegian LLM that understands and generates culturally appropriate Norwegian content.

### Phases of the Project:

1. **Benchmark Development:**
    - **Data Collection:**
        - **Legal Texts:** Collect data from Norwegian legal databases such as Lovdata, including statutes, regulations, and court decisions.
        - **Popular Music:** Gather lyrics and metadata from popular Norwegian songs using sources like Spotify, Genius, or MusikkOnline.
        - **Literature:** Compile summaries and full texts from classic and contemporary Norwegian literature, potentially using sources like the National Library of Norway (Nasjonalbiblioteket) or Bokhylla.
        - **Film Data:** Gather information on Norwegian films, including plots, director data, and release dates from sources such as IMDb, Filmarkivet, or the Norwegian Film Institute (Norsk Filminstitutt).
        - **MMLUPro Norwegian Adaptation:** Translate and adapt the MMLUPro dataset for Norwegian, ensuring relevance to Norwegian cultural and legal contexts.
    - **Data Processing:**
        - **Cleaning:** Ensure all collected data is accurate, clean, and free of irrelevant content.
        - **Filtering:** Curate the dataset to ensure it reflects a broad range of Norwegian cultural contexts.
        - **Structuring:** Organize the data for easy use in benchmarking tasks, ensuring a variety of tasks including multiple-choice, comprehension, and reasoning are represented.
    - **Benchmark Assembly:**
        - Design tasks that reflect the unique aspects of Norwegian culture, law, and general knowledge.
        - Develop a series of multiple-choice questions and other task types to evaluate the model’s capabilities across different domains.

2. **Model Tuning and Evaluation:**
    - **Vocabulary Adaptation:** Modify the tokenizer to handle Norwegian words efficiently, improving text generation quality.
    - **Continued Pre-Training:**
        - Perform continued pre-training on the Norwegian datasets to integrate the model’s understanding of Norwegian-specific language and cultural references.
    - **Instruction Tuning:**
        - Fine-tune the model on instruction datasets specifically tailored to Norwegian contexts, ensuring it can follow instructions and generate appropriate responses in Norwegian.
    - **Evaluation:**
        - Use the developed benchmark to assess the performance of Norwegian language models, comparing them against existing models.
        - Implement an ELO rating system to continuously evaluate the performance of different models on the benchmark tasks.

3. **Deployment and Open-Source Contribution:**
    - **Integration:** Integrate the benchmark and the tuned model into a fork of `lm_eval` with all tasks focused on Norwegian cultural content.
    - **Open-Source Release:** Publish the benchmark, tuned models, and associated tools on platforms like GitHub and Hugging Face to contribute to the broader community and facilitate further research.

### Roles and Responsibilities:

- **Project Lead:** Oversees the project, ensuring milestones are met and coordinating between team members.
- **Data Engineers:** Handle the collection, cleaning, filtering, and structuring of the datasets.
- **Machine Learning Engineers:** Focus on model adaptation, continued pre-training, and instruction tuning.
- **Benchmark Developers:** Design and implement the Norwegian-specific tasks for the benchmark.

### Resources Required:

- **Computational Resources:** Access to GPUs such as NVIDIA A100 for model training and fine-tuning [Vikhr's hardware].
- **Data Storage:** Sufficient storage for handling and processing large datasets.
- **Collaboration Tools:** Use of shared Git repositories and JupyterHub for efficient collaboration.

### Timeline:

- **Phase 1:** Benchmark Development (Weeks 1-2)
- **Phase 2:** Model Tuning and Evaluation (Weeks 3-4)
- **Phase 3:** Integration and Open-Source Release (End of Week 4)

### References

1. **Aleksandr Nikolich, Konstantin Korolev, Artem Shelmanov, Igor Kiselev. "Vikhr: The Family of Open-Source Instruction-Tuned Large Language Models for Russian."** This paper introduces Vikhr, a cutting-edge open-source language model specifically designed for the Russian language. The model features a uniquely adapted tokenizer and undergoes thorough pre-training and instruction tuning, outperforming many existing models. [Read more](https://doi.org/10.48550/arXiv.2405.13929).

2. **MMLUPRO**: A multi-modal benchmark designed to evaluate the understanding capabilities of AI systems across various languages and modalities. [ArXiv](https://arxiv.org/abs/2406.01574) | [GitHub](https://github.com/TIGER-AI-Lab/MMLU-Pro?tab=readme-ov-file).

3. **ScandEval**: An evaluation suite for assessing language models specifically in Scandinavian languages. It provides tools and datasets to test models on various linguistic tasks across Scandinavian languages. [GitHub](https://github.com/ScandEval/ScandEval) | [ArXiv](https://arxiv.org/abs/2304.00906).

4. **NorBench -- A Benchmark for Norwegian Language Models**: NorBench is a benchmark tailored for evaluating the performance of Norwegian language models. It includes a wide array of tasks that reflect the diverse linguistic challenges present in Norwegian. [GitHub](https://github.com/ltgoslo/norbench) | [ArXiv](https://arxiv.org/abs/2305.03880) | [ACL Anthology](https://aclanthology.org/2021.nodalida-main.4/).

### Extra Resources

- **Researcher Access Program**: OpenAI's program offering researchers access to advanced models for non-commercial use. [More information](https://openai.com/form/researcher-access-program/).
