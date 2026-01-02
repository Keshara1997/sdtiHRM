# Load Sample Data - Complete Command List

This document contains all the commands to load sample data into the Horilla HRMS database via command line.

## For Windows (PowerShell/CMD)

### Individual Commands (Run in order):

```powershell
# Core data files (must be loaded first)
python manage.py loaddata load_data/user_data.json
python manage.py loaddata load_data/employee_info_data.json
python manage.py loaddata load_data/base_data.json
python manage.py loaddata load_data/work_info_data.json

# Module-specific data files
python manage.py loaddata load_data/attendance_data.json
python manage.py loaddata load_data/leave_data.json
python manage.py loaddata load_data/asset_data.json
python manage.py loaddata load_data/recruitment_data.json
python manage.py loaddata load_data/onboarding_data.json
python manage.py loaddata load_data/offboarding_data.json
python manage.py loaddata load_data/pms_data.json
python manage.py loaddata load_data/payroll_data.json
python manage.py loaddata load_data/payroll_loanaccount_data.json
python manage.py loaddata load_data/project_data.json

# Additional data files
python manage.py loaddata load_data/faq_category.json
python manage.py loaddata load_data/faq.json
python manage.py loaddata load_data/mail_automations.json
python manage.py loaddata load_data/mail_templates.json
python manage.py loaddata load_data/tags.json
```

### Using Batch Script:

```powershell
.\load_sample_data.bat
```

## For Linux/macOS

### Individual Commands (Run in order):

```bash
# Core data files (must be loaded first)
python3 manage.py loaddata load_data/user_data.json
python3 manage.py loaddata load_data/employee_info_data.json
python3 manage.py loaddata load_data/base_data.json
python3 manage.py loaddata load_data/work_info_data.json

# Module-specific data files
python3 manage.py loaddata load_data/attendance_data.json
python3 manage.py loaddata load_data/leave_data.json
python3 manage.py loaddata load_data/asset_data.json
python3 manage.py loaddata load_data/recruitment_data.json
python3 manage.py loaddata load_data/onboarding_data.json
python3 manage.py loaddata load_data/offboarding_data.json
python3 manage.py loaddata load_data/pms_data.json
python3 manage.py loaddata load_data/payroll_data.json
python3 manage.py loaddata load_data/payroll_loanaccount_data.json
python3 manage.py loaddata load_data/project_data.json

# Additional data files
python3 manage.py loaddata load_data/faq_category.json
python3 manage.py loaddata load_data/faq.json
python3 manage.py loaddata load_data/mail_automations.json
python3 manage.py loaddata load_data/mail_templates.json
python3 manage.py loaddata load_data/tags.json
```

### Using Shell Script:

```bash
chmod +x load_sample_data.sh
./load_sample_data.sh
```

## Quick Load All (Alternative Method)

You can also try loading all JSON files at once (may fail if dependencies aren't met):

### Windows:

```powershell
python manage.py loaddata load_data/*.json
```

### Linux/macOS:

```bash
python3 manage.py loaddata load_data/*.json
```

**Note:** This method may fail if there are dependency issues. It's recommended to use the individual commands in the correct order.

## File Descriptions

- **user_data.json** - Sample user accounts
- **employee_info_data.json** - Employee information
- **base_data.json** - Companies, departments, job positions
- **work_info_data.json** - Employee work information
- **attendance_data.json** - Attendance records
- **leave_data.json** - Leave management data
- **asset_data.json** - Asset management data
- **recruitment_data.json** - Recruitment data
- **onboarding_data.json** - Onboarding data
- **offboarding_data.json** - Offboarding data
- **pms_data.json** - Performance management system data
- **payroll_data.json** - Payroll data
- **payroll_loanaccount_data.json** - Loan account data
- **project_data.json** - Project management data
- **faq_category.json** - FAQ categories
- **faq.json** - FAQ entries
- **mail_automations.json** - Email automation rules
- **mail_templates.json** - Email templates
- **tags.json** - Tag data

## Important Notes

1. **Order Matters**: Core data files (users, employees, base) must be loaded before module-specific data
2. **Database Must Be Initialized**: Make sure you've run migrations first:
   ```bash
   python manage.py migrate
   ```
3. **Virtual Environment**: Ensure your virtual environment is activated
4. **Dependencies**: Some files may fail if the corresponding app is not installed. This is normal and expected.



