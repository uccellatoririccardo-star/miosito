# miosito
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Analisi Mercato Globale - 9 Novembre 2025</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #F8F9FA;
            color: #003F5C;
        }
        
        .palette-bg-darkest { background-color: #003F5C; }
        .palette-text-darkest { color: #003F5C; }
        .palette-text-dark { color: #2F4B7C; }
        .palette-text-accent-hot { color: #F95D6A; }
        .palette-bg-accent-hot { background-color: #F95D6A; }
        .palette-border-accent-hot { border-color: #F95D6A; }

        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }

        @media (min-width: 640px) {
            .chart-container {
                height: 350px;
            }
        }

        @media (min-width: 1024px) {
            .chart-container {
                height: 400px;
            }
        }
    </style>
</head>
<body class="antialiased">

    <main class="container mx-auto p-4 md:p-8">

        <header class="text-center mb-12 md:mb-16">
            <h1 class="text-3xl md:text-5xl font-bold palette-text-darkest mb-3">Mercati Globali: L'Ora della Prudenza</h1>
            <p class="text-lg md:text-xl palette-text-dark font-semibold">Il tech frena e l'incertezza macro-US pesa sull'Europa</p>
            <p class="text-md text-gray-500 mt-2">Analisi basata sul report del 9 Novembre 2025</p>
        </header>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-6 md:gap-8">

            <div class="lg:col-span-2 bg-white rounded-lg shadow-lg p-6 md:p-8">
                <h2 class="text-2xl font-bold palette-text-dark mb-4">Panoramica Globale: Chiusura Mista</h2>
                <p class="text-gray-700 mb-6">
                    I mercati globali chiudono la settimana con un sentiment contrastante. Mentre gli indici tradizionali USA mostrano guadagni limitati, il settore tecnologico frena bruscamente, trascinando al ribasso il Nasdaq. L'Asia e l'Europa seguono con debolezza, scontando i rischi sulla crescita e l'incertezza della politica monetaria.
                </p>
                <div class="chart-container">
                    <canvas id="globalIndicesChart"></canvas>
                </div>
                <p class="text-sm text-gray-600 text-center mt-4">Variazione % settimanale (dati illustrativi)</p>
            </div>

            <div class="bg-white rounded-lg shadow-lg p-6 md:p-8">
                <h2 class="text-2xl font-bold palette-text-dark mb-4">I Fattori Chiave del Rischio</h2>
                <p class="text-gray-700 mb-6">
                    Tre preoccupazioni principali dominano il sentiment degli investitori: le valutazioni eccessive nel settore tech/IA, l'incertezza sui dati macro USA dovuta allo shutdown e la mancanza di una direzione chiara da parte delle banche centrali.
                </p>
                <div class="chart-container" style="max-width: 450px; height: 300px; max-height: 350px;">
                    <canvas id="concernsDoughnutChart"></canvas>
                </div>
                <p class="text-sm text-gray-600 text-center mt-4">Principali preoccupazioni degli investitori (illustrativo)</p>
            </div>

            <div class="bg-white rounded-lg shadow-lg p-6 md:p-8 flex flex-col justify-center">
                <h2 class="text-2xl font-bold palette-text-dark mb-4">L'Impatto dello Shutdown USA</h2>
                <p class="text-gray-700 mb-6">
                    Il prolungato shutdown del governo federale USA ha creato un "buco nero" informativo. La mancanza di dati macroeconomici ufficiali (inflazione, occupazione) rende imprevedibili le prossime mosse della Federal Reserve, aumentando la volatilità e la riluttanza al rischio sui mercati finanziari.
                </p>
                <div class="bg-red-50 border-l-4 border-red-500 text-red-800 p-4 rounded-md">
                    <h3 class="font-bold">Incertezza sulla FED</h3>
                    <p>Senza dati, la politica "data-dependent" della Fed è paralizzata, costringendo gli investitori a navigare alla cieca.</p>
                </div>
            </div>

            <div class="lg:col-span-2 bg-white rounded-lg shadow-lg p-6 md:p-8">
                <h2 class="text-2xl font-bold palette-text-dark mb-4">Analisi dei Flussi: Non Fuga, ma Riassetto</h2>
                <p class="text-gray-700 mb-6">
                    Non assistiamo a un abbandono totale dell'equity. Piuttosto, i flussi indicano una rotazione strategica: gli investitori stanno riducendo l'esposizione agli asset growth (come il tech) per aumentare l'interesse verso strumenti a minor rischio, come le obbligazioni a breve termine e la liquidità.
                </p>
                <div class="chart-container">
                    <canvas id="flowsStackedBarChart"></canvas>
                </div>
                <p class="text-sm text-gray-600 text-center mt-4">Allocazione % dei flussi netti (dati illustrativi Q3 vs Q4)</p>
            </div>

            <div class="lg:col-span-2 bg-white rounded-lg shadow-lg p-6 md:p-8">
                <h2 class="text-2xl font-bold palette-text-dark mb-4">Focus Italia & Europa: Analisi Settoriale</h2>
                <p class="text-gray-700 mb-6">
                    L'Europa si trova in bilico. L'analisi dei principali settori italiani ed europei rivela un quadro complesso, con le utility "green" che emergono come resilienti, mentre i titoli sovrani e l'energia tradizionale affrontano rischi crescenti legati ai tassi e alla domanda.
                </p>
                <div class="chart-container" style="max-width: 500px;">
                    <canvas id="sectorRadarChart"></canvas>
                </div>
                <p class="text-sm text-gray-600 text-center mt-4">Scala 1 (Basso) - 5 (Alto). Dati illustrativi.</p>
            </div>

            <div class="bg-white rounded-lg shadow-lg p-6 md:p-8">
                <h2 class="text-2xl font-bold palette-text-dark mb-4">Approfondimento: Banche Italiane</h2>
                <p class="text-gray-700 mb-5">
                    Il settore bancario è esposto a forze contrapposte. Da un lato, i margini di interesse beneficiano di tassi più alti; dall'altro, l'economia in rallentamento minaccia i costi di raccolta e la qualità del credito.
                </p>
                <div class="space-y-4">
                    <div class="p-4 rounded-lg bg-green-50 border border-green-200">
                        <h3 class="font-bold text-green-800">PRO: Margini Favorevoli</h3>
                        <p class="text-green-700 text-sm">Contesto di tassi più favorevole rispetto all'era dei tassi zero.</p>
                    </div>
                    <div class="p-4 rounded-lg bg-yellow-50 border border-yellow-200">
                        <h3 class="font-bold text-yellow-800">CONTRO: Incertezza Credito</h3>
                        <p class="text-yellow-700 text-sm">Rallentamento economico e aumento dei costi di raccolta pesano sulla vulnerabilità.</p>
                    </div>
                </div>
                <p class="text-gray-700 mt-5">
                    <span class="font-semibold">Chi vince:</span> Banche con forte trasformazione digitale e ricavi diversificati.
                    <br>
                    <span class="font-semibold">Chi è vulnerabile:</span> Istituti tradizionali esposti a shock sui tassi.
                </p>
            </div>

            <div class="bg-white rounded-lg shadow-lg p-6 md:p-8">
                <h2 class="text-2xl font-bold palette-text-dark mb-4">Approfondimento: Settore Energia</h2>
                <p class="text-gray-700 mb-5">
                    Il settore energetico vive una doppia contraddizione: la debolezza dei prezzi del petrolio penalizza le società integrate tradizionali, mentre la spinta regolatoria verso la decarbonizzazione favorisce le utility "green".
                </p>
                <div class="chart-container" style="height: 300px; max-height: 350px;">
                    <canvas id="energyRiskRewardChart"></canvas>
                </div>
                <p class="text-sm text-gray-600 text-center mt-4">Profilo Rischio/Rendimento (illustrativo)</p>
                <p class="text-gray-700 mt-5">
                    Aziende come Enel ed Edison stanno rimodellando i piani industriali verso le rinnovabili, mostrando un profilo di rischio/rendimento più favorevole rispetto alle società petrolifere integrate.
                </p>
            </div>

            <div class="lg:col-span-2 bg-white rounded-lg shadow-lg p-6 md:p-8">
                <h2 class="text-2xl font-bold palette-text-dark mb-4">Outlook Trimestrale: I Rischi da Monitorare</h2>
                <p class="text-gray-700 mb-6">
                    Lo scenario base per l'Europa è di tassi stabili o in lieve aumento, con inflazione vischiosa e crescita modesta. In questo contesto, la selettività è fondamentale. I rischi principali per il prossimo trimestre includono:
                </p>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div class="border-l-4 palette-border-accent-hot bg-red-50 p-4 rounded-md">
                        <h3 class="font-bold palette-text-accent-hot">1. Rialzo Tassi Globale</h3>
                        <p class="text-gray-700 text-sm">Un rialzo imprevisto dei rendimenti comprimerebbe finanziarie e obbligazioni.</p>
                    </div>
                    <div class="border-l-4 palette-border-accent-hot bg-red-50 p-4 rounded-md">
                        <h3 class="font-bold palette-text-accent-hot">2. Peggioramento Macro</h3>
                        <p class="text-gray-700 text-sm">Un rallentamento economico globale più rapido del previsto.</p>
                    </div>
                    <div class="border-l-4 palette-border-accent-hot bg-red-50 p-4 rounded-md">
                        <h3 class="font-bold palette-text-accent-hot">3. Regolamentazione</h3>
                        <p class="text-gray-700 text-sm">Interventi regolatori in Europa/Italia che comprimono gli utili nel settore energia.</p>
                    </div>
                    <div class="border-l-4 palette-border-accent-hot bg-red-50 p-4 rounded-md">
                        <h3 class="font-bold palette-text-accent-hot">4. Correzione Tech/IA</h3>
                        <p class="text-gray-700 text-sm">Una correzione estesa che trascina i mercati globali in una fase di alta volatilità.</p>
                    </div>
                </div>
                <p class="text-gray-700 mt-6 text-center font-semibold text-lg palette-text-dark">
                    La gestione della duration, la conservazione della liquidità e un'attenta selezione dei titoli restano essenziali.
                </p>
            </div>

        </div>

    </main>

    <footer class="text-center p-6 mt-8">
        <p class="text-sm text-gray-500">Questa è un'infografica generata automaticamente basata su report di mercato. Non costituisce consulenza finanziaria. Dati del 9 Novembre 2025.</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            
            const chartColors = {
                darkestBlue: '#003F5C',
                darkBlue: '#2F4B7C',
                purple: '#665191',
                magenta: '#A05195',
                pink: '#D45087',
                red: '#F95D6A',
                orange: '#FF7C43',
                yellow: '#FFA600'
            };

            const defaultTooltipCallback = {
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
            
            const globalIndicesCtx = document.getElementById('globalIndicesChart');
            if (globalIndicesCtx) {
                new Chart(globalIndicesCtx, {
                    type: 'bar',
                    data: {
                        labels: ['S&P 500', 'Dow Jones', 'Nasdaq', 'Europa (Stoxx)', 'Asia (Nikkei)'],
                        datasets: [{
                            label: 'Variazione % Settimanale',
                            data: [0.1, 0.2, -0.5, -0.3, -0.4],
                            backgroundColor: [
                                chartColors.purple,
                                chartColors.magenta,
                                chartColors.red,
                                chartColors.darkBlue,
                                chartColors.orange
                            ],
                            borderRadius: 4,
                            barPercentage: 0.6
                        }]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        plugins: {
                            legend: {
                                display: false
                            },
                            tooltip: {
                                callbacks: defaultTooltipCallback
                            }
                        },
                        scales: {
                            y: {
                                beginAtZero: true,
                                grid: {
                                    color: '#E5E7EB'
                                },
                                ticks: {
                                    color: '#6B7280'
                                }
                            },
                            x: {
                                grid: {
                                    display: false
                                },
                                ticks: {
                                    color: '#1F2937'
                                }
                            }
                        }
                    }
                });
            }

            const concernsDoughnutCtx = document.getElementById('concernsDoughnutChart');
            if (concernsDoughnutCtx) {
                new Chart(concernsDoughnutCtx, {
                    type: 'doughnut',
                    data: {
                        labels: ['Valutazioni Tech/IA', 'Incertezza Macro US', 'Politica Monetaria'],
                        datasets: [{
                            data: [50, 30, 20],
                            backgroundColor: [
                                chartColors.red,
                                chartColors.orange,
                                chartColors.purple
                            ],
                            borderColor: '#FFFFFF',
                            borderWidth: 2
                        }]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        plugins: {
                            legend: {
                                position: 'bottom',
                                labels: {
                                    color: '#1F2937'
                                }
                            },
                            tooltip: {
                                callbacks: defaultTooltipCallback
                            }
                        }
                    }
                });
            }

            const flowsStackedBarCtx = document.getElementById('flowsStackedBarChart');
            if (flowsStackedBarCtx) {
                new Chart(flowsStackedBarCtx, {
                    type: 'bar',
                    data: {
                        labels: ['Q3 2025', 'Q4 2025'],
                        datasets: [
                            {
                                label: 'Equity Growth/Tech',
                                data: [60, 40],
                                backgroundColor: chartColors.red,
                            },
                            {
                                label: 'Obbligazioni Brevi',
                                data: [20, 35],
                                backgroundColor: chartColors.purple,
                            },
                            {
                                label: 'Liquidità / Basso Rischio',
                                data: [20, 25],
                                backgroundColor: chartColors.darkBlue,
                            }
                        ]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        plugins: {
                            legend: {
                                position: 'bottom',
                                labels: {
                                    color: '#1F2937'
                                }
                            },
                            tooltip: {
                                callbacks: defaultTooltipCallback
                            }
                        },
                        scales: {
                            y: {
                                stacked: true,
                                beginAtZero: true,
                                max: 100,
                                grid: {
                                    color: '#E5E7EB'
                                },
                                ticks: {
                                    color: '#6B7280'
                                }
                            },
                            x: {
                                stacked: true,
                                grid: {
                                    display: false
                                },
                                ticks: {
                                    color: '#1F2937'
                                }
                            }
                        }
                    }
                });
            }
            
            const sectorRadarCtx = document.getElementById('sectorRadarChart');
            if (sectorRadarCtx) {
                new Chart(sectorRadarCtx, {
                    type: 'radar',
                    data: {
                        labels: [
                            'Banche', 
                            ['Obbligazioni', 'Sovrane'], 
                            ['Energia', 'Tradizionale'], 
                            ['Utility', 'Green']
                        ],
                        datasets: [
                            {
                                label: 'Opportunità',
                                data: [3, 1, 2, 5],
                                backgroundColor: 'rgba(102, 81, 145, 0.2)',
                                borderColor: chartColors.purple,
                                pointBackgroundColor: chartColors.purple,
                                pointBorderColor: '#fff',
                                pointHoverBackgroundColor: '#fff',
                                pointHoverBorderColor: chartColors.purple
                            },
                            {
                                label: 'Rischio',
                                data: [3, 4, 3, 2],
                                backgroundColor: 'rgba(249, 93, 106, 0.2)',
                                borderColor: chartColors.red,
                                pointBackgroundColor: chartColors.red,
                                pointBorderColor: '#fff',
                                pointHoverBackgroundColor: '#fff',
                                pointHoverBorderColor: chartColors.red
                            }
                        ]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        plugins: {
                            legend: {
                                position: 'bottom',
                                labels: {
                                    color: '#1F2937'
                                }
                            },
                            tooltip: {
                                callbacks: defaultTooltipCallback
                            }
                        },
                        scales: {
                            r: {
                                beginAtZero: true,
                                max: 5,
                                stepSize: 1,
                                grid: {
                                    color: '#E5E7EB'
                                },
                                pointLabels: {
                                    color: '#003F5C',
                                    font: {
                                        size: 13
                                    }
                                },
                                ticks: {
                                    backdropColor: '#F8F9FA',
                                    color: '#6B7280'
                                }
                            }
                        }
                    }
                });
            }
            
            const energyRiskRewardCtx = document.getElementById('energyRiskRewardChart');
            if (energyRiskRewardCtx) {
                new Chart(energyRiskRewardCtx, {
                    type: 'bar',
                    data: {
                        labels: ['Utility Green', ['Integrati', 'Tradizionali']],
                        datasets: [
                            {
                                label: 'Rendimento Potenziale',
                                data: [4.5, 2],
                                backgroundColor: chartColors.purple,
                                order: 1
                            },
                            {
                                label: 'Rischio Percepito',
                                data: [2.5, 3.5],
                                backgroundColor: chartColors.red,
                                order: 2
                            }
                        ]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        plugins: {
                            legend: {
                                position: 'bottom',
                                labels: {
                                    color: '#1F2937'
                                }
                            },
                            tooltip: {
                                callbacks: defaultTooltipCallback
                            }
                        },
                        scales: {
                            y: {
                                beginAtZero: true,
                                max: 5,
                                grid: {
                                    color: '#E5E7EB'
                                },
                                ticks: {
                                    color: '#6B7280'
                                }
                            },
                            x: {
                                grid: {
                                    display: false
                                },
                                ticks: {
                                    color: '#1F2937'
                                }
                            }
                        }
                    }
                });
            }
        });
    </script>
</body>
</html>
