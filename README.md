# Change log

## 0.0.1c
- change max-length of project key to 32
- change project key rule to [A-Z][A-Z0-9_]*

## 0.0.1b
- add support for issue id auto-complete function
- fix creating sub issue bug

# introduction

https://github.com/kaikuo/issue_id.git

fork from 

https://github.com/VoronyukM/issue_id

# Installation notes

Copy issue_id directory to: #{RAILS_ROOT}/plugins
Run: 

```
bundle exec rake redmine:plugins:migrate RAILS_ENV=production
```

# docker iamges

sameersbn/postgresql:9.4-23
sameersbn/redmine:2.6.1

# master commands

su redmine

cd ~/redmine/plugins && git clone https://github.com/kaikuo/issue_id.git && bundle exec rake redmine:plugins:migrate RAILS_ENV=production

# branch  commands
su redmine

cd ~/redmine/plugins && git clone https://github.com/kaikuo/issue_id.git && cd issue_id && git checkout -t origin/autoid && cd ../..  && bundle exec rake redmine:plugins:migrate RAILS_ENV=production

bundle exec rake redmine:plugins:migrate RAILS_ENV=production

bundle exec rake redmine:plugins:migrate RAILS_ENV=development

Restart Redmine/ChiliProject
