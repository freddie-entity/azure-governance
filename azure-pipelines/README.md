# Sample Azure Pipeline YAML structure
```yaml
name: $(BuildID)
trigger:
- main
pool:
  name: 'MyAgent'
#   vmImage: 'ubuntu-latest'
variables:
  mykey: myvalue
# - template: <path_to_yaml>
stages:
- stage: Build
  displayName: Build
  condition: ""
  jobs:
    # - template: <path_to_yaml>
    - job: FirstBuild
      displayName: First Build
    #   dependsOn: <another_job>
      steps:
        # - template: <path_to_yaml>
        - bash: |
            echo 'First Build'
          displayName: First Build
      
```