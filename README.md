# LLM Benchmarking

This project is about a novel approach to benchmarking Large Language Models (LLMs) using grade school tests across various languages and cultures, emphasizing real-world comprehension and reasoning capabilities. Key points include:

Novel Testing Framework: A method of using grade school tests (real and synthetic) to evaluate LLMs was proposed, focusing on reading comprehension, logical deduction, and context understanding. This method aims for universality and practical applicability in assessing AI understanding and reasoning, mirroring tasks humans perform naturally.

Cultural and Linguistic Diversity: The testing can expand to include materials from various societies and languages (e.g., Spanish, Portuguese, Russian, Chinese), aiming to assess the global competence and cultural sensitivity of LLMs.

Detecting Biases and Lingering Focus: The proposed tests might incidentally reveal biases and the "lingering focus" effect—where recent topics unduly influence responses to subsequent, unrelated queries. Identifying such patterns is crucial for developing more objective and contextually adept LLMs.

Real-World Relevance and Human Relatability: Emphasizing that any LLM claiming general applicability should exhibit flawless performance in these tests, akin to "graduating grade school," before undertaking more complex or critical tasks. This stance underlines the expectation for LLMs to achieve a high level of understanding and functionality, reflective of practical, everyday intelligence. Moreover, the use of grade school tests introduces a level of human relatability to the evaluation process, connecting it to a universal human experience and making the assessment of LLM capabilities more accessible and comprehensible to the general public.

Evaluation Methodology Enhancement: A unique aspect of this framework is administering tests without multiple-choice answers, requiring LLMs to provide open responses. Then, an existing LLM with established capabilities analyzes the results, utilizing known answers for large-scale evaluation. This process is akin to a fine-tuning session, potentially involving multiple epochs, thereby leveraging the strengths and recognizing the limitations of current LLMs at a significant scale. This dual-layered approach provides a nuanced understanding of the tested LLM’s capabilities, including how it handles tasks without the aid of pre-defined choices and its performance on open-ended questions, across a comprehensive and extensive dataset.

Highlights of the potential of the proposed testing framework to significantly advance LLM evaluation methodologies are:
- Providing a clear, understandable, and relevant benchmark for AI capabilities.
- The introduction of a secondary evaluation layer, using an existing LLM, enriches the assessment process, offers a comprehensive understanding of a tested LLM's real-world applicability and reasoning skills, with an added emphasis on making the evaluation process relatable and engaging for a broader audience.

[You will find the tests used in the Proof of Concept project here](https://github.com/Walter-Stroebel/Jllama/tree/main/src/main/resources). The files ending in JSON are the actual test files, their format should be quite easy to understand.

Within this repository, a comprehensive test run is documented, showcasing 'Mistral 7B'—a highly regarded model—serving both as the LLM under examination and the evaluator. Detailed insights are available [here](mistral.md). 
Given the thorough nature of the testing process, where each question is posed ten times followed by an evaluation of all responses at the document's end, the file is sizeable.
The scoring methodology is rigorously designed to pursue perfection, allocating 0.1 point for each affirmative (YES) response and deducting 0.2 points for each negative (NO) response.

Additionally, an HTML version, suitable for download, is available [here](mistral.html)
The HTML version is created using PanDoc (pandoc -f markdown mistral.md mistral.html).

[This](running.png) is a screenshot of the test being run; it takes a few minutes for most small models. The complete source code, along with additional functionalities, is accessible through the [Jllama](https://github.com/Walter-Stroebel/Jllama) project here on GitHub.

Note that running the test requires a bit of knowledge and skill, you will need to have [Ollama](https://github.com/ollama/ollama) installed and be able to build the repo using Maven, which in turn requires Java.
I have only tested this on Linux but it should be possible to get things running on Windows and MacOS as well.

Some more runs:
[gemma2b](gemma2b.md)
[gemma7b](gemma7b.md)
