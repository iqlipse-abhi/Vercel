# Code Deployment Service

This project is a **Code Deployment Service** that automates the process of deploying repositories, uploading files to AWS S3, and managing deployment tasks using Redis queues. The service supports repository cloning, file uploads, status tracking, and content retrieval from S3 based on dynamic subdomains, similar to Vercel's deployment process.

## Features

- **Backend API**:  
  - An Express-based API built using TypeScript for managing repository cloning, file uploads, and deployment status updates.
  - Integrates with AWS S3 for file storage and retrieval, including metadata handling.
  - Redis queue management for task processing and deployment tracking.

- **Repository Cloning & Deployment**:  
  - Clone Git repositories using `simple-git`.
  - Process repository files and deploy them by uploading to S3.

- **AWS S3 File Management**:  
  - Upload and download files to/from AWS S3.
  - Supports folder downloads from S3.
  - Upload directories with metadata (e.g., content-type for HTML files).

- **Redis Queue Management**:  
  - Use Redis queues to handle deployment tasks, track statuses, and update users on deployment progress.

- **Dynamic Subdomain-based Deployment**:  
  - Deploy content dynamically based on the subdomain (e.g., `id.vercel.com`), retrieving content from the corresponding S3 bucket.

## Technologies Used

- **Node.js**
- **TypeScript**
- **Express.js**
- **AWS SDK** (S3)
- **Redis** (Queue Management)
- **simple-git** (Git Operations)
- **CORS** (Cross-Origin Resource Sharing)

## Installation

Follow these steps to set up and run the project:

### Prerequisites

- Node.js (>=14.x)
- npm (>=6.x)
- Redis (Running locally or using a cloud instance)
- AWS Account (for S3 access)

### Setup Instructions

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
