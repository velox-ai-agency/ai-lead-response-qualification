# Google Form Setup

## Form Title: Get Your Free AI Automation Assessment

## Questions (in order):

1. **Full Name*** (Short answer)
   - Required

2. **Email Address*** (Short answer)
   - Required
   
3. **Company Name** (Short answer)
   - Optional

4. **What's your estimated budget?** (Multiple choice)
   - Under $1,000
   - $1,000 - $5,000
   - $5,000 - $15,000
   - $15,000+
   - Rather discuss

5. **When do you need this solution?** (Multiple choice)
   - ASAP (within 2 weeks)
   - Within 1 month
   - Next 2-3 months
   - Just exploring

6. **Tell us about your project*** (Paragraph)
   - Required
   - Placeholder: "Describe the automation you need, current pain points, and goals..."

7. **How did you hear about us?** (Short answer)
   - Optional

---

## Form Configuration:
- **Confirmation message**: "Thanks! We'll analyze your requirements and get back within 24 hours."
- **Response destination**: Create spreadsheet (name: "Velox AI Leads")
- **Notification**: Email on new response → leads@veloxai.work

## n8n Integration:
Google Sheets Trigger → n8n Webhook → Claude Qualification → Router → Response
