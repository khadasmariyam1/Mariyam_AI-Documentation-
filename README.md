# Update the notebook with custom project info for Reshma and Mariyam

notebook_content["cells"][1]["source"] = [
    "# Build Mariyam’s AI Project Documentation in Google Colab\n",
    "This notebook helps Reshma and Mariyam generate documentation for their AI project using Sphinx and the Read the Docs theme."
]

notebook_content["cells"][2]["source"] = [
    "# Step 1: Install Sphinx and Read the Docs theme\n",
    "!pip install sphinx sphinx-rtd-theme"
]

notebook_content["cells"][3]["source"] = [
    "# Step 2: Create project folder and run sphinx-quickstart\n",
    "!mkdir -p mariyam_ai/docs\n",
    "%cd mariyam_ai/docs\n",
    "!sphinx-quickstart --quiet --project=\"AI for Rare Diseases\" --author=\"Reshma & Mariyam\" --release=\"1.0\" --makefile=no --batchfile=no --sep"
]

# Save the updated notebook
updated_path = Path("/mnt/data/Mariyam_AI_Documentation_Notebook.ipynb")
with open(updated_path, "w") as f:
    json.dump(notebook_content, f)

updated_path.name
