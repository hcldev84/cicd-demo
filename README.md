# CICD Demo

GitHub settings:

- Create a branch protection rule to only allow merging to the main branch through Pull Request. Remember to also enable the rule "Do not allow bypassing the above settings"
- Test branch protection rule. 

Jenkins settings:
- Manage Jenkins - System - "Github API usage rate limiting strategy": "Throttle at/near rate limit"
- M1-Pipeline - Configuration - "Discover branches": "All branches"

