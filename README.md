# Canvas Assignment Uploader

This is a command-line tool to help upload assignments to Canvas automatically.

It takes an `.ods` or `.xlsx` file and creates assignments in the selected Canvas course.

## How to use

1. Install required Python packages:

```bash
pip install -r requirements.txt
```

2. Set up your `.env` file with Canvas API URL and API Key:

```env
API_URL=https://canvas.yourschool.edu/api/v1
API_KEY=your_canvas_api_key
```

You might need to request one from canvas -> Account -> setting -> New Access Token

Mine looks like:

```env
API_URL=https://canvas.uw.edu
API_KEY=1xxxxxxxxxxxxxxx
```

1. Run the script:

```bash
python upload_assignments.py
```

4. Follow the prompts:

- Select the course
- Enter path to schedule file (ODS or XLSX)
- Configure assignment groups (due date offset, points, due time)
- Upload assignments

## Schedule file format

The schedule file should contain columns like, week, date, Lab (Tue, Wed evening), PS (Sunday night)...

The tool will detect columns with names like `Lab (xxx)` or `PS (xxx)` and treat them as assignment groups.


