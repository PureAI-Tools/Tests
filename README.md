# Tests 
Step-by-Step Instructions
Create a new branch from the Tests repository

Go to https://github.com/PureAI-Tools/Tests.

Click Branch: main (or the current default branch).

Type a new branch name, for example: feature/tests-example.

Click Create branch to confirm.

Clone the repository locally (optional)

If you want to work on your computer, run:
git clone https://github.com/PureAI-Tools/Tests.git
cd Tests
git checkout -b feature/tests-example
Otherwise, you can create and edit the new branch directly via the GitHub web interface.

Add or modify the Jupyter Notebook

Inside the new branch, add a new file: for example x_test.ipynb.

You can also modify test.ipynb if needed.

Important: The notebook should include the commands below so everything installs and clones the required files when run in Colab:

!pip install purecpp_extract purecpp_chunks_clean
!git clone https://github.com/PureAI-Tools/Tests.git
This ensures that all .pdf, .docx, or other files are pulled locally in the Colab environment.

Commit and push the new branch to GitHub

If working locally:

git add .
git commit -m "Add example_test.ipynb with install and clone steps"
git push origin feature/tests-example

If editing in the GitHub web interface, simply Commit changes and select ‘feature/tests-example’ as the branch to commit to.

Adjust the Colab URL to point to your new branch and file

The general Colab URL format for a file in a specific branch is:

https://colab.research.google.com/github/<ORG_OR_USER>/<REPO>/blob/<BRANCH>/<NOTEBOOK>.ipynb
For example, if your branch is feature/tests-example and your notebook is example_test.ipynb, the URL would be:

https://colab.research.google.com/github/PureAI-Tools/Tests/blob/feature/tests-example/example_test.ipynb
Alternatively, if you kept the same file name (test.ipynb) in your new branch, just replace <NOTEBOOK>.ipynb with test.ipynb.

Open the notebook in Colab

Paste the adjusted URL into your browser.

Once Colab loads, check that the !pip install commands and !git clone commands run properly.

Verify that you can access the cloned files (pdfs, docxs, etc.) inside your notebook.

Confirm everything works

When you run the notebook in Colab, it should install the required libraries (purecpp_extract, purecpp_chunks_clean).

Then it should clone the repository, so you can read or process your PDF and DOCX files.

If something fails, double-check the paths and repository name in your !git clone command.

(Optional) Merge back into main

Once testing is done and everything is working, create a Pull Request to merge feature/tests-example into main if that’s desired for your workflow.
