# Employee Network Management System

A C++ application that manages employees and their professional relationships as a network graph, utilizing advanced data structures and algorithms for efficient network analysis.

## 📋 Overview

This system models an organization as a graph where:
- **Nodes** represent employees with their professional attributes
- **Edges** represent professional connections/relationships between employees
- **Weights** on edges represent the strength or type of relationship

## ✨ Features

### Employee Management
- **Add Employees**: Register new employees with full profile information
- **Remove Employees**: Delete employees from the system
- **Employee Lookup**: Find employees by registration number
- **View All Employees**: Display complete employee roster

### Network Analysis
- **Connect Employees**: Establish relationships between employees with weighted connections
- **Disconnect Employees**: Remove relationships between employees
- **Find Shortest Path**: Calculate shortest distance between two employees in the network
- **Breadth-First Search (BFS)**: Traverse network to explore direct and indirect connections
- **Depth-First Search (DFS)**: Deep network exploration for hierarchical analysis
- **Minimum Spanning Tree (MST)**: Find Prim's MST to identify core network structure

## 📊 Data Structures

### Employee Structure
```cpp
struct Employee {
    std::string registrationNumber;  // Unique identifier
    int age;
    std::string gender;
    std::string educationLevel;
    std::string jobTitle;
    int yearsOfExperience;
    int salary;
};
```

### System Architecture
- **Adjacency Matrix**: O(1) edge lookup for relationship data (200×200 matrix)
- **Employee Array**: Fast employee access by index
- **Graph-based Relationships**: Network analysis capabilities

## 🔧 System Specifications

- **Maximum Employees**: 200
- **Language**: C++
- **Key Algorithms**: BFS, DFS, Dijkstra (shortest path), Prim's MST

## 📖 API Reference

### Core Methods

| Method | Description |
|--------|-------------|
| `addEmployee()` | Register a new employee |
| `removeEmployee()` | Remove employee by registration number |
| `connectEmployees()` | Create weighted relationship between employees |
| `disconnectEmployees()` | Remove relationship between employees |
| `findEmployee()` | Retrieve employee details by registration number |
| `shortestDistanceBetweenEmployees()` | Calculate shortest path distance |
| `breadthFirstSearch()` | Perform BFS traversal from an employee |
| `depthFirstSearch()` | Perform DFS traversal from an employee |
| `primMST()` | Compute Minimum Spanning Tree of network |
| `printEmployees()` | Display all employees in system |

## 🚀 Usage

```cpp
EmployeeManagementSystem system;

// Add employees
Employee* emp1 = new Employee("EMP001", 28, "M", "Bachelor", "Engineer", 3, 50000);
system.addEmployee(emp1);

// Connect employees
system.connectEmployees("EMP001", "EMP002", 1);

// Find relationships
int distance = system.shortestDistanceBetweenEmployees("EMP001", "EMP003");

// Analyze network
system.breadthFirstSearch("EMP001");
system.primMST();
```

## 💡 Use Cases

- **Organizational Structure Analysis**: Understand reporting relationships and team connections
- **Professional Network Mapping**: Identify collaboration networks within the company
- **Path Finding**: Discover connection paths between employees
- **Network Optimization**: Find minimal spanning tree for essential connections
- **Talent Management**: Analyze employee networks for succession planning

## 📝 Notes

- Each employee has a unique registration number
- Relationships are weighted (can represent collaboration strength, direct reports, etc.)
- The system supports up to 200 employees maximum
- Adjacency matrix provides O(1) relationship lookup

## 🔗 Dependencies

- Standard C++ Library (`iostream`, `string`, `queue`, `deque`)
- Custom parameter file (`params.hpp`)

