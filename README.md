# 🪷 Natya.AI

### AI-Powered Indian Classical Dance Movement & Mudra Recognition

Natya.AI is an AI-powered platform designed to help people understand the meaning and significance behind Indian classical dance movements and hand gestures.

Many people watch traditional Indian dances but may not understand the meaning behind specific **mudras, poses, and movements**. Natya.AI addresses this problem by using **computer vision and AI** to analyze dance movements and provide meaningful information to the user.

The initial focus of the project is **Bharatanatyam**, with the architecture designed to support other Indian classical dance forms in the future.

---

## 🎯 Problem Statement

Indian classical dances contain a rich collection of hand gestures, body movements, poses, and expressions that communicate stories, emotions, and cultural meanings.

However, viewers who are unfamiliar with the traditional dance forms may find it difficult to understand:

- What a particular hand gesture represents
- What a specific dance pose means
- How movements are interpreted according to traditional knowledge
- The cultural significance behind different gestures

Natya.AI aims to bridge this gap between **traditional knowledge and modern technology**.

---

## 💡 Our Solution

Natya.AI allows users to use their camera or upload a dance video/image.

The system analyzes the dancer's body and hand positions using computer vision and AI techniques and identifies relevant dance movements or mudras.

The platform then provides:

- 🕺 Detected dance movement
- 🤲 Hand mudra recognition
- 📖 Meaning and interpretation
- 🪷 Cultural significance
- 📚 Relevant traditional knowledge
- 🤖 AI-generated additional information

---

## ✨ Features

### 🎥 Real-Time Dance Analysis
Analyze dance movements through the camera and process the dancer's pose in real time.

### 🦴 Pose Detection
Uses computer vision techniques to detect important body landmarks and create a skeletal representation of the dancer.

### 🤲 Mudra Detection
Analyzes hand landmarks and identifies relevant hand gestures used in Indian classical dance.

### 🧠 Dance Pose Classification
Extracted pose and hand features are processed to classify the detected dance movement.

### 📚 Cultural Knowledge
Provides information about the meaning and significance of detected movements based on traditional Indian dance knowledge.

### 🤖 AI-Powered Information
Generative AI can be used to provide additional explanations and contextual information about the detected movement.

### 🌐 Web-Based Platform
Users can access the system through a web interface without requiring specialized hardware.

---

## 🏗️ System Architecture

```text
                ┌──────────────────┐
                │      User        │
                │ Camera / Video   │
                └────────┬─────────┘
                         │
                         ▼
                ┌──────────────────┐
                │   React Frontend │
                │   + Tailwind CSS │
                └────────┬─────────┘
                         │
                         ▼
                ┌──────────────────┐
                │   Video / Frame  │
                │     Processing   │
                └────────┬─────────┘
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
      ┌───────────────┐     ┌───────────────┐
      │ Pose Detection│     │ Hand Detection│
      │   MediaPipe   │     │   MediaPipe   │
      └───────┬───────┘     └───────┬───────┘
              │                     │
              └──────────┬──────────┘
                         ▼
                ┌──────────────────┐
                │ Feature Extraction│
                │ & Pose Analysis   │
                └────────┬─────────┘
                         │
                         ▼
                ┌──────────────────┐
                │ Dance Pose /     │
                │ Mudra Classifier │
                └────────┬─────────┘
                         │
                         ▼
                ┌──────────────────┐
                │ Cultural Meaning │
                │ & Interpretation │
                └────────┬─────────┘
                         │
                         ▼
                ┌──────────────────┐
                │      Result      │
                │ Meaning + Info   │
                └──────────────────┘
