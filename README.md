# Personal-Document-Explainer-Agent
Low-Vision &amp; Rural Personal Document Explainer Agent 

Title: Low-Vision & Rural Personal Document Explainer Agent

An autonomous, stateful, multi-step agentic pipeline built entirely on n8n Cloud designed to ingest, process, audit, and verbally synthesize physical text documents for visually impaired and rural individuals.

The Multi-Step Pipeline Flow:

[Webhook Intake Node] ➔ [HTTP: Nebius Llama 3.2 Vision] ➔ [HTTP: Keenable Search] ➔ [HTTP: ElevenLabs TTS]
• Node 1 (Webhook Trigger): Acts as the secure interface entry point, mimicking a mobile application or messaging bot interface where a low-vision user uploads an image of physical mail.
• Node 2 (Vision Processing Engine): Integrates Meta Llama 3.2 11B Vision Instruct via a custom Nebius/Fireworks endpoint override to dynamically analyze pixel layouts, check text legibility, and extract structural data.
• Node 3 (Autonomous Tool Use - Keenable Search): Connects to the Keenable Web Search API to parse the extracted metadata, searching the live web to verify official corporate customer support contact info and flag potential mail scams.
• Node 4 (Vocal User Interface - ElevenLabs API): Calls the ElevenLabs Text-to-Speech API utilizing the eleven_multilingual_v2 model to synthesize the final verified report into human speech.
