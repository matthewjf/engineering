![Web Crawler](images/web_crawler.png)

# Topics to cover
### Failures and retries
  - Break up the crawling into a pipeline (fetching vs parsing)
  - Automatic retries using SQS and lambdas or serverless technology
### Politeness
  - Fetch the robots.txt before crawling the page
  - Check for last visited timestamp
  - Redis with domain key for rate limiting
### DNS caching and multiple providers
  - DNS caching in the crawlers
  - Spread load across multiple DNS providers
### Identical content
  - Hash the content and store in the DB to check for existence
  - Also could use bloom filters (false positives)
