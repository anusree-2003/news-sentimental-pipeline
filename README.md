# **News Sentiment Analysis Pipeline**

A cloud-native pipeline to fetch real-time news, analyze sentiment using TESTBLOB, store it in PostgreSQL (RDS), and visualize insights via a Streamlit dashboard hosted on ECS Fargate.

---

## **Architecture**

![Architecture Diagram](architecture.jpeg)

---

## **Tech Stack**

- **AWS Lambda** – News fetching & sentiment scoring  
- **Amazon RDS** – PostgreSQL for structured sentiment storage  
- **Amazon S3** – Store raw JSON files  
- **Amazon ECS Fargate** – Hosts the Streamlit dashboard  
- **Amazon EventBridge** – Triggers Lambda every 5 minutes  
- **Streamlit** – Dashboard to display sentiment trends  
- **Docker + ECR** – For containerized dashboard deployment

---

## **Features**

- Automated news fetching from News API  
- Real-time sentiment analysis 
- Raw and structured storage using S3 & RDS  
- Dockerized Streamlit dashboard  
- Serverless and cost-effective architecture

## **Overview**

This project is an end-to-end cloud-based pipeline that automates the collection, analysis, and visualization of news sentiment using a fully serverless and containerized architecture on AWS. It fetches real-time news articles from an external API every 5 minutes using Amazon EventBridge to trigger an AWS Lambda function. The Lambda function stores raw news data in Amazon S3 and inserts it into Amazon RDS (PostgreSQL). Sentiment analysis is performed locally using TextBlob, and the results are visualized through a Streamlit dashboard. The dashboard is containerized, pushed to Amazon ECR, and deployed via Amazon ECS Fargate. This architecture enables scalable, real-time sentiment tracking of news content with minimal operational overhead.
