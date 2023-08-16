# Questrom MSBA Capstone Project - Summer 2023
BA888 Team Defactor Global Repository

# Organization
deFacto Global, Inc.

The deFacto Global Inc. is an industry-leading company specializing in comprehensive business modeling and planning capabilities integrated directly into Excel, Power BI, and web interfaces as part of their cutting-edge xP&A platform. With a strong focus on delivering enterprise-quality solutions, defacto Global Inc aims to provide organizations with the tools and technologies required to optimize their planning, analysis, and decision-making processes. By creating solutions for data collection, analysis, and simulations, deFacto Global Inc. explores in the future of business modeling and enables businesses to enhance their modeling accuracy, improve operational efficiency, and gain deeper insights into their financial and operational data. As a key player in the field of xP&A, deFacto Global Inc. strives to empower businesses with a robust and user-friendly platform that seamlessly integrates into their existing workflows, ultimately driving better planning outcomes and facilitating strategic growth.

# Business Advisor
Name: Bob Bedard

# Faculty Advisor
Name: Elgar Pichler

# Group Member
Name: Boyuan (Daniel) Zhang, Vibhas Goel, Jacky Yang, Tao Li

# Project Purpose
The objective of this project is to develop an AI-based bot utilizing a small Large Language Model (LLM) that can run on a laptop or small server. This bot will be trained using deFacto's existing training materials, with an initial step involving the evaluation and selection of the most suitable LLM based on a predetermined set of criteria.

Further enhancements to the bot's capabilities may be explored if time allows.

# Significance
This project holds significant importance for deFacto Global Inc. as LLMs are expected to have a massive impact on the software industry. We aim to harness the power of LLMs to perform a wide range of functions, including potentially replacing software. This project will allow us to assess the feasibility of using small, domain-specific LLMs tailored exclusively to our product.

# Objectives
1. LLM Selection (Critical): Evaluate and select an LLM based on predefined selection criteria.
2. Training Material Compilation (Critical): Compile deFacto's training materials in a format suitable for LLM training.
3. LLM Training (Critical): Evaluate options for training the LLM and conduct the training using deFacto's materials.
4. Update Pipeline/Process Development (Critical): Develop a system for updating the LLM's knowledge as deFacto's product evolves.
5. User Interface Development (Important but not critical): Develop user interfaces as required.
6. Bot Capability Expansion (Nice to have): Enhance the bot's capabilities to support other functional needs of users, including executing instructions.

# Files Overview
## Description

This repository contains a collection of Jupyter notebooks, Excel files, and other resources used in the project related to the deFacto training material processing and querying using various methods like embeddings, Pinecone, and GPT models.

## `Data_Extraction.ipynb`
* **Purpose**: Extracts and reads the deFacto training material.
* **Description**: This Colab notebook is responsible for scraping the training material and converting it into a `.txt` format. The text data is then easier to process for embedding purposes.

## `GPT4_Model.ipynb`
* **Purpose**: Contains the complete operational code for the project.
* **Description**: Excluding the data extraction from the training material, this notebook encompasses the entire process. It involves creating a Pinecone index, embedding the deFacto training material as vectors, and storing them in the Pinecone database. The data can then be fetched using the ChatGPT API for answering queries. Additionally, it includes code for analysis.

## `Query.ipynb`
* **Purpose**: Demonstrates querying the data.
* **Description**: A sample notebook that uses the GPT API to fetch relevant content from Pinecone and leverages GPT to generate answers based on the fetched content.

## `Scraped Data.xlsx`
* **Purpose**: Storage of updated training material.
* **Description**: This Excel file contains the training material updates, sourced through web scraping.

## `Training_material_visualization.ipynb`
* **Purpose**: Visualization of the scraped training material.
* **Description**: This notebook is dedicated to creating visual representations of the extracted training material, aiding in easier understanding and analysis.

# Deploy
## Overview

**Pinecone Model.ipynb**: This notebook provides the necessary steps to create your Pinecone server and upload your material. Once you've uploaded your .docx file, you can leverage this notebook to save your material to the Pinecone server.

**Query.ipynb**: In this notebook, you can fill in your OpenAI, Pinecone API, and Pinecone server environments. With these details filled in, you can interact with the GPT customer service bot. The bot will search the relevant material you uploaded to Pinecone and answer your questions based on that material.

## Prerequisites
* An account with `OpenAI`.
* An account with `Pinecone`.
* Your material in `.docx` format.

## Setup
1. Open `Pinecone Model.ipynb`:
* Fill in your `OpenAI`, `Pinecone API`, and Pinecone server details.
* Follow the steps to create a Pinecone server and upload your material.
2. Open `Query.ipynb`:
* Fill in your `OpenAI`, `Pinecone API`, and Pinecone server details.
* Interact with the GPT customer service bot. Ask questions, and the bot will search the material you've uploaded to Pinecone to provide answers.

# Previous Work / Foreseen Challenges
## Previous Work
In our earlier attempts to build an efficient and responsive customer service bot, we explored various local deployment models. Among them:

* Dolly2: While Dolly2 offered a promising start, we found that its performance in our specific use case was not up to par. Its limitations in handling complex queries and providing concise answers led us to search for better alternatives.

* GPT4All: Similarly, GPT4All, despite its widespread use, did not yield satisfactory results in our application. The smaller, locally deployed model had constraints in terms of processing power and versatility.

Given the challenges we faced with these models, we decided to pivot our approach.

## Current Approach
Our present strategy is to leverage the GPT API. There are several reasons for this shift:

* Maintenance and Usability: Using the GPT API simplifies the maintenance process. We no longer have to worry about updates, optimizations, and other technical intricacies that come with local deployments.

* Flexibility: With the integration of Pinecone, we can easily upload and adjust our knowledge base. This means that our customer service bot can be updated with new information, making it more versatile and adaptive to changing needs.

## Foreseen Challenges
One of the challenges we anticipate as we continue to refine our bot is addressing the hallucination issue associated with the larger language models (LLMs) like GPT. Hallucination in the context of LLMs refers to the model generating information that may not be accurate or factual. As customer service accuracy is paramount, we will be focusing our efforts on:

* Detection: Implementing mechanisms to detect when the model might be hallucinating.

* Correction: Developing methods to correct or redirect the output in real-time, ensuring that the information provided is accurate and reliable.

Our team is committed to overcoming these challenges to provide the best possible service to our users.

# Data
All materials required to train the model, i.e., deFacto's training materials, are readily available. The format may need to be adjusted based on the LLM's requirements.

# License
MIT
