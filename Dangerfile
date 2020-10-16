commit_lint.check
welcome_message.greet

# Make it more obvious that a PR is a work in progress and shouldn't be merged yet
warn("PR is classed as Work in Progress") if github.pr_title.include? "[WIP]"

# Warn when there is a big PR
warn("Lots of changes here!") if git.lines_of_code > 500

prose.disable_linters = ["misc.scare_quotes", "misc.tense_present"]
prose.lint_files
