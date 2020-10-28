commit_lint.check
welcome_message.greet

# Mainly to encourage writing up some reasoning about the PR, rather than
# just leaving a title
if github.pr_body.length < 5
  fail "Please provide a summary in the Pull Request description"
end

# Make it more obvious that a PR is a work in progress and shouldn't be merged yet
warn("PR is classed as Work in Progress") if github.pr_title.include? "[WIP]"

# Warn when there is a big PR
warn("Lots of changes here!") if git.lines_of_code > 500

prose.disable_linters = ["misc.scare_quotes", "misc.tense_present"]
prose.lint_files
prose.check_spelling markdown_files
