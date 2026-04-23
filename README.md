# Text-to-SQL-AI-Agent
Production-Grade Text-to-SQL AI Agent (AWS Bedrock)

🚀 Production-Grade Text-to-SQL AI Agent (AWS Bedrock)

An AI-powered system that converts natural language queries into executable SQL using Large Language Models (LLMs). This project enables non-technical users to interact with structured databases through simple English queries.

# Overview

This project implements a Text-to-SQL AI Agent that:

Translates user questions → SQL queries
Executes queries on a database
Returns structured results in a human-readable format

Built with a GenAI + serverless architecture, the system leverages LLM reasoning, schema awareness, and agentic workflows for accurate query generation.

# Key Features

🔹 Natural Language → SQL conversion using LLMs

🔹 Schema-aware prompting for improved query accuracy

🔹 Support for complex queries (joins, filters, aggregations)

🔹 Agentic workflow for query refinement and error handling

🔹 Serverless and scalable architecture using AWS

🔹 Fast and low-latency responses


# Architecture

User Query

   ↓
   
API Gateway

   ↓
   
AWS Lambda

   ↓
   
AWS Bedrock (LLM)

   ↓
   
SQL Query Generation

   ↓
   
Database Execution

   ↓
   
Response Formatting

   ↓
   
User Output

# Tech Stack

LLM: AWS Bedrock

Frameworks: LangChain

Backend: AWS Lambda, API Gateway

Database: MySQL / PostgreSQL

Vector Store (optional): FAISS / Pinecone

Language: Python

🚀 How It Works

User enters a natural language query

Example: “Show top 5 customers by revenue”

The system:
Understands intent using LLM
Injects database schema into prompt
Generates SQL query
Query is validated and executed

Results are returned in a readable format

# Example

Input:

Get total sales by region for last quarter

Generated SQL:

SELECT region, SUM(sales) 
FROM orders 
WHERE order_date >= DATE_SUB(CURDATE(), INTERVAL 3 MONTH)
GROUP BY region;

# Performance Optimizations

Prompt engineering for improved SQL accuracy

Schema injection for context awareness

Query validation to prevent invalid SQL execution

Optimized Lambda execution for low latency

# Future Improvements

Add query caching for faster responses

Fine-tune LLM using LoRA/QLoRA for domain-specific SQL generation

Add role-based access control

Integrate with BI dashboards

# Use Cases

Business analytics for non-technical users

Data exploration tools

Internal enterprise assistants

Self-service BI systems

# Contact

Feel free to connect if you’re working on GenAI, LLMs, or AI Agents!

⭐ If you like this project, give it a star!
