# Claude Code Agents Collection

A comprehensive set of specialized AI agents for Claude Code that automate software development workflows, enforce quality standards, and facilitate systematic decision-making.

## 🎯 Overview

This collection provides production-ready agents that handle the complete software development lifecycle - from architecture planning to code quality enforcement. Each agent is designed with specific expertise and follows systematic methodologies to ensure consistent, high-quality outcomes.

## 📁 Agent Categories

### 🏗️ Architecture & Planning

- **[spec-driven-architect](spec-driven-architect.md)** - Ensures proper specification-driven development by creating detailed specs before implementation begins
- **[decision-coordinator](consensus/decision-coordinator.md)** - Orchestrates multi-agent decision-making for complex architectural choices and technical decisions

### 🔍 Quality Assurance

- **[code-quality-enforcer](code-quality-enforcer.md)** - Maintains code quality through automated formatting, linting, type checking, and testing
- **[test-maintainer](test-maintainer.md)** - Ensures comprehensive test coverage and maintains test suite integrity after development tasks

### 📚 Documentation & Sync

- **[docs-sync-checker](docs-sync-checker.md)** - Keeps documentation synchronized with codebase changes, especially CLAUDE.md files

### 🌐 Research & Intelligence

- **[web-research-specialist](web-research-specialist.md)** - Conducts targeted web research for current information beyond Claude's training data

### 🤝 Consensus System

A sophisticated multi-agent decision-making framework:

- **[consensus-judge](consensus/consensus-judge.md)** - Evaluates proposals and makes final decisions using context-appropriate consensus mechanisms
- **[pragmatic-proposer](consensus/pragmatic-proposer.md)** - Generates practical, immediately implementable solutions
- **[quality-proposer](consensus/quality-proposer.md)** - Focuses on robustness, maintainability, and long-term sustainability
- **[innovative-proposer](consensus/innovative-proposer.md)** - Creates outside-the-box solutions that challenge conventional approaches
- **[efficiency-proposer](consensus/efficiency-proposer.md)** - Optimizes for performance, resource usage, and operational efficiency
- **[risk-aware-proposer](consensus/risk-aware-proposer.md)** - Considers and mitigates potential risks and failure modes

## 🚀 Quick Start

### Installation

1. Clone the repository and copy agent files to your Claude Code agents directory:

   ```bash
   # Clone the repository
   git clone https://github.com/alexferrari88/cc-agents.git
   
   # For project-specific agents
   cp -r cc-agents/*.md cc-agents/consensus/ /path/to/your/project/.claude/agents/
   
   # For user-global agents
   cp -r cc-agents/*.md cc-agents/consensus/ ~/.claude/agents/
   
   # Clean up
   rm -rf cc-agents/
   ```

2. Restart Claude Code or run `/agents` to verify installation

### Basic Usage

Agents can be used in two ways:

**Automatic Activation**: Claude Code will automatically use appropriate agents based on context and task requirements.

**Explicit Invocation**: Request specific agents directly:

```md
Use the code-quality-enforcer agent to check my recent changes
Use the spec-driven-architect agent to plan this new feature
Use the test-maintainer agent to update test coverage
```

## 📋 Agent Workflows

### Development Lifecycle Integration

1. **Planning Phase**: `spec-driven-architect` creates detailed specifications
2. **Decision Making**: `decision-coordinator` handles complex architectural choices
3. **Implementation**: Standard development with quality checks
4. **Quality Assurance**: `code-quality-enforcer` ensures standards compliance
5. **Testing**: `test-maintainer` maintains comprehensive test coverage
6. **Documentation**: `docs-sync-checker` keeps docs current

### Multi-Agent Decision Making

For complex decisions, the consensus system provides structured evaluation:

1. **decision-coordinator** orchestrates the process
2. Multiple **proposer agents** generate diverse solutions in parallel
3. **consensus-judge** evaluates proposals and selects optimal solutions

## 🛠️ Configuration

### Tool Access

Each agent is configured with specific tool access appropriate to its role:

- Planning agents: Read, Grep, Glob for analysis
- Quality agents: Full toolset including Bash for execution
- Research agents: Web tools and documentation access
- Consensus agents: Analysis tools only

### Customization

Agents can be customized by editing their markdown files:

- Modify the `description` field to change activation criteria
- Update system prompts to adjust behavior
- Modify `tools` field to change permitted operations

## 📊 Quality Standards

All agents follow consistent principles:

- **Systematic Workflows**: Each agent follows a defined multi-phase process
- **Error Handling**: Comprehensive error detection and recovery
- **Communication**: Clear progress updates and status reporting
- **Integration**: Seamless interaction with existing development workflows

## 🎯 Best Practices

### Agent Selection

- Use **code-quality-enforcer** after any significant code changes
- Invoke **test-maintainer** when implementing new features
- Use **spec-driven-architect** for any new feature or significant modification
- Deploy **decision-coordinator** for architectural decisions or complex trade-offs

### Workflow Integration

1. Plan with `spec-driven-architect` before major implementations
2. Make complex decisions using the consensus system
3. Enforce quality with `code-quality-enforcer` after changes
4. Maintain tests with `test-maintainer` for new/modified functionality
5. Sync documentation with `docs-sync-checker` after feature completion

## 🤝 Contributing

To extend this agent collection:

1. Follow the established agent format (YAML frontmatter + markdown content)
2. Provide clear `description` fields for automatic activation
3. Include comprehensive system prompts with specific workflows
4. Add usage examples in the description
5. Test agents thoroughly before sharing

## 📄 License

These agents are designed for development workflow automation and quality assurance. They focus exclusively on defensive security practices and do not include any malicious capabilities.

## 🔗 Related Resources

- **[Agent Workflows & Use Cases](workflows.md)** - Comprehensive guide to typical workflows and integration patterns
- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Subagents Guide](https://docs.anthropic.com/en/docs/claude-code/subagents)
- [Agent Configuration Reference](https://docs.anthropic.com/en/docs/claude-code/settings#tools-available-to-claude)
