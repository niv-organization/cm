# -*- mode: yaml -*-

manifest:
  version: 1.0
 
config:
  admin:
    users: ['nivSwisa1']

automations:
  assign_code_editors:
      if:
        - true
      run:
        - action: add-reviewers@v1
          args:
            reviewers: ['saharAvishag']

calc:
  owners: {{ repo | rankByGitBlame(gt=25) }}
