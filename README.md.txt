# TruthMesh

TruthMesh is a tool for checking and keeping records of data claims.

## What is in this project?

* **architecture/SPECIFICATIONS.md**: System design notes.
* **data/claims.json**: Sample data claims.
* **data/decision_receipts.json**: Results and receipts.
* **schemas/**: Validation rules for data.
* **DEVELOPMENT_RECORD.md**: Record of original files vs new setup files.
* **README.md**: Overview and instructions for judges.

## How to test the data (Python)

```bash
pip install jsonschema
python -c "import json, jsonschema; claim=json.load(open('data/claims.json')); schema=json.load(open('schemas/claim.schema.json')); jsonschema.validate(claim, schema)"