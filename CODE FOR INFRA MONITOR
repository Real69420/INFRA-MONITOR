import React, { useState } from "react";

function App() {
  const [infrastructure, setInfrastructure] = useState("");
  const [energyUsage, setEnergyUsage] = useState("");
  const [carbonOutput, setCarbonOutput] = useState("");
  const [suggestion, setSuggestion] = useState("");

  const handleAnalyze = () => {
    let suggestionText = "";
    if (parseInt(energyUsage) > 500 || parseInt(carbonOutput) > 300) {
      suggestionText =
        "⚠️ High energy or carbon output detected. Consider using renewable energy, optimizing operations, or switching to sustainable materials.";
    } else {
      suggestionText =
        "✅ Energy and carbon levels are within sustainable limits. Keep monitoring regularly!";
    }
    setSuggestion(suggestionText);
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-green-100 to-white p-8">
      <div className="max-w-4xl mx-auto bg-white rounded-3xl shadow-xl overflow-hidden">
        <div className="grid md:grid-cols-2">
          {/* Left Section */}
          <div className="bg-green-700 text-white p-8 flex flex-col justify-between">
            <div>
              <h1 className="text-4xl font-bold mb-4">🌱 Green Pune</h1>
              <p className="text-lg">
                Promote sustainable infrastructure by monitoring energy usage and
                carbon emissions in Pune's industrial zones.
              </p>
            </div>
            <div className="text-6xl text-white opacity-20 self-end">🌿</div>
          </div>

          {/* Right Section */}
          <div className="p-8 space-y-5">
            <input
              type="text"
              placeholder="Infrastructure name or location"
              className="w-full p-3 border rounded-md focus:ring-2 focus:ring-green-400"
              value={infrastructure}
              onChange={(e) => setInfrastructure(e.target.value)}
            />

            <input
              type="number"
              placeholder="Energy Usage (kWh)"
              className="w-full p-3 border rounded-md focus:ring-2 focus:ring-yellow-400"
              value={energyUsage}
              onChange={(e) => setEnergyUsage(e.target.value)}
            />

            <input
              type="number"
              placeholder="Carbon Output (kg CO₂)"
              className="w-full p-3 border rounded-md focus:ring-2 focus:ring-red-400"
              value={carbonOutput}
              onChange={(e) => setCarbonOutput(e.target.value)}
            />

            <button
              onClick={handleAnalyze}
              className="w-full bg-green-600 text-white p-3 rounded-md font-semibold hover:bg-green-700 transition"
            >
              Analyze Sustainability
            </button>

            {suggestion && (
              <div className="bg-green-50 border border-green-300 p-4 rounded-md text-green-800 text-sm mt-2">
                {suggestion}
              </div>
            )}
          </div>
        </div>
      </div>
    </div>
  );
}

export default App;
