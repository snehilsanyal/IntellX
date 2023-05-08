## Utilities 

Folder for Data utility functions

1. Data scrapers
- Slack, Jira
- Sight
2. Data transformations
- Tokenizers
- Preprocessing of all sorts

### How to use

```py3
from intellx.utils.data import jira_scraper

data = jira_scraper(verbose = True)

print(data)
```