# CI/CD Pipeline for API Java

## Requirements
1. s3_bucket (Storage Artifacts)
2. Elastic Beanstalk application

## Notes
In path ./src/main/resources/application.yml replace the following info:
info:
  app:
    version: CI_PIPELINE_IID
    commit: CI_COMMIT_SHORT_SHA
    branch: CI_COMMIT_BRANCH
When replace values in application.yml, API looks like:

```bash
{
  "app": {
      "version": 12,
      "commit": "b657a2fa",
      "branch": "main"
    }
}
```
## Deployment
## Local
To deploy this project run

```bash
  PS C:\Users\Ivancho\Documents\Disney\cars-api> ./gradlew clean          

  BUILD SUCCESSFUL in 903ms
  1 actionable task: 1 executed
  PS C:\Users\Ivancho\Documents\Disney\cars-api> ./gradlew build
  BUILD SUCCESSFUL in 12s
  5 actionable tasks: 5 executed
```