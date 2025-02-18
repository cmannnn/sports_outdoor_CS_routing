# DTSA 5511 - Intro to Deep Learning

## Building a Customer Service Router for Outdoor Gear Retail

## Overview

In this project, we will aim to develop a customer service routing system that will aid outdoor gear and apparel customer questions to route text inquiries into three distinct categories. This classification system could be implemented as a tool for an online outdoor gear customer service tean to more efficiently route customer questions to specific individuals with knowledge on the topic. The tool would be able to streamline the following:

Reducing response time through automatic routing
Ensuring consistent handling of common inquiry types
Allowing customer service representatives to focus on complex cases
This project will utilize deep learning, specifically a Bidirectional Long Short-Term Memory (BiLSTM) neural network architecture with attention mechanisms to classify customer inquiries into three distinct categories.

The Data
To train the BiLSTM model, we will be using the Amazon Sports & Outdoors product dataset. This dataset contains product reviews and metadata from Amazon including 12.8 million reviews from May 1996 -> July 2014. While the dataset wasn't originally designed for customer service applications, the customer insights included is very valuable to train a BiLSTM model for a project such as this. The dataset includes reviews including rating specific columns (text, a helpfulnes score, etc.) and product columns (descriptions, category info, price, brand, image features, etc.).

Intent Classification System
The model that will be developed in this notebook will aim to accurately categorize customer questions into three categories:

Sizing Questions (fit guidance, size comparisons)
Technical Specifications (material properties, product features)
Product Recommendations (=gear suggestions based on use case)
There will also be a catch all 'other' category.

Technical Implementation
From a technical perspective a BiLSTM architecture model will be built and trained with bi-directional processing, attention mechanisms that will provide greater weight to critial parts of a customer quesion, word embeddings to capture semantic relationships.

Here is a step by step overview to on how the BiLSTM classifier will be implemented.

Input Processing
Customer inquiries are tokenized and converted into word embeddings. Then these sequences are standardized.

Core Architecture
The Bidirectional LSTM layers will process text in both a forward and backward manner. Attention mechanisms will achieve to identify key phrases. Dropout layers will attempt to prevent overfitting. Dense layers will map to the final classifications.

This system will serve as an automated customer service routing system with the ability for potential expansion and implementation to a online outdoor gear platform.
