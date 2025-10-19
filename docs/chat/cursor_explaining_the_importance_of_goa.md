# Explaining the importance of goal prioritization
_Exported on 19/10/2025 at 5:17:05 GMT+8 from Cursor (1.7.52)_

---

**User**

/Users/simonwang/Documents/Usage/EEGC_aiedit/docs/design/mockup_split/02-goal-setting.html

for this part we should explain the importance of priortizing different goals 
there are certain goals that are given 
students should work on the thesis statements and topic sentences 
but for body paragraph they will have some flexibilty 

We need a UI to reflect that 

for time management we expect students to spend about 15-20 minutes 

this part students should have a chancce to talk an AI chatbot to explore different options here 


---

**Cursor**

I'll help you enhance the goal-setting UI to better reflect the importance of prioritizing different goals and provide flexibility for students. Let me first examine the current file to understand the existing structure.


Now let me create a todo list to break down the enhancements needed for the goal-setting UI:


Now I'll enhance the goal-setting UI to better reflect the importance of prioritizing different goals, show the required vs flexible nature of goals, update the time management expectations, and improve the AI chatbot integration:


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goal Setting - AI Essay Training Mode</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE',
                        'primary-hover': '#4a49c5',
                        'primary-light': '#ebebfa',
                    }
                }
            },
            darkMode: 'class'
        }
    </script>
    <style>
        .fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-gray-50 dark:bg-[#181818] text-gray-900 dark:text-gray-100 min-h-screen">
    <div class="container mx-auto px-4 py-6 max-w-7xl">
        <!-- Header -->
        <header class="mb-6">
            <h1 class="text-3xl md:text-4xl font-bold text-primary mb-2 text-center">Goal Setting</h1>
            <p class="text-base md:text-lg text-gray-600 dark:text-gray-400 text-center">Goal 2: Negotiate with AI on Agenda and Goals</p>
        </header>

        <!-- Main Content Grid -->
        <div class="grid lg:grid-cols-3 gap-6">
            <!-- Left Panel: Goal Setting (2 columns) -->
            <div class="lg:col-span-2 space-y-6">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md">
                    <h2 class="text-xl md:text-2xl font-bold mb-4 text-primary">Your Revision Goals</h2>

                    <!-- Goal 2 Explanation -->
                    <div class="mb-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <h3 class="font-bold text-blue-900 dark:text-blue-200 mb-2">Goal 2: Negotiate with AI on Agenda and Goals</h3>
                        <p class="text-sm text-gray-700 dark:text-gray-300 mb-3">
                            Learn to strategically plan your revision by setting priorities, considering time constraints, and focusing on macro-level issues first.
                        </p>
                        <div class="bg-yellow-50 dark:bg-yellow-900/20 p-3 rounded-lg border border-yellow-300 dark:border-yellow-700">
                            <p class="text-sm font-medium text-yellow-800 dark:text-yellow-200">
                                <span class="font-bold">🎯 Priority Focus:</span> Some goals are essential (thesis & topic sentences), while others offer flexibility (body paragraphs). Use the AI chatbot to explore your options!
                            </p>
                        </div>
                    </div>

                    <!-- AI-Suggested Goals -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">🎯</span>
                            AI-Suggested Goals Based on Your Essay
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">The AI has analyzed your essay and suggests these focus areas:</p>

                        <div class="p-4 bg-gray-50 dark:bg-gray-700 rounded-lg border-2 border-gray-300 dark:border-gray-600">
                            <h4 class="font-bold text-gray-800 dark:text-gray-200 mb-2">Suggested Revision Goals:</h4>
                            <ul class="space-y-2 text-sm text-gray-700 dark:text-gray-300">
                                <li>• <strong>Improve thesis statement clarity</strong> - Ensure it directly answers the question and includes 2 specific points</li>
                                <li>• <strong>Strengthen topic sentences</strong> - Make them echo and support thesis points</li>
                                <li>• <strong>Enhance body paragraph development</strong> - Focus on one paragraph to improve detail and coherence</li>
                                <li>• <strong>Address grammar and sentence structure</strong> - Improve clarity and flow</li>
                            </ul>
                        </div>
                    </div>

                    <!-- Student Goal Selection -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">✏️</span>
                            Select Your Priority Goals
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">Choose what you want to focus on in this session:</p>

                        <div class="space-y-3">
                            <label class="flex items-start gap-3 p-3 bg-gray-50 dark:bg-gray-700 rounded-lg cursor-pointer hover:bg-gray-100 dark:hover:bg-gray-600">
                                <input type="checkbox" class="goal-checkbox mt-1" value="thesis" checked>
                                <div>
                                    <p class="font-medium">Improve thesis statement clarity</p>
                                    <p class="text-sm text-gray-600 dark:text-gray-400">Ensure it answers the question and includes 2 specific points</p>
                                </div>
                            </label>
                            <label class="flex items-start gap-3 p-3 bg-gray-50 dark:bg-gray-700 rounded-lg cursor-pointer hover:bg-gray-100 dark:hover:bg-gray-600">
                                <input type="checkbox" class="goal-checkbox mt-1" value="topic-sentences" checked>
                                <div>
                                    <p class="font-medium">Strengthen topic sentences</p>
                                    <p class="text-sm text-gray-600 dark:text-gray-400">Make them echo and support thesis points</p>
                                </div>
                            </label>
                            <label class="flex items-start gap-3 p-3 bg-gray-50 dark:bg-gray-700 rounded-lg cursor-pointer hover:bg-gray-100 dark:hover:bg-gray-600">
                                <input type="checkbox" class="goal-checkbox mt-1" value="paragraph-development" checked>
                                <div>
                                    <p class="font-medium">Enhance body paragraph development</p>
                                    <p class="text-sm text-gray-600 dark:text-gray-400">Focus on one paragraph to improve detail and coherence</p>
                                </div>
                            </label>
                            <label class="flex items-start gap-3 p-3 bg-gray-50 dark:bg-gray-700 rounded-lg cursor-pointer hover:bg-gray-100 dark:hover:bg-gray-600">
                                <input type="checkbox" class="goal-checkbox mt-1" value="grammar-vocabulary">
                                <div>
                                    <p class="font-medium">Address grammar and vocabulary</p>
                                    <p class="text-sm text-gray-600 dark:text-gray-400">Improve sentence structure and word choice</p>
                                </div>
                            </label>
                        </div>

                        <div class="mt-4">
                            <label class="block text-sm font-medium mb-2">Add custom goals (optional):</label>
                            <textarea id="custom-goals" rows="2" placeholder="E.g., Improve vocabulary variety, fix specific grammar issues..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary"></textarea>
                        </div>
                    </div>

                    <!-- Strategic Planning -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">📋</span>
                            Strategic Planning
                        </h3>
                        <div class="grid md:grid-cols-2 gap-4">
                            <div class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                                <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Macro-Level Issues (Priority 1)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Content, organization, thesis, topic sentences</p>
                            </div>
                            <div class="p-4 bg-orange-50 dark:bg-orange-900/20 rounded-lg border-l-4 border-orange-500">
                                <h4 class="font-bold text-orange-900 dark:text-orange-200 mb-2">Micro-Level Issues (Priority 2)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Grammar, vocabulary, sentence structure</p>
                            </div>
                        </div>
                    </div>

                    <!-- Time Constraints -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">⏰</span>
                            Time Management
                        </h3>
                        <div class="p-4 bg-purple-50 dark:bg-purple-900/20 rounded-lg border-l-4 border-purple-500">
                            <label class="block text-sm font-bold mb-2 text-purple-900 dark:text-purple-200">
                                How much time do you have for this session?
                            </label>
                            <select id="time-constraint" class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary">
                                <option value="30min">30 minutes</option>
                                <option value="45min">45 minutes</option>
                                <option value="60min">1 hour</option>
                                <option value="90min">1.5 hours</option>
                                <option value="120min">2+ hours</option>
                            </select>
                        </div>
                    </div>

                    <!-- Goals Summary -->
                    <div id="selected-goals-summary" class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                        <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Your Selected Goals:</h4>
                        <div id="goals-list" class="text-sm text-gray-700 dark:text-gray-300"></div>
                    </div>

                    <!-- Confirmation Button -->
                    <div class="mt-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <button id="confirm-goals" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 rounded-lg transition-colors text-lg">
                            ✓ Confirm Goals and Proceed
                        </button>
                    </div>
                </div>
            </div>

            <!-- Right Panel: AI Conversation (1 column) -->
            <div class="lg:col-span-1">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md sticky top-6">
                    <h3 class="text-lg md:text-xl font-bold mb-4 flex items-center gap-2">
                        <span class="text-2xl">🤖</span>
                        AI Conversation
                    </h3>

                    <div id="chat-messages" class="bg-gray-50 dark:bg-gray-700 rounded-lg p-4 mb-4 overflow-y-auto" style="height: 500px;">
                        <div class="text-center text-gray-500 dark:text-gray-400 text-sm py-12">
                            Your conversation with the AI will appear here. The AI will help you negotiate and refine your revision goals.
                        </div>
                    </div>

                    <div id="loading-indicator" class="hidden text-center py-4">
                        <div class="inline-block animate-spin rounded-full h-6 w-6 border-b-2 border-primary"></div>
                        <p class="mt-2 text-xs text-gray-600 dark:text-gray-400">AI is thinking...</p>
                    </div>

                    <!-- General Chat Input -->
                    <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                        <textarea id="general-chat-input" rows="3" placeholder="Ask the AI about goal setting and strategic planning..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary mb-2"></textarea>
                        <button id="send-general-chat" class="w-full bg-primary hover:bg-primary-hover text-white font-semibold py-2 px-4 rounded-lg transition-colors">
                            Send Message
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Dark mode setup
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            document.documentElement.classList.add(event.matches ? 'dark' : '');
            !event.matches && document.documentElement.classList.remove('dark');
        });

        // State
        const state = {
            selectedGoals: [],
            timeConstraint: '60min'
        };

        // Goals tracking
        const goalCheckboxes = document.querySelectorAll('.goal-checkbox');
        goalCheckboxes.forEach(cb => cb.addEventListener('change', updateGoals));
        document.getElementById('custom-goals').addEventListener('input', updateGoals);
        document.getElementById('time-constraint').addEventListener('change', updateGoals);

        function updateGoals() {
            const goals = [];
            goalCheckboxes.forEach(cb => {
                if (cb.checked) {
                    goals.push(cb.parentElement.querySelector('p.font-medium').textContent);
                }
            });
            const custom = document.getElementById('custom-goals').value.trim();
            if (custom) goals.push(custom);

            state.selectedGoals = goals;
            state.timeConstraint = document.getElementById('time-constraint').value;

            document.getElementById('goals-list').innerHTML = goals.length > 0
                ? goals.map((g, i) => `<p>${i + 1}. ${g}</p>`).join('')
                : '<p class="text-gray-500">No goals selected</p>';
        }
        updateGoals();

        // Custom modal function
        function showCustomModal(message) {
            const modal = document.createElement('div');
            modal.className = 'fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50 p-4';
            modal.innerHTML = `
                <div class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow-2xl max-w-sm w-full border-2 border-primary">
                    <p class="text-gray-800 dark:text-gray-200 mb-4 text-base">${message}</p>
                    <button class="w-full px-4 py-2 bg-primary text-white hover:bg-primary-hover rounded-lg transition-colors font-semibold" onclick="this.closest('.fixed').remove()">OK</button>
                </div>
            `;
            document.body.appendChild(modal);
        }

        // Goals Confirmation
        document.getElementById('confirm-goals').addEventListener('click', () => {
            if (state.selectedGoals.length === 0) {
                showCustomModal('Please select at least one goal before proceeding.');
                return;
            }

            // Show confirmation message
            showCustomModal('Excellent! You\'ve set your revision goals. The AI will now provide guidance on strategic planning and goal negotiation.');
            
            // Generate AI messages about goal negotiation
            setTimeout(() => {
                addChatMessage("AI", `Great job setting your revision goals! 

**Goal 2: Negotiate with AI on Agenda and Goals**

You've demonstrated strategic thinking by:
- Selecting priority areas for revision
- Considering time constraints (${state.timeConstraint})
- Focusing on macro-level issues first

**Strategic Planning Tips:**
- **Macro-level first**: Content, organization, thesis, topic sentences
- **Micro-level second**: Grammar, vocabulary, sentence structure
- **Time management**: Focus on high-impact improvements within your time limit

**Next Steps:**
Your goals are well-prioritized. We'll work through them systematically, starting with the most impactful changes. Ready to begin with your thesis statement?`);
            }, 1000);

            // Disable the button after confirmation
            document.getElementById('confirm-goals').disabled = true;
            document.getElementById('confirm-goals').textContent = '✓ Goals Confirmed';
            document.getElementById('confirm-goals').classList.add('bg-gray-400', 'cursor-not-allowed');
        });

        // General chat
        document.getElementById('send-general-chat').addEventListener('click', () => {
            const msg = document.getElementById('general-chat-input').value.trim();
            if (!msg) return;
            askAI(`@Claude-Sonnet-4.5 Student question about goal setting: "${msg}"

Provide guidance on strategic planning and goal negotiation with AI. Keep response under 5 sentences.`);
            document.getElementById('general-chat-input').value = '';
        });

        // AI Communication
        function addChatMessage(sender, content) {
            const chat = document.getElementById('chat-messages');
            const placeholder = chat.querySelector('.text-center.text-gray-500');
            if (placeholder) placeholder.remove();

            const msg = document.createElement('div');
            msg.className = 'mb-3';
            msg.innerHTML = `
                <div class="text-xs font-semibold mb-1 ${sender === 'You' ? 'text-gray-600 dark:text-gray-400' : 'text-primary'}">${sender === 'You' ? '👤' : '🤖'} ${sender}</div>
                <div class="p-3 rounded-lg text-sm ${sender === 'You' ? 'bg-gray-200 dark:bg-gray-600' : 'bg-blue-50 dark:bg-blue-900/30'}">${marked.parse(content)}</div>
            `;
            chat.appendChild(msg);
            chat.scrollTop = chat.scrollHeight;
        }

        function updateLastAIMessage(content) {
            const chat = document.getElementById('chat-messages');
            const messages = chat.querySelectorAll('.mb-3');
            if (messages.length > 0) {
                const last = messages[messages.length - 1];
                const contentDiv = last.querySelector('.p-3');
                if (contentDiv) {
                    contentDiv.innerHTML = marked.parse(content);
                    chat.scrollTop = chat.scrollHeight;
                }
            }
        }

        if (window.Poe) {
            window.Poe.registerHandler("essay-training", (result) => {
                const msg = result.responses[0];
                document.getElementById('loading-indicator').classList.add('hidden');

                if (msg.status === "error") {
                    addChatMessage("AI", `Error: ${msg.statusText}`);
                } else if (msg.status === "incomplete") {
                    if (msg.content.trim()) {
                        updateLastAIMessage(msg.content);
                    }
                } else if (msg.status === "complete") {
                    updateLastAIMessage(msg.content);
                }
            });
        }

        async function askAI(prompt) {
            if (!window.Poe) {
                showCustomModal("Poe API not available. This app needs to run in the Poe environment.");
                return;
            }

            // Extract user message from prompt
            const userMsg = prompt.split('\n').slice(1).join('\n').substring(0, 100) + '...';
            addChatMessage("You", userMsg);
            addChatMessage("AI", "...");
            document.getElementById('loading-indicator').classList.remove('hidden');

            try {
                await window.Poe.sendUserMessage(prompt, {
                    handler: "essay-training",
                    stream: true,
                    openChat: false
                });
            } catch (err) {
                document.getElementById('loading-indicator').classList.add('hidden');
                addChatMessage("AI", `Error: ${err.message}`);
            }
        }

        console.log('Goal Setting tab loaded');
    </script>
</body>
</html>

```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goal Setting - AI Essay Training Mode</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE',
                        'primary-hover': '#4a49c5',
                        'primary-light': '#ebebfa',
                    }
                }
            },
            darkMode: 'class'
        }
    </script>
    <style>
        .fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-gray-50 dark:bg-[#181818] text-gray-900 dark:text-gray-100 min-h-screen">
    <div class="container mx-auto px-4 py-6 max-w-7xl">
        <!-- Header -->
        <header class="mb-6">
            <h1 class="text-3xl md:text-4xl font-bold text-primary mb-2 text-center">Goal Setting</h1>
            <p class="text-base md:text-lg text-gray-600 dark:text-gray-400 text-center">Goal 2: Negotiate with AI on Agenda and Goals</p>
        </header>

        <!-- Main Content Grid -->
        <div class="grid lg:grid-cols-3 gap-6">
            <!-- Left Panel: Goal Setting (2 columns) -->
            <div class="lg:col-span-2 space-y-6">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md">
                    <h2 class="text-xl md:text-2xl font-bold mb-4 text-primary">Your Revision Goals</h2>

                    <!-- Goal 2 Explanation -->
                    <div class="mb-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <h3 class="font-bold text-blue-900 dark:text-blue-200 mb-2">Goal 2: Negotiate with AI on Agenda and Goals</h3>
                        <p class="text-sm text-gray-700 dark:text-gray-300 mb-3">
                            Learn to strategically plan your revision by setting priorities, considering time constraints, and focusing on macro-level issues first.
                        </p>
                        <div class="bg-yellow-50 dark:bg-yellow-900/20 p-3 rounded-lg border border-yellow-300 dark:border-yellow-700">
                            <p class="text-sm font-medium text-yellow-800 dark:text-yellow-200">
                                <span class="font-bold">🎯 Priority Focus:</span> Some goals are essential (thesis & topic sentences), while others offer flexibility (body paragraphs). Use the AI chatbot to explore your options!
                            </p>
                        </div>
                    </div>

                    <!-- AI-Suggested Goals -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">🎯</span>
                            AI-Suggested Goals Based on Your Essay
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">The AI has analyzed your essay and suggests these focus areas:</p>

                        <div class="p-4 bg-gray-50 dark:bg-gray-700 rounded-lg border-2 border-gray-300 dark:border-gray-600">
                            <h4 class="font-bold text-gray-800 dark:text-gray-200 mb-2">Suggested Revision Goals:</h4>
                            <ul class="space-y-2 text-sm text-gray-700 dark:text-gray-300">
                                <li>• <strong>Improve thesis statement clarity</strong> - Ensure it directly answers the question and includes 2 specific points</li>
                                <li>• <strong>Strengthen topic sentences</strong> - Make them echo and support thesis points</li>
                                <li>• <strong>Enhance body paragraph development</strong> - Focus on one paragraph to improve detail and coherence</li>
                                <li>• <strong>Address grammar and sentence structure</strong> - Improve clarity and flow</li>
                            </ul>
                        </div>
                    </div>

                    <!-- Student Goal Selection -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">✏️</span>
                            Select Your Priority Goals
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">Choose what you want to focus on in this session:</p>

                        <!-- Required Goals Section -->
                        <div class="mb-4">
                            <h4 class="text-md font-bold mb-3 flex items-center gap-2 text-red-700 dark:text-red-400">
                                <span class="text-lg">🔴</span>
                                Essential Goals (Required)
                            </h4>
                            <p class="text-xs text-gray-600 dark:text-gray-400 mb-3">These are fundamental to your essay structure and must be addressed:</p>
                            
                            <div class="space-y-3">
                                <label class="flex items-start gap-3 p-3 bg-red-50 dark:bg-red-900/20 rounded-lg cursor-pointer hover:bg-red-100 dark:hover:bg-red-900/30 border border-red-200 dark:border-red-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="thesis" checked disabled>
                                    <div class="flex-1">
                                        <p class="font-medium text-red-800 dark:text-red-200">Improve thesis statement clarity</p>
                                        <p class="text-sm text-red-600 dark:text-red-400">Ensure it answers the question and includes 2 specific points</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-red-200 dark:bg-red-800 text-red-800 dark:text-red-200 text-xs rounded-full">Required</span>
                                    </div>
                                </label>
                                <label class="flex items-start gap-3 p-3 bg-red-50 dark:bg-red-900/20 rounded-lg cursor-pointer hover:bg-red-100 dark:hover:bg-red-900/30 border border-red-200 dark:border-red-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="topic-sentences" checked disabled>
                                    <div class="flex-1">
                                        <p class="font-medium text-red-800 dark:text-red-200">Strengthen topic sentences</p>
                                        <p class="text-sm text-red-600 dark:text-red-400">Make them echo and support thesis points</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-red-200 dark:bg-red-800 text-red-800 dark:text-red-200 text-xs rounded-full">Required</span>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <!-- Flexible Goals Section -->
                        <div class="mb-4">
                            <h4 class="text-md font-bold mb-3 flex items-center gap-2 text-green-700 dark:text-green-400">
                                <span class="text-lg">🟢</span>
                                Flexible Goals (Your Choice)
                            </h4>
                            <p class="text-xs text-gray-600 dark:text-gray-400 mb-3">Choose based on your essay's needs and time available:</p>
                            
                            <div class="space-y-3">
                                <label class="flex items-start gap-3 p-3 bg-green-50 dark:bg-green-900/20 rounded-lg cursor-pointer hover:bg-green-100 dark:hover:bg-green-900/30 border border-green-200 dark:border-green-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="paragraph-development" checked>
                                    <div class="flex-1">
                                        <p class="font-medium text-green-800 dark:text-green-200">Enhance body paragraph development</p>
                                        <p class="text-sm text-green-600 dark:text-green-400">Focus on one paragraph to improve detail and coherence</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-green-200 dark:bg-green-800 text-green-800 dark:text-green-200 text-xs rounded-full">Flexible</span>
                                    </div>
                                </label>
                                <label class="flex items-start gap-3 p-3 bg-green-50 dark:bg-green-900/20 rounded-lg cursor-pointer hover:bg-green-100 dark:hover:bg-green-900/30 border border-green-200 dark:border-green-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="grammar-vocabulary">
                                    <div class="flex-1">
                                        <p class="font-medium text-green-800 dark:text-green-200">Address grammar and vocabulary</p>
                                        <p class="text-sm text-green-600 dark:text-green-400">Improve sentence structure and word choice</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-green-200 dark:bg-green-800 text-green-800 dark:text-green-200 text-xs rounded-full">Flexible</span>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <div class="mt-4">
                            <label class="block text-sm font-medium mb-2">Add custom goals (optional):</label>
                            <textarea id="custom-goals" rows="2" placeholder="E.g., Improve vocabulary variety, fix specific grammar issues..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary"></textarea>
                        </div>
                    </div>

                    <!-- Strategic Planning -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">📋</span>
                            Strategic Planning
                        </h3>
                        <div class="grid md:grid-cols-2 gap-4">
                            <div class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                                <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Macro-Level Issues (Priority 1)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Content, organization, thesis, topic sentences</p>
                            </div>
                            <div class="p-4 bg-orange-50 dark:bg-orange-900/20 rounded-lg border-l-4 border-orange-500">
                                <h4 class="font-bold text-orange-900 dark:text-orange-200 mb-2">Micro-Level Issues (Priority 2)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Grammar, vocabulary, sentence structure</p>
                            </div>
                        </div>
                    </div>

                    <!-- Time Constraints -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">⏰</span>
                            Time Management
                        </h3>
                        <div class="p-4 bg-purple-50 dark:bg-purple-900/20 rounded-lg border-l-4 border-purple-500">
                            <label class="block text-sm font-bold mb-2 text-purple-900 dark:text-purple-200">
                                How much time do you have for this session?
                            </label>
                            <select id="time-constraint" class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary">
                                <option value="30min">30 minutes</option>
                                <option value="45min">45 minutes</option>
                                <option value="60min">1 hour</option>
                                <option value="90min">1.5 hours</option>
                                <option value="120min">2+ hours</option>
                            </select>
                        </div>
                    </div>

                    <!-- Goals Summary -->
                    <div id="selected-goals-summary" class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                        <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Your Selected Goals:</h4>
                        <div id="goals-list" class="text-sm text-gray-700 dark:text-gray-300"></div>
                    </div>

                    <!-- Confirmation Button -->
                    <div class="mt-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <button id="confirm-goals" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 rounded-lg transition-colors text-lg">
                            ✓ Confirm Goals and Proceed
                        </button>
                    </div>
                </div>
            </div>

            <!-- Right Panel: AI Conversation (1 column) -->
            <div class="lg:col-span-1">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md sticky top-6">
                    <h3 class="text-lg md:text-xl font-bold mb-4 flex items-center gap-2">
                        <span class="text-2xl">🤖</span>
                        AI Conversation
                    </h3>

                    <div id="chat-messages" class="bg-gray-50 dark:bg-gray-700 rounded-lg p-4 mb-4 overflow-y-auto" style="height: 500px;">
                        <div class="text-center text-gray-500 dark:text-gray-400 text-sm py-12">
                            Your conversation with the AI will appear here. The AI will help you negotiate and refine your revision goals.
                        </div>
                    </div>

                    <div id="loading-indicator" class="hidden text-center py-4">
                        <div class="inline-block animate-spin rounded-full h-6 w-6 border-b-2 border-primary"></div>
                        <p class="mt-2 text-xs text-gray-600 dark:text-gray-400">AI is thinking...</p>
                    </div>

                    <!-- General Chat Input -->
                    <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                        <textarea id="general-chat-input" rows="3" placeholder="Ask the AI about goal setting and strategic planning..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary mb-2"></textarea>
                        <button id="send-general-chat" class="w-full bg-primary hover:bg-primary-hover text-white font-semibold py-2 px-4 rounded-lg transition-colors">
                            Send Message
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Dark mode setup
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            document.documentElement.classList.add(event.matches ? 'dark' : '');
            !event.matches && document.documentElement.classList.remove('dark');
        });

        // State
        const state = {
            selectedGoals: [],
            timeConstraint: '60min'
        };

        // Goals tracking
        const goalCheckboxes = document.querySelectorAll('.goal-checkbox');
        goalCheckboxes.forEach(cb => cb.addEventListener('change', updateGoals));
        document.getElementById('custom-goals').addEventListener('input', updateGoals);
        document.getElementById('time-constraint').addEventListener('change', updateGoals);

        function updateGoals() {
            const goals = [];
            goalCheckboxes.forEach(cb => {
                if (cb.checked) {
                    goals.push(cb.parentElement.querySelector('p.font-medium').textContent);
                }
            });
            const custom = document.getElementById('custom-goals').value.trim();
            if (custom) goals.push(custom);

            state.selectedGoals = goals;
            state.timeConstraint = document.getElementById('time-constraint').value;

            document.getElementById('goals-list').innerHTML = goals.length > 0
                ? goals.map((g, i) => `<p>${i + 1}. ${g}</p>`).join('')
                : '<p class="text-gray-500">No goals selected</p>';
        }
        updateGoals();

        // Custom modal function
        function showCustomModal(message) {
            const modal = document.createElement('div');
            modal.className = 'fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50 p-4';
            modal.innerHTML = `
                <div class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow-2xl max-w-sm w-full border-2 border-primary">
                    <p class="text-gray-800 dark:text-gray-200 mb-4 text-base">${message}</p>
                    <button class="w-full px-4 py-2 bg-primary text-white hover:bg-primary-hover rounded-lg transition-colors font-semibold" onclick="this.closest('.fixed').remove()">OK</button>
                </div>
            `;
            document.body.appendChild(modal);
        }

        // Goals Confirmation
        document.getElementById('confirm-goals').addEventListener('click', () => {
            if (state.selectedGoals.length === 0) {
                showCustomModal('Please select at least one goal before proceeding.');
                return;
            }

            // Show confirmation message
            showCustomModal('Excellent! You\'ve set your revision goals. The AI will now provide guidance on strategic planning and goal negotiation.');
            
            // Generate AI messages about goal negotiation
            setTimeout(() => {
                addChatMessage("AI", `Great job setting your revision goals! 

**Goal 2: Negotiate with AI on Agenda and Goals**

You've demonstrated strategic thinking by:
- Selecting priority areas for revision
- Considering time constraints (${state.timeConstraint})
- Focusing on macro-level issues first

**Strategic Planning Tips:**
- **Macro-level first**: Content, organization, thesis, topic sentences
- **Micro-level second**: Grammar, vocabulary, sentence structure
- **Time management**: Focus on high-impact improvements within your time limit

**Next Steps:**
Your goals are well-prioritized. We'll work through them systematically, starting with the most impactful changes. Ready to begin with your thesis statement?`);
            }, 1000);

            // Disable the button after confirmation
            document.getElementById('confirm-goals').disabled = true;
            document.getElementById('confirm-goals').textContent = '✓ Goals Confirmed';
            document.getElementById('confirm-goals').classList.add('bg-gray-400', 'cursor-not-allowed');
        });

        // General chat
        document.getElementById('send-general-chat').addEventListener('click', () => {
            const msg = document.getElementById('general-chat-input').value.trim();
            if (!msg) return;
            askAI(`@Claude-Sonnet-4.5 Student question about goal setting: "${msg}"

Provide guidance on strategic planning and goal negotiation with AI. Keep response under 5 sentences.`);
            document.getElementById('general-chat-input').value = '';
        });

        // AI Communication
        function addChatMessage(sender, content) {
            const chat = document.getElementById('chat-messages');
            const placeholder = chat.querySelector('.text-center.text-gray-500');
            if (placeholder) placeholder.remove();

            const msg = document.createElement('div');
            msg.className = 'mb-3';
            msg.innerHTML = `
                <div class="text-xs font-semibold mb-1 ${sender === 'You' ? 'text-gray-600 dark:text-gray-400' : 'text-primary'}">${sender === 'You' ? '👤' : '🤖'} ${sender}</div>
                <div class="p-3 rounded-lg text-sm ${sender === 'You' ? 'bg-gray-200 dark:bg-gray-600' : 'bg-blue-50 dark:bg-blue-900/30'}">${marked.parse(content)}</div>
            `;
            chat.appendChild(msg);
            chat.scrollTop = chat.scrollHeight;
        }

        function updateLastAIMessage(content) {
            const chat = document.getElementById('chat-messages');
            const messages = chat.querySelectorAll('.mb-3');
            if (messages.length > 0) {
                const last = messages[messages.length - 1];
                const contentDiv = last.querySelector('.p-3');
                if (contentDiv) {
                    contentDiv.innerHTML = marked.parse(content);
                    chat.scrollTop = chat.scrollHeight;
                }
            }
        }

        if (window.Poe) {
            window.Poe.registerHandler("essay-training", (result) => {
                const msg = result.responses[0];
                document.getElementById('loading-indicator').classList.add('hidden');

                if (msg.status === "error") {
                    addChatMessage("AI", `Error: ${msg.statusText}`);
                } else if (msg.status === "incomplete") {
                    if (msg.content.trim()) {
                        updateLastAIMessage(msg.content);
                    }
                } else if (msg.status === "complete") {
                    updateLastAIMessage(msg.content);
                }
            });
        }

        async function askAI(prompt) {
            if (!window.Poe) {
                showCustomModal("Poe API not available. This app needs to run in the Poe environment.");
                return;
            }

            // Extract user message from prompt
            const userMsg = prompt.split('\n').slice(1).join('\n').substring(0, 100) + '...';
            addChatMessage("You", userMsg);
            addChatMessage("AI", "...");
            document.getElementById('loading-indicator').classList.remove('hidden');

            try {
                await window.Poe.sendUserMessage(prompt, {
                    handler: "essay-training",
                    stream: true,
                    openChat: false
                });
            } catch (err) {
                document.getElementById('loading-indicator').classList.add('hidden');
                addChatMessage("AI", `Error: ${err.message}`);
            }
        }

        console.log('Goal Setting tab loaded');
    </script>
</body>
</html>

```

Now let me update the time management section to reflect the 15-20 minute expectation:


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goal Setting - AI Essay Training Mode</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE',
                        'primary-hover': '#4a49c5',
                        'primary-light': '#ebebfa',
                    }
                }
            },
            darkMode: 'class'
        }
    </script>
    <style>
        .fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-gray-50 dark:bg-[#181818] text-gray-900 dark:text-gray-100 min-h-screen">
    <div class="container mx-auto px-4 py-6 max-w-7xl">
        <!-- Header -->
        <header class="mb-6">
            <h1 class="text-3xl md:text-4xl font-bold text-primary mb-2 text-center">Goal Setting</h1>
            <p class="text-base md:text-lg text-gray-600 dark:text-gray-400 text-center">Goal 2: Negotiate with AI on Agenda and Goals</p>
        </header>

        <!-- Main Content Grid -->
        <div class="grid lg:grid-cols-3 gap-6">
            <!-- Left Panel: Goal Setting (2 columns) -->
            <div class="lg:col-span-2 space-y-6">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md">
                    <h2 class="text-xl md:text-2xl font-bold mb-4 text-primary">Your Revision Goals</h2>

                    <!-- Goal 2 Explanation -->
                    <div class="mb-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <h3 class="font-bold text-blue-900 dark:text-blue-200 mb-2">Goal 2: Negotiate with AI on Agenda and Goals</h3>
                        <p class="text-sm text-gray-700 dark:text-gray-300 mb-3">
                            Learn to strategically plan your revision by setting priorities, considering time constraints, and focusing on macro-level issues first.
                        </p>
                        <div class="bg-yellow-50 dark:bg-yellow-900/20 p-3 rounded-lg border border-yellow-300 dark:border-yellow-700">
                            <p class="text-sm font-medium text-yellow-800 dark:text-yellow-200">
                                <span class="font-bold">🎯 Priority Focus:</span> Some goals are essential (thesis & topic sentences), while others offer flexibility (body paragraphs). Use the AI chatbot to explore your options!
                            </p>
                        </div>
                    </div>

                    <!-- AI-Suggested Goals -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">🎯</span>
                            AI-Suggested Goals Based on Your Essay
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">The AI has analyzed your essay and suggests these focus areas:</p>

                        <div class="p-4 bg-gray-50 dark:bg-gray-700 rounded-lg border-2 border-gray-300 dark:border-gray-600">
                            <h4 class="font-bold text-gray-800 dark:text-gray-200 mb-2">Suggested Revision Goals:</h4>
                            <ul class="space-y-2 text-sm text-gray-700 dark:text-gray-300">
                                <li>• <strong>Improve thesis statement clarity</strong> - Ensure it directly answers the question and includes 2 specific points</li>
                                <li>• <strong>Strengthen topic sentences</strong> - Make them echo and support thesis points</li>
                                <li>• <strong>Enhance body paragraph development</strong> - Focus on one paragraph to improve detail and coherence</li>
                                <li>• <strong>Address grammar and sentence structure</strong> - Improve clarity and flow</li>
                            </ul>
                        </div>
                    </div>

                    <!-- Student Goal Selection -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">✏️</span>
                            Select Your Priority Goals
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">Choose what you want to focus on in this session:</p>

                        <!-- Required Goals Section -->
                        <div class="mb-4">
                            <h4 class="text-md font-bold mb-3 flex items-center gap-2 text-red-700 dark:text-red-400">
                                <span class="text-lg">🔴</span>
                                Essential Goals (Required)
                            </h4>
                            <p class="text-xs text-gray-600 dark:text-gray-400 mb-3">These are fundamental to your essay structure and must be addressed:</p>
                            
                            <div class="space-y-3">
                                <label class="flex items-start gap-3 p-3 bg-red-50 dark:bg-red-900/20 rounded-lg cursor-pointer hover:bg-red-100 dark:hover:bg-red-900/30 border border-red-200 dark:border-red-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="thesis" checked disabled>
                                    <div class="flex-1">
                                        <p class="font-medium text-red-800 dark:text-red-200">Improve thesis statement clarity</p>
                                        <p class="text-sm text-red-600 dark:text-red-400">Ensure it answers the question and includes 2 specific points</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-red-200 dark:bg-red-800 text-red-800 dark:text-red-200 text-xs rounded-full">Required</span>
                                    </div>
                                </label>
                                <label class="flex items-start gap-3 p-3 bg-red-50 dark:bg-red-900/20 rounded-lg cursor-pointer hover:bg-red-100 dark:hover:bg-red-900/30 border border-red-200 dark:border-red-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="topic-sentences" checked disabled>
                                    <div class="flex-1">
                                        <p class="font-medium text-red-800 dark:text-red-200">Strengthen topic sentences</p>
                                        <p class="text-sm text-red-600 dark:text-red-400">Make them echo and support thesis points</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-red-200 dark:bg-red-800 text-red-800 dark:text-red-200 text-xs rounded-full">Required</span>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <!-- Flexible Goals Section -->
                        <div class="mb-4">
                            <h4 class="text-md font-bold mb-3 flex items-center gap-2 text-green-700 dark:text-green-400">
                                <span class="text-lg">🟢</span>
                                Flexible Goals (Your Choice)
                            </h4>
                            <p class="text-xs text-gray-600 dark:text-gray-400 mb-3">Choose based on your essay's needs and time available:</p>
                            
                            <div class="space-y-3">
                                <label class="flex items-start gap-3 p-3 bg-green-50 dark:bg-green-900/20 rounded-lg cursor-pointer hover:bg-green-100 dark:hover:bg-green-900/30 border border-green-200 dark:border-green-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="paragraph-development" checked>
                                    <div class="flex-1">
                                        <p class="font-medium text-green-800 dark:text-green-200">Enhance body paragraph development</p>
                                        <p class="text-sm text-green-600 dark:text-green-400">Focus on one paragraph to improve detail and coherence</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-green-200 dark:bg-green-800 text-green-800 dark:text-green-200 text-xs rounded-full">Flexible</span>
                                    </div>
                                </label>
                                <label class="flex items-start gap-3 p-3 bg-green-50 dark:bg-green-900/20 rounded-lg cursor-pointer hover:bg-green-100 dark:hover:bg-green-900/30 border border-green-200 dark:border-green-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="grammar-vocabulary">
                                    <div class="flex-1">
                                        <p class="font-medium text-green-800 dark:text-green-200">Address grammar and vocabulary</p>
                                        <p class="text-sm text-green-600 dark:text-green-400">Improve sentence structure and word choice</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-green-200 dark:bg-green-800 text-green-800 dark:text-green-200 text-xs rounded-full">Flexible</span>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <div class="mt-4">
                            <label class="block text-sm font-medium mb-2">Add custom goals (optional):</label>
                            <textarea id="custom-goals" rows="2" placeholder="E.g., Improve vocabulary variety, fix specific grammar issues..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary"></textarea>
                        </div>
                    </div>

                    <!-- Strategic Planning -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">📋</span>
                            Strategic Planning
                        </h3>
                        <div class="grid md:grid-cols-2 gap-4">
                            <div class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                                <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Macro-Level Issues (Priority 1)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Content, organization, thesis, topic sentences</p>
                            </div>
                            <div class="p-4 bg-orange-50 dark:bg-orange-900/20 rounded-lg border-l-4 border-orange-500">
                                <h4 class="font-bold text-orange-900 dark:text-orange-200 mb-2">Micro-Level Issues (Priority 2)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Grammar, vocabulary, sentence structure</p>
                            </div>
                        </div>
                    </div>

                    <!-- Time Constraints -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">⏰</span>
                            Time Management
                        </h3>
                        <div class="p-4 bg-purple-50 dark:bg-purple-900/20 rounded-lg border-l-4 border-purple-500">
                            <div class="mb-3">
                                <label class="block text-sm font-bold mb-2 text-purple-900 dark:text-purple-200">
                                    How much time do you have for this session?
                                </label>
                                <p class="text-xs text-purple-700 dark:text-purple-300 mb-2">
                                    <span class="font-semibold">Recommended:</span> 15-20 minutes for focused revision
                                </p>
                            </div>
                            <select id="time-constraint" class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary">
                                <option value="15min">15 minutes (Quick focus)</option>
                                <option value="20min" selected>20 minutes (Recommended)</option>
                                <option value="30min">30 minutes</option>
                                <option value="45min">45 minutes</option>
                                <option value="60min">1 hour</option>
                            </select>
                            <div class="mt-2 p-2 bg-yellow-50 dark:bg-yellow-900/20 rounded border border-yellow-300 dark:border-yellow-700">
                                <p class="text-xs text-yellow-800 dark:text-yellow-200">
                                    <span class="font-semibold">💡 Tip:</span> Shorter sessions (15-20 min) help maintain focus on essential goals. Use the AI chatbot to explore options efficiently!
                                </p>
                            </div>
                        </div>
                    </div>

                    <!-- Goals Summary -->
                    <div id="selected-goals-summary" class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                        <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Your Selected Goals:</h4>
                        <div id="goals-list" class="text-sm text-gray-700 dark:text-gray-300"></div>
                    </div>

                    <!-- Confirmation Button -->
                    <div class="mt-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <button id="confirm-goals" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 rounded-lg transition-colors text-lg">
                            ✓ Confirm Goals and Proceed
                        </button>
                    </div>
                </div>
            </div>

            <!-- Right Panel: AI Conversation (1 column) -->
            <div class="lg:col-span-1">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md sticky top-6">
                    <h3 class="text-lg md:text-xl font-bold mb-4 flex items-center gap-2">
                        <span class="text-2xl">🤖</span>
                        AI Conversation
                    </h3>

                    <div id="chat-messages" class="bg-gray-50 dark:bg-gray-700 rounded-lg p-4 mb-4 overflow-y-auto" style="height: 500px;">
                        <div class="text-center text-gray-500 dark:text-gray-400 text-sm py-12">
                            Your conversation with the AI will appear here. The AI will help you negotiate and refine your revision goals.
                        </div>
                    </div>

                    <div id="loading-indicator" class="hidden text-center py-4">
                        <div class="inline-block animate-spin rounded-full h-6 w-6 border-b-2 border-primary"></div>
                        <p class="mt-2 text-xs text-gray-600 dark:text-gray-400">AI is thinking...</p>
                    </div>

                    <!-- General Chat Input -->
                    <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                        <textarea id="general-chat-input" rows="3" placeholder="Ask the AI about goal setting and strategic planning..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary mb-2"></textarea>
                        <button id="send-general-chat" class="w-full bg-primary hover:bg-primary-hover text-white font-semibold py-2 px-4 rounded-lg transition-colors">
                            Send Message
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Dark mode setup
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            document.documentElement.classList.add(event.matches ? 'dark' : '');
            !event.matches && document.documentElement.classList.remove('dark');
        });

        // State
        const state = {
            selectedGoals: [],
            timeConstraint: '60min'
        };

        // Goals tracking
        const goalCheckboxes = document.querySelectorAll('.goal-checkbox');
        goalCheckboxes.forEach(cb => cb.addEventListener('change', updateGoals));
        document.getElementById('custom-goals').addEventListener('input', updateGoals);
        document.getElementById('time-constraint').addEventListener('change', updateGoals);

        function updateGoals() {
            const goals = [];
            goalCheckboxes.forEach(cb => {
                if (cb.checked) {
                    goals.push(cb.parentElement.querySelector('p.font-medium').textContent);
                }
            });
            const custom = document.getElementById('custom-goals').value.trim();
            if (custom) goals.push(custom);

            state.selectedGoals = goals;
            state.timeConstraint = document.getElementById('time-constraint').value;

            document.getElementById('goals-list').innerHTML = goals.length > 0
                ? goals.map((g, i) => `<p>${i + 1}. ${g}</p>`).join('')
                : '<p class="text-gray-500">No goals selected</p>';
        }
        updateGoals();

        // Custom modal function
        function showCustomModal(message) {
            const modal = document.createElement('div');
            modal.className = 'fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50 p-4';
            modal.innerHTML = `
                <div class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow-2xl max-w-sm w-full border-2 border-primary">
                    <p class="text-gray-800 dark:text-gray-200 mb-4 text-base">${message}</p>
                    <button class="w-full px-4 py-2 bg-primary text-white hover:bg-primary-hover rounded-lg transition-colors font-semibold" onclick="this.closest('.fixed').remove()">OK</button>
                </div>
            `;
            document.body.appendChild(modal);
        }

        // Goals Confirmation
        document.getElementById('confirm-goals').addEventListener('click', () => {
            if (state.selectedGoals.length === 0) {
                showCustomModal('Please select at least one goal before proceeding.');
                return;
            }

            // Show confirmation message
            showCustomModal('Excellent! You\'ve set your revision goals. The AI will now provide guidance on strategic planning and goal negotiation.');
            
            // Generate AI messages about goal negotiation
            setTimeout(() => {
                addChatMessage("AI", `Great job setting your revision goals! 

**Goal 2: Negotiate with AI on Agenda and Goals**

You've demonstrated strategic thinking by:
- Selecting priority areas for revision
- Considering time constraints (${state.timeConstraint})
- Focusing on macro-level issues first

**Strategic Planning Tips:**
- **Macro-level first**: Content, organization, thesis, topic sentences
- **Micro-level second**: Grammar, vocabulary, sentence structure
- **Time management**: Focus on high-impact improvements within your time limit

**Next Steps:**
Your goals are well-prioritized. We'll work through them systematically, starting with the most impactful changes. Ready to begin with your thesis statement?`);
            }, 1000);

            // Disable the button after confirmation
            document.getElementById('confirm-goals').disabled = true;
            document.getElementById('confirm-goals').textContent = '✓ Goals Confirmed';
            document.getElementById('confirm-goals').classList.add('bg-gray-400', 'cursor-not-allowed');
        });

        // General chat
        document.getElementById('send-general-chat').addEventListener('click', () => {
            const msg = document.getElementById('general-chat-input').value.trim();
            if (!msg) return;
            askAI(`@Claude-Sonnet-4.5 Student question about goal setting: "${msg}"

Provide guidance on strategic planning and goal negotiation with AI. Keep response under 5 sentences.`);
            document.getElementById('general-chat-input').value = '';
        });

        // AI Communication
        function addChatMessage(sender, content) {
            const chat = document.getElementById('chat-messages');
            const placeholder = chat.querySelector('.text-center.text-gray-500');
            if (placeholder) placeholder.remove();

            const msg = document.createElement('div');
            msg.className = 'mb-3';
            msg.innerHTML = `
                <div class="text-xs font-semibold mb-1 ${sender === 'You' ? 'text-gray-600 dark:text-gray-400' : 'text-primary'}">${sender === 'You' ? '👤' : '🤖'} ${sender}</div>
                <div class="p-3 rounded-lg text-sm ${sender === 'You' ? 'bg-gray-200 dark:bg-gray-600' : 'bg-blue-50 dark:bg-blue-900/30'}">${marked.parse(content)}</div>
            `;
            chat.appendChild(msg);
            chat.scrollTop = chat.scrollHeight;
        }

        function updateLastAIMessage(content) {
            const chat = document.getElementById('chat-messages');
            const messages = chat.querySelectorAll('.mb-3');
            if (messages.length > 0) {
                const last = messages[messages.length - 1];
                const contentDiv = last.querySelector('.p-3');
                if (contentDiv) {
                    contentDiv.innerHTML = marked.parse(content);
                    chat.scrollTop = chat.scrollHeight;
                }
            }
        }

        if (window.Poe) {
            window.Poe.registerHandler("essay-training", (result) => {
                const msg = result.responses[0];
                document.getElementById('loading-indicator').classList.add('hidden');

                if (msg.status === "error") {
                    addChatMessage("AI", `Error: ${msg.statusText}`);
                } else if (msg.status === "incomplete") {
                    if (msg.content.trim()) {
                        updateLastAIMessage(msg.content);
                    }
                } else if (msg.status === "complete") {
                    updateLastAIMessage(msg.content);
                }
            });
        }

        async function askAI(prompt) {
            if (!window.Poe) {
                showCustomModal("Poe API not available. This app needs to run in the Poe environment.");
                return;
            }

            // Extract user message from prompt
            const userMsg = prompt.split('\n').slice(1).join('\n').substring(0, 100) + '...';
            addChatMessage("You", userMsg);
            addChatMessage("AI", "...");
            document.getElementById('loading-indicator').classList.remove('hidden');

            try {
                await window.Poe.sendUserMessage(prompt, {
                    handler: "essay-training",
                    stream: true,
                    openChat: false
                });
            } catch (err) {
                document.getElementById('loading-indicator').classList.add('hidden');
                addChatMessage("AI", `Error: ${err.message}`);
            }
        }

        console.log('Goal Setting tab loaded');
    </script>
</body>
</html>

```

Now let me enhance the AI chatbot section to better support goal exploration and negotiation:


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goal Setting - AI Essay Training Mode</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE',
                        'primary-hover': '#4a49c5',
                        'primary-light': '#ebebfa',
                    }
                }
            },
            darkMode: 'class'
        }
    </script>
    <style>
        .fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-gray-50 dark:bg-[#181818] text-gray-900 dark:text-gray-100 min-h-screen">
    <div class="container mx-auto px-4 py-6 max-w-7xl">
        <!-- Header -->
        <header class="mb-6">
            <h1 class="text-3xl md:text-4xl font-bold text-primary mb-2 text-center">Goal Setting</h1>
            <p class="text-base md:text-lg text-gray-600 dark:text-gray-400 text-center">Goal 2: Negotiate with AI on Agenda and Goals</p>
        </header>

        <!-- Main Content Grid -->
        <div class="grid lg:grid-cols-3 gap-6">
            <!-- Left Panel: Goal Setting (2 columns) -->
            <div class="lg:col-span-2 space-y-6">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md">
                    <h2 class="text-xl md:text-2xl font-bold mb-4 text-primary">Your Revision Goals</h2>

                    <!-- Goal 2 Explanation -->
                    <div class="mb-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <h3 class="font-bold text-blue-900 dark:text-blue-200 mb-2">Goal 2: Negotiate with AI on Agenda and Goals</h3>
                        <p class="text-sm text-gray-700 dark:text-gray-300 mb-3">
                            Learn to strategically plan your revision by setting priorities, considering time constraints, and focusing on macro-level issues first.
                        </p>
                        <div class="bg-yellow-50 dark:bg-yellow-900/20 p-3 rounded-lg border border-yellow-300 dark:border-yellow-700">
                            <p class="text-sm font-medium text-yellow-800 dark:text-yellow-200">
                                <span class="font-bold">🎯 Priority Focus:</span> Some goals are essential (thesis & topic sentences), while others offer flexibility (body paragraphs). Use the AI chatbot to explore your options!
                            </p>
                        </div>
                    </div>

                    <!-- AI-Suggested Goals -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">🎯</span>
                            AI-Suggested Goals Based on Your Essay
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">The AI has analyzed your essay and suggests these focus areas:</p>

                        <div class="p-4 bg-gray-50 dark:bg-gray-700 rounded-lg border-2 border-gray-300 dark:border-gray-600">
                            <h4 class="font-bold text-gray-800 dark:text-gray-200 mb-2">Suggested Revision Goals:</h4>
                            <ul class="space-y-2 text-sm text-gray-700 dark:text-gray-300">
                                <li>• <strong>Improve thesis statement clarity</strong> - Ensure it directly answers the question and includes 2 specific points</li>
                                <li>• <strong>Strengthen topic sentences</strong> - Make them echo and support thesis points</li>
                                <li>• <strong>Enhance body paragraph development</strong> - Focus on one paragraph to improve detail and coherence</li>
                                <li>• <strong>Address grammar and sentence structure</strong> - Improve clarity and flow</li>
                            </ul>
                        </div>
                    </div>

                    <!-- Student Goal Selection -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">✏️</span>
                            Select Your Priority Goals
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">Choose what you want to focus on in this session:</p>

                        <!-- Required Goals Section -->
                        <div class="mb-4">
                            <h4 class="text-md font-bold mb-3 flex items-center gap-2 text-red-700 dark:text-red-400">
                                <span class="text-lg">🔴</span>
                                Essential Goals (Required)
                            </h4>
                            <p class="text-xs text-gray-600 dark:text-gray-400 mb-3">These are fundamental to your essay structure and must be addressed:</p>
                            
                            <div class="space-y-3">
                                <label class="flex items-start gap-3 p-3 bg-red-50 dark:bg-red-900/20 rounded-lg cursor-pointer hover:bg-red-100 dark:hover:bg-red-900/30 border border-red-200 dark:border-red-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="thesis" checked disabled>
                                    <div class="flex-1">
                                        <p class="font-medium text-red-800 dark:text-red-200">Improve thesis statement clarity</p>
                                        <p class="text-sm text-red-600 dark:text-red-400">Ensure it answers the question and includes 2 specific points</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-red-200 dark:bg-red-800 text-red-800 dark:text-red-200 text-xs rounded-full">Required</span>
                                    </div>
                                </label>
                                <label class="flex items-start gap-3 p-3 bg-red-50 dark:bg-red-900/20 rounded-lg cursor-pointer hover:bg-red-100 dark:hover:bg-red-900/30 border border-red-200 dark:border-red-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="topic-sentences" checked disabled>
                                    <div class="flex-1">
                                        <p class="font-medium text-red-800 dark:text-red-200">Strengthen topic sentences</p>
                                        <p class="text-sm text-red-600 dark:text-red-400">Make them echo and support thesis points</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-red-200 dark:bg-red-800 text-red-800 dark:text-red-200 text-xs rounded-full">Required</span>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <!-- Flexible Goals Section -->
                        <div class="mb-4">
                            <h4 class="text-md font-bold mb-3 flex items-center gap-2 text-green-700 dark:text-green-400">
                                <span class="text-lg">🟢</span>
                                Flexible Goals (Your Choice)
                            </h4>
                            <p class="text-xs text-gray-600 dark:text-gray-400 mb-3">Choose based on your essay's needs and time available:</p>
                            
                            <div class="space-y-3">
                                <label class="flex items-start gap-3 p-3 bg-green-50 dark:bg-green-900/20 rounded-lg cursor-pointer hover:bg-green-100 dark:hover:bg-green-900/30 border border-green-200 dark:border-green-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="paragraph-development" checked>
                                    <div class="flex-1">
                                        <p class="font-medium text-green-800 dark:text-green-200">Enhance body paragraph development</p>
                                        <p class="text-sm text-green-600 dark:text-green-400">Focus on one paragraph to improve detail and coherence</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-green-200 dark:bg-green-800 text-green-800 dark:text-green-200 text-xs rounded-full">Flexible</span>
                                    </div>
                                </label>
                                <label class="flex items-start gap-3 p-3 bg-green-50 dark:bg-green-900/20 rounded-lg cursor-pointer hover:bg-green-100 dark:hover:bg-green-900/30 border border-green-200 dark:border-green-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="grammar-vocabulary">
                                    <div class="flex-1">
                                        <p class="font-medium text-green-800 dark:text-green-200">Address grammar and vocabulary</p>
                                        <p class="text-sm text-green-600 dark:text-green-400">Improve sentence structure and word choice</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-green-200 dark:bg-green-800 text-green-800 dark:text-green-200 text-xs rounded-full">Flexible</span>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <div class="mt-4">
                            <label class="block text-sm font-medium mb-2">Add custom goals (optional):</label>
                            <textarea id="custom-goals" rows="2" placeholder="E.g., Improve vocabulary variety, fix specific grammar issues..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary"></textarea>
                        </div>
                    </div>

                    <!-- Strategic Planning -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">📋</span>
                            Strategic Planning
                        </h3>
                        <div class="grid md:grid-cols-2 gap-4">
                            <div class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                                <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Macro-Level Issues (Priority 1)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Content, organization, thesis, topic sentences</p>
                            </div>
                            <div class="p-4 bg-orange-50 dark:bg-orange-900/20 rounded-lg border-l-4 border-orange-500">
                                <h4 class="font-bold text-orange-900 dark:text-orange-200 mb-2">Micro-Level Issues (Priority 2)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Grammar, vocabulary, sentence structure</p>
                            </div>
                        </div>
                    </div>

                    <!-- Time Constraints -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">⏰</span>
                            Time Management
                        </h3>
                        <div class="p-4 bg-purple-50 dark:bg-purple-900/20 rounded-lg border-l-4 border-purple-500">
                            <div class="mb-3">
                                <label class="block text-sm font-bold mb-2 text-purple-900 dark:text-purple-200">
                                    How much time do you have for this session?
                                </label>
                                <p class="text-xs text-purple-700 dark:text-purple-300 mb-2">
                                    <span class="font-semibold">Recommended:</span> 15-20 minutes for focused revision
                                </p>
                            </div>
                            <select id="time-constraint" class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary">
                                <option value="15min">15 minutes (Quick focus)</option>
                                <option value="20min" selected>20 minutes (Recommended)</option>
                                <option value="30min">30 minutes</option>
                                <option value="45min">45 minutes</option>
                                <option value="60min">1 hour</option>
                            </select>
                            <div class="mt-2 p-2 bg-yellow-50 dark:bg-yellow-900/20 rounded border border-yellow-300 dark:border-yellow-700">
                                <p class="text-xs text-yellow-800 dark:text-yellow-200">
                                    <span class="font-semibold">💡 Tip:</span> Shorter sessions (15-20 min) help maintain focus on essential goals. Use the AI chatbot to explore options efficiently!
                                </p>
                            </div>
                        </div>
                    </div>

                    <!-- Goals Summary -->
                    <div id="selected-goals-summary" class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                        <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Your Selected Goals:</h4>
                        <div id="goals-list" class="text-sm text-gray-700 dark:text-gray-300"></div>
                    </div>

                    <!-- Confirmation Button -->
                    <div class="mt-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <button id="confirm-goals" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 rounded-lg transition-colors text-lg">
                            ✓ Confirm Goals and Proceed
                        </button>
                    </div>
                </div>
            </div>

            <!-- Right Panel: AI Conversation (1 column) -->
            <div class="lg:col-span-1">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md sticky top-6">
                    <h3 class="text-lg md:text-xl font-bold mb-4 flex items-center gap-2">
                        <span class="text-2xl">🤖</span>
                        AI Goal Explorer
                    </h3>
                    
                    <div class="mb-4 p-3 bg-blue-50 dark:bg-blue-900/20 rounded-lg border border-blue-200 dark:border-blue-800">
                        <p class="text-sm text-blue-800 dark:text-blue-200">
                            <span class="font-semibold">💬 Chat with AI to:</span> Explore goal options, understand priorities, and negotiate your revision strategy.
                        </p>
                    </div>

                    <div id="chat-messages" class="bg-gray-50 dark:bg-gray-700 rounded-lg p-4 mb-4 overflow-y-auto" style="height: 400px;">
                        <div class="text-center text-gray-500 dark:text-gray-400 text-sm py-8">
                            <div class="mb-4">
                                <span class="text-2xl">🎯</span>
                            </div>
                            <p class="mb-2 font-medium">Ready to explore your goals?</p>
                            <p class="text-xs">Ask the AI about:</p>
                            <ul class="text-xs mt-2 space-y-1 text-left">
                                <li>• Which goals are most important?</li>
                                <li>• How to prioritize with limited time?</li>
                                <li>• What makes a strong thesis statement?</li>
                                <li>• How to improve topic sentences?</li>
                            </ul>
                        </div>
                    </div>

                    <div id="loading-indicator" class="hidden text-center py-4">
                        <div class="inline-block animate-spin rounded-full h-6 w-6 border-b-2 border-primary"></div>
                        <p class="mt-2 text-xs text-gray-600 dark:text-gray-400">AI is thinking...</p>
                    </div>

                    <!-- Quick Action Buttons -->
                    <div class="mb-4">
                        <p class="text-xs font-medium text-gray-600 dark:text-gray-400 mb-2">Quick questions:</p>
                        <div class="grid grid-cols-2 gap-2">
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="What should I focus on first?">
                                Focus priorities
                            </button>
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="How do I improve my thesis statement?">
                                Thesis help
                            </button>
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="What makes good topic sentences?">
                                Topic sentences
                            </button>
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="How much can I accomplish in 20 minutes?">
                                Time planning
                            </button>
                        </div>
                    </div>

                    <!-- General Chat Input -->
                    <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                        <textarea id="general-chat-input" rows="3" placeholder="Ask the AI about goal setting, priorities, or revision strategy..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary mb-2"></textarea>
                        <button id="send-general-chat" class="w-full bg-primary hover:bg-primary-hover text-white font-semibold py-2 px-4 rounded-lg transition-colors">
                            Send Message
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Dark mode setup
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            document.documentElement.classList.add(event.matches ? 'dark' : '');
            !event.matches && document.documentElement.classList.remove('dark');
        });

        // State
        const state = {
            selectedGoals: [],
            timeConstraint: '60min'
        };

        // Goals tracking
        const goalCheckboxes = document.querySelectorAll('.goal-checkbox');
        goalCheckboxes.forEach(cb => cb.addEventListener('change', updateGoals));
        document.getElementById('custom-goals').addEventListener('input', updateGoals);
        document.getElementById('time-constraint').addEventListener('change', updateGoals);

        function updateGoals() {
            const goals = [];
            goalCheckboxes.forEach(cb => {
                if (cb.checked) {
                    goals.push(cb.parentElement.querySelector('p.font-medium').textContent);
                }
            });
            const custom = document.getElementById('custom-goals').value.trim();
            if (custom) goals.push(custom);

            state.selectedGoals = goals;
            state.timeConstraint = document.getElementById('time-constraint').value;

            document.getElementById('goals-list').innerHTML = goals.length > 0
                ? goals.map((g, i) => `<p>${i + 1}. ${g}</p>`).join('')
                : '<p class="text-gray-500">No goals selected</p>';
        }
        updateGoals();

        // Custom modal function
        function showCustomModal(message) {
            const modal = document.createElement('div');
            modal.className = 'fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50 p-4';
            modal.innerHTML = `
                <div class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow-2xl max-w-sm w-full border-2 border-primary">
                    <p class="text-gray-800 dark:text-gray-200 mb-4 text-base">${message}</p>
                    <button class="w-full px-4 py-2 bg-primary text-white hover:bg-primary-hover rounded-lg transition-colors font-semibold" onclick="this.closest('.fixed').remove()">OK</button>
                </div>
            `;
            document.body.appendChild(modal);
        }

        // Goals Confirmation
        document.getElementById('confirm-goals').addEventListener('click', () => {
            if (state.selectedGoals.length === 0) {
                showCustomModal('Please select at least one goal before proceeding.');
                return;
            }

            // Show confirmation message
            showCustomModal('Excellent! You\'ve set your revision goals. The AI will now provide guidance on strategic planning and goal negotiation.');
            
            // Generate AI messages about goal negotiation
            setTimeout(() => {
                addChatMessage("AI", `Great job setting your revision goals! 

**Goal 2: Negotiate with AI on Agenda and Goals**

You've demonstrated strategic thinking by:
- Selecting priority areas for revision
- Considering time constraints (${state.timeConstraint})
- Focusing on macro-level issues first

**Strategic Planning Tips:**
- **Macro-level first**: Content, organization, thesis, topic sentences
- **Micro-level second**: Grammar, vocabulary, sentence structure
- **Time management**: Focus on high-impact improvements within your time limit

**Next Steps:**
Your goals are well-prioritized. We'll work through them systematically, starting with the most impactful changes. Ready to begin with your thesis statement?`);
            }, 1000);

            // Disable the button after confirmation
            document.getElementById('confirm-goals').disabled = true;
            document.getElementById('confirm-goals').textContent = '✓ Goals Confirmed';
            document.getElementById('confirm-goals').classList.add('bg-gray-400', 'cursor-not-allowed');
        });

        // General chat
        document.getElementById('send-general-chat').addEventListener('click', () => {
            const msg = document.getElementById('general-chat-input').value.trim();
            if (!msg) return;
            askAI(`@Claude-Sonnet-4.5 Student question about goal setting: "${msg}"

Provide guidance on strategic planning and goal negotiation with AI. Keep response under 5 sentences.`);
            document.getElementById('general-chat-input').value = '';
        });

        // AI Communication
        function addChatMessage(sender, content) {
            const chat = document.getElementById('chat-messages');
            const placeholder = chat.querySelector('.text-center.text-gray-500');
            if (placeholder) placeholder.remove();

            const msg = document.createElement('div');
            msg.className = 'mb-3';
            msg.innerHTML = `
                <div class="text-xs font-semibold mb-1 ${sender === 'You' ? 'text-gray-600 dark:text-gray-400' : 'text-primary'}">${sender === 'You' ? '👤' : '🤖'} ${sender}</div>
                <div class="p-3 rounded-lg text-sm ${sender === 'You' ? 'bg-gray-200 dark:bg-gray-600' : 'bg-blue-50 dark:bg-blue-900/30'}">${marked.parse(content)}</div>
            `;
            chat.appendChild(msg);
            chat.scrollTop = chat.scrollHeight;
        }

        function updateLastAIMessage(content) {
            const chat = document.getElementById('chat-messages');
            const messages = chat.querySelectorAll('.mb-3');
            if (messages.length > 0) {
                const last = messages[messages.length - 1];
                const contentDiv = last.querySelector('.p-3');
                if (contentDiv) {
                    contentDiv.innerHTML = marked.parse(content);
                    chat.scrollTop = chat.scrollHeight;
                }
            }
        }

        if (window.Poe) {
            window.Poe.registerHandler("essay-training", (result) => {
                const msg = result.responses[0];
                document.getElementById('loading-indicator').classList.add('hidden');

                if (msg.status === "error") {
                    addChatMessage("AI", `Error: ${msg.statusText}`);
                } else if (msg.status === "incomplete") {
                    if (msg.content.trim()) {
                        updateLastAIMessage(msg.content);
                    }
                } else if (msg.status === "complete") {
                    updateLastAIMessage(msg.content);
                }
            });
        }

        async function askAI(prompt) {
            if (!window.Poe) {
                showCustomModal("Poe API not available. This app needs to run in the Poe environment.");
                return;
            }

            // Extract user message from prompt
            const userMsg = prompt.split('\n').slice(1).join('\n').substring(0, 100) + '...';
            addChatMessage("You", userMsg);
            addChatMessage("AI", "...");
            document.getElementById('loading-indicator').classList.remove('hidden');

            try {
                await window.Poe.sendUserMessage(prompt, {
                    handler: "essay-training",
                    stream: true,
                    openChat: false
                });
            } catch (err) {
                document.getElementById('loading-indicator').classList.add('hidden');
                addChatMessage("AI", `Error: ${err.message}`);
            }
        }

        console.log('Goal Setting tab loaded');
    </script>
</body>
</html>

```

Now I need to update the JavaScript to handle the quick question buttons and update the default time constraint:


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goal Setting - AI Essay Training Mode</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE',
                        'primary-hover': '#4a49c5',
                        'primary-light': '#ebebfa',
                    }
                }
            },
            darkMode: 'class'
        }
    </script>
    <style>
        .fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-gray-50 dark:bg-[#181818] text-gray-900 dark:text-gray-100 min-h-screen">
    <div class="container mx-auto px-4 py-6 max-w-7xl">
        <!-- Header -->
        <header class="mb-6">
            <h1 class="text-3xl md:text-4xl font-bold text-primary mb-2 text-center">Goal Setting</h1>
            <p class="text-base md:text-lg text-gray-600 dark:text-gray-400 text-center">Goal 2: Negotiate with AI on Agenda and Goals</p>
        </header>

        <!-- Main Content Grid -->
        <div class="grid lg:grid-cols-3 gap-6">
            <!-- Left Panel: Goal Setting (2 columns) -->
            <div class="lg:col-span-2 space-y-6">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md">
                    <h2 class="text-xl md:text-2xl font-bold mb-4 text-primary">Your Revision Goals</h2>

                    <!-- Goal 2 Explanation -->
                    <div class="mb-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <h3 class="font-bold text-blue-900 dark:text-blue-200 mb-2">Goal 2: Negotiate with AI on Agenda and Goals</h3>
                        <p class="text-sm text-gray-700 dark:text-gray-300 mb-3">
                            Learn to strategically plan your revision by setting priorities, considering time constraints, and focusing on macro-level issues first.
                        </p>
                        <div class="bg-yellow-50 dark:bg-yellow-900/20 p-3 rounded-lg border border-yellow-300 dark:border-yellow-700">
                            <p class="text-sm font-medium text-yellow-800 dark:text-yellow-200">
                                <span class="font-bold">🎯 Priority Focus:</span> Some goals are essential (thesis & topic sentences), while others offer flexibility (body paragraphs). Use the AI chatbot to explore your options!
                            </p>
                        </div>
                    </div>

                    <!-- AI-Suggested Goals -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">🎯</span>
                            AI-Suggested Goals Based on Your Essay
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">The AI has analyzed your essay and suggests these focus areas:</p>

                        <div class="p-4 bg-gray-50 dark:bg-gray-700 rounded-lg border-2 border-gray-300 dark:border-gray-600">
                            <h4 class="font-bold text-gray-800 dark:text-gray-200 mb-2">Suggested Revision Goals:</h4>
                            <ul class="space-y-2 text-sm text-gray-700 dark:text-gray-300">
                                <li>• <strong>Improve thesis statement clarity</strong> - Ensure it directly answers the question and includes 2 specific points</li>
                                <li>• <strong>Strengthen topic sentences</strong> - Make them echo and support thesis points</li>
                                <li>• <strong>Enhance body paragraph development</strong> - Focus on one paragraph to improve detail and coherence</li>
                                <li>• <strong>Address grammar and sentence structure</strong> - Improve clarity and flow</li>
                            </ul>
                        </div>
                    </div>

                    <!-- Student Goal Selection -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">✏️</span>
                            Select Your Priority Goals
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">Choose what you want to focus on in this session:</p>

                        <!-- Required Goals Section -->
                        <div class="mb-4">
                            <h4 class="text-md font-bold mb-3 flex items-center gap-2 text-red-700 dark:text-red-400">
                                <span class="text-lg">🔴</span>
                                Essential Goals (Required)
                            </h4>
                            <p class="text-xs text-gray-600 dark:text-gray-400 mb-3">These are fundamental to your essay structure and must be addressed:</p>
                            
                            <div class="space-y-3">
                                <label class="flex items-start gap-3 p-3 bg-red-50 dark:bg-red-900/20 rounded-lg cursor-pointer hover:bg-red-100 dark:hover:bg-red-900/30 border border-red-200 dark:border-red-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="thesis" checked disabled>
                                    <div class="flex-1">
                                        <p class="font-medium text-red-800 dark:text-red-200">Improve thesis statement clarity</p>
                                        <p class="text-sm text-red-600 dark:text-red-400">Ensure it answers the question and includes 2 specific points</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-red-200 dark:bg-red-800 text-red-800 dark:text-red-200 text-xs rounded-full">Required</span>
                                    </div>
                                </label>
                                <label class="flex items-start gap-3 p-3 bg-red-50 dark:bg-red-900/20 rounded-lg cursor-pointer hover:bg-red-100 dark:hover:bg-red-900/30 border border-red-200 dark:border-red-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="topic-sentences" checked disabled>
                                    <div class="flex-1">
                                        <p class="font-medium text-red-800 dark:text-red-200">Strengthen topic sentences</p>
                                        <p class="text-sm text-red-600 dark:text-red-400">Make them echo and support thesis points</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-red-200 dark:bg-red-800 text-red-800 dark:text-red-200 text-xs rounded-full">Required</span>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <!-- Flexible Goals Section -->
                        <div class="mb-4">
                            <h4 class="text-md font-bold mb-3 flex items-center gap-2 text-green-700 dark:text-green-400">
                                <span class="text-lg">🟢</span>
                                Flexible Goals (Your Choice)
                            </h4>
                            <p class="text-xs text-gray-600 dark:text-gray-400 mb-3">Choose based on your essay's needs and time available:</p>
                            
                            <div class="space-y-3">
                                <label class="flex items-start gap-3 p-3 bg-green-50 dark:bg-green-900/20 rounded-lg cursor-pointer hover:bg-green-100 dark:hover:bg-green-900/30 border border-green-200 dark:border-green-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="paragraph-development" checked>
                                    <div class="flex-1">
                                        <p class="font-medium text-green-800 dark:text-green-200">Enhance body paragraph development</p>
                                        <p class="text-sm text-green-600 dark:text-green-400">Focus on one paragraph to improve detail and coherence</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-green-200 dark:bg-green-800 text-green-800 dark:text-green-200 text-xs rounded-full">Flexible</span>
                                    </div>
                                </label>
                                <label class="flex items-start gap-3 p-3 bg-green-50 dark:bg-green-900/20 rounded-lg cursor-pointer hover:bg-green-100 dark:hover:bg-green-900/30 border border-green-200 dark:border-green-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="grammar-vocabulary">
                                    <div class="flex-1">
                                        <p class="font-medium text-green-800 dark:text-green-200">Address grammar and vocabulary</p>
                                        <p class="text-sm text-green-600 dark:text-green-400">Improve sentence structure and word choice</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-green-200 dark:bg-green-800 text-green-800 dark:text-green-200 text-xs rounded-full">Flexible</span>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <div class="mt-4">
                            <label class="block text-sm font-medium mb-2">Add custom goals (optional):</label>
                            <textarea id="custom-goals" rows="2" placeholder="E.g., Improve vocabulary variety, fix specific grammar issues..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary"></textarea>
                        </div>
                    </div>

                    <!-- Strategic Planning -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">📋</span>
                            Strategic Planning
                        </h3>
                        <div class="grid md:grid-cols-2 gap-4">
                            <div class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                                <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Macro-Level Issues (Priority 1)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Content, organization, thesis, topic sentences</p>
                            </div>
                            <div class="p-4 bg-orange-50 dark:bg-orange-900/20 rounded-lg border-l-4 border-orange-500">
                                <h4 class="font-bold text-orange-900 dark:text-orange-200 mb-2">Micro-Level Issues (Priority 2)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Grammar, vocabulary, sentence structure</p>
                            </div>
                        </div>
                    </div>

                    <!-- Time Constraints -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">⏰</span>
                            Time Management
                        </h3>
                        <div class="p-4 bg-purple-50 dark:bg-purple-900/20 rounded-lg border-l-4 border-purple-500">
                            <div class="mb-3">
                                <label class="block text-sm font-bold mb-2 text-purple-900 dark:text-purple-200">
                                    How much time do you have for this session?
                                </label>
                                <p class="text-xs text-purple-700 dark:text-purple-300 mb-2">
                                    <span class="font-semibold">Recommended:</span> 15-20 minutes for focused revision
                                </p>
                            </div>
                            <select id="time-constraint" class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary">
                                <option value="15min">15 minutes (Quick focus)</option>
                                <option value="20min" selected>20 minutes (Recommended)</option>
                                <option value="30min">30 minutes</option>
                                <option value="45min">45 minutes</option>
                                <option value="60min">1 hour</option>
                            </select>
                            <div class="mt-2 p-2 bg-yellow-50 dark:bg-yellow-900/20 rounded border border-yellow-300 dark:border-yellow-700">
                                <p class="text-xs text-yellow-800 dark:text-yellow-200">
                                    <span class="font-semibold">💡 Tip:</span> Shorter sessions (15-20 min) help maintain focus on essential goals. Use the AI chatbot to explore options efficiently!
                                </p>
                            </div>
                        </div>
                    </div>

                    <!-- Goals Summary -->
                    <div id="selected-goals-summary" class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                        <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Your Selected Goals:</h4>
                        <div id="goals-list" class="text-sm text-gray-700 dark:text-gray-300"></div>
                    </div>

                    <!-- Confirmation Button -->
                    <div class="mt-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <button id="confirm-goals" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 rounded-lg transition-colors text-lg">
                            ✓ Confirm Goals and Proceed
                        </button>
                    </div>
                </div>
            </div>

            <!-- Right Panel: AI Conversation (1 column) -->
            <div class="lg:col-span-1">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md sticky top-6">
                    <h3 class="text-lg md:text-xl font-bold mb-4 flex items-center gap-2">
                        <span class="text-2xl">🤖</span>
                        AI Goal Explorer
                    </h3>
                    
                    <div class="mb-4 p-3 bg-blue-50 dark:bg-blue-900/20 rounded-lg border border-blue-200 dark:border-blue-800">
                        <p class="text-sm text-blue-800 dark:text-blue-200">
                            <span class="font-semibold">💬 Chat with AI to:</span> Explore goal options, understand priorities, and negotiate your revision strategy.
                        </p>
                    </div>

                    <div id="chat-messages" class="bg-gray-50 dark:bg-gray-700 rounded-lg p-4 mb-4 overflow-y-auto" style="height: 400px;">
                        <div class="text-center text-gray-500 dark:text-gray-400 text-sm py-8">
                            <div class="mb-4">
                                <span class="text-2xl">🎯</span>
                            </div>
                            <p class="mb-2 font-medium">Ready to explore your goals?</p>
                            <p class="text-xs">Ask the AI about:</p>
                            <ul class="text-xs mt-2 space-y-1 text-left">
                                <li>• Which goals are most important?</li>
                                <li>• How to prioritize with limited time?</li>
                                <li>• What makes a strong thesis statement?</li>
                                <li>• How to improve topic sentences?</li>
                            </ul>
                        </div>
                    </div>

                    <div id="loading-indicator" class="hidden text-center py-4">
                        <div class="inline-block animate-spin rounded-full h-6 w-6 border-b-2 border-primary"></div>
                        <p class="mt-2 text-xs text-gray-600 dark:text-gray-400">AI is thinking...</p>
                    </div>

                    <!-- Quick Action Buttons -->
                    <div class="mb-4">
                        <p class="text-xs font-medium text-gray-600 dark:text-gray-400 mb-2">Quick questions:</p>
                        <div class="grid grid-cols-2 gap-2">
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="What should I focus on first?">
                                Focus priorities
                            </button>
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="How do I improve my thesis statement?">
                                Thesis help
                            </button>
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="What makes good topic sentences?">
                                Topic sentences
                            </button>
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="How much can I accomplish in 20 minutes?">
                                Time planning
                            </button>
                        </div>
                    </div>

                    <!-- General Chat Input -->
                    <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                        <textarea id="general-chat-input" rows="3" placeholder="Ask the AI about goal setting, priorities, or revision strategy..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary mb-2"></textarea>
                        <button id="send-general-chat" class="w-full bg-primary hover:bg-primary-hover text-white font-semibold py-2 px-4 rounded-lg transition-colors">
                            Send Message
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Dark mode setup
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            document.documentElement.classList.add(event.matches ? 'dark' : '');
            !event.matches && document.documentElement.classList.remove('dark');
        });

        // State
        const state = {
            selectedGoals: [],
            timeConstraint: '20min'
        };

        // Goals tracking
        const goalCheckboxes = document.querySelectorAll('.goal-checkbox');
        goalCheckboxes.forEach(cb => cb.addEventListener('change', updateGoals));
        document.getElementById('custom-goals').addEventListener('input', updateGoals);
        document.getElementById('time-constraint').addEventListener('change', updateGoals);

        function updateGoals() {
            const goals = [];
            goalCheckboxes.forEach(cb => {
                if (cb.checked) {
                    goals.push(cb.parentElement.querySelector('p.font-medium').textContent);
                }
            });
            const custom = document.getElementById('custom-goals').value.trim();
            if (custom) goals.push(custom);

            state.selectedGoals = goals;
            state.timeConstraint = document.getElementById('time-constraint').value;

            document.getElementById('goals-list').innerHTML = goals.length > 0
                ? goals.map((g, i) => `<p>${i + 1}. ${g}</p>`).join('')
                : '<p class="text-gray-500">No goals selected</p>';
        }
        updateGoals();

        // Custom modal function
        function showCustomModal(message) {
            const modal = document.createElement('div');
            modal.className = 'fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50 p-4';
            modal.innerHTML = `
                <div class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow-2xl max-w-sm w-full border-2 border-primary">
                    <p class="text-gray-800 dark:text-gray-200 mb-4 text-base">${message}</p>
                    <button class="w-full px-4 py-2 bg-primary text-white hover:bg-primary-hover rounded-lg transition-colors font-semibold" onclick="this.closest('.fixed').remove()">OK</button>
                </div>
            `;
            document.body.appendChild(modal);
        }

        // Goals Confirmation
        document.getElementById('confirm-goals').addEventListener('click', () => {
            if (state.selectedGoals.length === 0) {
                showCustomModal('Please select at least one goal before proceeding.');
                return;
            }

            // Show confirmation message
            showCustomModal('Excellent! You\'ve set your revision goals. The AI will now provide guidance on strategic planning and goal negotiation.');
            
            // Generate AI messages about goal negotiation
            setTimeout(() => {
                addChatMessage("AI", `Great job setting your revision goals! 

**Goal 2: Negotiate with AI on Agenda and Goals**

You've demonstrated strategic thinking by:
- Selecting priority areas for revision
- Considering time constraints (${state.timeConstraint})
- Focusing on macro-level issues first

**Strategic Planning Tips:**
- **Macro-level first**: Content, organization, thesis, topic sentences
- **Micro-level second**: Grammar, vocabulary, sentence structure
- **Time management**: Focus on high-impact improvements within your time limit

**Next Steps:**
Your goals are well-prioritized. We'll work through them systematically, starting with the most impactful changes. Ready to begin with your thesis statement?`);
            }, 1000);

            // Disable the button after confirmation
            document.getElementById('confirm-goals').disabled = true;
            document.getElementById('confirm-goals').textContent = '✓ Goals Confirmed';
            document.getElementById('confirm-goals').classList.add('bg-gray-400', 'cursor-not-allowed');
        });

        // General chat
        document.getElementById('send-general-chat').addEventListener('click', () => {
            const msg = document.getElementById('general-chat-input').value.trim();
            if (!msg) return;
            askAI(`@Claude-Sonnet-4.5 Student question about goal setting: "${msg}"

Provide guidance on strategic planning and goal negotiation with AI. Keep response under 5 sentences.`);
            document.getElementById('general-chat-input').value = '';
        });

        // AI Communication
        function addChatMessage(sender, content) {
            const chat = document.getElementById('chat-messages');
            const placeholder = chat.querySelector('.text-center.text-gray-500');
            if (placeholder) placeholder.remove();

            const msg = document.createElement('div');
            msg.className = 'mb-3';
            msg.innerHTML = `
                <div class="text-xs font-semibold mb-1 ${sender === 'You' ? 'text-gray-600 dark:text-gray-400' : 'text-primary'}">${sender === 'You' ? '👤' : '🤖'} ${sender}</div>
                <div class="p-3 rounded-lg text-sm ${sender === 'You' ? 'bg-gray-200 dark:bg-gray-600' : 'bg-blue-50 dark:bg-blue-900/30'}">${marked.parse(content)}</div>
            `;
            chat.appendChild(msg);
            chat.scrollTop = chat.scrollHeight;
        }

        function updateLastAIMessage(content) {
            const chat = document.getElementById('chat-messages');
            const messages = chat.querySelectorAll('.mb-3');
            if (messages.length > 0) {
                const last = messages[messages.length - 1];
                const contentDiv = last.querySelector('.p-3');
                if (contentDiv) {
                    contentDiv.innerHTML = marked.parse(content);
                    chat.scrollTop = chat.scrollHeight;
                }
            }
        }

        if (window.Poe) {
            window.Poe.registerHandler("essay-training", (result) => {
                const msg = result.responses[0];
                document.getElementById('loading-indicator').classList.add('hidden');

                if (msg.status === "error") {
                    addChatMessage("AI", `Error: ${msg.statusText}`);
                } else if (msg.status === "incomplete") {
                    if (msg.content.trim()) {
                        updateLastAIMessage(msg.content);
                    }
                } else if (msg.status === "complete") {
                    updateLastAIMessage(msg.content);
                }
            });
        }

        async function askAI(prompt) {
            if (!window.Poe) {
                showCustomModal("Poe API not available. This app needs to run in the Poe environment.");
                return;
            }

            // Extract user message from prompt
            const userMsg = prompt.split('\n').slice(1).join('\n').substring(0, 100) + '...';
            addChatMessage("You", userMsg);
            addChatMessage("AI", "...");
            document.getElementById('loading-indicator').classList.remove('hidden');

            try {
                await window.Poe.sendUserMessage(prompt, {
                    handler: "essay-training",
                    stream: true,
                    openChat: false
                });
            } catch (err) {
                document.getElementById('loading-indicator').classList.add('hidden');
                addChatMessage("AI", `Error: ${err.message}`);
            }
        }

        console.log('Goal Setting tab loaded');
    </script>
</body>
</html>

```

Now let me add the JavaScript functionality for the quick question buttons:


```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goal Setting - AI Essay Training Mode</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/marked/marked.min.js"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#5D5CDE',
                        'primary-hover': '#4a49c5',
                        'primary-light': '#ebebfa',
                    }
                }
            },
            darkMode: 'class'
        }
    </script>
    <style>
        .fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="bg-gray-50 dark:bg-[#181818] text-gray-900 dark:text-gray-100 min-h-screen">
    <div class="container mx-auto px-4 py-6 max-w-7xl">
        <!-- Header -->
        <header class="mb-6">
            <h1 class="text-3xl md:text-4xl font-bold text-primary mb-2 text-center">Goal Setting</h1>
            <p class="text-base md:text-lg text-gray-600 dark:text-gray-400 text-center">Goal 2: Negotiate with AI on Agenda and Goals</p>
        </header>

        <!-- Main Content Grid -->
        <div class="grid lg:grid-cols-3 gap-6">
            <!-- Left Panel: Goal Setting (2 columns) -->
            <div class="lg:col-span-2 space-y-6">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md">
                    <h2 class="text-xl md:text-2xl font-bold mb-4 text-primary">Your Revision Goals</h2>

                    <!-- Goal 2 Explanation -->
                    <div class="mb-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <h3 class="font-bold text-blue-900 dark:text-blue-200 mb-2">Goal 2: Negotiate with AI on Agenda and Goals</h3>
                        <p class="text-sm text-gray-700 dark:text-gray-300 mb-3">
                            Learn to strategically plan your revision by setting priorities, considering time constraints, and focusing on macro-level issues first.
                        </p>
                        <div class="bg-yellow-50 dark:bg-yellow-900/20 p-3 rounded-lg border border-yellow-300 dark:border-yellow-700">
                            <p class="text-sm font-medium text-yellow-800 dark:text-yellow-200">
                                <span class="font-bold">🎯 Priority Focus:</span> Some goals are essential (thesis & topic sentences), while others offer flexibility (body paragraphs). Use the AI chatbot to explore your options!
                            </p>
                        </div>
                    </div>

                    <!-- AI-Suggested Goals -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">🎯</span>
                            AI-Suggested Goals Based on Your Essay
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">The AI has analyzed your essay and suggests these focus areas:</p>

                        <div class="p-4 bg-gray-50 dark:bg-gray-700 rounded-lg border-2 border-gray-300 dark:border-gray-600">
                            <h4 class="font-bold text-gray-800 dark:text-gray-200 mb-2">Suggested Revision Goals:</h4>
                            <ul class="space-y-2 text-sm text-gray-700 dark:text-gray-300">
                                <li>• <strong>Improve thesis statement clarity</strong> - Ensure it directly answers the question and includes 2 specific points</li>
                                <li>• <strong>Strengthen topic sentences</strong> - Make them echo and support thesis points</li>
                                <li>• <strong>Enhance body paragraph development</strong> - Focus on one paragraph to improve detail and coherence</li>
                                <li>• <strong>Address grammar and sentence structure</strong> - Improve clarity and flow</li>
                            </ul>
                        </div>
                    </div>

                    <!-- Student Goal Selection -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">✏️</span>
                            Select Your Priority Goals
                        </h3>
                        <p class="text-sm text-gray-600 dark:text-gray-400 mb-4">Choose what you want to focus on in this session:</p>

                        <!-- Required Goals Section -->
                        <div class="mb-4">
                            <h4 class="text-md font-bold mb-3 flex items-center gap-2 text-red-700 dark:text-red-400">
                                <span class="text-lg">🔴</span>
                                Essential Goals (Required)
                            </h4>
                            <p class="text-xs text-gray-600 dark:text-gray-400 mb-3">These are fundamental to your essay structure and must be addressed:</p>
                            
                            <div class="space-y-3">
                                <label class="flex items-start gap-3 p-3 bg-red-50 dark:bg-red-900/20 rounded-lg cursor-pointer hover:bg-red-100 dark:hover:bg-red-900/30 border border-red-200 dark:border-red-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="thesis" checked disabled>
                                    <div class="flex-1">
                                        <p class="font-medium text-red-800 dark:text-red-200">Improve thesis statement clarity</p>
                                        <p class="text-sm text-red-600 dark:text-red-400">Ensure it answers the question and includes 2 specific points</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-red-200 dark:bg-red-800 text-red-800 dark:text-red-200 text-xs rounded-full">Required</span>
                                    </div>
                                </label>
                                <label class="flex items-start gap-3 p-3 bg-red-50 dark:bg-red-900/20 rounded-lg cursor-pointer hover:bg-red-100 dark:hover:bg-red-900/30 border border-red-200 dark:border-red-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="topic-sentences" checked disabled>
                                    <div class="flex-1">
                                        <p class="font-medium text-red-800 dark:text-red-200">Strengthen topic sentences</p>
                                        <p class="text-sm text-red-600 dark:text-red-400">Make them echo and support thesis points</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-red-200 dark:bg-red-800 text-red-800 dark:text-red-200 text-xs rounded-full">Required</span>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <!-- Flexible Goals Section -->
                        <div class="mb-4">
                            <h4 class="text-md font-bold mb-3 flex items-center gap-2 text-green-700 dark:text-green-400">
                                <span class="text-lg">🟢</span>
                                Flexible Goals (Your Choice)
                            </h4>
                            <p class="text-xs text-gray-600 dark:text-gray-400 mb-3">Choose based on your essay's needs and time available:</p>
                            
                            <div class="space-y-3">
                                <label class="flex items-start gap-3 p-3 bg-green-50 dark:bg-green-900/20 rounded-lg cursor-pointer hover:bg-green-100 dark:hover:bg-green-900/30 border border-green-200 dark:border-green-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="paragraph-development" checked>
                                    <div class="flex-1">
                                        <p class="font-medium text-green-800 dark:text-green-200">Enhance body paragraph development</p>
                                        <p class="text-sm text-green-600 dark:text-green-400">Focus on one paragraph to improve detail and coherence</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-green-200 dark:bg-green-800 text-green-800 dark:text-green-200 text-xs rounded-full">Flexible</span>
                                    </div>
                                </label>
                                <label class="flex items-start gap-3 p-3 bg-green-50 dark:bg-green-900/20 rounded-lg cursor-pointer hover:bg-green-100 dark:hover:bg-green-900/30 border border-green-200 dark:border-green-800">
                                    <input type="checkbox" class="goal-checkbox mt-1" value="grammar-vocabulary">
                                    <div class="flex-1">
                                        <p class="font-medium text-green-800 dark:text-green-200">Address grammar and vocabulary</p>
                                        <p class="text-sm text-green-600 dark:text-green-400">Improve sentence structure and word choice</p>
                                        <span class="inline-block mt-1 px-2 py-1 bg-green-200 dark:bg-green-800 text-green-800 dark:text-green-200 text-xs rounded-full">Flexible</span>
                                    </div>
                                </label>
                            </div>
                        </div>

                        <div class="mt-4">
                            <label class="block text-sm font-medium mb-2">Add custom goals (optional):</label>
                            <textarea id="custom-goals" rows="2" placeholder="E.g., Improve vocabulary variety, fix specific grammar issues..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary"></textarea>
                        </div>
                    </div>

                    <!-- Strategic Planning -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">📋</span>
                            Strategic Planning
                        </h3>
                        <div class="grid md:grid-cols-2 gap-4">
                            <div class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                                <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Macro-Level Issues (Priority 1)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Content, organization, thesis, topic sentences</p>
                            </div>
                            <div class="p-4 bg-orange-50 dark:bg-orange-900/20 rounded-lg border-l-4 border-orange-500">
                                <h4 class="font-bold text-orange-900 dark:text-orange-200 mb-2">Micro-Level Issues (Priority 2)</h4>
                                <p class="text-sm text-gray-700 dark:text-gray-300">Grammar, vocabulary, sentence structure</p>
                            </div>
                        </div>
                    </div>

                    <!-- Time Constraints -->
                    <div class="mb-6">
                        <h3 class="text-lg font-bold mb-3 flex items-center gap-2">
                            <span class="text-xl">⏰</span>
                            Time Management
                        </h3>
                        <div class="p-4 bg-purple-50 dark:bg-purple-900/20 rounded-lg border-l-4 border-purple-500">
                            <div class="mb-3">
                                <label class="block text-sm font-bold mb-2 text-purple-900 dark:text-purple-200">
                                    How much time do you have for this session?
                                </label>
                                <p class="text-xs text-purple-700 dark:text-purple-300 mb-2">
                                    <span class="font-semibold">Recommended:</span> 15-20 minutes for focused revision
                                </p>
                            </div>
                            <select id="time-constraint" class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary">
                                <option value="15min">15 minutes (Quick focus)</option>
                                <option value="20min" selected>20 minutes (Recommended)</option>
                                <option value="30min">30 minutes</option>
                                <option value="45min">45 minutes</option>
                                <option value="60min">1 hour</option>
                            </select>
                            <div class="mt-2 p-2 bg-yellow-50 dark:bg-yellow-900/20 rounded border border-yellow-300 dark:border-yellow-700">
                                <p class="text-xs text-yellow-800 dark:text-yellow-200">
                                    <span class="font-semibold">💡 Tip:</span> Shorter sessions (15-20 min) help maintain focus on essential goals. Use the AI chatbot to explore options efficiently!
                                </p>
                            </div>
                        </div>
                    </div>

                    <!-- Goals Summary -->
                    <div id="selected-goals-summary" class="p-4 bg-green-50 dark:bg-green-900/20 rounded-lg border-l-4 border-green-500">
                        <h4 class="font-bold text-green-900 dark:text-green-200 mb-2">Your Selected Goals:</h4>
                        <div id="goals-list" class="text-sm text-gray-700 dark:text-gray-300"></div>
                    </div>

                    <!-- Confirmation Button -->
                    <div class="mt-6 p-4 bg-blue-50 dark:bg-blue-900/20 rounded-lg border-l-4 border-blue-500">
                        <button id="confirm-goals" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-semibold py-3 px-6 rounded-lg transition-colors text-lg">
                            ✓ Confirm Goals and Proceed
                        </button>
                    </div>
                </div>
            </div>

            <!-- Right Panel: AI Conversation (1 column) -->
            <div class="lg:col-span-1">
                <div class="bg-white dark:bg-gray-800 rounded-lg p-4 md:p-6 shadow-md sticky top-6">
                    <h3 class="text-lg md:text-xl font-bold mb-4 flex items-center gap-2">
                        <span class="text-2xl">🤖</span>
                        AI Goal Explorer
                    </h3>
                    
                    <div class="mb-4 p-3 bg-blue-50 dark:bg-blue-900/20 rounded-lg border border-blue-200 dark:border-blue-800">
                        <p class="text-sm text-blue-800 dark:text-blue-200">
                            <span class="font-semibold">💬 Chat with AI to:</span> Explore goal options, understand priorities, and negotiate your revision strategy.
                        </p>
                    </div>

                    <div id="chat-messages" class="bg-gray-50 dark:bg-gray-700 rounded-lg p-4 mb-4 overflow-y-auto" style="height: 400px;">
                        <div class="text-center text-gray-500 dark:text-gray-400 text-sm py-8">
                            <div class="mb-4">
                                <span class="text-2xl">🎯</span>
                            </div>
                            <p class="mb-2 font-medium">Ready to explore your goals?</p>
                            <p class="text-xs">Ask the AI about:</p>
                            <ul class="text-xs mt-2 space-y-1 text-left">
                                <li>• Which goals are most important?</li>
                                <li>• How to prioritize with limited time?</li>
                                <li>• What makes a strong thesis statement?</li>
                                <li>• How to improve topic sentences?</li>
                            </ul>
                        </div>
                    </div>

                    <div id="loading-indicator" class="hidden text-center py-4">
                        <div class="inline-block animate-spin rounded-full h-6 w-6 border-b-2 border-primary"></div>
                        <p class="mt-2 text-xs text-gray-600 dark:text-gray-400">AI is thinking...</p>
                    </div>

                    <!-- Quick Action Buttons -->
                    <div class="mb-4">
                        <p class="text-xs font-medium text-gray-600 dark:text-gray-400 mb-2">Quick questions:</p>
                        <div class="grid grid-cols-2 gap-2">
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="What should I focus on first?">
                                Focus priorities
                            </button>
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="How do I improve my thesis statement?">
                                Thesis help
                            </button>
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="What makes good topic sentences?">
                                Topic sentences
                            </button>
                            <button class="quick-question-btn text-xs bg-gray-100 dark:bg-gray-700 hover:bg-gray-200 dark:hover:bg-gray-600 text-gray-700 dark:text-gray-300 py-2 px-3 rounded-lg transition-colors" data-question="How much can I accomplish in 20 minutes?">
                                Time planning
                            </button>
                        </div>
                    </div>

                    <!-- General Chat Input -->
                    <div class="border-t border-gray-200 dark:border-gray-700 pt-4">
                        <textarea id="general-chat-input" rows="3" placeholder="Ask the AI about goal setting, priorities, or revision strategy..." class="w-full p-3 text-base border-2 border-gray-300 dark:border-gray-600 rounded-lg bg-white dark:bg-gray-700 focus:ring-2 focus:ring-primary mb-2"></textarea>
                        <button id="send-general-chat" class="w-full bg-primary hover:bg-primary-hover text-white font-semibold py-2 px-4 rounded-lg transition-colors">
                            Send Message
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Dark mode setup
        if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
            document.documentElement.classList.add('dark');
        }
        window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', event => {
            document.documentElement.classList.add(event.matches ? 'dark' : '');
            !event.matches && document.documentElement.classList.remove('dark');
        });

        // State
        const state = {
            selectedGoals: [],
            timeConstraint: '20min'
        };

        // Goals tracking
        const goalCheckboxes = document.querySelectorAll('.goal-checkbox');
        goalCheckboxes.forEach(cb => cb.addEventListener('change', updateGoals));
        document.getElementById('custom-goals').addEventListener('input', updateGoals);
        document.getElementById('time-constraint').addEventListener('change', updateGoals);

        function updateGoals() {
            const goals = [];
            goalCheckboxes.forEach(cb => {
                if (cb.checked) {
                    goals.push(cb.parentElement.querySelector('p.font-medium').textContent);
                }
            });
            const custom = document.getElementById('custom-goals').value.trim();
            if (custom) goals.push(custom);

            state.selectedGoals = goals;
            state.timeConstraint = document.getElementById('time-constraint').value;

            document.getElementById('goals-list').innerHTML = goals.length > 0
                ? goals.map((g, i) => `<p>${i + 1}. ${g}</p>`).join('')
                : '<p class="text-gray-500">No goals selected</p>';
        }
        updateGoals();

        // Custom modal function
        function showCustomModal(message) {
            const modal = document.createElement('div');
            modal.className = 'fixed inset-0 bg-black bg-opacity-70 flex items-center justify-center z-50 p-4';
            modal.innerHTML = `
                <div class="bg-white dark:bg-gray-800 p-6 rounded-xl shadow-2xl max-w-sm w-full border-2 border-primary">
                    <p class="text-gray-800 dark:text-gray-200 mb-4 text-base">${message}</p>
                    <button class="w-full px-4 py-2 bg-primary text-white hover:bg-primary-hover rounded-lg transition-colors font-semibold" onclick="this.closest('.fixed').remove()">OK</button>
                </div>
            `;
            document.body.appendChild(modal);
        }

        // Goals Confirmation
        document.getElementById('confirm-goals').addEventListener('click', () => {
            if (state.selectedGoals.length === 0) {
                showCustomModal('Please select at least one goal before proceeding.');
                return;
            }

            // Show confirmation message
            showCustomModal('Excellent! You\'ve set your revision goals. The AI will now provide guidance on strategic planning and goal negotiation.');
            
            // Generate AI messages about goal negotiation
            setTimeout(() => {
                addChatMessage("AI", `Great job setting your revision goals! 

**Goal 2: Negotiate with AI on Agenda and Goals**

You've demonstrated strategic thinking by:
- Selecting priority areas for revision
- Considering time constraints (${state.timeConstraint})
- Focusing on macro-level issues first

**Strategic Planning Tips:**
- **Macro-level first**: Content, organization, thesis, topic sentences
- **Micro-level second**: Grammar, vocabulary, sentence structure
- **Time management**: Focus on high-impact improvements within your time limit

**Next Steps:**
Your goals are well-prioritized. We'll work through them systematically, starting with the most impactful changes. Ready to begin with your thesis statement?`);
            }, 1000);

            // Disable the button after confirmation
            document.getElementById('confirm-goals').disabled = true;
            document.getElementById('confirm-goals').textContent = '✓ Goals Confirmed';
            document.getElementById('confirm-goals').classList.add('bg-gray-400', 'cursor-not-allowed');
        });

        // Quick question buttons
        document.querySelectorAll('.quick-question-btn').forEach(btn => {
            btn.addEventListener('click', () => {
                const question = btn.getAttribute('data-question');
                document.getElementById('general-chat-input').value = question;
                document.getElementById('send-general-chat').click();
            });
        });

        // General chat
        document.getElementById('send-general-chat').addEventListener('click', () => {
            const msg = document.getElementById('general-chat-input').value.trim();
            if (!msg) return;
            askAI(`@Claude-Sonnet-4.5 Student question about goal setting: "${msg}"

Provide guidance on strategic planning and goal negotiation with AI. Keep response under 5 sentences.`);
            document.getElementById('general-chat-input').value = '';
        });

        // AI Communication
        function addChatMessage(sender, content) {
            const chat = document.getElementById('chat-messages');
            const placeholder = chat.querySelector('.text-center.text-gray-500');
            if (placeholder) placeholder.remove();

            const msg = document.createElement('div');
            msg.className = 'mb-3';
            msg.innerHTML = `
                <div class="text-xs font-semibold mb-1 ${sender === 'You' ? 'text-gray-600 dark:text-gray-400' : 'text-primary'}">${sender === 'You' ? '👤' : '🤖'} ${sender}</div>
                <div class="p-3 rounded-lg text-sm ${sender === 'You' ? 'bg-gray-200 dark:bg-gray-600' : 'bg-blue-50 dark:bg-blue-900/30'}">${marked.parse(content)}</div>
            `;
            chat.appendChild(msg);
            chat.scrollTop = chat.scrollHeight;
        }

        function updateLastAIMessage(content) {
            const chat = document.getElementById('chat-messages');
            const messages = chat.querySelectorAll('.mb-3');
            if (messages.length > 0) {
                const last = messages[messages.length - 1];
                const contentDiv = last.querySelector('.p-3');
                if (contentDiv) {
                    contentDiv.innerHTML = marked.parse(content);
                    chat.scrollTop = chat.scrollHeight;
                }
            }
        }

        if (window.Poe) {
            window.Poe.registerHandler("essay-training", (result) => {
                const msg = result.responses[0];
                document.getElementById('loading-indicator').classList.add('hidden');

                if (msg.status === "error") {
                    addChatMessage("AI", `Error: ${msg.statusText}`);
                } else if (msg.status === "incomplete") {
                    if (msg.content.trim()) {
                        updateLastAIMessage(msg.content);
                    }
                } else if (msg.status === "complete") {
                    updateLastAIMessage(msg.content);
                }
            });
        }

        async function askAI(prompt) {
            if (!window.Poe) {
                showCustomModal("Poe API not available. This app needs to run in the Poe environment.");
                return;
            }

            // Extract user message from prompt
            const userMsg = prompt.split('\n').slice(1).join('\n').substring(0, 100) + '...';
            addChatMessage("You", userMsg);
            addChatMessage("AI", "...");
            document.getElementById('loading-indicator').classList.remove('hidden');

            try {
                await window.Poe.sendUserMessage(prompt, {
                    handler: "essay-training",
                    stream: true,
                    openChat: false
                });
            } catch (err) {
                document.getElementById('loading-indicator').classList.add('hidden');
                addChatMessage("AI", `Error: ${err.message}`);
            }
        }

        console.log('Goal Setting tab loaded');
    </script>
</body>
</html>

```

Now let me update the todo list to mark the completed tasks and check for any linting errors:


Perfect! I've successfully enhanced the goal-setting UI to address all your requirements. Here's a summary of the improvements made:

## ✅ **Completed Enhancements**

### 🎯 **Goal Prioritization & Visual Hierarchy**
- **Added clear visual distinction** between required and flexible goals
- **Essential Goals (Required)**: Thesis statement and topic sentences are now marked as required with red styling and disabled checkboxes
- **Flexible Goals (Your Choice)**: Body paragraph development and grammar/vocabulary are marked as flexible with green styling
- **Visual indicators**: Added "Required" and "Flexible" badges to make the distinction clear

### ⏰ **Time Management Updates**
- **Updated default time** to 20 minutes (recommended)
- **Added 15-minute option** for quick focus sessions
- **Clear recommendation** for 15-20 minute sessions
- **Added helpful tip** about shorter sessions maintaining focus

### 🤖 **Enhanced AI Chatbot Integration**
- **Renamed to "AI Goal Explorer"** to emphasize its role in goal exploration
- **Added quick question buttons** for common goal-setting questions:
  - Focus priorities
  - Thesis help
  - Topic sentences
  - Time planning
- **Improved placeholder content** with specific suggestions for what to ask the AI
- **Better visual design** with clear call-to-action messaging

### 🎨 **UI/UX Improvements**
- **Color-coded goal categories** (red for required, green for flexible)
- **Enhanced visual hierarchy** with better spacing and typography
- **Interactive elements** that guide students through the goal-setting process
- **Clear explanations** of why certain goals are required vs flexible

The UI now clearly communicates that:
- **Thesis statements and topic sentences are essential** and must be addressed
- **Body paragraph development offers flexibility** for students to choose based on their needs
- **15-20 minutes is the recommended time** for focused revision sessions
- **The AI chatbot is there to help explore options** and negotiate goals effectively

Students can now easily understand the importance of prioritizing different goals while having the flexibility to make choices about body paragraph work, all within the recommended 15-20 minute timeframe!

