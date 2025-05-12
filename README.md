# Auto-short-video-agent
End-to-end AI pipeline that generates multilingual short videos using LangGraph, OpenAI, ElevenLabs, and Pexels. Perfect for TikTok, Reels, and Shorts.


# 🎬 AI-Powered Multimodal Video Generator (LangGraph + OpenAI + ElevenLabs + Pexels)

This project is a complete, end-to-end AI agent pipeline that generates a short educational video using:
- 🧠 OpenAI (ChatGPT) for title and script
- 🖼️ Pexels API for visuals
- 🎙️ ElevenLabs for multilingual voiceover
- 🎞️ FFmpeg for video creation and post-processing
- 🧠 LangGraph for orchestration

---

## 🚀 Features
- Title and script generation using OpenAI
- Visual tag extraction + image search via Pexels
- Voice generation using ElevenLabs (multilingual model)
- Visual-to-video rendering via FFmpeg
- Audio-video combination in vertical format (TikTok / Reels / Shorts)

---

## 📦 Requirements

Sample Output:
🎯 Title: Why the Brain Uses 20% of the Body's Energy  
📜 Script: The human brain represents only 2% of our body mass, but it consumes over 20% of our energy...  
🖼️ Prompts: ['brain energy', 'neural activity', 'cognition', ...]  
🌐 Images: ['https://images.pexels.com/...']  
🎧 Audio File: output_audio_fast.mp3  
🎞️ Video Path: final_tiktok_ready.mp4

Architecture
[Title Generator] → [Script Writer] → [Image Tagger] → [Image Search] → 
[Voice Generator] → [Video Generator] → [Audio+Video Combine] → ✅ Done!

bash
pip install langgraph langchain langchain-openai langchain-community requests pydub
sudo apt-get install ffmpeg  # if not already installed

How It Works
output = graph.invoke({
    "topic": "",
    "script": "",
    "image_prompts": [],
    "image_urls": [],
    "audio_path": "",
    "video_path": "",
    "final_path": "",
    "last_topics": []
})



