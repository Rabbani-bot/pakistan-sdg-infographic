<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pakistan's SDG Progress: A 2025 Snapshot</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f4f8;
        }
        .chart-container {
            position: relative;
            width: 100%;
            height: 95%;
        }
        .kpi-card {
            border-left: 4px solid;
            transition: all 0.3s ease;
        }
        .kpi-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
        }
        .section-title {
            position: relative;
            padding-bottom: 0.5rem;
            margin-bottom: 1.5rem;
        }
        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            border-radius: 2px;
        }
    </style>
</head>
<body class="text-slate-700">

    <header class="bg-white text-center p-8 shadow-md">
        <div class="max-w-4xl mx-auto">
            <h1 class="text-4xl md:text-5xl font-extrabold text-[#00425A] mb-2">Pakistan & The SDGs: A 2025 Snapshot</h1>
            <p class="text-lg text-slate-500">Assessing the nation's journey towards the 2030 Agenda amidst achievements and persistent hurdles.</p>
        </div>
    </header>

    <main class="container mx-auto p-4 md:p-8">

        <section id="overview" class="mb-12">
            <div class="bg-white rounded-xl shadow-lg p-8 grid grid-cols-1 md:grid-cols-3 gap-8 items-center">
                <div class="md:col-span-1 text-center">
                     <h2 class="text-2xl font-bold text-[#1F8A70] mb-2">Global SDG Ranking</h2>
                     <p class="text-7xl font-extrabold text-[#00425A]">125<span class="text-3xl font-semibold text-slate-400">/167</span></p>
                     <p class="text-slate-500 mt-2 text-lg">SDG Index Score: <strong>58.4</strong></p>
                </div>
                <div class="md:col-span-2 text-slate-600 text-lg">
                    <p>Pakistan's path to achieving the Sustainable Development Goals is a study in contrasts. While the nation has made commendable progress in expanding its digital footprint and improving certain health metrics, this momentum is severely hampered by deep-rooted challenges. Stagnation in education, coupled with significant economic volatility and extreme vulnerability to climate change, creates a complex and fragile development landscape.</p>
                </div>
            </div>
        </section>

        <section class="mb-12">
            <h2 class="section-title text-3xl font-bold text-center text-[#00425A] after:bg-[#1F8A70]">Key Success Areas</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="kpi-card bg-white rounded-lg shadow-md p-6 border-[#4E9F3D]">
                    <h3 class="text-xl font-bold text-center mb-4 text-[#00425A]">Digital Transformation</h3>
                    <p class="text-center text-slate-500 mb-4 text-sm">A massive expansion in mobile and broadband access serves as a critical enabler for economic and social development across other goals.</p>
                    <div class="h-64 chart-container">
                        <canvas id="digitalGrowthChart"></canvas>
                    </div>
                </div>
                <div class="kpi-card bg-white rounded-lg shadow-md p-6 border-[#FFC300]">
                    <h3 class="text-xl font-bold text-center mb-4 text-[#00425A]">Improved Health Outcomes</h3>
                    <p class="text-center text-slate-500 mb-4 text-sm">Significant gains in maternal and child health, marked by a rise in births attended by skilled personnel, signal progress in foundational healthcare.</p>
                    <div class="h-64 chart-container">
                        <canvas id="healthChart"></canvas>
                    </div>
                </div>
                <div class="kpi-card bg-white rounded-lg shadow-md p-6 border-[#BF3325]">
                     <h3 class="text-xl font-bold text-center mb-4 text-[#00425A]">Women in Leadership</h3>
                    <p class="text-center text-slate-500 mb-4 text-sm">Though starting from a low base, the share of women in managerial roles has nearly doubled, a positive step towards gender equality.</p>
                    <div class="h-64 chart-container">
                        <canvas id="genderChart"></canvas>
                    </div>
                </div>
            </div>
        </section>
        
        <section class="mb-12">
             <h2 class="section-title text-3xl font-bold text-center text-[#00425A] after:bg-[#BF3325]">Significant Challenges</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-xl font-bold text-center mb-4 text-[#00425A]">Education Stagnation (SDG 4)</h3>
                    <p class="text-center text-slate-500 mb-4">The national literacy rate and primary school completion have seen minimal improvement, representing a critical failure that impedes long-term human capital development and economic growth.</p>
                    <div class="h-80 chart-container">
                         <canvas id="educationChart"></canvas>
                    </div>
                </div>
                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-xl font-bold text-center mb-4 text-[#00425A]">Climate Vulnerability (SDG 13)</h3>
                    <p class="text-center text-slate-500 mb-4">Pakistan remains acutely vulnerable to climate change. Rising emissions and the increasing frequency of climate-related disasters, like the devastating 2022 floods, threaten to erase development gains overnight.</p>
                    <div class="h-80 chart-container">
                         <canvas id="climateChart"></canvas>
                    </div>
                </div>
            </div>
        </section>

        <section>
            <h2 class="section-title text-3xl font-bold text-center text-[#00425A] after:bg-slate-400">Systemic Hurdles to Progress</h2>
             <p class="text-center text-slate-500 mb-8 max-w-3xl mx-auto">Progress is not just about individual goals. A complex web of interconnected challenges consistently undermines efforts across the board, requiring systemic solutions.</p>
            <div class="flex flex-col md:flex-row justify-center items-stretch space-y-6 md:space-y-0 md:space-x-6">
                
                <div class="flex-1 text-center p-6 bg-white border-t-4 border-[#BF3325] rounded-lg shadow-lg">
                    <div class="text-5xl mb-3">💰</div>
                    <h4 class="font-bold text-xl text-[#BF3325] mb-2">Economic Instability</h4>
                    <p class="text-sm text-slate-600">High inflation, soaring debt, and fiscal deficits divert critical funds from development projects in health, education, and infrastructure, trapping the nation in a cycle of crisis management.</p>
                </div>

                <div class="flex-1 text-center p-6 bg-white border-t-4 border-[#FFC300] rounded-lg shadow-lg">
                    <div class="text-5xl mb-3">🏛️</div>
                    <h4 class="font-bold text-xl text-[#FFC300] mb-2">Governance & Policy</h4>
                    <p class="text-sm text-slate-600">Political instability fosters policy discontinuity, preventing long-term planning. Weak institutional capacity and accountability gaps hamper the effective implementation and monitoring of SDG initiatives.</p>
                </div>

                <div class="flex-1 text-center p-6 bg-white border-t-4 border-[#00425A] rounded-lg shadow-lg">
                    <div class="text-5xl mb-3">🌊</div>
                    <h4 class="font-bold text-xl text-[#00425A] mb-2">Environmental Shocks</h4>
                    <p class="text-sm text-slate-600">Recurrent extreme weather events cause massive economic losses, displace populations, and systematically reverse years of hard-won development gains, particularly for the most vulnerable communities.</p>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-[#00425A] text-white text-center p-4 mt-12">
        <p class="text-sm">Data sourced from UN, UNDP, and Government of Pakistan reports. Infographic for illustrative purposes.</p>
    </footer>

    <script>
        const chartTooltipTitleCallback = {
            title: function(tooltipItems) {
                const item = tooltipItems[0];
                let label = item.chart.data.labels[item.dataIndex];
                if (Array.isArray(label)) {
                    return label.join(' ');
                } else {
                    return label;
                }
            }
        };

        const palette = {
            darkBlue: '#00425A',
            green: '#1F8A70',
            yellow: '#FFC300',
            red: '#BF3325',
            lightGray: '#f0f4f8'
        };

        new Chart(document.getElementById('digitalGrowthChart'), {
            type: 'line',
            data: {
                labels: ['2018', '2020', '2022', '2024'],
                datasets: [{
                    label: 'Mobile Subscribers (M)',
                    data: [152, 167, 194, 190],
                    borderColor: palette.green,
                    backgroundColor: 'rgba(31, 138, 112, 0.1)',
                    fill: true,
                    tension: 0.4
                }, {
                    label: 'Broadband Subscribers (M)',
                    data: [61, 87, 124, 131],
                    borderColor: palette.darkBlue,
                    backgroundColor: 'rgba(0, 66, 90, 0.1)',
                    fill: true,
                    tension: 0.4
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: { legend: { position: 'bottom', labels: { boxWidth: 12, padding: 20 } }, tooltip: { callbacks: chartTooltipTitleCallback } },
                scales: { y: { beginAtZero: true } }
            }
        });

        new Chart(document.getElementById('healthChart'), {
            type: 'doughnut',
            data: {
                labels: ['Skilled Birth Attendance (%)', 'Other'],
                datasets: [{
                    data: [73, 27],
                    backgroundColor: [palette.yellow, palette.lightGray],
                    borderColor: ['#fff'],
                    borderWidth: 2,
                    hoverOffset: 4
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                cutout: '70%',
                plugins: { legend: { display: false }, tooltip: { callbacks: chartTooltipTitleCallback } }
            }
        });
        
        new Chart(document.getElementById('genderChart'), {
            type: 'bar',
            data: {
                labels: ['2015', '2019'],
                datasets: [{
                    label: 'Women in Managerial Positions (%)',
                    data: [2.7, 4.5],
                    backgroundColor: [palette.red, '#f08080'],
                    borderRadius: 4,
                    barThickness: 25
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: { legend: { display: false }, tooltip: { callbacks: chartTooltipTitleCallback } },
                scales: { x: { grid: { display: false } }, y: { beginAtZero: true } }
            }
        });

        new Chart(document.getElementById('educationChart'), {
            type: 'bar',
            data: {
                labels: ['Literacy Rate', 'Primary Completion Rate'],
                datasets: [{
                    label: 'Rate (%)',
                    data: [60, 67],
                    backgroundColor: [palette.darkBlue, palette.green],
                    borderRadius: 4,
                }]
            },
            options: {
                indexAxis: 'y',
                responsive: true,
                maintainAspectRatio: false,
                plugins: { legend: { display: false }, tooltip: { callbacks: chartTooltipTitleCallback } },
                scales: { x: { beginAtZero: true, max: 100, grid: { color: '#e2e8f0' } }, y: { grid: { display: false } } }
            }
        });

        new Chart(document.getElementById('climateChart'), {
            type: 'line',
            data: {
                labels: ['2015', '2018', '2021'],
                datasets: [{
                    label: 'CO₂ Emissions (Metric Tons Per Capita)',
                    data: [0.96, 1.05, 0.98],
                    borderColor: palette.red,
                    backgroundColor: 'rgba(191, 51, 37, 0.1)',
                    pointBackgroundColor: palette.red,
                    pointRadius: 5,
                    fill: true,
                    tension: 0.3
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                plugins: { legend: { display: false }, tooltip: { callbacks: chartTooltipTitleCallback } },
                scales: { y: { beginAtZero: false, title: { display: true, text: 'Metric Tons Per Capita' } } }
            }
        });
    </script>
</body>
</html>

