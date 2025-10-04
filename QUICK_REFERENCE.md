# PTC Quick Reference Guide

## Quick Start

1. **Copy the template**: Start with `PTC_TEMPLATE.md`
2. **Fill in test case info**: Add ID, date, and procedure details
3. **List prerequisites**: Document all requirements
4. **Write test steps**: Break procedure into clear steps
5. **Execute**: Follow steps and record results
6. **Document**: Complete all sections
7. **Review**: Get peer review before finalizing

## Naming Convention

**Format:** `PTC-YYYY-NNN`
- YYYY = Year (e.g., 2025)
- NNN = Sequential number (e.g., 001, 002, 003)

**Example:** PTC-2025-001

## Priority Levels

- **High**: Critical functionality, security, data integrity
- **Medium**: Important features, common workflows
- **Low**: Nice-to-have features, edge cases

## Test Status Values

- **Draft**: Being written
- **In Review**: Under peer review
- **Approved**: Approved for execution
- **Executed**: Has been run
- **Archived**: No longer active

## Step Status Values

- **Pass**: Step completed successfully
- **Fail**: Step did not meet expected result
- **Blocked**: Cannot execute due to dependency
- **Skipped**: Intentionally not executed
- **N/A**: Not applicable for this run

## Common Test Types

- **Functional**: Tests specific functionality
- **Integration**: Tests interaction between components
- **Regression**: Verifies existing functionality still works
- **Performance**: Tests speed and efficiency
- **Security**: Tests for vulnerabilities
- **Usability**: Tests user experience

## Severity Levels for Defects

- **Critical**: System crash, data loss, security breach
- **High**: Major functionality broken, no workaround
- **Medium**: Functionality impaired, workaround exists
- **Low**: Minor issue, cosmetic problem

## Best Practice Checklist

- [ ] Test case has unique ID
- [ ] Objective is clear and specific
- [ ] Prerequisites are complete
- [ ] Steps are numbered and sequential
- [ ] Expected results are specific
- [ ] Test data is documented
- [ ] Pass/fail criteria defined
- [ ] Test is repeatable
- [ ] Evidence is captured
- [ ] Results are documented

## Common Mistakes to Avoid

1. **Vague expected results**: Be specific and measurable
2. **Missing prerequisites**: Document everything needed
3. **Too many objectives**: One test case = one objective
4. **No test data**: Always specify what data to use
5. **Skipping documentation**: Document during execution, not after
6. **No peer review**: Always get another pair of eyes
7. **Ignoring failures**: Document all failures, even minor ones

## Tips for Writing Good Test Steps

✅ **Do:**
- Use clear, action-oriented language
- Be specific about what to do
- Include exact values and data
- Number steps sequentially
- Keep steps atomic (one action per step)

❌ **Don't:**
- Use vague terms like "check", "verify" without specifics
- Combine multiple actions in one step
- Assume knowledge not in prerequisites
- Skip documenting actual results
- Rush through execution

## Documentation Tips

- Capture screenshots at key points
- Save log files before they rotate
- Note exact error messages
- Record timestamps for time-sensitive tests
- Document environment details

## When to Create a New PTC

Create a new PTC when:
- Testing a new procedure
- Procedure significantly changes
- Different test objective for same procedure
- Different test data or environment needed
- Previous PTC archived

Update existing PTC when:
- Minor procedure changes
- Fixing typos or clarity issues
- Adding notes from execution
- Updating expected results

## File Organization

```
/PTC_FINAL
├── README.md                    # Main documentation
├── PTC_TEMPLATE.md             # Empty template
├── EXAMPLE_PTC.md              # Filled example
├── QUICK_REFERENCE.md          # This file
└── ptc_cases/                  # Directory for your PTCs
    ├── PTC-2025-001.md
    ├── PTC-2025-002.md
    └── ...
```

## Useful Commands

### Check for duplicate IDs:
```bash
grep -r "Test Case ID:" ptc_cases/ | sort
```

### List all PTCs by status:
```bash
grep -h "Status:" ptc_cases/*.md | sort | uniq -c
```

### Find all failed test cases:
```bash
grep -l "Overall Test Result: Fail" ptc_cases/*.md
```

## Resources

- Full documentation: `README.md`
- Template: `PTC_TEMPLATE.md`
- Example: `EXAMPLE_PTC.md`
- This guide: `QUICK_REFERENCE.md`

## Support

For questions:
1. Review this guide and README.md
2. Check example PTC
3. Consult with QA team
4. Submit issue in repository

---

**Version:** 1.0  
**Last Updated:** 2025
