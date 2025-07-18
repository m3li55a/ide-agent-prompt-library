# Aligned with Clean Code principles (Robert C. Martin), SOLID principles, and ISO/IEC 25010 for software quality.

# Code Quality Optimization and Refactoring

Act as a senior software architect following Clean Code and SOLID principles. Review the codebase for readability, maintainability, and efficiency. Refactor unclear variable/function names to be descriptive and consistent. Standardize formatting using tools like Prettier or ESLint. Replace magic strings/numbers with constants. Enhance comments for clarity, removing redundant ones. Refactor for single responsibility, loose coupling, and modularity. Optimize performance anti-patterns (e.g., nested loops, redundant computations). Eliminate code smells (e.g., long methods, large classes) using tools like SonarQube. Apply changes directly, preserving functionality, and provide a refactoring summary.

#Deprecated Code Modernization

Identify deprecated functions, APIs, or libraries using static analysis tools (e.g., Deprecation Detector). Refactor to modern alternatives, ensuring compatibility and functionality. Document changes with version references and migration guides.

#Modular Codebase Restructuring

Assess code organization for modularity and maintainability per ISO/IEC 25010. Identify overly complex methods/classes or duplicated logic. Refactor into smaller, cohesive modules with clear interfaces. Apply patterns like Factory or Strategy where applicable. Update imports and references, applying changes directly.

# File and Asset Cleanup
Scan for unused files, scripts, tests, or assets using tools like unused or deadcode. Remove orphaned items and consolidate redundant utilities into shared modules. Provide a cleanup report with removed and consolidated items.

#IDE-Driven Issue Resolution

Address IDE-reported issues (errors, warnings, dependency conflicts, broken navigation) systematically. Categorize issues by severity, provide root cause analysis, and implement fixes with code edits or build commands. Request clarification for ambiguous issues. Ensure builds succeed post-fix.

#Technical Debt Assessment and Reduction

Evaluate the codebase for technical debt using metrics like code complexity (Cyclomatic Complexity), duplication, and test coverage (aim for >80% per industry standards). Prioritize high-impact areas (e.g., critical paths, frequently modified code). Refactor to reduce debt, providing before/after metrics and justifications.
