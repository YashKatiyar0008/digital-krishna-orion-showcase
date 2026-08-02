# Project Overview

## Inspiration

Digital Krishna explores how culturally familiar wisdom can be translated into responsible, practical reflection without claiming divine authority.

## Problem

General assistants may be generic, culturally disconnected, inconsistent across English, Hindi, and Hinglish, or unreliable when quoting spiritual sources.

## Target users

People seeking reflective, culturally grounded general guidance in English, Hindi, or Hinglish. It is not intended for emergencies, diagnosis, treatment, or professional decision-making.

## Product vision

Offer accessible guidance that combines thoughtful clarification, structured next steps, transparent limitations, and source verification when exact teachings matter.

## What Digital Krishna does

It interprets a user's general-life question, asks for clarification when needed, and produces structured guidance through text, scripture, voice-oriented, and story experiences. The private product includes a React web interface, Python backend, Krishna and Saathi chat, journaling, breathing, scripture reading, and stories. Public screenshots and demo links are still being prepared.

## Why SFT was necessary

Supervised fine-tuning is intended to teach stable behavior: tone, multilingual style, clarification, culturally appropriate framing, safety boundaries, and action-oriented structure. Training completion and results remain subject to evidence verification.

## Why this is not only a chatbot

The conversational interface is one delivery layer. The project also encompasses dataset design, model adaptation, evaluation, safety policy, verified retrieval, and experience formats.

## Multilingual design

The target languages are English, Hindi, and Hinglish. Evaluation must separately test meaning, fluency, tone, code-switching, and safety in each.

## Practical guidance framework

The intended response pattern is: understand the situation, clarify ambiguity, frame a grounded perspective, suggest small actions, and state limitations. Exact private templates are not disclosed.

## Responsible cultural AI

The system avoids impersonating a deity, unsupported quotations, guaranteed outcomes, and replacing qualified professionals. Cultural interpretations should be respectful and presented with appropriate uncertainty.

## Current scope

The current scope includes a private Qwen3 1.7B LoRA adapter, a private 1,760-conversation SFT corpus, English/Hindi/Hinglish interaction, deterministic safety and retrieval checks, and a private web product. The public repository exposes documentation, sanitized samples, methodology, and verified summaries only.

## Future roadmap

Complete blind base-versus-SFT evaluation, conduct human review of the 97 held-out conversations, publish redacted evidence, improve mobile accessibility, expand verified retrieval, and evaluate a scalable private deployment.
