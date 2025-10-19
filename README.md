# EEGC AI Training and Assessment Component

## Project Overview
This repository contains the complete documentation and implementation for the EEGC (English for Academic and Professional Communication) AI Training and Assessment Component, designed for remedial English courses at HKBU.

## Folder Structure

### 📁 `reference/`
Contains reference materials and sample content:
- `model_Russell.md` - Bertrand Russell's "What I Have Lived For" model essay
- `rubrics4essay.md` - Essay assessment rubrics (5-point scale)
- `rubrics4AIcommunication.md` - AI communication skills rubrics
- `sampleEssay2edit.md` - Sample essay for student practice

### 📁 `docs/`
Documentation and design materials:

#### `docs/design/`
UI/UX design files and prototypes:
- `briefing.html` - Comprehensive briefing page with platform information
- `intro-to-AI-tutor.html` - AI tutor introduction interface
- `training.html` - Training mode interface prototype

#### `docs/chat/`
Chat history and agent conversations (to be populated)

#### Documentation Files:
- `learning-objectives-and-context.md` - Complete learning objectives and course context
- `user-journey-training-mode.md` - Detailed user journey with Russell model integration
- `ui-design-analysis.md` - Analysis of training.html UI design
- `ui-expectations-training-mode.md` - UI specifications for contextualized interface
- `redesign-requirements.md` - Requirements for redesigning the HTML page

### 📁 `implementation/`
Vue.js frontend application:
- `new-bytewise-frontend/` - Cleaned Vue.js application focused on EEGC
  - `src/botConfig/` - EEGC-specific bot configurations (3 files)
  - `src/components/writing_bot/` - Writing bot components (6 files)
  - `src/views/WritingBot.vue` - Main EEGC interface
  - Simplified router focused on writing and essay training

## Key Features

### Three-Mode Structure
1. **Briefing Mode**: Introduction to AI collaboration skills
2. **Training Mode**: Guided practice with contextualized UI
3. **Assessment Mode**: Independent demonstration of AI skills

### Russell Model Integration
- Students learn essay structure using Bertrand Russell's "What I Have Lived For"
- Clear thesis with 2-3 specific points
- Topic sentences that echo thesis points
- Detailed paragraph development

### Assessment Framework
- **Dual Assessment**: Essay quality + AI communication skills
- **5-Point Rubric**: Content, Organisation, Vocabulary, Grammar
- **AI Skills**: Context provision, goal negotiation, critical evaluation, strategic implementation

### UI Design
- **Contextualized Interface**: Purpose-specific input boxes replace traditional chat
- **Training Mode**: Guided learning with provided context
- **Assessment Mode**: Independent context provision and goal setting
- **Targeted AI Responses**: Specific feedback areas for different interaction types

## Technical Implementation
- **Frontend**: Vue.js 3 with Vite
- **Styling**: Tailwind CSS
- **AI Integration**: Poe platform with Claude-Sonnet-4
- **Assessment**: Automated dual assessment system

## Getting Started
1. Navigate to `implementation/new-bytewise-frontend/`
2. Install dependencies: `npm install`
3. Run development server: `npm run dev`
4. Access the application at `http://localhost:5173`

## Repository Status
- **Git Remote**: https://github.com/tesolchina/eegcaiEdit.git
- **Branch**: main
- **Status**: All files organized and ready for development

## Implementation Notes
- **AI Tutor Backend**: See `KAI_TAI_IMPLEMENTATION_NOTES.md` for comprehensive implementation guidance
- **Four Learning Goals**: Context provision, goal negotiation, critical review, independent work
- **Assessment Framework**: Dual assessment (essay quality + AI communication skills)
- **Technical Requirements**: Multi-turn conversations, rubric scoring, progress tracking

## Key Implementation Files
- `KAI_TAI_IMPLEMENTATION_NOTES.md` - Complete backend implementation guide
- `docs/design/mockup_split/index.html` - Unified training interface
- `reference/four-goals-of-learning-ai.md` - Learning goals framework
- `reference/AI-communication-rubrics.md` - Assessment criteria
- `reference/sampleEssay2edit.md` - Practice essay with specific issues

---

*This project supports the development of AI literacy skills in academic writing contexts, following HKBU's LANG 0036 curriculum requirements.*
