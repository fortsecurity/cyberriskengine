# Contributing to FAIR Risk Analysis Dashboard

Thank you for your interest in contributing! This document provides guidelines for contributing to the project.

## 🎯 Ways to Contribute

### Reporting Bugs
- Use the GitHub Issues tab
- Include detailed steps to reproduce
- Provide screenshots if applicable
- Note your Python and Streamlit versions

### Suggesting Enhancements
- Open a GitHub Issue with the "enhancement" label
- Clearly describe the feature and its benefits
- Explain how it aligns with FAIR methodology
- Consider backward compatibility

### Submitting Code
- Fork the repository
- Create a feature branch (`git checkout -b feature/AmazingFeature`)
- Make your changes
- Test thoroughly
- Commit with clear messages
- Push to your fork
- Open a Pull Request

## 💻 Development Setup

### Prerequisites
- Python 3.8 or higher
- Git
- Virtual environment tool

### Setup Steps
```bash
# Clone your fork
git clone https://github.com/your-username/fair-risk-dashboard.git
cd fair-risk-dashboard

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the dashboard
streamlit run fair_dashboard.py
```

## 📝 Coding Standards

### Python Style Guide
- Follow PEP 8 guidelines
- Use meaningful variable names
- Add docstrings to functions
- Keep functions focused and concise
- Maximum line length: 100 characters

### FAIR Methodology Alignment
- All terminology must match FAIR Institute standards
- Verify definitions against official FAIR documentation
- Maintain mathematical accuracy in calculations
- Include help text for new UI elements

### Help Text Guidelines
- Keep tooltips under 200 characters
- Use FAIR-standard terminology
- Provide practical examples
- Indicate if factor is external (🌍) or internal (🏢)
- Include formulas where relevant

### Code Structure
```python
# Function template
def calculate_risk_metric(parameter1: float, parameter2: float) -> dict:
    """
    Brief description of what this function does.
    
    Args:
        parameter1: Description of first parameter
        parameter2: Description of second parameter
        
    Returns:
        Dictionary containing calculated metrics
        
    Example:
        >>> calculate_risk_metric(0.25, 1000)
        {'ale': 250, 'lef': 0.25}
    """
    # Implementation
    pass
```

## 🧪 Testing

### Manual Testing Checklist
- [ ] All input fields accept valid values
- [ ] Help tooltips display correctly
- [ ] Calculations produce expected results
- [ ] Charts render properly
- [ ] Export functions work
- [ ] Preset scenarios load correctly
- [ ] No console errors

### Test Coverage
- Add tests for new functionality
- Maintain existing test coverage
- Test edge cases
- Verify error handling

## 📚 Documentation

### Required Documentation Updates
When adding features, update:
- [ ] Main README.md (if user-facing)
- [ ] CHANGELOG.md (version history)
- [ ] Help text tooltips (for UI elements)
- [ ] Code comments (for complex logic)
- [ ] FAIR_QUICK_REFERENCE.md (if adding new concepts)

### Documentation Style
- Use clear, concise language
- Provide examples where helpful
- Keep FAIR terminology consistent
- Include screenshots for UI changes
- Update version numbers appropriately

## 🔍 Pull Request Process

### Before Submitting
1. **Test Thoroughly**
   - Run all manual tests
   - Verify no regressions
   - Test on different screen sizes

2. **Update Documentation**
   - README.md if needed
   - CHANGELOG.md entry
   - Help text for UI changes
   - Code comments

3. **Clean Commit History**
   - Use descriptive commit messages
   - Squash related commits
   - Reference issues if applicable

### PR Title Format
```
[Type] Brief description

Types: Feature, Fix, Docs, Style, Refactor, Test, Chore

Examples:
- [Feature] Add control effectiveness calculator
- [Fix] Correct ALE calculation for zero LEF
- [Docs] Update installation instructions
- [Style] Improve container border styling
```

### PR Description Template
```markdown
## Description
Brief summary of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Refactoring
- [ ] Other (specify)

## Testing
- [ ] Manual testing completed
- [ ] All tests pass
- [ ] No regressions found

## Documentation
- [ ] README updated
- [ ] CHANGELOG updated
- [ ] Help text added/updated
- [ ] Comments added to code

## Screenshots (if applicable)
[Add screenshots here]

## Related Issues
Fixes #(issue number)
```

## 🎨 UI/UX Guidelines

### Visual Design Principles
- **Clarity:** Clear visual hierarchy
- **Consistency:** Consistent styling throughout
- **Accessibility:** High contrast, keyboard navigation
- **Education:** UI should teach FAIR concepts

### Color Usage
- External factors: Light blue/gray background
- Internal factors: Light green/teal background
- Risk levels: Green (low), Orange (medium), Red (high)
- Maintain BARE Cybersecurity brand colors where applicable

### Container Guidelines
- Use `st.container(border=True)` for grouping
- Add descriptive captions with `st.caption()`
- Include section headers with emoji icons
- Show formulas where relationships aren't obvious

## 🌍 FAIR Methodology Standards

### Terminology Requirements
All FAIR terms must match these standard definitions:

**External Factors:**
- Contact Frequency (CF): Industry-wide threat volume

**Internal Factors:**
- Probability of Action (PoA): Organization-specific targeting
- Threat Event Frequency (TEF): CF × PoA
- Vulnerability (V): Control effectiveness (inverse)
- Loss Event Frequency (LEF): TEF × V
- Loss Magnitude (LM): Primary + Secondary losses
- Annual Loss Expectancy (ALE): LEF × LM

### Mathematical Accuracy
- All formulas must be verifiable against FAIR standards
- Monte Carlo simulations must use appropriate distributions
- Statistical calculations must be mathematically sound
- Percentiles must be calculated correctly

## ❓ Questions?

### Getting Help
- **General Questions:** Open a GitHub Discussion
- **Bug Reports:** Open a GitHub Issue
- **FAIR Methodology:** Visit [fairinstitute.org](https://www.fairinstitute.org)
- **Feature Requests:** Open a GitHub Issue with "enhancement" label

### Contact
- **Project Maintainer:** [Your contact info]
- **BARE Cybersecurity:** [Organization contact]

## 📜 Code of Conduct

### Our Pledge
We pledge to make participation in this project a harassment-free experience for everyone, regardless of age, body size, disability, ethnicity, gender identity and expression, level of experience, nationality, personal appearance, race, religion, or sexual identity and orientation.

### Our Standards
**Positive behaviors:**
- Being respectful of differing viewpoints
- Gracefully accepting constructive criticism
- Focusing on what is best for the community
- Showing empathy towards other community members

**Unacceptable behaviors:**
- Trolling, insulting/derogatory comments, and personal attacks
- Public or private harassment
- Publishing others' private information without permission
- Other conduct which could reasonably be considered inappropriate

### Enforcement
Instances of abusive, harassing, or otherwise unacceptable behavior may be reported to the project maintainers. All complaints will be reviewed and investigated promptly and fairly.

## 🎖️ Recognition

Contributors will be recognized in:
- CHANGELOG.md for significant contributions
- GitHub Contributors page
- Project acknowledgments

## 📄 License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for helping make quantitative risk analysis more accessible! 🙏**
