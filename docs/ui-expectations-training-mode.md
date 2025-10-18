# UI Expectations - Training Mode Interface

## Overview
The training mode interface replaces the conventional chatbot UI with a more contextualized, structured approach. Students interact with specific input boxes and receive targeted AI responses in designated areas, creating a guided learning experience.

## Core UI Design Principles

### 1. Contextualized Input System
**Replaces**: Traditional chat input
**With**: Purpose-specific input boxes with clear labels and instructions

### 2. Targeted Response Areas
**Replaces**: General chat responses
**With**: Specific response boxes for different types of AI feedback

### 3. Guided Learning Structure
**Replaces**: Open-ended conversation
**With**: Step-by-step guided interactions with clear objectives

## Detailed UI Components

### Phase 1: Context Confirmation (Training Mode Only)
**Objective**: Students confirm understanding of provided contextual information

#### Context Display Section
- **Rubrics Display**: Essay assessment criteria (Content, Organisation, Vocabulary, Grammar)
- **Course Information**: LANG 0036 details and module information
- **Russell Model Essay**: "What I Have Lived For" with interactive annotations
- **Assessment Framework**: AI communication skills rubric

#### Student Action
- **Confirmation Button**: "I understand the context and am ready to proceed"
- **No input required**: Information is provided, students just confirm understanding

### Phase 2: Thesis Statement Assessment

#### Step 1: Locate Thesis Statement
**UI Component**: Essay text with clickable sentences
- **Student Action**: Click on thesis statement
- **AI Response Area**: Confirmation and explanation

#### Step 2: Combined Thesis Assessment
**Replaces**: Separate steps 2 and 3
**New Structure**: Single assessment with two criteria

**Input Box 1: Question Answering Check**
- **Label**: "Does your thesis directly answer the essay question?"
- **Student Input**: Text box for explanation
- **AI Response Area**: Targeted feedback on question alignment

**Input Box 2: Points Development Check**
- **Label**: "Does your thesis include 2 specific points that can be developed?"
- **Student Input**: Text box for explanation
- **AI Response Area**: Targeted feedback on point specificity

#### Step 3: Thesis Revision
**Input Box**: "Revise your thesis statement"
- **Student Input**: Text area for revised thesis
- **AI Response Area**: Assessment of revised thesis against both criteria

### Phase 3: Agenda and Goals Negotiation

#### Training Mode: Guided Goals Setting
**UI Components**:

**System-Provided Goals Box**:
- **Label**: "Suggested revision goals based on your essay"
- **Content**: Pre-populated with AI-suggested goals
- **Examples**: "Improve thesis statement clarity", "Strengthen topic sentences", "Enhance paragraph development"

**Student Goals Selection Box**:
- **Label**: "Select your priority goals"
- **UI**: Checkbox list of suggested goals
- **Additional Input**: Text box for custom goals

**Goals Confirmation Box**:
- **Label**: "Your selected revision goals"
- **Display**: Summary of chosen goals
- **Action**: "Confirm these goals and proceed"

#### Assessment Mode: Independent Goals Setting
**UI Components**:

**Context Information Boxes** (Student must provide):
- **Course Information**: Text input for course details
- **Assignment Details**: Text input for task description
- **Time Constraints**: Text input for available time
- **Assessment Criteria**: Text input for evaluation expectations

**Goals Setting Boxes**:
- **Primary Goals**: Text input for main revision objectives
- **Secondary Goals**: Text input for additional objectives
- **Priority Ranking**: Dropdown/selection for goal prioritization

**Submission Area**:
- **Submit Button**: "Submit context and goals"
- **AI Response Area**: Confirmation and feedback on provided information

### Phase 4: Critical Review of AI Responses

#### Training Mode: Guided Questioning
**UI Components**:

**AI Suggestion Display Box**:
- **Label**: "AI's revision suggestions"
- **Content**: AI-generated editing recommendations
- **Format**: Structured display of suggestions

**Guided Questioning Box**:
- **Label**: "Ask the AI to explain its suggestions"
- **Hints Provided**: 
  - "Ask: 'Can you explain why you suggest this change?'"
  - "Ask: 'How does this relate to the rubric criteria?'"
  - "Ask: 'What specific improvements will this make?'"
- **Student Input**: Text box for questions
- **AI Response Area**: Targeted explanations

**Critical Evaluation Box**:
- **Label**: "Evaluate the AI's suggestions"
- **Student Input**: Text area for critical analysis
- **AI Response Area**: Feedback on evaluation quality

#### Assessment Mode: Independent Critical Review
**UI Components**:

**AI Suggestion Display Box**:
- **Label**: "AI's revision suggestions"
- **Content**: AI-generated editing recommendations

**Student Question Box**:
- **Label**: "Ask questions about the suggestions"
- **Student Input**: Text area for independent questioning
- **AI Response Area**: AI explanations

**Critical Analysis Box**:
- **Label**: "Your critical evaluation"
- **Student Input**: Text area for independent analysis
- **AI Response Area**: Feedback on critical thinking

### Phase 5: Independent Writing and Editing

#### Training Mode: Guided Implementation
**UI Components**:

**Revision Implementation Box**:
- **Label**: "Implement your chosen revisions"
- **Student Input**: Text area for revised content
- **AI Response Area**: Feedback on implementation

**Self-Assessment Box**:
- **Label**: "Reflect on your changes"
- **Student Input**: Text area for self-reflection
- **AI Response Area**: Guidance on self-assessment

#### Assessment Mode: Independent Implementation
**UI Components**:

**Final Revision Box**:
- **Label**: "Your final revised essay"
- **Student Input**: Large text area for complete essay
- **AI Response Area**: Final assessment feedback

## UI Layout Structure

### Main Interface Layout
```
┌─────────────────────────────────────────────────────────┐
│                    Header Section                       │
│              (Progress, Points, Badges)                 │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────┐  ┌─────────────────────────────┐  │
│  │   Input Area    │  │     AI Response Area        │  │
│  │                 │  │                             │  │
│  │ [Purpose Box]   │  │ [Targeted Feedback]         │  │
│  │ [Student Input] │  │ [AI Analysis]               │  │
│  │ [Action Button] │  │ [Suggestions]               │  │
│  └─────────────────┘  └─────────────────────────────┘  │
│                                                         │
│  ┌─────────────────────────────────────────────────────┐ │
│  │              Context Display Area                   │ │
│  │        (Rubrics, Russell Model, etc.)              │ │
│  └─────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────┘
```

### Responsive Design Considerations
- **Desktop**: Side-by-side input and response areas
- **Tablet**: Stacked layout with collapsible sections
- **Mobile**: Full-width stacked layout with touch-friendly inputs

## Key UI Features

### 1. Purpose-Specific Input Boxes
- **Clear Labels**: Each input box has a descriptive label
- **Instructions**: Contextual help text for each input
- **Validation**: Real-time feedback on input quality

### 2. Targeted AI Response Areas
- **Structured Responses**: AI feedback organized by purpose
- **Visual Hierarchy**: Different response types clearly distinguished
- **Actionable Feedback**: Specific suggestions for improvement

### 3. Progress Tracking
- **Visual Progress**: Clear indication of completed steps
- **Skill Development**: Tracking of specific skill acquisition
- **Achievement System**: Badges and points for motivation

### 4. Contextual Help System
- **Tooltips**: Hover explanations for complex concepts
- **Examples**: Model responses and sample inputs
- **Hints**: Progressive disclosure of guidance

## Training vs Assessment Mode Differences

### Training Mode Features
- **Guided Inputs**: Pre-filled suggestions and hints
- **Step-by-Step**: Clear progression through tasks
- **Educational Focus**: Learning-oriented feedback
- **Context Provided**: All necessary information displayed

### Assessment Mode Features
- **Independent Input**: Students must provide all context
- **Minimal Guidance**: Reduced scaffolding
- **Evaluation Focus**: Assessment-oriented feedback
- **Self-Directed**: Students drive the interaction

## Accessibility Features

### Visual Accessibility
- **High Contrast**: Clear color differentiation
- **Font Sizing**: Adjustable text sizes
- **Focus Indicators**: Clear keyboard navigation

### Cognitive Accessibility
- **Clear Instructions**: Step-by-step guidance
- **Progress Indicators**: Visual feedback on completion
- **Error Prevention**: Input validation and suggestions

### Motor Accessibility
- **Large Touch Targets**: Easy interaction on mobile
- **Keyboard Navigation**: Full keyboard support
- **Voice Input**: Speech-to-text capabilities

---

*This document outlines the UI expectations for the training mode interface, emphasizing contextualized input systems and targeted AI responses over traditional chatbot interactions.*
