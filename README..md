# FamEase
## AI-Assisted Medication Support for Elderly People

**Team Name:** NEXA  
**Track:** Healthcare  
**Event:** Ideathon 3.0

## 1. Problem Statement

Many elderly people face difficulties managing their daily medication routines. Smartphone applications may be challenging to use, medicine labels can be difficult to read, and similar-looking tablets can cause confusion. Family members who live away from them may not know whether reminders were answered or assistance is needed.

Traditional reminder systems can also become frustrating when patients must press a button after every call.

## 2. Proposed Solution

FamEase is an AI-assisted, voice-first medication support system designed for elderly people, including those who use basic keypad phones.

It combines scheduled voice calls, optional keypad responses, caregiver-reviewed prescription information, and a shared family dashboard to simplify medication routines and help families respond to unresolved concerns.

The objective is to make routine care effortless while ensuring important concerns are not overlooked.

## 3. Key Features

### 3.1 Voice-Based Medication Reminders

- Scheduled voice calls in Tamil and English.
- Simple instructions designed for elderly users.
- No smartphone or application installation required on the patient's phone.
- Routine reminders do not require mandatory keypad confirmation.

### 3.2 Keypad-Based Interaction

Patients can optionally respond using their phone keypad.

| Key | Action |
|---|---|
| 1 | Report that the medicine was taken |
| 2 | Request a later reminder |
| 3 | Request assistance from a caregiver |

A keypad response is recorded as a self-report, not proof that the medicine was swallowed. If there is no response, the dose remains unconfirmed.

### 3.3 AI-Assisted Prescription Recognition

- Extract medicine information from prescription images using OCR or a vision-language model.
- Present extracted details for caregiver verification.
- Store approved medicine schedules and instructions.
- Require review before activating a new or updated schedule.

AI assists with organizing prescription information; it does not prescribe medicines or change prescribed doses.

### 3.4 Medicine Identification Support

FamEase helps caregivers associate verified medicine information with labelled packaging and clearly labelled medicine compartments.

If a patient is uncertain about a loose tablet, the system directs them to a caregiver or pharmacist rather than guessing based on appearance.

### 3.5 Smart Follow-Up and Escalation

- Reduce unnecessary repeated calls.
- Apply configurable retry limits and follow-up windows.
- Notify designated caregivers about help requests or unresolved concerns.
- Maintain a history of reminder outcomes.

### 3.6 Family Dashboard

- Manage patient profiles and approved medicine schedules.
- Review reported doses and unanswered reminders.
- Track requests for assistance.
- Support coordination among authorized caregivers.

### 3.7 Medicine Stock Monitoring

- Estimate remaining medicine stock using recorded quantities and approved schedules.
- Provide alerts when a refill may be approaching.
- Allow caregivers to update stock information.

Stock estimates do not prove actual medicine consumption.

## 4. Role of Artificial Intelligence

FamEase uses AI to assist caregivers and reduce manual work.

| AI Capability | Purpose |
|---|---|
| OCR and vision-language models | Extract medicine details from prescription images for review |
| Adaptive reminder logic | Support suitable reminder and follow-up schedules |
| Exception handling | Identify unresolved reminders and route follow-up according to predefined rules |
| Stock estimation | Estimate when medicine supplies may run low |
| Future speech recognition | Explore optional spoken responses in supported languages |

AI supports the workflow but does not independently make medical decisions.

## 5. System Workflow

1. **Patient Setup:** A family member or authorized caregiver creates the patient's profile.
2. **Prescription Review:** Medicine details are entered or extracted and verified before activation.
3. **Voice Reminder:** FamEase calls the patient at the scheduled time.
4. **Optional Response:** The patient can report a dose, request a later reminder, or ask for assistance.
5. **Status Update:** The backend records the call outcome and updates the family dashboard.
6. **Smart Follow-Up:** Configured rules determine whether another reminder or caregiver notification is needed.
7. **Stock Monitoring:** FamEase estimates remaining supplies and alerts caregivers about potential refills.

## 6. Technology Stack

| Component | Technology |
|---|---|
| Frontend Dashboard | React |
| Backend | Python, FastAPI |
| Database | SQLite |
| Voice Calling | Telephony API, such as Exotel |
| Keypad Input | DTMF and webhooks |
| Voice Reminders | Tamil and English audio |
| Prescription Processing | OCR or vision-language model with caregiver review |

### System Architecture

```text
Family Dashboard (React)
          |
          v
    FastAPI Backend
          |
    +-----+------+
    |            |
    v            v
SQLite       Reminder and
Database     Follow-Up Logic
                  |
                  v
             Telephony API
                  |
                  v
         Patient's Basic Phone
                  |
           Keypad Response
                  |
                  v
            DTMF Webhook
                  |
                  v
           FastAPI Backend
                  |
                  v
        Updated Family Dashboard
```

## 7. Safety and Privacy

- Prescription information extracted by AI must be verified before use.
- Patients should provide consent and be able to pause or stop reminders.
- Personal and medicine information should be accessible only to authorized users.
- A delivered call or keypad response must not be treated as verified medication intake.
- FamEase does not diagnose conditions, prescribe medicines, or change prescribed doses.
- AI must not identify a loose tablet as safe to take based only on colour, shape, or image similarity.
- FamEase is not a replacement for professional healthcare or emergency services.
- Demonstrations should use fictional or properly consented test data.

## 8. Expected Impact

### For Elderly People

- Accessible medication reminders through familiar phone calls.
- Less dependence on smartphone applications.
- Reduced pressure to confirm every routine reminder.

### For Families

- Better visibility into reminder outcomes and requests for assistance.
- More useful alerts and fewer unnecessary follow-ups.
- Early warnings about potential medicine shortages.

### For Caregivers

- Easier management of approved medicine schedules.
- A shared history of reported outcomes.
- Improved coordination among authorized family members.

These expected benefits should be evaluated through user testing.

## 9. Initial Prototype Scope

- [ ] Patient profile and preferred language
- [ ] Caregiver-reviewed medicine schedule
- [ ] Scheduled outbound voice reminder
- [ ] DTMF keypad response handling
- [ ] Dashboard status updates
- [ ] Unanswered-call and assistance-request workflow
- [ ] Estimated low-stock alert

## 10. Demonstration Workflow

1. Create a test patient profile using fictional information.
2. Add a fictional medicine schedule and verify the details.
3. Trigger a Tamil or English voice reminder.
4. Simulate an optional keypad response.
5. Update the dashboard through a webhook.
6. Demonstrate an unanswered reminder or assistance request.
7. Display a potential low-stock alert.

## 11. Future Enhancements

- Support for additional regional languages.
- Optional voice-based responses.
- Improved accessibility for people with limited vision or hearing.
- Appointment reminders.
- Integration with approved healthcare services.
- Advanced medicine stock monitoring.

## 12. Team

**NEXA**  
Healthcare Track — Ideathon 3.0

Team member names, responsibilities, and contact details can be added here.

## 13. Project Status

FamEase is a proposed prototype. Features described as planned or future enhancements should not be considered implemented until they are available and tested in the repository.

## 14. License

An appropriate open-source license should be added before distributing the project or accepting external contributions.

---

**FamEase — Family care, made easy: a call, and a family at ease.**
