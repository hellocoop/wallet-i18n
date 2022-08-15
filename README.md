# Hellō Wallet Translation Guide
Welcome to the Hellō Wallet i18n repository! Great to have you here.  
In this repository, we coordinate all community-driven translation efforts for [wallet.hello.coop](https://wallet.hello.coop).

This step-by-step guide is written assuming that this may be your first time contributing on GitHub. If you're familiar with GitHub, you can skim through this guide. If you have questions or concerns, feel free to file an [issue](https://github.com/hellocoop/wallet-i18n/issues/new) or send us an [email](mailto:contact@hello.coop).

## Currently supported locales
| Short code | Language | Status | Contributors | 
| --- | ----------- | ----------- | ----------- |
| en | English | Complete | Hellō
| hi | Hindi | Complete | [Rohan Harikumar](https://github.com/rohanharikr), S. Harikumar, Vinod Kandra
| ar | Arabic | Complete | Kishor Kumar
| fr | French | Complete | Jennifer Hardt
| de | German | Complete | Nicole Fior-Greant, [Zak Greant](https://github.com/zakgreant)
| es | Spanish | Complete | Santiago Madrid
| xx | Don't see a locale? PR's welcome! | In Progress | your-name-here

### Want to add a locale or make corrections? Follow the guide below and we will happily review and merge!

## Adding or editing a locale
0. **Log in to GitHub**  
*If you don't have an account, follow this [guide](https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account) to create one.*
1. **Fork this repository**  
*Click the `Fork` button on the top right. This will create your own personal copy of the repository (known as a fork).*
2. **Add yourself to locales table**  
*To let everyone know that a new locale is in progress, please click on the edit icon on the top right and add the locale short code, language, status as "In Progress", and your name (which links to your GitHub profile) to the locales table. Once the changes have been saved, please send us a Pull request. If you are unfamilar with sending Pull requests, please refer to [this](#submitting-a-pull-request) section.*  
3. **Clone the fork to your machine**  
*If you are unfamilar with git operations, this is a good [guide](https://education.github.com/git-cheat-sheet-education.pdf) to get started.*
4. **Duplicate `en.json` and rename**  
*In the `locale` directory, duplicate `en.json` (this is the base for our translations) and rename to the short code of the locale you are planning to add (eg: `ja.json` for Japanese locale). You can find short codes for locales [here](https://www.loc.gov/standards/iso639-2/php/code_list.php). If you want to make any corrections, simply edit the existing locale file.*
5. **Commit and push changes**  
*If you are using VS Code, we recommend installing the [i18n ally plugin](https://marketplace.visualstudio.com/items?itemName=lokalise.i18n-ally) for a better localising experience which also enforces consistent formatting across locale files.*
6. **Submit a Pull request**  
*Please make sure the title of the Pull request matches the file name. In case of corrections, prepend the Pull request title with `fix:`. (eg: "fix: de.json").*

## Working with variables

While localising, you'll come across text that contains keys contained in curly braces, such as `Continue with {provider}` and `Welcome {name}`.
The keys should **not** be translated, neither should "Hellō".

These keys are replaced with a value generated by the system. For example, `{date}` would be replaced with a date such as `22 March 2022`. See the table below for a description of each key.

| Variable | Description                                        | Example Occurrence                   | Example Output                                   |
| ----------- | -------------------------------------------------- | ------------------------------------ | ------------------------------------------------ |
| {provider}  | {provider} can be Google, Facebook, etc.           | Continue with {provider}             | Continue with Google                             |
| {appName}   | {appName} can be Spotify, YouTube, etc.            | Return to {appName}                  | Return to Spotify                                |
| {date}      | {date} can be 22 March 2022, etc.                  | Member since {date}                  | Member since 22 March 2022                       |
| {contact}   | {contact} can be an email address or phone number. | {contact} has already been verified  | john.smith@example.com has already been verified |
| {label}     | {label} can be an email address or username.       | {provider} {label} is now preferred  | Google (john.smith@gmail.com) is now preferred   |
| {language}  | {language} can be English, Hindi, etc.             | Preferred language is now {language} | Preferred language is now English                |
| {address}   | {address} is an ethereum hexadecimal address.      | Wallet Connected ({address})         | Wallet Connected (0xb794...579268)             |
| {name}   | {name} is user provided preferred name.               | Welcome {name}                       | Welcome John             |

`<br/>` - Indicates a line break; the text following this would be pushed to the next line. When localising, please add `<br/>` where necessary for readibility.

## Submitting a Pull Request
In the GitHub repo page (https://github.com/your-username/wallet-i18n), click on the `Pull requests` tab and then the `New pull request` button. Please merge your changes to the `main` branch of `hellocoop/wallet-i18n`. Learn more [here](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).

## License
[CC0-1.0](./license.txt)<br/>
<img src="https://cdn.hello.coop/images/cc0-icon.png" alt="CC0-1.0" style="width: 120px; margin-top: 6px;" />

---

[Propose changes to this guide](https://github.com/hellocoop/wallet-i18n/edit/main/README.md)
