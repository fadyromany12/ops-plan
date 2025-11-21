import React, { useState } from 'react';
import { Calendar, Users, BarChart3, ClipboardCheck, Trophy, Target, CheckCircle2, AlertTriangle, ShieldAlert } from 'lucide-react';

const App = () => {
  const [activeTab, setActiveTab] = useState('timeline');

  // --- DATA SECTIONS ---

  const timelineData = [
    {
      phase: "Phase 1: Foundation (NOW - Nov 30)",
      focus: "Stabilization & Documentation",
      tasks: [
        { task: "Build Master Performance Tracker (WBR View)", status: "Urgent", owner: "You", type: "Data" },
        { task: "Document 'Perfect Call' Flow (Standardize the 5 reps)", status: "Pending", owner: "You + Top Rep", type: "Process" },
        { task: "Create 'Cheat Sheets' for Objection Handling", status: "Done", owner: "You", type: "Sales" },
        { task: "Identify Top 2 Reps as 'Floor Walkers' for Dec Wave", status: "In Progress", owner: "You", type: "People" },
        { task: "Audit CRM Data Integrity (Clean junk leads before scaling)", status: "Urgent", owner: "You", type: "Ops" },
        { task: "Calibration Session with Client (Align on QA scoring)", status: "Pending", owner: "You", type: "Quality" }
      ]
    },
    {
      phase: "Phase 2: The Dec Wave (Dec 1 - Dec 31)",
      focus: "Scalability Proof of Concept",
      tasks: [
        { task: "IT Handshake: Verify Headsets/Licenses 48hrs prior", status: "Future", owner: "You + IT", type: "Ops" },
        { task: "Launch 'Buddy System' (New hires shadow your Top 5)", status: "Future", owner: "You", type: "People" },
        { task: "Daily 'War Room' Stand-up (15 mins - Blockers only)", status: "Future", owner: "You", type: "Ops" },
        { task: "Implement 'Red Flag' System (Day 3 Attrition check)", status: "Future", owner: "You", type: "HR" },
        { task: "Present 'Launch Success' Report to Client", status: "Critical", owner: "You", type: "Strategy" }
      ]
    },
    {
      phase: "Phase 3: Full Ops Mode (Jan 1 - Onwards)",
      focus: "Optimization & Consistency",
      tasks: [
        { task: "Implement formal PIP (Performance Improvement) process", status: "Future", owner: "You", type: "HR" },
        { task: "Forecast Q1 Hiring Needs vs Lead Flow", status: "Future", owner: "You", type: "Strategy" },
        { task: "Assume full financial reporting (Billable Hours/Margin)", status: "Goal", owner: "You", type: "Finance" }
      ]
    }
  ];

  const kpiData = [
    { metric: "Sales Conversion", goal: "15%+", freq: "Hourly", note: "The heartbeat. Monitor hourly to spot drifts." },
    { metric: "Lead Utilization", goal: "90%+", freq: "Daily", note: "Are we burning leads? (Called vs Answered vs Closed). Crucial for Ops efficiency." },
    { metric: "AHT (Handle Time)", goal: "< 450s", freq: "Daily", note: "Lower AHT = Higher Margin. Ops Managers obsess over this." },
    { metric: "Occupancy", goal: "85%", freq: "Daily", note: "% of time reps are actually working vs idle. Too high = burnout; Too low = waste." },
    { metric: "Attendance/Shrinkage", goal: "< 5%", freq: "Daily", note: "If heads aren't in seats, we lose money. Track strictly." },
    { metric: "Ramp Speed", goal: "2 Weeks", freq: "Per Wave", note: "Time to 80% quota. This is your 'Ops Superpower' metric." }
  ];

  const logisticsData = [
    { category: "Tech Readiness", item: "Are all Lenovo portal logins created & tested?", deadline: "T-minus 5 Days", check: false },
    { category: "Tech Readiness", item: "Do we have enough active CRM licenses?", deadline: "T-minus 5 Days", check: false },
    { category: "People", item: "Assign Seating Chart (Mix New Hires with Old)", deadline: "T-minus 2 Days", check: false },
    { category: "Training", item: "Print 'Battle Cards' (Product Specs/Pricing)", deadline: "T-minus 1 Day", check: false },
    { category: "Ops", item: "Create temporary 'Nesting' scorecard (lower targets)", deadline: "T-minus 3 Days", check: false },
    { category: "Access", item: "Building Access Cards for new wave requested?", deadline: "T-minus 7 Days", check: false },
  ];

  const riskData = [
    { risk: "System Outage/CRM Down", impact: "High", mitigation: "Create manual 'Downtime Trackers' (paper forms) so sales continue offline.", status: "Open" },
    { risk: "High Attrition in Dec Wave", impact: "High", mitigation: "Over-recruit by 10% to create a buffer. Implement 'Day 1' Welcome warm-up.", status: "Planned" },
    { risk: "Lead Source Dry Up", impact: "Critical", mitigation: "Flag lead volume trends to Client 2 weeks in advance. Request new data lists.", status: "Monitoring" },
    { risk: "Knowledge Gap (SME Burnout)", impact: "Medium", mitigation: "Rotate the 5 current reps on 'Floor Walking' shifts so they don't stop selling.", status: "Planned" }
  ];

  // --- RENDER HELPERS ---

  const renderTimeline = () => (
    <div className="space-y-6">
      <div className="bg-blue-50 border-l-4 border-blue-600 p-4 mb-6">
        <p className="text-blue-800 text-sm font-medium">
          <strong>Strategy:</strong> This timeline proves you aren't just reacting to the day, but planning for the quarter.
        </p>
      </div>
      {timelineData.map((phase, idx) => (
        <div key={idx} className="bg-white border rounded-lg shadow-sm overflow-hidden">
          <div className="bg-slate-100 px-4 py-3 border-b flex justify-between items-center">
            <h3 className="font-bold text-slate-700">{phase.phase}</h3>
            <span className="text-xs font-bold px-2 py-1 bg-slate-200 text-slate-600 rounded uppercase">{phase.focus}</span>
          </div>
          <table className="w-full text-sm text-left">
            <thead className="bg-slate-50 text-slate-500">
              <tr>
                <th className="px-4 py-2">Task</th>
                <th className="px-4 py-2">Type</th>
                <th className="px-4 py-2">Owner</th>
                <th className="px-4 py-2">Status</th>
              </tr>
            </thead>
            <tbody className="divide-y divide-slate-100">
              {phase.tasks.map((t, i) => (
                <tr key={i}>
                  <td className="px-4 py-3 font-medium text-slate-700">{t.task}</td>
                  <td className="px-4 py-3">
                    <span className="text-xs bg-slate-100 text-slate-500 px-2 py-1 rounded border">
                      {t.type}
                    </span>
                  </td>
                  <td className="px-4 py-3 text-slate-500">{t.owner}</td>
                  <td className="px-4 py-3">
                    <span className={`px-2 py-1 rounded-full text-xs font-bold ${
                      t.status === 'Urgent' || t.status === 'Critical' ? 'bg-red-100 text-red-700' :
                      t.status === 'Future' ? 'bg-purple-100 text-purple-700' : 
                      t.status === 'Done' ? 'bg-green-100 text-green-700' :
                      'bg-amber-100 text-amber-700'
                    }`}>
                      {t.status}
                    </span>
                  </td>
                </tr>
              ))}
            </tbody>
          </table>
        </div>
      ))}
    </div>
  );

  const renderKPIs = () => (
    <div>
      <div className="bg-green-50 border-l-4 border-green-600 p-4 mb-6">
        <p className="text-green-800 text-sm font-medium">
          <strong>The "Ops" Dashboard:</strong> Don't just track these. Send a summary of these to your boss every Friday at 2 PM.
        </p>
      </div>
      <div className="grid gap-4">
        <table className="w-full text-sm text-left border rounded-lg overflow-hidden">
          <thead className="bg-slate-800 text-white">
            <tr>
              <th className="px-4 py-3">Metric Name</th>
              <th className="px-4 py-3">Target Goal</th>
              <th className="px-4 py-3">Frequency</th>
              <th className="px-4 py-3">Why Ops Managers Care</th>
            </tr>
          </thead>
          <tbody className="divide-y divide-slate-200 bg-white">
            {kpiData.map((k, i) => (
              <tr key={i} className="hover:bg-slate-50">
                <td className="px-4 py-3 font-bold text-slate-700">{k.metric}</td>
                <td className="px-4 py-3 font-mono text-blue-600 font-bold">{k.goal}</td>
                <td className="px-4 py-3 text-slate-500">{k.freq}</td>
                <td className="px-4 py-3 text-slate-600 italic">{k.note}</td>
              </tr>
            ))}
          </tbody>
        </table>
      </div>
    </div>
  );

  const renderRisks = () => (
    <div>
      <div className="bg-red-50 border-l-4 border-red-600 p-4 mb-6">
        <p className="text-red-800 text-sm font-medium">
          <strong>Risk Register:</strong> Showing you anticipate problems *before* they happen is the hallmark of a Senior Ops Manager.
        </p>
      </div>
      <div className="grid gap-4 grid-cols-1 md:grid-cols-2">
        {riskData.map((r, i) => (
           <div key={i} className="bg-white p-4 rounded-lg border border-slate-200 shadow-sm flex flex-col justify-between">
             <div>
               <div className="flex justify-between items-start mb-2">
                 <h4 className="font-bold text-slate-800 flex items-center gap-2">
                   <AlertTriangle className="w-4 h-4 text-amber-500" />
                   {r.risk}
                 </h4>
                 <span className={`text-xs font-bold px-2 py-1 rounded uppercase ${r.impact === 'Critical' || r.impact === 'High' ? 'bg-red-100 text-red-700' : 'bg-amber-100 text-amber-800'}`}>
                   {r.impact}
                 </span>
               </div>
               <p className="text-sm text-slate-600 mb-3">
                 <strong>Mitigation:</strong> {r.mitigation}
               </p>
             </div>
             <div className="mt-2 pt-2 border-t text-xs text-slate-400 font-medium">
               Status: {r.status}
             </div>
           </div>
        ))}
      </div>
    </div>
  );

  const renderLogistics = () => (
    <div>
       <div className="bg-amber-50 border-l-4 border-amber-600 p-4 mb-6">
        <p className="text-amber-800 text-sm font-medium">
          <strong>Wave Readiness:</strong> This is where you win the job. If the December wave starts smoothly because of you, you are the Ops Manager.
        </p>
      </div>
      <div className="bg-white rounded-lg border shadow-sm">
        <table className="w-full text-sm text-left">
          <thead className="bg-slate-100 text-slate-600 uppercase text-xs">
            <tr>
              <th className="px-4 py-3">Category</th>
              <th className="px-4 py-3">Verification Item</th>
              <th className="px-4 py-3">Deadline</th>
              <th className="px-4 py-3 text-center">Done?</th>
            </tr>
          </thead>
          <tbody className="divide-y divide-slate-100">
            {logisticsData.map((item, i) => (
              <tr key={i}>
                <td className="px-4 py-3 font-bold text-slate-500">{item.category}</td>
                <td className="px-4 py-3">{item.item}</td>
                <td className="px-4 py-3 text-red-600 font-medium">{item.deadline}</td>
                <td className="px-4 py-3 text-center">
                  <input type="checkbox" className="w-5 h-5 text-blue-600 rounded focus:ring-blue-500 border-gray-300" />
                </td>
              </tr>
            ))}
          </tbody>
        </table>
      </div>
    </div>
  );

  const renderGovernance = () => (
    <div className="space-y-6">
      <div className="p-6 bg-white rounded-lg border shadow-sm">
        <h3 className="text-lg font-bold text-slate-800 mb-4 flex items-center">
          <ClipboardCheck className="w-5 h-5 mr-2 text-red-600" />
          The "S.O.P." Library
        </h3>
        <p className="text-slate-600 mb-4 text-sm">
          Create these 4 documents immediately. Store them in a shared folder and send the link to your Director.
        </p>
        <ul className="space-y-3">
          <li className="flex items-start p-3 bg-slate-50 rounded">
            <CheckCircle2 className="w-5 h-5 text-green-500 mr-3 mt-0.5 flex-shrink-0" />
            <div>
              <span className="font-bold text-slate-700">The Attendance Policy</span>
              <p className="text-xs text-slate-500 mt-1">Exactly what happens when someone is late? (Verbal → Written → Final). Don't make it up as you go.</p>
            </div>
          </li>
          <li className="flex items-start p-3 bg-slate-50 rounded">
            <CheckCircle2 className="w-5 h-5 text-green-500 mr-3 mt-0.5 flex-shrink-0" />
            <div>
              <span className="font-bold text-slate-700">The End-of-Day (EOD) Report Format</span>
              <p className="text-xs text-slate-500 mt-1">A standard template all reps (and you) fill out daily: Calls Made, Sales Closed, Blockers.</p>
            </div>
          </li>
          <li className="flex items-start p-3 bg-slate-50 rounded">
            <CheckCircle2 className="w-5 h-5 text-green-500 mr-3 mt-0.5 flex-shrink-0" />
            <div>
              <span className="font-bold text-slate-700">The Escalation Matrix</span>
              <p className="text-xs text-slate-500 mt-1">Who do we call when the internet dies? Who do we call when a customer asks for legal? Write it down.</p>
            </div>
          </li>
          <li className="flex items-start p-3 bg-slate-50 rounded">
            <CheckCircle2 className="w-5 h-5 text-green-500 mr-3 mt-0.5 flex-shrink-0" />
            <div>
              <span className="font-bold text-slate-700">The Q1 Forecast</span>
              <p className="text-xs text-slate-500 mt-1">A simple Excel sheet predicting performance for Jan/Feb/Mar based on hiring numbers.</p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  );

  return (
    <div className="min-h-screen bg-slate-50 p-4 md:p-8 font-sans text-slate-900">
      {/* Header */}
      <header className="max-w-5xl mx-auto mb-8 bg-gradient-to-r from-red-600 to-slate-900 text-white rounded-xl p-6 shadow-lg">
        <div className="flex flex-col md:flex-row md:items-center justify-between">
          <div>
            <h1 className="text-2xl font-bold flex items-center gap-2">
              <Trophy className="w-6 h-6 text-yellow-400" />
              Project: Ops Ascension
            </h1>
            <p className="text-red-100 mt-1">Lenovo Account • Launch Phase • Dec/Jan Wave Prep</p>
          </div>
          <div className="mt-4 md:mt-0 bg-white/10 backdrop-blur-sm px-4 py-2 rounded-lg">
            <p className="text-xs text-red-100 uppercase tracking-wider">Current Focus</p>
            <p className="font-bold">Stabilize & Scale</p>
          </div>
        </div>
      </header>

      {/* Main Content */}
      <main className="max-w-5xl mx-auto bg-white rounded-xl shadow-xl overflow-hidden min-h-[600px] flex flex-col md:flex-row">
        
        {/* Sidebar Navigation */}
        <nav className="w-full md:w-64 bg-slate-100 border-r p-4 flex flex-row md:flex-col gap-2 overflow-x-auto">
          <button 
            onClick={() => setActiveTab('timeline')}
            className={`flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium transition-all ${activeTab === 'timeline' ? 'bg-white text-red-600 shadow-md' : 'text-slate-500 hover:bg-slate-200'}`}
          >
            <Calendar className="w-4 h-4" /> Timeline (Nov-Jan)
          </button>
          <button 
            onClick={() => setActiveTab('kpi')}
            className={`flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium transition-all ${activeTab === 'kpi' ? 'bg-white text-red-600 shadow-md' : 'text-slate-500 hover:bg-slate-200'}`}
          >
            <BarChart3 className="w-4 h-4" /> KPI Dashboard
          </button>
          <button 
            onClick={() => setActiveTab('logistics')}
            className={`flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium transition-all ${activeTab === 'logistics' ? 'bg-white text-red-600 shadow-md' : 'text-slate-500 hover:bg-slate-200'}`}
          >
            <Users className="w-4 h-4" /> Wave Logistics
          </button>
          <button 
            onClick={() => setActiveTab('risks')}
            className={`flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium transition-all ${activeTab === 'risks' ? 'bg-white text-red-600 shadow-md' : 'text-slate-500 hover:bg-slate-200'}`}
          >
            <ShieldAlert className="w-4 h-4" /> Risk Register
          </button>
          <button 
            onClick={() => setActiveTab('governance')}
            className={`flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium transition-all ${activeTab === 'governance' ? 'bg-white text-red-600 shadow-md' : 'text-slate-500 hover:bg-slate-200'}`}
          >
            <ClipboardCheck className="w-4 h-4" /> Process & SOPs
          </button>
        </nav>

        {/* Tab Content */}
        <div className="flex-1 p-6 md:p-8 overflow-y-auto">
          {activeTab === 'timeline' && renderTimeline()}
          {activeTab === 'kpi' && renderKPIs()}
          {activeTab === 'logistics' && renderLogistics()}
          {activeTab === 'governance' && renderGovernance()}
          {activeTab === 'risks' && renderRisks()}
        </div>

      </main>

      {/* Footer Tip */}
      <div className="max-w-5xl mx-auto mt-6 p-4 bg-blue-50 rounded-lg border border-blue-100 flex items-start gap-3">
        <Target className="w-6 h-6 text-blue-600 flex-shrink-0" />
        <div>
          <h4 className="font-bold text-blue-800 text-sm">Pro-Tip for Promotion:</h4>
          <p className="text-blue-700 text-sm mt-1">
            Ops Managers solve problems before they happen. When you present this plan to your boss, don't say "Here is what I think." Say: 
            <span className="italic font-semibold"> "Here is the infrastructure I have built to ensure the December wave hits 100% of their target by Week 3."</span>
          </p>
        </div>
      </div>
    </div>
  );
};

export default App;
