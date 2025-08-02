# Agent Workflows & Use Cases

This document outlines the typical workflows and use cases for the Claude Code Agents Collection, showing how different agents work together to automate and enhance software development processes.

## 🎯 Core Workflow Patterns

### 1. Complete Feature Development Lifecycle

**Use Case**: Implementing a new feature from conception to production-ready code

**Workflow Steps**:
1. **Planning**: `spec-driven-architect` creates detailed specifications before any code is written
2. **Research** (if needed): `web-research-specialist` gathers current information about technologies or approaches
3. **Complex Decisions**: `decision-coordinator` orchestrates multi-agent decision making for architectural choices
4. **Implementation**: Standard development work
5. **Quality Assurance**: `code-quality-enforcer` ensures code standards, formatting, linting, and type checking
6. **Testing**: `test-maintainer` ensures comprehensive test coverage for new functionality
7. **Documentation**: `docs-sync-checker` updates all documentation to reflect changes

**Example Scenario**:
```
User: "I need to add real-time notifications to our app"
→ spec-driven-architect: Creates notification system specification
→ decision-coordinator: Evaluates WebSocket vs SSE vs polling approaches
→ Development: Implement chosen solution
→ code-quality-enforcer: Runs linting, formatting, type checks
→ test-maintainer: Adds notification tests
→ docs-sync-checker: Updates API docs and CLAUDE.md
```

### 2. Multi-Agent Consensus Decision Making

**Use Case**: Making complex technical decisions that require multiple perspectives

**Workflow Steps**:
1. **Coordination**: `decision-coordinator` analyzes the decision complexity and selects appropriate proposer agents
2. **Parallel Proposal Generation**: Multiple proposer agents generate diverse solutions simultaneously:
   - `pragmatic-proposer`: Practical, proven approaches
   - `quality-proposer`: Maintainable, robust solutions
   - `innovative-proposer`: Creative, breakthrough ideas
   - `efficiency-proposer`: Performance-optimized solutions
   - `risk-aware-proposer`: Safe, defensive approaches
3. **Consensus**: `consensus-judge` evaluates all proposals and selects the optimal solution

**Example Scenario**:
```
Decision: "Choose database architecture for high-traffic analytics system"
→ decision-coordinator: Selects efficiency + risk-aware + pragmatic proposers
→ efficiency-proposer: Suggests columnar database with caching layer
→ risk-aware-proposer: Recommends proven SQL database with read replicas
→ pragmatic-proposer: Suggests existing PostgreSQL with partitioning
→ consensus-judge: Weighs proposals and selects optimal approach
```

### 3. Code Quality Enforcement Pipeline

**Use Case**: Maintaining consistent code quality across all changes

**Workflow Steps**:
1. **Automated Quality Checks**: `code-quality-enforcer` runs formatting, linting, type checking
2. **Issue Resolution**: Systematic fixing of quality issues
3. **Test Execution**: Running test suites to ensure no regressions
4. **Verification**: Final quality verification

**Example Scenario**:
```
After implementing search filters:
→ code-quality-enforcer: Runs ruff format, ruff check, mypy
→ Fixes import ordering and type annotations
→ Runs pytest suite
→ Reports final quality status
```

### 4. Research-Driven Development

**Use Case**: Making informed decisions based on current technology trends and best practices

**Workflow Steps**:
1. **Research**: `web-research-specialist` gathers current information
2. **Decision Making**: `decision-coordinator` uses research to inform technical choices
3. **Implementation**: Development guided by research insights

**Example Scenario**:
```
User: "What's the best approach for implementing OAuth 2.1 in our FastAPI app?"
→ web-research-specialist: Researches OAuth 2.1 specifications, FastAPI libraries, security best practices
→ decision-coordinator: Evaluates library options based on research
→ spec-driven-architect: Creates implementation specification
→ Development proceeds with informed choices
```

## 🔄 Specialized Workflow Scenarios

### Architecture & Planning Workflows

#### **Greenfield Project Architecture**
```
Agents: decision-coordinator → innovative + quality + pragmatic proposers
Focus: Breakthrough potential, solid foundations, practical implementation
Use Case: Designing new microservices architecture
```

#### **Legacy System Modernization**
```
Agents: decision-coordinator → pragmatic + risk-aware + quality + efficiency proposers  
Focus: Safe migration, performance improvement, maintainability
Use Case: Migrating monolith to microservices
```

#### **Technology Stack Selection**
```
Agents: web-research-specialist → decision-coordinator → all proposers → consensus-judge
Focus: Current technology assessment, comprehensive evaluation
Use Case: Choosing between React/Vue/Angular for new frontend
```

### Quality Assurance Workflows

#### **Post-Implementation Quality Gate**
```
Sequence: code-quality-enforcer → test-maintainer → docs-sync-checker
Focus: Comprehensive quality verification before code review
Use Case: After implementing complex feature
```

#### **Technical Debt Reduction**
```
Agents: decision-coordinator → quality + efficiency + pragmatic proposers
Focus: Systematic improvement without breaking changes
Use Case: Refactoring legacy codebase
```

### Crisis Response Workflows

#### **Production Issue Resolution**
```
Agents: decision-coordinator → pragmatic + risk-aware + efficiency proposers
Focus: Rapid stabilization, minimal disruption, monitoring
Use Case: Database performance crisis, service outage
```

#### **Security Incident Response**
```
Agents: web-research-specialist → decision-coordinator → risk-aware + pragmatic proposers
Focus: Current threat assessment, safe remediation
Use Case: Vulnerability discovered in dependencies
```

### Research & Discovery Workflows

#### **Technology Evaluation**
```
Sequence: web-research-specialist → decision-coordinator → consensus-judge
Focus: Informed decision making based on current information
Use Case: Evaluating new frameworks, libraries, or tools
```

#### **Best Practices Research**
```
Agents: web-research-specialist → spec-driven-architect
Focus: Implementing current industry standards
Use Case: Implementing CI/CD pipeline, testing strategies
```

## 🚀 Agent Activation Patterns

### Proactive Activation
Some agents are designed to activate automatically:

- **decision-coordinator**: Activates for complex technical decisions
- **code-quality-enforcer**: Triggers after significant code changes
- **test-maintainer**: Activates when new features are implemented
- **docs-sync-checker**: Triggers after feature completion

### Explicit Invocation
Other agents work best when explicitly requested:

- **spec-driven-architect**: "Create a spec for this feature"
- **web-research-specialist**: "Research current best practices for..."
- **consensus system**: "Evaluate different approaches for..."

## 🎯 Workflow Selection Guide

### Choose **Complete Feature Development** when:
- Implementing new user-facing features
- Adding new API endpoints
- Building new system components

### Choose **Multi-Agent Consensus** when:
- Multiple technical approaches are viable
- Decision affects multiple teams/systems
- High-impact architectural choices
- Technology selection decisions

### Choose **Quality Enforcement** when:
- After any code changes
- Before code reviews
- Preparing for releases
- Maintaining coding standards

### Choose **Research-Driven** when:
- Working with unfamiliar technologies
- Need current industry best practices
- Evaluating new tools or frameworks
- Implementing security or performance optimizations

## 📊 Workflow Metrics & Success Indicators

### Feature Development Success:
- ✅ Comprehensive specification exists
- ✅ All quality checks pass
- ✅ Test coverage maintained/improved
- ✅ Documentation synchronized

### Decision Making Success:
- ✅ Multiple perspectives considered
- ✅ Trade-offs clearly documented
- ✅ Implementation plan defined
- ✅ Success metrics established

### Quality Enforcement Success:
- ✅ All linting/formatting issues resolved
- ✅ Type checking passes
- ✅ Test suite passes
- ✅ No regressions introduced

## 🔗 Integration with Development Tools

These workflows integrate seamlessly with standard development practices:

- **Git workflows**: Agents work with feature branches and pull requests
- **CI/CD pipelines**: Quality enforcement integrates with automated testing
- **Code reviews**: Specifications and quality checks improve review efficiency
- **Documentation systems**: Automatic synchronization reduces maintenance overhead

The agent collection transforms ad-hoc development processes into systematic, repeatable workflows that consistently deliver high-quality results while reducing cognitive load on developers.