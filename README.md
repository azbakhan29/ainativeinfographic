<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Chosen Palette: Vibrant Professional (Light Cream, Deep Blue, Teal, Yellow, Coral) -->
    <!-- 
        Application Structure Plan: 
        The SPA is structured as a top-to-bottom narrative telling the story of the AI-Native Sprint.
        1.  Hero Section: A bold title and subtitle to introduce the topic and hook the user.
        2.  The Journey: A 3-step visual process flow (built with HTML/CSS) to explain the sprint's methodology (Discovery -> Theorizing -> The Pivot). This makes the process easy to follow.
        3.  The "AI Bell Curve": A dedicated section with a Chart.js line chart to visualize the key finding about AI productivity. This isolates the most important learning for maximum impact.
        4.  Key Reflections: A responsive grid of cards, each representing one of the five main learnings. This breaks down complex insights into digestible, visually separated chunks.
        5.  The Playbook: A three-column layout presenting the actionable playbook for UXers, making it easy to scan and use as a reference.
        This thematic, narrative structure was chosen over a direct report-to-page mapping because it guides the user through a story of discovery, challenge, and resolution, which is more engaging and improves comprehension and retention of the key takeaways.
    -->
    <!-- 
        Visualization & Content Choices:
        -   Sprint Journey: (Goal: Organize/Change) -> A styled HTML/CSS flexbox diagram was chosen to represent the process flow. This method is lightweight, fully responsive, and avoids the use of prohibited SVG or Mermaid JS, while clearly showing the progression of the sprint.
        -   AI Productivity: (Goal: Change) -> A Chart.js Line Chart is used to create the "AI Bell Curve." A line chart is the ideal visualization to show a trend or change over distinct phases, perfectly capturing the rise and fall of productivity described in the report. It is rendered on a Canvas, adhering to requirements.
        -   Key Reflections: (Goal: Inform/Organize) -> A grid of cards with Unicode icons. This presentation method breaks down the five key learnings into manageable pieces. The card format gives each point its own space, and the icons add visual interest without using image files or SVG.
        -   The Playbook: (Goal: Organize) -> A three-column list layout. This is a clear and conventional way to present a multi-part guide, allowing for easy scanning of the different phases and their associated actions.
        All visualizations are accompanied by descriptive text to provide context and explain the key message, ensuring the infographic is not just a collection of data points but a coherent story.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Learnings from an AI-Native Sprint | An Interactive Infographic</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #F8F7F4;
            color: #1a202c;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }
        .flow-arrow {
            color: #D1D5DB;
            font-size: 2.5rem;
            line-height: 1;
        }
        .card-icon {
            font-size: 2.5rem;
            line-height: 1;
            width: 4rem;
            height: 4rem;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 0.5rem;
        }
    </style>
</head>
<body class="antialiased">

    <div class="container mx-auto p-4 md:p-8">

        <header class="text-center my-12 md:my-20">
            <h1 class="text-4xl md:text-6xl font-black text-gray-900 leading-tight">Learnings from an <span class="text-[#087E8B]">AI-Native Sprint</span></h1>
            <p class="mt-4 text-lg md:text-xl text-gray-600 max-w-3xl mx-auto">An interactive report on our experiment to challenge traditional problem-solving by building with AI at the core.</p>
        </header>

        <main>
            <section id="journey" class="mb-16 md:mb-24">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-4 text-gray-900">The Sprint Journey</h2>
                <p class="text-center text-gray-600 max-w-2xl mx-auto mb-12">Our two-week sprint followed a "try-fail-try-scale" framework, leading to a critical pivot in our approach.</p>
                <div class="flex flex-col md:flex-row justify-center items-center text-center gap-4 md:gap-8">

                    <div class="w-full md:w-1/3">
                        <div class="bg-white rounded-lg p-6 shadow-md h-full">
                            <div class="text-sm font-bold text-[#087E8B]">PHASE 1</div>
                            <h3 class="text-xl font-bold text-gray-900 mt-1">Deep Dive Discovery</h3>
                            <p class="mt-2 text-gray-600 text-sm">We began with extensive user shadowing and process overviews, using NotebookLM to capture and map our initial findings from AV technicians.</p>
                        </div>
                    </div>

                    <div class="flow-arrow my-4 md:my-0">&rarr;</div>

                    <div class="w-full md:w-1/3">
                        <div class="bg-white rounded-lg p-6 shadow-md h-full">
                            <div class="text-sm font-bold text-[#FF5A5F]">PHASE 2</div>
                            <h3 class="text-xl font-bold text-gray-900 mt-1">Preparing & Theorizing</h3>
                            <p class="mt-2 text-gray-600 text-sm">We applied JTBD & 5 Whys frameworks, using a custom "JTBD Expert" Gemini agent for AI-powered brainstorming and opportunity generation.</p>
                        </div>
                    </div>

                     <div class="flow-arrow my-4 md:my-0">&rarr;</div>
                    
                    <div class="w-full md:w-1/3">
                         <div class="bg-[#3C3C3C] text-white rounded-lg p-6 shadow-lg h-full">
                            <div class="text-sm font-bold text-[#F7B801]">THE PIVOT</div>
                            <h3 class="text-xl font-bold text-white mt-1">Human-Led Refinement</h3>
                            <p class="mt-2 text-gray-300 text-sm">AI's generic outputs led to a crucial shift: we reverted to human-led analysis with AI for recall, not primary generation.</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <section id="bell-curve" class="mb-16 md:mb-24 bg-white rounded-lg p-6 md:p-8 shadow-md">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-4 text-gray-900">The "AI Bell Curve" of Productivity</h2>
                <p class="text-center text-gray-600 max-w-2xl mx-auto mb-8">A key learning was observing a distinct pattern in AI's utility. It provides incredible initial acceleration, but its effectiveness can peak and then decelerate without deep human collaboration to guide it.</p>
                <div class="chart-container">
                    <canvas id="bellCurveChart"></canvas>
                </div>
            </section>

            <section id="learnings" class="mb-16 md:mb-24">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 text-gray-900">Our Top 5 Reflections</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    
                    <div class="bg-white rounded-lg p-6 shadow-md flex items-start gap-4">
                        <div class="card-icon bg-[#087E8B] bg-opacity-10 text-[#087E8B]">🎭</div>
                        <div>
                            <h3 class="text-xl font-bold mb-2">The New Face of Bias</h3>
                            <p class="text-gray-600">A crucial learning was seeing how human bias in input data directly translates into "Gem Bias." The quality and diversity of the context we provide to AI is paramount to getting objective, useful outputs.</p>
                        </div>
                    </div>

                    <div class="bg-white rounded-lg p-6 shadow-md flex items-start gap-4">
                        <div class="card-icon bg-[#087E8B] bg-opacity-10 text-[#087E8B]">🔄</div>
                        <div>
                            <h3 class="text-xl font-bold mb-2">UX Redefined</h3>
                            <p class="text-gray-600">The "prompt-and-answer loop" became a major time sink. This highlighted a need for new UX paradigms for human-AI collaboration that go beyond simple text queries to foster true partnership.</p>
                        </div>
                    </div>

                    <div class="bg-white rounded-lg p-6 shadow-md flex items-start gap-4">
                        <div class="card-icon bg-[#087E8B] bg-opacity-10 text-[#087E8B]">🧠</div>
                        <div>
                            <h3 class="text-xl font-bold mb-2">Human Intuition is Key</h3>
                            <p class="text-gray-600">AI augments, but it doesn't replace deep qualitative analysis and contextual understanding. Our pivot to a human-led JTBD exercise proved that human synthesis is still unparalleled for grounded insights.</p>
                        </div>
                    </div>
                    
                    <div class="bg-white rounded-lg p-6 shadow-md flex items-start gap-4">
                         <div class="card-icon bg-[#087E8B] bg-opacity-10 text-[#087E8B]">🤝</div>
                        <div>
                            <h3 class="text-xl font-bold mb-2">Multidisciplinary Alignment</h3>
                            <p class="text-gray-600">Generic AI ideas can disengage a team, especially engineers. Human-led collaboration is vital for grounding ideas in reality, ensuring buy-in, and identifying what is truly valuable to test.</p>
                        </div>
                    </div>
                    
                    <div class="bg-white rounded-lg p-6 shadow-md flex items-start gap-4 md:col-span-2">
                         <div class="card-icon bg-[#FF5A5F] bg-opacity-10 text-[#FF5A5F]">💡</div>
                        <div>
                            <h3 class="text-xl font-bold mb-2">AI Excels at Specific Tasks</h3>
                            <p class="text-gray-600">While AI struggled with novel, grounded ideation, it was an invaluable 'teammate' for consolidating information, quickly mapping processes from transcripts, and answering domain-specific questions based on the data we provided.</p>
                        </div>
                    </div>

                </div>
            </section>

            <section id="playbook">
                <h2 class="text-3xl md:text-4xl font-bold text-center mb-4 text-gray-900">The AI-Native Sprint Playbook</h2>
                <p class="text-center text-gray-600 max-w-3xl mx-auto mb-12">Based on our experience, here is an actionable playbook for any UXer embarking on a similar journey.</p>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8 text-left">

                    <div class="bg-white rounded-lg p-6 shadow-md">
                        <h3 class="text-xl font-bold text-[#087E8B] mb-4">Phase 1: Grounding the AI</h3>
                        <ul class="space-y-4 text-gray-600">
                            <li class="flex items-start"><span class="font-bold text-[#087E8B] mr-3 mt-1">1</span><span><strong class="text-gray-800">Observe First:</strong> Prioritize direct user shadowing. Raw, real-world data is the best foundation for avoiding generic outputs.</span></li>
                            <li class="flex items-start"><span class="font-bold text-[#087E8B] mr-3 mt-1">2</span><span><strong class="text-gray-800">Curate Input:</strong> Feed AI diverse, high-quality data. The more nuanced the input, the better the output.</span></li>
                            <li class="flex items-start"><span class="font-bold text-[#087E8B] mr-3 mt-1">3</span><span><strong class="text-gray-800">Be Specific:</strong> Ask for detailed, grounded outputs with constraints. Avoid generic prompts to get actionable insights.</span></li>
                        </ul>
                    </div>

                    <div class="bg-white rounded-lg p-6 shadow-md">
                        <h3 class="text-xl font-bold text-[#FF5A5F] mb-4">Phase 2: Collaborative Ideation</h3>
                        <ul class="space-y-4 text-gray-600">
                            <li class="flex items-start"><span class="font-bold text-[#FF5A5F] mr-3 mt-1">1</span><span><strong class="text-gray-800">AI for Recall:</strong> Use AI as a super-powered memory aid for fact-checking and context retrieval during human-led discussions.</span></li>
                            <li class="flex items-start"><span class="font-bold text-[#FF5A5F] mr-3 mt-1">2</span><span><strong class="text-gray-800">Human Synthesis:</strong> Conduct core analysis (like JTBD) as a team with whiteboards. This ensures collective understanding and buy-in.</span></li>
                             <li class="flex items-start"><span class="font-bold text-[#FF5A5F] mr-3 mt-1">3</span><span><strong class="text-gray-800">Feasibility Filter:</strong> Involve engineers early to prune impractical ideas and focus on what's truly testable and valuable.</span></li>
                        </ul>
                    </div>
                    
                    <div class="bg-white rounded-lg p-6 shadow-md">
                        <h3 class="text-xl font-bold text-[#F7B801] mb-4">Phase 3: Actionable Outcomes</h3>
                        <ul class="space-y-4 text-gray-600">
                            <li class="flex items-start"><span class="font-bold text-[#F7B801] mr-3 mt-1">1</span><span><strong class="text-gray-800">Link to Metrics:</strong> Ensure any selected opportunity has a clear, measurable outcome, like reducing time on a task or improving user experience.</span></li>
                            <li class="flex items-start"><span class="font-bold text-[#F7B801] mr-3 mt-1">2</span><span><strong class="text-gray-800">Prepare for MVTs:</strong> Develop Minimum Viable Tests to validate the AI's accuracy and impact, like our plan to classify tickets and compare against technician responses.</span></li>
                        </ul>
                    </div>
                </div>
            </section>
            
            <footer class="text-center my-16 md:my-24 border-t pt-8">
                <p class="text-lg text-gray-600 max-w-3xl mx-auto">The key takeaway is that the future is a <strong class="text-gray-900">symbiotic human-AI collaboration</strong>, using AI's strengths to augment our own intuition and problem-solving capabilities.</p>
            </footer>

        </main>
    </div>

    <script>
        function wrapText(text, maxLength) {
            if (typeof text !== 'string' || text.length <= maxLength) {
                return text;
            }
            const words = text.split(' ');
            const lines = [];
            let currentLine = '';
            words.forEach(word => {
                if ((currentLine + ' ' + word).trim().length > maxLength && currentLine.length > 0) {
                    lines.push(currentLine.trim());
                    currentLine = word;
                } else {
                    currentLine += (currentLine ? ' ' : '') + word;
                }
            });
            if (currentLine) {
                lines.push(currentLine.trim());
            }
            return lines;
        }

        const bellCurveCtx = document.getElementById('bellCurveChart').getContext('2d');
        const bellCurveChart = new Chart(bellCurveCtx, {
            type: 'line',
            data: {
                labels: ['Initial Acceleration', 'Peak AI Utility', 'Deceleration & Repetition', 'Human-Led Refinement'],
                datasets: [{
                    label: 'Team Productivity & Momentum',
                    data: [20, 85, 50, 75], 
                    backgroundColor: 'rgba(8, 126, 139, 0.1)',
                    borderColor: '#087E8B',
                    tension: 0.4,
                    fill: true,
                    pointBackgroundColor: '#087E8B',
                    pointRadius: 5,
                    pointHoverRadius: 8
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    y: {
                        beginAtZero: true,
                        grid: {
                            color: 'rgba(0, 0, 0, 0.05)'
                        },
                        ticks: {
                            color: '#4A5568'
                        }
                    },
                    x: {
                        grid: {
                           display: false
                        },
                        ticks: {
                            color: '#4A5568',
                            callback: function(value, index, values) {
                                const label = this.getLabelForValue(value);
                                return wrapText(label, 16);
                            }
                        }
                    }
                },
                plugins: {
                    legend: {
                        display: false
                    },
                    tooltip: {
                        backgroundColor: '#ffffff',
                        titleColor: '#1a202c',
                        bodyColor: '#4A5568',
                        borderColor: '#E2E8F0',
                        borderWidth: 1,
                        callbacks: {
                            title: function(tooltipItems) {
                                const item = tooltipItems[0];
                                let label = item.chart.data.labels[item.dataIndex];
                                if (Array.isArray(label)) {
                                  return label.join(' ');
                                }
                                return label;
                            }
                        }
                    }
                }
            }
        });
    </script>
</body>
</html>
