name: Super-Linter

# Run this workflow every time a new commit pushed to your repository
on: push

jobs:
  # Set the job key. The key is displayed as the job name
  # when a job name is not provided
  super-lint:
    # Name the Job
    name: Lint code base
    # Set the type of machine to run on
    runs-on: ubuntu-latest

    steps:
      # Checks out a copy of your repository on the ubuntu-latest machine
      - name: Checkout code
        uses: actions/checkout@v2

      # Runs the Super-Linter action
      - name: Run Super-Linter
        uses: github/super-linter@v3
        env:
          DEFAULT_BRANCH: main
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}---
title: GitHub Insights Documentation
shortTitle: GitHub Insights
intro: 'Understand and improve your software delivery process through data with {% data variables.product.prodname_insights %}. You can view customized reports based on data from {% data variables.product.prodname_enterprise %}.'
featuredLinks:
  gettingStarted:
    - /insights/installing-and-configuring-github-insights/about-github-insights
    - /insights/installing-and-configuring-github-insights/system-overview-for-github-insights
    - /insights/installing-and-configuring-github-insights/installing-github-insights
    - /insights/exploring-your-usage-of-github-enterprise/viewing-key-metrics-and-reports
  popular:
    - /insights/installing-and-configuring-github-insights/about-data-in-github-insights
    - /insights/exploring-your-usage-of-github-enterprise/metrics-available-with-github-insights
redirect_from:
  - /github/installing-and-configuring-github-insights
versions:
  enterprise-server: '*'
---

{% link_with_intro /installing-and-configuring-github-insights %}
{% link_with_intro /exploring-your-usage-of-github-enterprise %}
