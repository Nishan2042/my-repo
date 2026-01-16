import React, { useState } from 'react';
import { Calendar, Plus, TrendingUp, Users, Clock, Activity, X, AlertCircle, Check } from 'lucide-react';

const PTOTracker = () => {
  const [employees, setEmployees] = useState([
    { 
      id: 1, 
      name: 'Sarah Johnson', 
      department: 'Engineering',
      ptoTotal: 15,
      ptoUsed: 7,
      sickTotal: 10,
      sickUsed: 2,
      requests: []
    },
    { 
      id: 2, 
      name: 'Mike Chen', 
      department: 'Marketing',
      ptoTotal: 15,
      ptoUsed: 3,
      sickTotal: 10,
      sickUsed: 5,
      requests: []
    },
    { 
      id: 3, 
      name: 'Emily Rodriguez', 
      department: 'Sales',
      ptoTotal: 20,
      ptoUsed: 12,
      sickTotal: 10,
      sickUsed: 1,
      requests: []
    },
    { 
      id: 4, 
      name: 'James Wilson', 
      department: 'Engineering',
      ptoTotal: 15,
      ptoUsed: 8,
      sickTotal: 10,
      sickUsed: 3,
      requests: []
    },
    { 
      id: 5, 
      name: 'Lisa Patel', 
      department: 'HR',
      ptoTotal: 20,
      ptoUsed: 5,
      sickTotal: 10,
      sickUsed: 0,
      requests: []
    },
  ]);

  const [leaveRequests, setLeaveRequests] = useState([
    { id: 1, employeeId: 1, employeeName: 'Sarah Johnson', type: 'PTO', startDate: '2025-01-15', endDate: '2025-01-17', days: 3, status: 'pending', reason: 'Family vacation' },
    { id: 2, employeeId: 2, employeeName: 'Mike Chen', type: 'Sick', startDate: '2025-01-10', endDate: '2025-01-10', days: 1, status: 'approved', reason: 'Medical appointment' },
    { id: 3, employeeId: 3, employeeName: 'Emily Rodriguez', type: 'PTO', startDate: '2025-02-01', endDate: '2025-02-05', days: 5, status: 'pending', reason: 'Beach vacation' },
  ]);

  const [activeTab, setActiveTab] = useState('overview');
  const [showAddModal, setShowAddModal] = useState(false);
  const [showRequestModal, setShowRequestModal] = useState(false);
  const [selectedEmployee, setSelectedEmployee] = useState(null);
  const [newEmployee, setNewEmployee] = useState({
    name: '',
    department: 'Engineering',
    ptoTotal: 15,
    sickTotal: 10
  });
  const [newRequest, setNewRequest] = useState({
    employeeId: '',
    type: 'PTO',
    startDate: '',
    endDate: '',
    reason: ''
  });

  const departments = ['Engineering', 'Marketing', 'Sales', 'HR', 'Finance', 'Operations'];

  const calculateDays = (start, end) => {
    const startDate = new Date(start);
    const endDate = new Date(end);
    const diffTime = Math.abs(endDate - startDate);
    const diffDays = Math.ceil(diffTime / (1000 * 60 * 60 * 24)) + 1;
    return diffDays;
  };

  const handleAddEmployee = () => {
    if (newEmployee.name) {
      setEmployees([...employees, {
        ...newEmployee,
        id: Date.now(),
        ptoUsed: 0,
        sickUsed: 0,
        requests: []
      }]);
      setNewEmployee({ name: '', department: 'Engineering', ptoTotal: 15, sickTotal: 10 });
      setShowAddModal(false);
    }
  };

  const handleSubmitRequest = () => {
    if (newRequest.employeeId && newRequest.startDate && newRequest.endDate) {
      const employee = employees.find(e => e.id === parseInt(newRequest.employeeId));
      const days = calculateDays(newRequest.startDate, newRequest.endDate);
      
      const request = {
        id: Date.now(),
        employeeId: employee.id,
        employeeName: employee.name,
        type: newRequest.type,
        startDate: newRequest.startDate,
        endDate: newRequest.endDate,
        days: days,
        status: 'pending',
        reason: newRequest.reason
      };

      setLeaveRequests([...leaveRequests, request]);
      setNewRequest({ employeeId: '', type: 'PTO', startDate: '', endDate: '', reason: '' });
      setShowRequestModal(false);
    }
  };

  const handleApproveRequest = (requestId) => {
    const request = leaveRequests.find(r => r.id === requestId);
    if (request) {
      setEmployees(employees.map(emp => {
        if (emp.id === request.employeeId) {
          if (request.type === 'PTO') {
            return { ...emp, ptoUsed: emp.ptoUsed + request.days };
          } else {
            return { ...emp, sickUsed: emp.sickUsed + request.days };
          }
        }
        return emp;
      }));

      setLeaveRequests(leaveRequests.map(req => 
        req.id === requestId ? { ...req, status: 'approved' } : req
      ));
    }
  };

  const handleDenyRequest = (requestId) => {
    setLeaveRequests(leaveRequests.map(req => 
      req.id === requestId ? { ...req, status: 'denied' } : req
    ));
  };

  const getUtilizationRate = (employee) => {
    const totalAvailable = employee.ptoTotal + employee.sickTotal;
    const totalUsed = employee.ptoUsed + employee.sickUsed;
    return ((totalUsed / totalAvailable) * 100).toFixed(0);
  };

  const getTotalStats = () => {
    const totalPTO = employees.reduce((sum, emp) => sum + emp.ptoTotal, 0);
    const totalPTOUsed = employees.reduce((sum, emp) => sum + emp.ptoUsed, 0);
    const totalSick = employees.reduce((sum, emp) => sum + emp.sickTotal, 0);
    const totalSickUsed = employees.reduce((sum, emp) => sum + emp.sickUsed, 0);
    
    return {
      totalPTO,
      totalPTOUsed,
      totalSick,
      totalSickUsed,
      ptoUtilization: ((totalPTOUsed / totalPTO) * 100).toFixed(0),
      sickUtilization: ((totalSickUsed / totalSick) * 100).toFixed(0)
    };
  };

  const stats = getTotalStats();

  return (
    <div className="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-50 p-4">
      <div className="max-w-7xl mx-auto">
        {/* Header */}
        <div className="bg-white rounded-2xl shadow-xl p-6 mb-6">
          <div className="flex items-center justify-between mb-6">
            <div className="flex items-center gap-3">
              <Calendar className="w-8 h-8 text-blue-600" />
              <h1 className="text-3xl font-bold text-gray-800">PTO & Sick Leave Tracker</h1>
            </div>
            <div className="flex gap-3">
              <button 
                onClick={() => setShowRequestModal(true)}
                className="bg-blue-600 text-white rounded-lg px-4 py-2 hover:bg-blue-700 transition flex items-center gap-2"
              >
                <Plus className="w-5 h-5" />
                New Request
              </button>
              <button 
                onClick={() => setShowAddModal(true)}
                className="bg-indigo-600 text-white rounded-lg px-4 py-2 hover:bg-indigo-700 transition flex items-center gap-2"
              >
                <Users className="w-5 h-5" />
                Add Employee
              </button>
            </div>
          </div>

          {/* Stats Cards */}
          <div className="grid grid-cols-4 gap-4">
            <div className="bg-gradient-to-br from-blue-50 to-blue-100 rounded-xl p-4">
              <div className="flex items-center gap-2 mb-2">
                <Users className="w-5 h-5 text-blue-600" />
                <p className="text-sm text-gray-600">Total Employees</p>
              </div>
              <p className="text-3xl font-bold text-blue-700">{employees.length}</p>
            </div>
            <div className="bg-gradient-to-br from-green-50 to-green-100 rounded-xl p-4">
              <div className="flex items-center gap-2 mb-2">
                <Activity className="w-5 h-5 text-green-600" />
                <p className="text-sm text-gray-600">PTO Utilization</p>
              </div>
              <p className="text-3xl font-bold text-green-700">{stats.ptoUtilization}%</p>
            </div>
            <div className="bg-gradient-to-br from-orange-50 to-orange-100 rounded-xl p-4">
              <div className="flex items-center gap-2 mb-2">
                <AlertCircle className="w-5 h-5 text-orange-600" />
                <p className="text-sm text-gray-600">Sick Leave Used</p>
              </div>
              <p className="text-3xl font-bold text-orange-700">{stats.totalSickUsed}/{stats.totalSick}</p>
            </div>
            <div className="bg-gradient-to-br from-purple-50 to-purple-100 rounded-xl p-4">
              <div className="flex items-center gap-2 mb-2">
                <Clock className="w-5 h-5 text-purple-600" />
                <p className="text-sm text-gray-600">Pending Requests</p>
              </div>
              <p className="text-3xl font-bold text-purple-700">
                {leaveRequests.filter(r => r.status === 'pending').length}
              </p>
            </div>
          </div>
        </div>

        {/* Tabs */}
        <div className="bg-white rounded-2xl shadow-xl overflow-hidden">
          <div className="flex border-b">
            <button 
              onClick={() => setActiveTab('overview')}
              className={`flex-1 p-4 font-medium transition ${activeTab === 'overview' ? 'bg-blue-50 text-blue-700 border-b-2 border-blue-600' : 'text-gray-600 hover:bg-gray-50'}`}
            >
              <Users className="w-5 h-5 inline mr-2" />
              Employee Overview
            </button>
            <button 
              onClick={() => setActiveTab('requests')}
              className={`flex-1 p-4 font-medium transition ${activeTab === 'requests' ? 'bg-blue-50 text-blue-700 border-b-2 border-blue-600' : 'text-gray-600 hover:bg-gray-50'}`}
            >
              <Clock className="w-5 h-5 inline mr-2" />
              Leave Requests
            </button>
            <button 
              onClick={() => setActiveTab('analytics')}
              className={`flex-1 p-4 font-medium transition ${activeTab === 'analytics' ? 'bg-blue-50 text-blue-700 border-b-2 border-blue-600' : 'text-gray-600 hover:bg-gray-50'}`}
            >
              <TrendingUp className="w-5 h-5 inline mr-2" />
              Analytics
            </button>
          </div>

          <div className="p-6">
            {activeTab === 'overview' && (
              <div className="space-y-4">
                {employees.map(employee => (
                  <div key={employee.id} className="bg-gray-50 rounded-xl p-5 hover:shadow-md transition">
                    <div className="flex items-start justify-between mb-4">
                      <div>
                        <h3 className="text-lg font-semibold text-gray-800">{employee.name}</h3>
                        <p className="text-sm text-gray-500">{employee.department}</p>
                      </div>
                      <div className="text-right">
                        <p className="text-xs text-gray-500">Overall Utilization</p>
                        <p className="text-2xl font-bold text-blue-600">{getUtilizationRate(employee)}%</p>
                      </div>
                    </div>

                    <div className="grid grid-cols-2 gap-4">
                      {/* PTO */}
                      <div className="bg-white rounded-lg p-4">
                        <div className="flex items-center justify-between mb-2">
                          <p className="text-sm font-medium text-gray-700">PTO Days</p>
                          <span className="text-xs text-blue-600 font-semibold">
                            {employee.ptoTotal - employee.ptoUsed} remaining
                          </span>
                        </div>
                        <div className="flex items-center gap-2 mb-2">
                          <div className="flex-1 bg-gray-200 rounded-full h-2">
                            <div 
                              className="bg-blue-500 h-2 rounded-full transition-all"
                              style={{ width: `${(employee.ptoUsed / employee.ptoTotal) * 100}%` }}
                            ></div>
                          </div>
                        </div>
                        <p className="text-xs text-gray-600">
                          {employee.ptoUsed} used of {employee.ptoTotal} days
                        </p>
                      </div>

                      {/* Sick Leave */}
                      <div className="bg-white rounded-lg p-4">
                        <div className="flex items-center justify-between mb-2">
                          <p className="text-sm font-medium text-gray-700">Sick Leave</p>
                          <span className="text-xs text-orange-600 font-semibold">
                            {employee.sickTotal - employee.sickUsed} remaining
                          </span>
                        </div>
                        <div className="flex items-center gap-2 mb-2">
                          <div className="flex-1 bg-gray-200 rounded-full h-2">
                            <div 
                              className="bg-orange-500 h-2 rounded-full transition-all"
                              style={{ width: `${(employee.sickUsed / employee.sickTotal) * 100}%` }}
                            ></div>
                          </div>
                        </div>
                        <p className="text-xs text-gray-600">
                          {employee.sickUsed} used of {employee.sickTotal} days
                        </p>
                      </div>
                    </div>
                  </div>
                ))}
              </div>
            )}

            {activeTab === 'requests' && (
              <div className="space-y-4">
                {leaveRequests.map(request => (
                  <div key={request.id} className="bg-gray-50 rounded-xl p-5">
                    <div className="flex items-start justify-between">
                      <div className="flex-1">
                        <div className="flex items-center gap-3 mb-2">
                          <h3 className="text-lg font-semibold text-gray-800">{request.employeeName}</h3>
                          <span className={`px-3 py-1 rounded-full text-xs font-semibold ${
                            request.type === 'PTO' ? 'bg-blue-100 text-blue-700' : 'bg-orange-100 text-orange-700'
                          }`}>
                            {request.type}
                          </span>
                          <span className={`px-3 py-1 rounded-full text-xs font-semibold ${
                            request.status === 'pending' ? 'bg-yellow-100 text-yellow-700' :
                            request.status === 'approved' ? 'bg-green-100 text-green-700' :
                            'bg-red-100 text-red-700'
                          }`}>
                            {request.status.toUpperCase()}
                          </span>
                        </div>
                        <div className="space-y-1 text-sm text-gray-600">
                          <p><strong>Dates:</strong> {request.startDate} to {request.endDate} ({request.days} days)</p>
                          {request.reason && <p><strong>Reason:</strong> {request.reason}</p>}
                        </div>
                      </div>
                      {request.status === 'pending' && (
                        <div className="flex gap-2">
                          <button 
                            onClick={() => handleApproveRequest(request.id)}
                            className="bg-green-500 text-white rounded-lg px-4 py-2 hover:bg-green-600 transition flex items-center gap-2"
                          >
                            <Check className="w-4 h-4" />
                            Approve
                          </button>
                          <button 
                            onClick={() => handleDenyRequest(request.id)}
                            className="bg-red-500 text-white rounded-lg px-4 py-2 hover:bg-red-600 transition flex items-center gap-2"
                          >
                            <X className="w-4 h-4" />
                            Deny
                          </button>
                        </div>
                      )}
                    </div>
                  </div>
                ))}
                {leaveRequests.length === 0 && (
                  <div className="text-center py-12 text-gray-400">
                    <Clock className="w-16 h-16 mx-auto mb-4 opacity-50" />
                    <p>No leave requests yet.</p>
                  </div>
                )}
              </div>
            )}

            {activeTab === 'analytics' && (
              <div className="space-y-6">
                <div className="bg-gradient-to-r from-blue-50 to-indigo-50 rounded-xl p-6">
                  <h3 className="text-xl font-semibold mb-4 text-gray-800">Department Breakdown</h3>
                  {departments.map(dept => {
                    const deptEmployees = employees.filter(e => e.department === dept);
                    const deptPTOUsed = deptEmployees.reduce((sum, e) => sum + e.ptoUsed, 0);
                    const deptPTOTotal = deptEmployees.reduce((sum, e) => sum + e.ptoTotal, 0);
                    
                    if (deptEmployees.length === 0) return null;
                    
                    return (
                      <div key={dept} className="mb-4">
                        <div className="flex items-center justify-between mb-2">
                          <span className="font-medium text-gray-700">{dept}</span>
                          <span className="text-sm text-gray-600">
                            {deptEmployees.length} employees • {deptPTOUsed}/{deptPTOTotal} PTO days used
                          </span>
                        </div>
                        <div className="bg-white rounded-full h-3 overflow-hidden">
                          <div 
                            className="bg-gradient-to-r from-blue-500 to-indigo-500 h-3 transition-all"
                            style={{ width: `${(deptPTOUsed / deptPTOTotal) * 100}%` }}
                          ></div>
                        </div>
                      </div>
                    );
                  })}
                </div>

                <div className="grid grid-cols-2 gap-4">
                  <div className="bg-green-50 rounded-xl p-6">
                    <h4 className="font-semibold text-gray-700 mb-2">Top PTO Users</h4>
                    {employees
                      .sort((a, b) => b.ptoUsed - a.ptoUsed)
                      .slice(0, 3)
                      .map((emp, idx) => (
                        <div key={emp.id} className="flex items-center justify-between py-2">
                          <span className="text-gray-700">#{idx + 1} {emp.name}</span>
                          <span className="font-semibold text-green-700">{emp.ptoUsed} days</span>
                        </div>
                      ))}
                  </div>
                  <div className="bg-orange-50 rounded-xl p-6">
                    <h4 className="font-semibold text-gray-700 mb-2">Most Sick Days</h4>
                    {employees
                      .sort((a, b) => b.sickUsed - a.sickUsed)
                      .slice(0, 3)
                      .map((emp, idx) => (
                        <div key={emp.id} className="flex items-center justify-between py-2">
                          <span className="text-gray-700">#{idx + 1} {emp.name}</span>
                          <span className="font-semibold text-orange-700">{emp.sickUsed} days</span>
                        </div>
                      ))}
                  </div>
                </div>
              </div>
            )}
          </div>
        </div>

        {/* Add Employee Modal */}
        {showAddModal && (
          <div className="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 z-50">
            <div className="bg-white rounded-2xl p-6 max-w-md w-full">
              <h2 className="text-2xl font-bold mb-4">Add New Employee</h2>
              <div className="space-y-4">
                <input 
                  type="text" 
                  placeholder="Employee Name"
                  value={newEmployee.name}
                  onChange={(e) => setNewEmployee({...newEmployee, name: e.target.value})}
                  className="w-full border rounded-lg px-4 py-2"
                />
                <select 
                  value={newEmployee.department}
                  onChange={(e) => setNewEmployee({...newEmployee, department: e.target.value})}
                  className="w-full border rounded-lg px-4 py-2"
                >
                  {departments.map(dept => <option key={dept} value={dept}>{dept}</option>)}
                </select>
                <input 
                  type="number" 
                  placeholder="Total PTO Days"
                  value={newEmployee.ptoTotal}
                  onChange={(e) => setNewEmployee({...newEmployee, ptoTotal: parseInt(e.target.value) || 0})}
                  className="w-full border rounded-lg px-4 py-2"
                />
                <input 
                  type="number" 
                  placeholder="Total Sick Days"
                  value={newEmployee.sickTotal}
                  onChange={(e) => setNewEmployee({...newEmployee, sickTotal: parseInt(e.target.value) || 0})}
                  className="w-full border rounded-lg px-4 py-2"
                />
                <div className="flex gap-3">
                  <button 
                    onClick={() => setShowAddModal(false)}
                    className="flex-1 border border-gray-300 text-gray-700 rounded-lg py-2 hover:bg-gray-50"
                  >
                    Cancel
                  </button>
                  <button 
                    onClick={handleAddEmployee}
                    className="flex-1 bg-blue-600 text-white rounded-lg py-2 hover:bg-blue-700"
                  >
                    Add Employee
                  </button>
                </div>
              </div>
            </div>
          </div>
        )}

        {/* New Request Modal */}
        {showRequestModal && (
          <div className="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 z-50">
            <div className="bg-white rounded-2xl p-6 max-w-md w-full">
              <h2 className="text-2xl font-bold mb-4">Submit Leave Request</h2>
              <div className="space-y-4">
                <select 
                  value={newRequest.employeeId}
                  onChange={(e) => setNewRequest({...newRequest, employeeId: e.target.value})}
                  className="w-full border rounded-lg px-4 py-2"
                >
                  <option value="">Select Employee</option>
                  {employees.map(emp => (
                    <option key={emp.id} value={emp.id}>{emp.name}</option>
                  ))}
                </select>
                <select 
                  value={newRequest.type}
                  onChange={(e) => setNewRequest({...newRequest, type: e.target.value})}
                  className="w-full border rounded-lg px-4 py-2"
                >
                  <option value="PTO">PTO</option>
                  <option value="Sick">Sick Leave</option>
                </select>
                <input 
                  type="date" 
                  placeholder="Start Date"
                  value={newRequest.startDate}
                  onChange={(e) => setNewRequest({...newRequest, startDate: e.target.value})}
                  className="w-full border rounded-lg px-4 py-2"
                />
                <input 
                  type="date" 
                  placeholder="End Date"
                  value={newRequest.endDate}
                  onChange={(e) => setNewRequest({...newRequest, endDate: e.target.value})}
                  className="w-full border rounded-lg px-4 py-2"
                />
                <textarea 
                  placeholder="Reason (optional)"
                  value={newRequest.reason}
                  onChange={(e) => setNewRequest({...newRequest, reason: e.target.value})}
                  className="w-full border rounded-lg px-4 py-2 h-24"
                />
                <div className="flex gap-3">
                  <button 
                    onClick={() => setShowRequestModal(false)}
                    className="flex-1 border border-gray-300 text-gray-700 rounded-lg py-2 hover:bg-gray-50"
                  >
                    Cancel
                  </button>
                  <button 
                    onClick={handleSubmitRequest}
                    className="flex-1 bg-blue-600 text-white rounded-lg py-2 hover:bg-blue-700"
                  >
                    Submit Request
                  </button>
                </div>
              </div>
            </div>
          </div>
        )}
      </div>
    </div>
  );
};

export default PTOTracker;
