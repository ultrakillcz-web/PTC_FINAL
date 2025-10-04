# Getting Started with PTC Creation

Welcome! This guide will help you create your first Procedure Test Case (PTC) in just a few minutes.

## What You Need

Before you begin, make sure you have:
1. The procedure you want to test clearly understood
2. Access to the system/environment you'll be testing
3. About 30-60 minutes to create your first PTC

## Step-by-Step: Create Your First PTC

### Step 1: Choose Your Template (2 minutes)

Copy the template file:
```bash
cp PTC_TEMPLATE.md ptc_cases/PTC-2025-001.md
```

Or simply open `PTC_TEMPLATE.md` and use it as a reference.

### Step 2: Fill in Basic Information (5 minutes)

Open your new file and fill in:
- **Test Case ID**: Use format PTC-2025-001 (increment the number)
- **Date Created**: Today's date
- **Created By**: Your name
- **Procedure Name**: What are you testing?
- **Test Objective**: Why are you testing it?

**Example:**
```
Test Case ID: PTC-2025-001
Date Created: 04/10/2025
Created By: John Smith
Procedure Name: User Password Reset
Test Objective: Validate that users can successfully reset forgotten passwords
```

### Step 3: Document Prerequisites (10 minutes)

List everything needed before testing:
- Environment setup
- User accounts
- Test data
- Special permissions

**Tip:** If you can't test without it, it's a prerequisite!

### Step 4: Write Test Steps (15 minutes)

Break your procedure into clear steps. For each step, specify:
1. The **action** to perform
2. The **input data** to use
3. The **expected result**

**Example:**
```
| Step | Action | Input Data | Expected Result |
|------|--------|------------|-----------------|
| 1 | Click "Forgot Password" link | N/A | Password reset form appears |
| 2 | Enter email address | test@example.com | Email field accepts input |
| 3 | Click "Send Reset Link" | N/A | Success message shown |
```

### Step 5: Define Pass/Fail Criteria (5 minutes)

Clearly state what makes the test pass or fail:

**Pass Criteria:**
- User receives reset email within 2 minutes
- Reset link works and is secure
- New password can be set successfully

**Fail Criteria:**
- Email not received after 5 minutes
- Reset link doesn't work
- System shows errors

### Step 6: Review Your PTC (5 minutes)

Check your work:
- [ ] Can someone else understand and execute this?
- [ ] Are all prerequisites listed?
- [ ] Are expected results specific?
- [ ] Is test data clearly specified?

### Step 7: Get Peer Review (Optional but Recommended)

Have a colleague review your PTC. Fresh eyes catch issues!

### Step 8: Execute the Test (Time varies)

When ready to test:
1. Verify all prerequisites are met
2. Follow each step exactly as written
3. Record actual results in the "Actual Result" column
4. Mark each step as Pass/Fail
5. Document any issues found

### Step 9: Document Results

After execution:
1. Fill in the "Actual Results Summary" section
2. Log any defects found
3. Complete the conclusion section
4. Update the status to "Executed"

## Quick Tips for Success

### ✅ DO:
- Be specific in your expected results
- Include exact values and data
- Test one thing at a time
- Document as you go
- Take screenshots of issues

### ❌ DON'T:
- Use vague terms like "it works"
- Skip prerequisites
- Combine too many steps
- Execute without documenting
- Forget to save your work

## Common First-Timer Mistakes

1. **Too broad scope**: Start with a simple, focused procedure
2. **Vague expected results**: "System works" is not specific enough
3. **Missing prerequisites**: Document everything needed
4. **No test data**: Always specify what data to use
5. **Skipping the review**: Always get feedback

## Example: Simple Login Test

Here's a minimal example to get you started:

```markdown
## Test Case Information
Test Case ID: PTC-2025-001
Procedure Name: User Login
Test Objective: Verify users can log in with valid credentials

## Test Steps
| Step | Action | Input | Expected Result |
|------|--------|-------|-----------------|
| 1 | Open login page | URL: /login | Login form displays |
| 2 | Enter username | "testuser" | Username accepted |
| 3 | Enter password | "Test123!" | Password accepted (masked) |
| 4 | Click Login button | N/A | Redirect to dashboard |

## Pass/Fail Criteria
Pass: User successfully logs in and sees dashboard
Fail: Error message or login fails
```

## Resources

- **Full Documentation**: [README.md](README.md)
- **Template**: [PTC_TEMPLATE.md](PTC_TEMPLATE.md)
- **Real Example**: [EXAMPLE_PTC.md](EXAMPLE_PTC.md)
- **Quick Reference**: [QUICK_REFERENCE.md](QUICK_REFERENCE.md)
- **Checklist**: [CHECKLIST.md](CHECKLIST.md)

## Need Help?

1. Check the [EXAMPLE_PTC.md](EXAMPLE_PTC.md) for a complete example
2. Review [QUICK_REFERENCE.md](QUICK_REFERENCE.md) for quick answers
3. Use [CHECKLIST.md](CHECKLIST.md) to ensure completeness
4. Consult your QA team

## Next Steps

After creating your first PTC:
1. Practice with 2-3 more test cases
2. Learn to handle edge cases
3. Explore negative test scenarios
4. Consider test automation opportunities

## Congratulations! 🎉

You're ready to create your first PTC. Remember:
- Start simple
- Be specific
- Document thoroughly
- Get feedback
- Improve with practice

Happy testing!

---

**Version:** 1.0  
**Last Updated:** 2025
