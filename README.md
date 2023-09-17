

# Job Description Matching System with Hugging Face Transformers

## Overview

This project demonstrates a job description matching system that matches extracted CV details against job descriptions based on skills and education. It uses the Hugging Face Transformers library for text embedding and similarity computation. Here's an overview of the key operations performed:

1. **Data Preparation:**
   - Extracts CV details from PDF files.
   - Fetches job descriptions from the "huggingface/job-descriptions" dataset using the Hugging Face datasets library.
   - Fetches 10-15 job descriptions for matching.

2. **Text Embedding:**
   - Uses the DistilBERT model for text embedding.
   - Converts both job descriptions and CVs into dense vector representations.
   - No tokenization or preprocessing is performed on job descriptions or CVs.

3. **Cosine Similarity Calculation:**
   - Calculates cosine similarity between job descriptions and CVs using their embeddings.
   - Cosine similarity is used as a similarity metric.

4. **Ranking and Presentation:**
   - Ranks CVs based on similarity scores for each job description.
   - Lists the top 5 CVs with the highest similarity scores for each job description.

## Usage

1. **Dependencies:**
   - Install the necessary dependencies using `pip install transformers datasets`.

2. **Data Preparation:**
   - Place your CVs in PDF format in a folder (set the path in the code).
   - Ensure that you have access to the internet to fetch job descriptions from the Hugging Face dataset.

3. **Execution:**
   - Run the provided Python script to execute the operations.

4. **Output:**
   - The script will print the job descriptions and the top 5 matching CVs for each job description based on similarity scores.

## Challenges Faced

Developing a job description matching system using Hugging Face Transformers library and working with PDF CVs can pose several challenges:

1. **Data Extraction from PDFs:**
   - Extracting text accurately from PDFs can be challenging due to variations in PDF structure and formatting.

2. **Tokenization and Embedding:**
   - Tokenizing and embedding text using pre-trained models like DistilBERT requires careful preprocessing and handling of different text formats.

3. **Scalability:**
   - Scaling the system to handle a large number of CVs and job descriptions efficiently can be complex.

4. **Model Selection:**
   - Choosing the appropriate pre-trained model and fine-tuning it for specific requirements can be challenging.

5. **Evaluation Metrics:**
   - Selecting suitable evaluation metrics for ranking CVs and job descriptions is important but may require domain expertise.

6. **Data Privacy:**
   - Ensuring the privacy and security of CV data is crucial, especially if the CVs contain sensitive information.

## Conclusion

This job description matching system demonstrates the use of Hugging Face Transformers for text processing and similarity computation. While the code provides a starting point, real-world applications may require further fine-tuning, scalability improvements, and additional considerations for data privacy and security.