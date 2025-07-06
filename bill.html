<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sales Report Dashboard</title>
    
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    
    <script src="https://cdn.jsdelivr.net/npm/chart.js@3.7.0/dist/chart.min.js"></script>
    
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap" rel="stylesheet">

    <style>
        /* Custom CSS for Parallax Effect and Card Consistency */
        .parallax-bg {
            background-image: url('https://source.unsplash.com/random/1600x900/?sales,report'); /* Placeholder background image */
            background-attachment: fixed; /* This creates the parallax effect */
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
            height: 40vh; /* Adjust height as needed */
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden; /* Important for fixed background */
        }

        .parallax-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5); /* Dark overlay for text readability */
        }

        /* Ensure charts have a defined height for responsiveness */
        .chart-container {
            position: relative;
            height: 300px; /* Fixed height for charts on all screen sizes */
            width: 100%;
        }

        /* Make the body use the Inter font */
        body {
            font-family: 'Inter', sans-serif;
        }

        /* Style for loading spinners (simplified) */
        .loading-spinner {
            border: 4px solid rgba(0, 0, 0, 0.1);
            border-left: 4px solid #3b82f6; /* Tailwind blue-500 */
            border-radius: 50%;
            width: 24px;
            height: 24px;
            animation: spin 1s linear infinite;
            display: inline-block;
            vertical-align: middle;
            margin-left: 8px;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body class="bg-gray-50 font-sans text-gray-800">

    <header class="parallax-bg">
        <div class="parallax-overlay"></div>
        <div class="relative z-10 text-center px-4">
            <h1 class="text-5xl md:text-6xl font-extrabold text-white leading-tight drop-shadow-lg">
                Sales Report Overview
            </h1>
            <p class="mt-4 text-xl md:text-2xl text-gray-200 drop-shadow-md">
                Analyze daily and monthly sales data.
            </p>
        </div>
    </header>

    <main class="container mx-auto p-6 md:p-8 -mt-20 relative z-20 bg-white rounded-lg shadow-xl border border-gray-200">
        
        <h2 class="text-3xl font-bold mb-8 text-center text-gray-900">Sales Report</h2>

        <div class="flex flex-col md:flex-row justify-center items-center mb-8 space-y-4 md:space-y-0 md:space-x-4">
            <label for="startDate" class="text-lg">From:</label>
            <input type="date" id="startDate" class="p-3 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-2 focus:ring-blue-400 text-lg">
            
            <label for="endDate" class="text-lg">To:</label>
            <input type="date" id="endDate" class="p-3 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-2 focus:ring-blue-400 text-lg">
            
            <button id="filterSalesBtn" class="px-6 py-3 text-lg font-semibold rounded-lg shadow-md bg-blue-600 text-white hover:bg-blue-700 focus:outline-none focus:ring-4 focus:ring-blue-400 transition duration-200">
                Apply Filter
                <span id="filterSpinner" class="hidden loading-spinner"></span>
            </button>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
            <div class="bg-blue-50 p-6 rounded-lg shadow-md border border-blue-200">
                <h3 class="text-xl font-bold text-blue-800 mb-4">Daily Sales Summary</h3>
                <div id="dailySalesSummary" class="space-y-2 max-h-60 overflow-y-auto">
                    <p class="text-gray-600">Loading daily sales...</p>
                </div>
            </div>
            <div class="bg-green-50 p-6 rounded-lg shadow-md border border-green-200">
                <h3 class="text-xl font-bold text-green-800 mb-4">Monthly Sales Summary</h3>
                <div id="monthlySalesSummary" class="space-y-2 max-h-60 overflow-y-auto">
                    <p class="text-gray-600">Loading monthly sales...</p>
                </div>
            </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
            <div class="bg-white p-6 rounded-lg shadow-md border border-gray-200">
                <h3 class="text-xl font-bold text-gray-800 mb-4 text-center">Daily Sales Trend</h3>
                <div class="chart-container">
                    <canvas id="dailySalesChart"></canvas>
                </div>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-md border border-gray-200">
                <h3 class="text-xl font-bold text-gray-800 mb-4 text-center">Monthly Sales Trend</h3>
                <div class="chart-container">
                    <canvas id="monthlySalesChart"></canvas>
                </div>
            </div>
        </div>

        <h3 class="text-2xl font-bold mb-4 text-gray-900">All Bill Details</h3>

        <div class="mb-6 text-right">
            <button id="generateCsvReportBtn" class="px-6 py-3 text-lg font-semibold rounded-lg shadow-md bg-purple-600 text-white hover:bg-purple-700 focus:outline-none focus:ring-4 focus:ring-purple-400 transition duration-200">
                Generate CSV Report
            </button>
        </div>

        <div class="overflow-x-auto bg-white rounded-lg shadow-md border border-gray-200">
            <table class="min-w-full divide-y divide-gray-200">
                <thead class="bg-gray-50">
                    <tr>
                        <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Timestamp</th>
                        <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Customer Name</th>
                        <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Phone Number</th>
                        <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Date</th>
                        <th class="px-6 py-3 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">Total Amount</th>
                    </tr>
                </thead>
                <tbody id="billDetailsTableBody" class="bg-white divide-y divide-gray-200">
                    <tr>
                        <td colspan="5" class="px-6 py-4 whitespace-nowrap text-center text-gray-500">Loading bill details...</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </main>

    <footer class="mt-12 py-8 bg-gray-800 text-white text-center text-sm">
        <p>&copy; 2025 Sales Dashboard. All rights reserved.</p>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            // !!! IMPORTANT: UPDATED CSV URL FOR SALES (BILL DETAILS) !!!
            const salesCsvUrl = 'https://docs.google.com/spreadsheets/d/e/2PACX-1vS6KGzR-BKL-JQaV3rkCxsdb-XZyQtaQLS4sV-_yCVAt0I2cgRDWG_FTDNSgjiNqLAfjTC2sItdrFBo/pub?gid=942116775&single=true&output=csv'; 
            
            // DOM Elements for Sales
            const startDateInput = document.getElementById('startDate');
            const endDateInput = document.getElementById('endDate');
            const filterSalesBtn = document.getElementById('filterSalesBtn');
            const filterSpinner = document.getElementById('filterSpinner'); // New spinner
            const dailySalesSummary = document.getElementById('dailySalesSummary');
            const monthlySalesSummary = document.getElementById('monthlySalesSummary');
            const billDetailsTableBody = document.getElementById('billDetailsTableBody');
            const generateCsvReportBtn = document.getElementById('generateCsvReportBtn'); 

            // Chart instances
            let dailySalesChartInstance = null;
            let monthlySalesChartInstance = null;

            let salesData = []; // To store parsed sales data
            let currentFilteredSales = []; // To store sales after date filtering, for report generation

            // Helper to show/hide loading spinner
            function showSpinner(show) {
                if (filterSpinner) {
                    filterSpinner.classList.toggle('hidden', !show);
                }
                if (filterSalesBtn) {
                    filterSalesBtn.disabled = show;
                }
            }

            // --- Generic CSV Parser (Optimized for robustness and performance) ---
            function parseCsv(csvString) {
                const lines = csvString.trim().split(/\r?\n/); // Handle different line endings
                if (lines.length <= 1) return { headers: [], data: [] };

                // Robustly split CSV lines by comma, handling quoted fields
                const parseLine = (line) => {
                    const values = [];
                    let inQuote = false;
                    let currentField = '';
                    for (let i = 0; i < line.length; i++) {
                        const char = line[i];
                        if (char === '"') {
                            if (i + 1 < line.length && line[i+1] === '"') {
                                currentField += '"'; // Escaped quote
                                i++;
                            } else {
                                inQuote = !inQuote; // Toggle quote state
                            }
                        } else if (char === ',' && !inQuote) {
                            values.push(currentField.trim());
                            currentField = '';
                        } else {
                            currentField += char;
                        }
                    }
                    values.push(currentField.trim()); // Add the last field
                    return values;
                };

                const rawHeaders = parseLine(lines[0]);
                
                // --- Specific Header Mapping for Sales --- (Matching your sheet's column names)
                const salesHeaderMap = {
                    "Timestamp": "TIMESTAMP",
                    "customer name": "CUSTOMER_NAME",
                    "Phone Number": "PHONE_NUMBER",
                    "DATE": "DATE",
                    "TOTAL AMOUNT": "TOTAL_AMOUNT"
                };
                
                const headers = rawHeaders.map(rawHeader => {
                    if (salesHeaderMap[rawHeader]) {
                        return salesHeaderMap[rawHeader];
                    }
                    // Fallback to generic cleaning if no specific map found
                    return rawHeader.toUpperCase()
                                    .replace(/[^A-Z0-9]/g, '_') 
                                    .replace(/_{2,}/g, '_')     
                                    .replace(/^_|_$/g, '');     
                });
                
                const data = [];
                for (let i = 1; i < lines.length; i++) {
                    const line = lines[i];
                    if (!line.trim()) continue; // Skip empty lines

                    const values = parseLine(line);
                    
                    const item = {};
                    for (let index = 0; index < headers.length; index++) {
                        const headerKey = headers[index];
                        item[headerKey] = values[index] !== undefined ? values[index] : ''; 
                    }

                    if (values.length > headers.length) {
                        console.warn(`Row ${i + 1} has more columns than headers. Extra values ignored.`, line);
                    } else if (values.length < headers.length) {
                        console.warn(`Row ${i + 1} has fewer columns than headers. Some values set to empty string.`, line);
                    }
                    data.push(item);
                }
                return { headers: headers, data: data }; 
            }

            // --- Sales Specific Functions ---

            async function fetchSalesData() {
                // Initial loading states
                billDetailsTableBody.innerHTML = '<tr><td colspan="5" class="px-6 py-4 whitespace-nowrap text-center text-gray-500"><div class="flex items-center justify-center"><div class="loading-spinner"></div> Loading bill details...</div></td></tr>';
                dailySalesSummary.innerHTML = '<p class="text-gray-600"><div class="loading-spinner"></div> Loading daily sales...</p>';
                monthlySalesSummary.innerHTML = '<p class="text-gray-600"><div class="loading-spinner"></div> Loading monthly sales...</p>';
                showSpinner(true);

                try {
                    const response = await fetch(salesCsvUrl);
                    if (!response.ok) {
                        throw new Error(`HTTP error! status: ${response.status}`);
                    }
                    const text = await response.text();
                    const { data } = parseCsv(text); 
                    salesData = data; // Store raw sales data
                    return data;
                } catch (error) {
                    console.error('Error fetching or parsing Sales CSV:', error);
                    billDetailsTableBody.innerHTML = '<tr><td colspan="5" class="px-6 py-4 whitespace-nowrap text-center text-red-600">Failed to load sales data. Please ensure the Google Sheet is published to web as CSV and the URL is correct.</td></tr>';
                    dailySalesSummary.innerHTML = '<p class="text-red-600">Failed to load daily sales.</p>';
                    monthlySalesSummary.innerHTML = '<p class="text-red-600">Failed to load monthly sales.</p>';
                    return [];
                } finally {
                    showSpinner(false);
                }
            }

            function renderSalesData() {
                showSpinner(true); // Show spinner while rendering
                
                // Small delay to allow spinner to render, then execute heavy tasks
                setTimeout(() => {
                    currentFilteredSales = filterSalesByDate(salesData, startDateInput.value, endDateInput.value);
                    
                    displayBillDetails(currentFilteredSales);
                    
                    const { dailyLabels, dailyAmounts, dailySummaryHtml } = calculateDailySales(currentFilteredSales);
                    dailySalesSummary.innerHTML = dailySummaryHtml; 
                    renderDailySalesChart(dailyLabels, dailyAmounts);

                    const { monthlyLabels, monthlyAmounts, monthlySummaryHtml } = calculateMonthlySales(currentFilteredSales);
                    monthlySalesSummary.innerHTML = monthlySummaryHtml; 
                    renderMonthlySalesChart(monthlyLabels, monthlyAmounts);

                    showSpinner(false); // Hide spinner after rendering
                }, 50); // A small delay, adjust if needed
            }

            function displayBillDetails(sales) {
                if(!billDetailsTableBody) return; 
                billDetailsTableBody.innerHTML = ''; // Clear existing rows

                if (sales.length === 0) {
                    billDetailsTableBody.innerHTML = '<tr><td colspan="5" class="px-6 py-4 whitespace-nowrap text-center text-gray-500">No sales data found for the selected period.</td></tr>';
                    return;
                }

                // Use DocumentFragment for performance when adding many rows
                const fragment = document.createDocumentFragment();
                sales.forEach(sale => {
                    const row = document.createElement('tr');
                    // Sanitize potential HTML in data to prevent XSS
                    row.innerHTML = `
                        <td class="px-6 py-4 whitespace-nowrap">${escapeHTML(sale.TIMESTAMP || 'N/A')}</td>
                        <td class="px-6 py-4 whitespace-nowrap">${escapeHTML(sale.CUSTOMER_NAME || 'N/A')}</td>
                        <td class="px-6 py-4 whitespace-nowrap">${escapeHTML(sale.PHONE_NUMBER || 'N/A')}</td>
                        <td class="px-6 py-4 whitespace-nowrap">${escapeHTML(sale.DATE || 'N/A')}</td>
                        <td class="px-6 py-4 whitespace-nowrap">₹${parseFloat(sale.TOTAL_AMOUNT || 0).toFixed(2)}</td>
                    `;
                    fragment.appendChild(row);
                });
                billDetailsTableBody.appendChild(fragment);
            }

            // Helper function to escape HTML for security
            function escapeHTML(str) {
                const div = document.createElement('div');
                div.appendChild(document.createTextNode(str));
                return div.innerHTML;
            }

            function parseDate(dateStr) {
                if (!dateStr) return null;
                // Attempt to parse as YYYY-MM-DD (standard HTML date input format)
                let date = new Date(dateStr + 'T00:00:00'); // Add time to avoid timezone issues
                if (!isNaN(date.getTime())) {
                    return date;
                }

                // Attempt to parse as MM/DD/YYYY (common Google Sheet format)
                let parts = dateStr.split('/');
                if (parts.length === 3) {
                    date = new Date(parseInt(parts[2]), parseInt(parts[0]) - 1, parseInt(parts[1]));
                    if (!isNaN(date.getTime())) {
                        return date;
                    }
                }
                // Attempt to parse as DD/MM/YYYY (another common format)
                if (parts.length === 3) {
                     date = new Date(parseInt(parts[2]), parseInt(parts[1]) - 1, parseInt(parts[0]));
                     if (!isNaN(date.getTime())) {
                         return date;
                     }
                }
                
                console.warn("Could not parse date:", dateStr);
                return null;
            }

            function filterSalesByDate(sales, startDateVal, endDateVal) {
                const start = parseDate(startDateVal);
                const end = parseDate(endDateVal);

                return sales.filter(sale => {
                    const saleDate = parseDate(sale.DATE);
                    if (!saleDate) return false;

                    let matchesStart = true;
                    if (start) {
                        matchesStart = saleDate >= start;
                    }

                    let matchesEnd = true;
                    if (end) {
                        // For end date, we want to include the entire day
                        const endOfDay = new Date(end);
                        endOfDay.setHours(23, 59, 59, 999);
                        matchesEnd = saleDate <= endOfDay;
                    }
                    return matchesStart && matchesEnd;
                });
            }

            function calculateDailySales(sales) {
                const dailyTotals = {};
                sales.forEach(sale => {
                    const saleDate = parseDate(sale.DATE); 
                    const amount = parseFloat(sale.TOTAL_AMOUNT || 0); 

                    if (saleDate && !isNaN(amount)) {
                        const dateKey = saleDate.toISOString().split('T')[0]; // YYYY-MM-DD format for key
                        if (dailyTotals[dateKey]) {
                            dailyTotals[dateKey] += amount;
                        } else {
                            dailyTotals[dateKey] = amount;
                        }
                    }
                });

                const sortedDates = Object.keys(dailyTotals).sort(); // YYYY-MM-DD sorts correctly

                let summaryHtml = '';
                const labels = [];
                const amounts = [];

                if (sortedDates.length === 0) {
                    summaryHtml = '<p class="text-gray-600">No daily sales data available for this period.</p>';
                } else {
                    sortedDates.forEach(date => {
                        const total = dailyTotals[date];
                        summaryHtml += `<p><strong>${date}:</strong> ₹${total.toFixed(2)}</p>`;
                        labels.push(date);
                        amounts.push(total);
                    });
                }
                return { dailyLabels: labels, dailyAmounts: amounts, dailySummaryHtml: summaryHtml };
            }

            function calculateMonthlySales(sales) {
                const monthlyTotals = {};
                sales.forEach(sale => {
                    const saleDate = parseDate(sale.DATE); 
                    const amount = parseFloat(sale.TOTAL_AMOUNT || 0); 

                    if (saleDate && !isNaN(amount)) {
                        const monthKey = `${saleDate.getFullYear()}-${String(saleDate.getMonth() + 1).padStart(2, '0')}`; 
                        if (monthlyTotals[monthKey]) {
                            monthlyTotals[monthKey] += amount;
                        } else {
                            monthlyTotals[monthKey] = amount;
                        }
                    }
                });

                const sortedMonths = Object.keys(monthlyTotals).sort();

                let summaryHtml = '';
                const labels = [];
                const amounts = [];

                if (sortedMonths.length === 0) {
                    summaryHtml = '<p class="text-gray-600">No monthly sales data available for this period.</p>';
                } else {
                    sortedMonths.forEach(monthKey => {
                        const total = monthlyTotals[monthKey];
                        const [year, monthNum] = monthKey.split('-');
                        const monthName = new Date(year, parseInt(monthNum, 10) - 1, 1).toLocaleString('en-US', { month: 'long' });
                        summaryHtml += `<p><strong>${monthName} ${year}:</strong> ₹${total.toFixed(2)}</p>`;
                        labels.push(`${monthName} ${year}`);
                        amounts.push(total);
                    });
                }
                return { monthlyLabels: labels, monthlyAmounts: amounts, monthlySummaryHtml: summaryHtml };
            }

            // --- Charting Functions ---
            function renderDailySalesChart(labels, data) {
                const ctx = document.getElementById('dailySalesChart');
                if (!ctx) return; 

                if (dailySalesChartInstance) {
                    dailySalesChartInstance.destroy(); 
                }

                dailySalesChartInstance = new Chart(ctx, {
                    type: 'bar', 
                    data: {
                        labels: labels,
                        datasets: [{
                            label: 'Daily Sales (₹)',
                            data: data,
                            backgroundColor: 'rgba(59, 130, 246, 0.6)', 
                            borderColor: 'rgba(59, 130, 246, 1)',
                            borderWidth: 1
                        }]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false, // Allow charts to adapt to container size
                        scales: {
                            y: {
                                beginAtZero: true,
                                title: {
                                    display: true,
                                    text: 'Amount (₹)'
                                }
                            },
                            x: {
                                title: {
                                    display: true,
                                    text: 'Date'
                                }
                            }
                        },
                        plugins: {
                            legend: {
                                display: true,
                                position: 'top'
                            },
                            tooltip: { // Add tooltip for better UX on mobile
                                mode: 'index',
                                intersect: false,
                            }
                        }
                    }
                });
            }

            function renderMonthlySalesChart(labels, data) {
                const ctx = document.getElementById('monthlySalesChart');
                if (!ctx) return; 

                if (monthlySalesChartInstance) {
                    monthlySalesChartInstance.destroy(); 
                }

                monthlySalesChartInstance = new Chart(ctx, {
                    type: 'line', 
                    data: {
                        labels: labels,
                        datasets: [{
                            label: 'Monthly Sales (₹)',
                            data: data,
                            backgroundColor: 'rgba(16, 185, 129, 0.6)', 
                            borderColor: 'rgba(16, 185, 129, 1)',
                            borderWidth: 2,
                            fill: true, 
                            tension: 0.2 
                        }]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        scales: {
                            y: {
                                beginAtZero: true,
                                title: {
                                    display: true,
                                    text: 'Amount (₹)'
                                }
                            },
                            x: {
                                title: {
                                    display: true,
                                    text: 'Month'
                                }
                            }
                        },
                        plugins: {
                            legend: {
                                display: true,
                                position: 'top'
                            },
                            tooltip: { // Add tooltip for better UX on mobile
                                mode: 'index',
                                intersect: false,
                            }
                        }
                    }
                });
            }

            // --- CSV Report Generation ---
            function generateCsvReport() {
                if (currentFilteredSales.length === 0) {
                    alert('No sales data to generate a report for the current filter.');
                    return;
                }

                const headers = ['Timestamp', 'Customer Name', 'Phone Number', 'Date', 'Total Amount'];
                
                const rows = currentFilteredSales.map(sale => [
                    `"${(sale.TIMESTAMP || '').replace(/"/g, '""')}"`, 
                    `"${(sale.CUSTOMER_NAME || '').replace(/"/g, '""')}"`,
                    `"${(sale.PHONE_NUMBER || '').replace(/"/g, '""')}"`,
                    `"${(sale.DATE || '').replace(/"/g, '""')}"`,
                    parseFloat(sale.TOTAL_AMOUNT || 0).toFixed(2)
                ]);

                const csvContent = [
                    headers.join(','),
                    ...rows.map(row => row.join(','))
                ].join('\n');

                const blob = new Blob([csvContent], { type: 'text/csv;charset=utf-8;' });
                const link = document.createElement('a');
                const url = URL.createObjectURL(blob);
                const today = new Date().toISOString().split('T')[0];
                link.setAttribute('href', url);
                link.setAttribute('download', `sales_report_${today}.csv`);
                link.style.visibility = 'hidden';
                document.body.appendChild(link);
                link.click();
                document.body.removeChild(link);
            }

            // Event Listeners for Sales filters and report
            if (filterSalesBtn) filterSalesBtn.addEventListener('click', renderSalesData);
            if (generateCsvReportBtn) generateCsvReportBtn.addEventListener('click', generateCsvReport);

            // --- Initialization ---
            async function init() {
                salesData = await fetchSalesData();

                // Set default dates to last 30 days
                const today = new Date();
                const thirtyDaysAgo = new Date(today);
                thirtyDaysAgo.setDate(today.getDate() - 30);

                if (startDateInput) {
                    startDateInput.value = thirtyDaysAgo.toISOString().split('T')[0];
                }
                if (endDateInput) {
                    endDateInput.value = today.toISOString().split('T')[0];
                }

                renderSalesData(); // Render sales data on initial load
            }

            init(); 
        });
    </script>
</body>
</html>
