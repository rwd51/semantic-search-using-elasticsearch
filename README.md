Here's your README with the Kaggle link properly hyperlinked:

# Fashion Product Semantic Search
A semantic search application for fashion products that uses vector embeddings and Elasticsearch to find products based on natural language queries.

## Overview
This project implements semantic search capabilities for fashion product data. Instead of relying on exact keyword matching, the system converts product descriptions into vector embeddings that capture semantic meaning, allowing users to find relevant products even when their search terms don't exactly match the product descriptions.

## Features
- **Semantic Search**: Find products based on meaning, not just keywords
- **Vector Embeddings**: Utilizes a language model to convert text to high-dimensional vectors
- **Elasticsearch Integration**: Leverages Elasticsearch's vector search capabilities
- **Streamlit UI**: Simple and intuitive user interface for search queries

## Technologies
- **Python**: Core programming language
- **Elasticsearch**: For storing and searching vector embeddings
- **Sentence Transformers**: For generating text embeddings
- **Pandas**: For data manipulation and processing
- **Streamlit**: For the web interface

## Setup
### Prerequisites
- Python 3.13.1
- Elasticsearch 8.17.3
- At least 10% free disk space for optimal Elasticsearch performance

### Installation
1. Clone the repository:
   ```
   git clone https://github.com/yourusername/fashion-product-search.git
   cd fashion-product-search
   ```
2. Create and activate a virtual environment:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
4. Start Elasticsearch:
   ```
   # Navigate to your Elasticsearch directory
   ./bin/elasticsearch
   ```

## Usage
1. Data Preparation:
   - Load your fashion product data into a pandas DataFrame
   - Generate vector embeddings for product descriptions
   - Convert to the format required by Elasticsearch

2. Indexing:
   - Create the Elasticsearch index with vector field mapping
   - Index the documents with their vector representations

3. Running the Search App:
   ```
   streamlit run searchApp.py
   ```

4. Performing searches:
   - Enter natural language queries in the Streamlit interface
   - View matching fashion products based on semantic similarity

## Future Improvements
- Implement user feedback mechanisms to improve search results
- Add filtering by product attributes (price, brand, color, etc.)
- Implement image-based search using visual embeddings
- Deploy as a web service with proper SSL certificate handling

## Troubleshooting
### Common Elasticsearch Issues
- **Disk Space**: Ensure at least 10% free disk space for optimal performance
- **TLS/SSL Errors**: Set `verify_certs=False` for development environments
- **Connection Issues**: Check if Elasticsearch is running and properly configured

## Acknowledgements
- Thanks to [Myntra Products Dataset](https://www.kaggle.com/datasets/ronakbokaria/myntra-products-dataset) for providing the fashion product data
- Built with Elasticsearch and Streamlit
