# PCF.AddressFinderAU
Dynamics 365/PowerApps PCF Control for AddressFinder (https://addressfinder.com.au/) - Australian Address

This PCF Control is a modified version of Sankal Bansal's PCF of New Zealand-based AddressFinder (https://github.com/SankalpBansal/PCF-AddressFinderNZ)

This PCF Control will bind the full address to a specific field and map the granular address breakdown:
* Address Name (Full Address) - main field
* Address Line 1
* Address Line 2
* Suburb
* State
* Postcode
* Country - note: country is hardcoded to "Australia" as the AddressFinder API only returns a specific country

# Building

Update the version in the xml file: `Solution/AddressFinderControlAU/Other/Solution.xml`

Update the version in the xml file: `AddressFinderAU/ControlManifest.Input.xml`

In the root folder

`npm install`
`npm build`

Build a new release - replacing the version number in the file appropriately (this will build and package a release)

`msbuild Solution\AddressFinderControlAU\AddressFinderControlAU.cdsproj /t:build /restore /p:configuration=Release`

Copy the release binary into the Release folder:

`cp .\Solution\AddressFinderControlAU\bin\Release\AddressFinderControlAU.zip .\Release\.`
