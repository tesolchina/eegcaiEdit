# AI Tutor Implementation Notes for Kai Tai

## Overview
This document provides comprehensive guidance for implementing the AI tutor backend system that will power the AI Essay Training Mode. Students will engage in multiple rounds of conversation with AI tutors and be assessed based on their AI communication skills.

## Project Context
- **Course**: LANG 0036: Enhancing English through Global Citizenship
- **Component**: AI Training and Assessment Component for remedial English courses
- **Goal**: Develop students' AI collaboration skills while improving their academic writing

## Core Implementation Requirements

### 1. **Four Learning Goals Framework**
The AI tutor must support and assess students across four critical learning goals:

#### **Goal 1: Provide Contextual Information**
- **Student Behavior**: Students share comprehensive context (course, assignment, personal background, session goals)
- **AI Tutor Response**: Acknowledge context, ask clarifying questions, provide targeted assistance
- **Assessment Focus**: Quality and comprehensiveness of contextual information provided

#### **Goal 2: Negotiate with AI on Agenda and Goals**
- **Student Behavior**: Students prioritize revision focus, negotiate with AI about approach, set realistic goals
- **AI Tutor Response**: Guide strategic planning, suggest priorities, help students make informed decisions
- **Assessment Focus**: Evidence of strategic planning and priority-setting abilities

#### **Goal 3: Critically Review AI Suggestions**
- **Student Behavior**: Students question AI recommendations, ask for explanations, evaluate suggestions against rubrics
- **AI Tutor Response**: Provide detailed explanations, encourage critical thinking, support evidence-based decisions
- **Assessment Focus**: Quality of critical evaluation and questioning of AI suggestions

#### **Goal 4: Do Your Own Writing and Editing**
- **Student Behavior**: Students implement all changes themselves, make final decisions, maintain ownership
- **AI Tutor Response**: Provide guidance and suggestions only, never do the actual writing/editing
- **Assessment Focus**: Evidence of student ownership and independent decision-making

### 2. **Assessment Rubrics Integration**

#### **AI Communication Skills Assessment** (Primary Focus)
Based on `/reference/AI-communication-rubrics.md`:

| Criteria | 1 (Limited) | 2 (Basic) | 3 (Developing) | 4 (Proficient) | 5 (Excellent) |
|----------|-------------|-----------|---------------|----------------|---------------|
| **A. In-Depth Conversation** | No exchanges | Sparse exchanges | Adequate exchanges | Robust exchanges | Extensive exchanges |
| **B. Critical Review** | All suggestions accepted | Most accepted with little analysis | Some evaluation | Most critically assessed | All thoroughly evaluated |
| **C. Refining Process** | No revisions | Minimal revisions | Some revisions | Clear iterative process | Extensive refinement |

#### **Essay Quality Assessment** (Secondary Focus)
- Content & Ideas (1-5 scale)
- Organisation & Logic (1-5 scale)  
- Vocabulary (1-5 scale)
- Grammar & Structure (1-5 scale)

### 3. **Technical Implementation Requirements**

#### **Conversation Management**
- **Multi-turn Conversations**: Support extended dialogue sessions
- **Context Persistence**: Maintain conversation history and context across turns
- **Session Tracking**: Track student progress through the four learning goals
- **Conversation Analytics**: Capture interaction patterns for assessment

#### **AI Tutor Personality & Behavior**
- **Socratic Method**: Ask probing questions rather than providing direct answers
- **Scaffolding**: Provide appropriate support level based on student needs
- **Encouragement**: Motivate students to think critically and independently
- **Boundary Setting**: Clearly distinguish between guidance and doing work for students

#### **Assessment Data Collection**
- **Conversation Logs**: Complete chat history with timestamps
- **Interaction Metrics**: Number of questions asked, suggestions evaluated, revisions made
- **Goal Achievement**: Evidence of progress across all four learning goals
- **Critical Thinking Indicators**: Quality of questions and evaluation of AI suggestions

### 4. **Sample Essay Integration**

#### **Essay Context**
- **Topic**: Climate change and individual vs. systemic action
- **Question**: "Some people believe that individual actions are insignificant in the fight against climate change compared to the efforts of governments and large corporations. To what extent do you agree or disagree with this statement?"
- **Quality Level**: Well-written with specific improvement opportunities

#### **Specific Issues to Address**
1. **Thesis Statement**: Needs clearer position on "extent" of agreement/disagreement
2. **Topic Sentences**: Could be more analytical and argumentative
3. **Evidence**: Needs more specific examples with data/statistics
4. **Critical Analysis**: Requires deeper evaluation of relationships
5. **Counter-arguments**: Limited consideration of opposing viewpoints
6. **Conclusion**: Needs more synthesis and forward-looking perspective

### 5. **AI Tutor Conversation Flow**

#### **Initial Interaction**
```
AI Tutor: "Thanks for sharing the essay! Could you provide more info about the task you're working on and tell me what help you need?"

Expected Student Response:
- Personal context (course, year level)
- Academic context (specific course)
- Task context (assignment details)
- Session goals (what they want to achieve)
```

#### **Follow-up Context**
```
AI Tutor: "How would you like to edit the essay?"

Expected Student Response:
- Assessment awareness (mention of dual rubrics)
- Priority setting (specific revision focus)
- Learning objectives (what they want to improve)
```

#### **Goal 2: Strategic Planning**
```
AI Tutor: "I can see several areas for improvement. Which would you like to focus on first, and why?"

Expected Student Response:
- Priority identification
- Justification for choices
- Time management considerations
- Strategic thinking about revision approach
```

#### **Goal 3: Critical Evaluation**
```
AI Tutor: "Here's my suggestion for improving your thesis. What do you think about this approach?"

Expected Student Response:
- Critical evaluation of suggestion
- Questions about rationale
- Comparison with rubrics
- Evidence-based decision making
```

#### **Goal 4: Independent Implementation**
```
AI Tutor: "I can guide you through the revision process, but you'll need to make the actual changes. What would you like to focus on first?"

Expected Student Response:
- Independent decision making
- Self-directed revision
- Ownership of writing process
- Implementation of chosen changes
```

### 6. **Assessment Implementation**

#### **Data Collection Points**
- **Context Provision Quality**: Comprehensiveness and relevance of information shared
- **Goal Negotiation Evidence**: Strategic planning and priority-setting abilities
- **Critical Review Indicators**: Quality of questions and evaluation of suggestions
- **Independent Work Evidence**: Student ownership and decision-making autonomy

#### **Scoring Algorithm**
- **Conversation Depth**: Measure of engagement and question quality
- **Critical Thinking**: Evaluation of AI suggestions and independent judgment
- **Iterative Process**: Evidence of revision and refinement based on feedback
- **Goal Achievement**: Progress across all four learning goals

### 7. **Technical Architecture Considerations**

#### **API Integration**
- **OpenRouter API**: For AI model access
- **Environment Variables**: Secure API key management
- **Rate Limiting**: Appropriate request throttling
- **Error Handling**: Graceful failure management

#### **Database Requirements**
- **User Sessions**: Track individual student progress
- **Conversation Storage**: Complete chat history preservation
- **Assessment Data**: Rubric scoring and analytics
- **Progress Tracking**: Learning goal achievement monitoring

#### **Security & Privacy**
- **Data Encryption**: Secure storage of conversation data
- **Access Control**: Appropriate user authentication
- **Privacy Compliance**: Student data protection
- **Audit Logging**: Track system usage and access

### 8. **Testing & Validation**

#### **Test Scenarios**
- **Goal 1 Testing**: Verify context provision quality
- **Goal 2 Testing**: Validate strategic planning abilities
- **Goal 3 Testing**: Confirm critical evaluation skills
- **Goal 4 Testing**: Ensure independent work evidence

#### **Assessment Validation**
- **Rubric Alignment**: Verify scoring matches assessment criteria
- **Inter-rater Reliability**: Consistent evaluation across different assessors
- **Student Feedback**: Validate learning experience quality
- **Performance Metrics**: Measure learning outcome achievement

### 9. **Implementation Timeline**

#### **Phase 1: Core Infrastructure**
- Basic conversation management
- API integration
- Database setup
- Authentication system

#### **Phase 2: AI Tutor Logic**
- Four learning goals implementation
- Assessment data collection
- Rubric scoring system
- Progress tracking

#### **Phase 3: Assessment Integration**
- Complete rubric implementation
- Analytics dashboard
- Reporting system
- Performance optimization

#### **Phase 4: Testing & Deployment**
- Comprehensive testing
- User acceptance testing
- Performance optimization
- Production deployment

### 10. **Success Metrics**

#### **Technical Metrics**
- **System Uptime**: 99.9% availability target
- **Response Time**: <2 seconds for AI responses
- **Scalability**: Support for concurrent users
- **Data Integrity**: 100% conversation preservation

#### **Learning Metrics**
- **Goal Achievement**: Progress across all four learning goals
- **Critical Thinking**: Evidence of analytical evaluation
- **Independent Work**: Student ownership and decision-making
- **Essay Improvement**: Measurable writing quality enhancement

### 11. **Resources & References**

#### **Key Documents**
- `/reference/four-goals-of-learning-ai.md` - Complete learning goals framework
- `/reference/AI-communication-rubrics.md` - Assessment criteria
- `/reference/sampleEssay2edit.md` - Practice essay with specific issues
- `/reference/rubrics4essay.md` - Essay quality assessment criteria

#### **Interface Files**
- `/docs/design/mockup_split/index.html` - Unified interface
- `/docs/design/mockup_split/01-context-confirmation.html` - Goal 1 implementation
- `/docs/design/mockup_split/02-goal-setting.html` - Goal 2 implementation
- `/docs/design/mockup_split/03-thesis.html` - Goal 3 implementation
- `/docs/design/mockup_split/04-topic-sentences.html` - Goal 3 implementation
- `/docs/design/mockup_split/05-body-paragraph.html` - Goal 3 implementation
- `/docs/design/mockup_split/06-reflection.html` - Goal 4 implementation

## Questions for Kai Tai

1. **API Integration**: What's your preferred approach for OpenRouter API integration?
2. **Database Design**: How do you plan to structure the conversation and assessment data?
3. **Real-time Features**: Do you need WebSocket support for live conversation updates?
4. **Assessment Timing**: Should assessment be real-time or batch processing?
5. **Scalability**: What's your expected user load and how will you handle it?

## Contact Information
- **Project Lead**: Simon Wang
- **Implementation**: Kai Tai
- **Repository**: https://github.com/tesolchina/eegcaiEdit.git
- **Documentation**: `/docs/` directory contains all reference materials

---

*This document provides the foundation for implementing a comprehensive AI tutor system that supports student learning while maintaining rigorous assessment standards.*
