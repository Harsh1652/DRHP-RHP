# Smart RHP/DRHP Platform

A specialized AI-powered solution designed to simplify and accelerate the review of Red Herring Prospectus (RHP) and Draft Red Herring Prospectus (DRHP) documents. This platform enables secure document management, intelligent summarization, interactive exploration, and automated comparison between draft and final versions.

## 📋 Overview

Financial documents such as RHPs and DRHPs are often lengthy, complex, and difficult for stakeholders to analyze efficiently. The Smart RHP/DRHP Platform consolidates manual effort into an intelligent assistant, allowing investors, analysts, and corporate teams to quickly identify important details, track changes between versions, and generate comparison reports with clarity and confidence.

## 🎯 Problem Statement

Financial documents such as RHPs and DRHPs present multiple challenges for stakeholders:

### Length and Complexity
These filings often run into hundreds of pages, filled with legal, financial, and regulatory language that is difficult to parse quickly.

### Inefficient Manual Review
Teams spend days manually extracting insights, comparing drafts with final versions, and preparing executive summaries, which slows decision making.

### Difficulty in Tracking Changes
Between DRHP and RHP versions, important adjustments are often buried within dense paragraphs, making it hard to track what has changed and why.

### Limited Accessibility of Insights
Once comparison reports are prepared, they often remain static documents. Stakeholders cannot ask dynamic questions or explore content beyond the original summary.

## 💡 Solution Overview

The Smart RHP/DRHP Platform directly addresses these pain points by introducing a modern, AI-powered workspace:

- **Intelligent Summarization**: Automatic generation of concise, accurate summaries of lengthy documents so readers can focus on key insights without wading through every page.

- **Interactive Exploration**: A chat-based interface that allows users to ask questions in plain language and receive document-grounded answers instantly.

- **Automated Comparison**: Side-by-side comparison between DRHP and RHP versions, highlighting textual, numerical, and structural changes to support faster decision making.

- **Streamlined Report Generation**: On-demand creation of professional comparison reports in user-friendly formats, ready for boardrooms, client discussions, or compliance reviews.

## 🏗️ Technical Architecture

The platform is built using **n8n** workflow automation with the following technology stack:

### Core Technologies

- **Workflow Engine**: [n8n](https://n8n.io/) - Open-source workflow automation platform
- **Vector Database**: [Pinecone](https://www.pinecone.io/) - Vector database for storing document embeddings
- **Embedding Model**: OpenAI GPT-3.5 Large - For creating document embeddings
- **Chat Model**: OpenAI GPT-4.1 Mini - For interactive chat functionality
- **Reranking**: Cohere Rerank - For ranking and improving search relevance

### Workflow Process

1. **Document Upload**: Users upload RHP/DRHP documents through the n8n workflow
2. **Embedding Generation**: Documents are processed and embeddings are created using OpenAI GPT-3.5 Large model
3. **Vector Storage**: Embeddings are stored in Pinecone vector database for efficient retrieval
4. **Reranking**: Cohere Rerank is used to improve the relevance of retrieved embeddings
5. **Interactive Chat**: Users can chat with documents using OpenAI GPT-4.1 Mini model
6. **Document Summarization**: Automatic generation of comprehensive summaries
7. **Comparison Analysis**: Automated comparison between DRHP and RHP versions

## ✨ Features

- 📄 **Document Management**: Secure upload and storage of RHP/DRHP documents
- 🤖 **AI-Powered Summarization**: Automatic generation of accurate, comprehensive summaries
- 💬 **Interactive Chat Interface**: Ask questions and get instant, document-grounded answers
- 🔍 **Intelligent Search**: Vector-based semantic search with reranking for improved accuracy
- 📊 **Version Comparison**: Automated comparison between draft and final versions
- 📈 **Report Generation**: On-demand creation of professional comparison reports

## 🚀 Getting Started

### Prerequisites

- n8n instance (self-hosted or cloud)
- Pinecone account and API key
- OpenAI API key
- Cohere API key
- Google Drive API credentials (for document access)

### Installation

1. Clone this repository:
```bash
git clone https://github.com/Harsh1652/DRHP-RHP.git
cd DRHP-RHP
```

2. Import the workflow:
   - Open your n8n instance
   - Import the `N8n.json` workflow file
   - Configure the required credentials:
     - OpenAI API credentials
     - Pinecone API credentials
     - Cohere API credentials
     - Google Drive OAuth credentials (if using Google Drive integration)

3. Configure the workflow:
   - Update API endpoints and credentials in the workflow nodes
   - Configure Pinecone index settings
   - Set up document upload endpoints

4. Activate the workflow in n8n

## 📖 Usage

### Uploading Documents

1. Upload your RHP/DRHP document through the configured endpoint
2. The system automatically processes the document and creates embeddings
3. Documents are stored in Pinecone vector database

### Chatting with Documents

1. Access the chat interface
2. Ask questions in plain language about the document content
3. Receive instant, accurate answers based on the document content

### Viewing Summaries

1. Navigate to the summary section
2. View automatically generated summaries of key sections
3. Export summaries for further analysis

### Comparing Versions

1. Upload both DRHP and RHP versions
2. The system automatically identifies and highlights changes
3. Generate comparison reports for review

## 🔧 Configuration

### Environment Variables

Ensure the following environment variables are configured in your n8n instance:

- `OPENAI_API_KEY`: Your OpenAI API key
- `PINECONE_API_KEY`: Your Pinecone API key
- `PINECONE_ENVIRONMENT`: Your Pinecone environment
- `COHERE_API_KEY`: Your Cohere API key

### Pinecone Index Configuration

- Create a Pinecone index with appropriate dimensions for your embedding model
- Configure the index name in the workflow nodes

## 📁 Project Structure

```
DRHP-RHP/
├── N8n.json          # n8n workflow configuration
└── README.md         # Project documentation
```

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👥 Authors

- **Harsh1652** - [GitHub Profile](https://github.com/Harsh1652)

## 🙏 Acknowledgments

- n8n for the workflow automation platform
- OpenAI for embedding and chat models
- Pinecone for vector database infrastructure
- Cohere for reranking capabilities

## 📞 Support

For issues, questions, or contributions, please open an issue on the [GitHub repository](https://github.com/Harsh1652/DRHP-RHP).

---

**Note**: This platform is designed for financial document analysis and should be used in compliance with relevant regulations and data privacy requirements.
