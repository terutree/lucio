# lucio
Homelab2022

Følgede er gjort 14:47 07.12.2022:
* laget en ny server på proliant boksen: prod2022
* laget en ny switch i hyperv for å få nett på prod2022
* installert og registrert gitlabs runner på prod2022 etter oppskrift på nett
* installert chocolatey på prod2022
* installert edge, dotnet6, dotnet6 sdk, webdeploy på prod2022 med chocolatey
* installert iis på prod2022 med basic authentication og url redirect som tilvalg (ellers standard) 
* endret gitlabs service fra NETWORK SERVICE til servicebruker og tipper creds i secret skal være 1:1 (trolig ikke nødvendig, men måtte kjøre som noe :shrug)
* endret webdeploy service til å kjøre som samme servicebruker
* endret dotnet.yml til å gå mot forhåpentligvis riktige plasser

15:54 10.12.2022
tildligere udokumenterte endringer fra 07.12
* la til webdeploy i PATH 
* det virker nå, men måtte sette opp siden som en webapplication ettersom alt kompileres til dll og ikke html. Mulig vi kan gjøre noe mer elegant her, men fuckit.

https://docs.gitlab.com/ee/ci/runners/runners_scope.html#specific-runners
https://docs.gitlab.com/runner/register/index.html

Bruker jeg egentlig web-deploy??
https://learn.microsoft.com/en-us/previous-versions/windows/it-pro/windows-server-2008-r2-and-2008/dd568996(v=ws.10)
https://learn.microsoft.com/en-us/iis/publish/using-web-deploy/configure-the-web-deployment-handler

https://github.com/marketplace/actions/iis-deploy