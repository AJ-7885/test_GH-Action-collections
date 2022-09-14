GITHUB ACTIONS WORKFLOW TO TRIGGER ACTION ON ANOTHER REPOSITORY:


curl --fail -X POST "https://github.com/idealo/ids-assets/blob/main/.github/workflows/deploy-to-akamai/dispatches"  -H "Accept: application/vnd.github.v3+json"  -H "Content-Type: application/json" \ -H "Authorization: Bearer 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" --data "{\"ref\":\"${ref}\",\"inputs\":${inputs}}"


curl -H "Accept: application/vnd.github+json" -H "Authorization: {{GH-TOKEN}}" --request POST --data '{"event_type": "do-something"}' https://api.github.com/repos/idealo/ids-assets/dispatches


 curl \
  -X POST -u "aj-7885:{{GH-TOKEN}}"  \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/AJ-7885/main-repo/actions/workflows/deploy.yml/dispatches \
  -d '{"ref":"main", "inputs": { "name":"Command Line User", "home":"CLI" }}'


 curl \
  -X POST -u "aj-7885:{{GH-TOKEN}}"  \
  -H "Accept: application/vnd.github.v3+json" \
  https://api.github.com/repos/idealo/ids-assets/actions/workflows/deploy-to-akamai.yml/dispatches \
  -d '{"ref":"main"}'
  -d '{"ref":"main", "inputs": { "name":"Command Line User", "home":"CLI" }}'



 curl -X POST https://api.github.com/repos/idealo/ids-assets/actions/workflows/deploy-to-akamai.yml/dispatches\
 -H “Accept: application/vnd.github.everest-preview+json” \
  -u {{GH-TOKEN}} \

_____________________WORKING SCRIPT____________________________

curl   -X POST -u "aj-7885:{{GH-TOKEN}}"    -H "Accept: application/vnd.github.v3+json"   https://api.github.com/repos/idealo/ids-assets/actions/workflows/deploy-to-akamai.yml/dispatches   -d '{"ref":"main"}'




main-repo


curl   -X POST -u "aj-7885:{{GH-TOKEN}}"    -H "Accept: application/vnd.github.v3+json"    https://api.github.com/repos/AJ-7885/main-repo/actions/workflows/deploy.yml/dispatches  -d '{"ref":"main"}'




 https://api.github.com/repos/AJ-7885/main-repo/actions/workflows/deploy.yml/dispatches
