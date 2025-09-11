# GitHub Metrics Setup

This repository is configured with two lowlighter/metrics cards that showcase:

## 📊 Metrics Cards

### 1. Main Metrics Card (`github-metrics.svg`)
- **Contribution Calendar**: Full year isometric calendar showing daily contributions
- **Language Statistics**: Most used programming languages with GitHub color scheme
- **Repository Overview**: Basic repository statistics and community metrics

### 2. Activity Metrics Card (`github-metrics-activity.svg`)
- **Recent Activity**: Last 14 days of activity including commits, issues, PRs
- **Achievements**: GitHub achievements with detailed display
- **Repository Metadata**: Repository statistics and contribution insights

## 🔧 Setup Instructions

To enable automatic metrics generation, you need to:

1. Go to your GitHub repository settings
2. Navigate to `Settings` > `Secrets and variables` > `Actions`
3. Create a new repository secret named `METRICS_TOKEN`
4. Generate a Personal Access Token with the following permissions:
   - `public_repo` (for public repositories)
   - `read:user`
   - `read:org` (if you want organization statistics)

## 🚀 How it Works

- **Automatic Updates**: The workflow runs daily at midnight (UTC+8)
- **Manual Trigger**: You can manually run the workflow from the Actions tab
- **Commit Trigger**: Metrics update automatically when pushing to main/master branch

The generated SVG files are committed back to the repository and displayed in the README.md file.

## 📝 Customization

You can modify the metrics configuration in `.github/workflows/metrics.yml` to:
- Add more plugins (habits, calendar, notable contributions, etc.)
- Change the update schedule
- Modify the appearance and colors
- Include additional statistics

For more configuration options, visit: https://github.com/lowlighter/metrics