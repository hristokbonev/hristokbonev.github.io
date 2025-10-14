<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>MagiDict Benchmark Results</title>

    <!-- React + ReactDOM -->
    <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>

    <!-- Babel (to interpret JSX in-browser) -->
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

    <!-- Recharts -->
    <script src="https://unpkg.com/recharts/umd/Recharts.min.js"></script>

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
  </head>

  <body class="bg-gray-900 text-white">
    <div id="root"></div>

    <script type="text/babel">
      const { useState } = React;
      const {
        BarChart, Bar, XAxis, YAxis, CartesianGrid,
        Tooltip, Legend, ResponsiveContainer,
        RadarChart, PolarGrid, PolarAngleAxis, PolarRadiusAxis, Radar
      } = Recharts;

      const BenchmarkCharts = () => {
        const [activeTab, setActiveTab] = useState('basic');

        const basicOpsData = [
          { operation: 'Contains', MagiDict: 112.50, Box: 463.73, DotMap: 205.70, Addict: 112.53 },
          { operation: 'Get Method', MagiDict: 153.25, Box: 770.52, DotMap: 249.78, Addict: 160.97 },
          { operation: 'Bracket Access', MagiDict: 546.54, Box: 802.42, DotMap: 440.67, Addict: 150.48 },
        ];

        const accessData = [
          { operation: 'Basic Access', MagiDict: 2864.83, Box: 2794.29, DotMap: 4746.58, Addict: 1820.58 },
          { operation: 'List Access', MagiDict: 2032.07, Box: 2399.41, DotMap: 3373.72, Addict: 1422.04 },
          { operation: 'Missing Key', MagiDict: 10425.85, Box: 5509.24, DotMap: 7789.80, Addict: 8488.66 },
        ];

        const initData = [
          { type: 'Standard', MagiDict: 56.80, Box: 869.70, DotMap: 867.85, Addict: 334.29 },
          { type: 'Deep Nested', MagiDict: 85.31, Box: 196.78, DotMap: 72.17, Addict: 39.91 },
          { type: 'Wide (1000 keys)', MagiDict: 10956.61, Box: 22336.51, DotMap: 8666.48, Addict: 5324.99 },
        ];

        const conversionData = [
          { operation: 'To Dict', MagiDict: 261.77, Box: 134.91, DotMap: 173.14, Addict: 225.82 },
          { operation: 'Deep Copy', MagiDict: 272.41, Box: 2408.81, DotMap: 423.78, Addict: 431.09 },
          { operation: 'Copy', MagiDict: 29.69, Box: 48.52, DotMap: 412.56, Addict: 13.31 },
        ];

        const iterationData = [
          { operation: 'List Iteration', MagiDict: 91.68, Box: 85.85, DotMap: 150.96, Addict: 58.80 },
          { operation: 'Keys', MagiDict: 2.27, Box: 'N/A', DotMap: 'N/A', Addict: 'N/A' },
          { operation: 'Values', MagiDict: 2.27, Box: 'N/A', DotMap: 'N/A', Addict: 'N/A' },
          { operation: 'Items', MagiDict: 2.42, Box: 'N/A', DotMap: 'N/A', Addict: 'N/A' },
        ];

        const updateData = [
          { operation: 'Single Update', MagiDict: 32.18, Box: 50.64, DotMap: 426.72, Addict: 337.63 },
          { operation: 'Bulk Update', MagiDict: 44.24, Box: 55.37, DotMap: 'N/A', Addict: 'N/A' },
          { operation: 'Setdefault', MagiDict: 37.32, Box: 64.05, DotMap: 'N/A', Addict: 'N/A' },
        ];

        const radarData = [
          { category: 'Basic Ops', MagiDict: 95, Box: 60, DotMap: 80, Addict: 95 },
          { category: 'Access Speed', MagiDict: 85, Box: 90, DotMap: 65, Addict: 95 },
          { category: 'Init Speed', MagiDict: 80, Box: 40, DotMap: 45, Addict: 90 },
          { category: 'Safety', MagiDict: 100, Box: 60, DotMap: 50, Addict: 80 },
          { category: 'Features', MagiDict: 100, Box: 70, DotMap: 60, Addict: 70 },
          { category: 'Memory', MagiDict: 85, Box: 70, DotMap: 80, Addict: 90 },
        ];

        const CustomTooltip = ({ active, payload, label }) => {
          if (active && payload && payload.length) {
            return (
              <div className="bg-gray-900 border border-gray-700 p-3 rounded-lg shadow-xl">
                <p className="text-white font-semibold mb-2">{label}</p>
                {payload.map((entry, index) => (
                  <p key={index} style={{ color: entry.color }} className="text-sm">
                    {entry.name}: {typeof entry.value === 'number' ? entry.value.toFixed(2) : entry.value}
                  </p>
                ))}
              </div>
            );
          }
          return null;
        };

        const tabs = [
          { id: 'basic', label: 'Basic Operations', data: basicOpsData },
          { id: 'access', label: 'Access Patterns', data: accessData },
          { id: 'init', label: 'Initialization', data: initData },
          { id: 'conversion', label: 'Conversions', data: conversionData },
          { id: 'iteration', label: 'Iterations', data: iterationData },
          { id: 'update', label: 'Updates', data: updateData },
          { id: 'radar', label: 'Overall', data: radarData },
        ];

        const renderChart = () => {
          if (activeTab === 'radar') {
            return (
              <ResponsiveContainer width="100%" height={500}>
                <RadarChart data={radarData}>
                  <PolarGrid stroke="#374151" />
                  <PolarAngleAxis dataKey="category" stroke="#9CA3AF" />
                  <PolarRadiusAxis angle={90} domain={[0, 100]} stroke="#9CA3AF" />
                  <Radar name="MagiDict" dataKey="MagiDict" stroke="#8B5CF6" fill="#8B5CF6" fillOpacity={0.6} />
                  <Radar name="Box" dataKey="Box" stroke="#EF4444" fill="#EF4444" fillOpacity={0.3} />
                  <Radar name="DotMap" dataKey="DotMap" stroke="#F59E0B" fill="#F59E0B" fillOpacity={0.3} />
                  <Radar name="Addict" dataKey="Addict" stroke="#10B981" fill="#10B981" fillOpacity={0.3} />
                  <Legend />
                  <Tooltip content={<CustomTooltip />} />
                </RadarChart>
              </ResponsiveContainer>
            );
          }

          const currentTab = tabs.find(t => t.id === activeTab);
          return (
            <ResponsiveContainer width="100%" height={400}>
              <BarChart data={currentTab.data}>
                <CartesianGrid strokeDasharray="3 3" stroke="#374151" />
                <XAxis dataKey={activeTab === 'init' ? 'type' : 'operation'} stroke="#9CA3AF" />
                <YAxis stroke="#9CA3AF" />
                <Tooltip content={<CustomTooltip />} />
                <Legend />
                <Bar dataKey="MagiDict" fill="#8B5CF6" />
                <Bar dataKey="Box" fill="#EF4444" />
                <Bar dataKey="DotMap" fill="#F59E0B" />
                <Bar dataKey="Addict" fill="#10B981" />
              </BarChart>
            </ResponsiveContainer>
          );
        };

        return (
          <div className="min-h-screen bg-gradient-to-br from-gray-900 via-purple-900 to-gray-900 p-8">
            <div className="max-w-7xl mx-auto">
              <div className="text-center mb-8">
                <h1 className="text-5xl font-bold text-white mb-4">✨ MagiDict Benchmark Results</h1>
                <p className="text-gray-300 text-lg">Performance comparison across different dict-like libraries</p>
              </div>

              <div className="flex flex-wrap justify-center gap-2 mb-8">
                {tabs.map((tab) => (
                  <button
                    key={tab.id}
                    onClick={() => setActiveTab(tab.id)}
                    className={`px-6 py-3 rounded-lg font-semibold transition-all ${
                      activeTab === tab.id
                        ? 'bg-purple-600 text-white shadow-lg scale-105'
                        : 'bg-gray-800 text-gray-300 hover:bg-gray-700'
                    }`}
                  >
                    {tab.label}
                  </button>
                ))}
              </div>

              <div className="bg-gray-800 rounded-xl shadow-2xl p-8">
                {renderChart()}
              </div>
            </div>
          </div>
        );
      };

      const root = ReactDOM.createRoot(document.getElementById('root'));
      root.render(<BenchmarkCharts />);
    </script>
  </body>
</html>
