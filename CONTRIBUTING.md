# Contributing To Grignr Happens By
Thank you for your interest in contributing to this mod. This project is very open to contributions,
from people of all skill levels and backgrounds.

Please note we have a [code of conduct](#contributor-covenant---code-of-conduct), please follow it in all your interactions with the project.

## Pull Request Process

1. When adding compatibility with another mod, make sure it is appropriately isolated using `MayRequire`, `PatchOperationFindMod` or an entry in [loadFolders.xml](loadFolders.xml)
2. Ensure your contribution is YouTube friendly and follows our code of conduct.
3. Update the README.md if necessary.
4. Make sure you add any `loadAfter` entries in [About.xml](About/About.xml)

### In Code
Be warned we have to be strict here, no stolen code! Breaches will be dealt will as laid out in the code of conduct.
Also please follow good code hygiene. If you make a mistake our reviewers should be able to help you out. Please make an issue for any change you think needs code to discuss first to make sure it won't be wasted effort and get help.

Try to be careful not to force other mods to be required. Use loadFolders where needed.

We will also be very strict about DLLs. When you use another mod to build on C# likes to take a copy of the DLLs and put them in it's own output folder. Any PR with someone else's DLLs in it will be rejected immediately. You can simply select `Copy Local` to be false in Visual Studio or set `<Private>False</Private>` in the `.csproj` file for the `Reference` entry achieves this e.g. to include HAR without accidentally copying their DLL:

```xml
<Reference Include="AlienRace">
  <HintPath>..\..\..\..\839005762\1.4\Assemblies\AlienRace.dll</HintPath>
  <Private>False</Private>
</Reference>
```

Please use relative paths like the above, any PR with your personal Steam folder in a path will be rejected. This can be tricky to get right. It's often added with an exact path. We have people working on this that do not use Steam so any steam paths would just be broken for them. Fortunately you can go pretty wild with these things as you can add conditions for example this will use the RimWorld dll if it's where it is expected to be, however if not it will default to using a NuGet package. You can use this same trick to add more options for paths if your machine is a bit different and the example paths aren't working for you. Please note that the given paths expect the code to be checked out into your mods folder.

# Contributor Covenant - Code of Conduct

## Our Pledge

We as members, contributors, and leaders pledge to make participation in our
community a harassment-free experience for everyone, regardless of age, body
size, visible or invisible disability, ethnicity, sex characteristics, gender
identity and expression, level of experience, education, socio-economic status,
nationality, personal appearance, race, caste, color, religion, or sexual
identity and orientation.

We pledge to act and interact in ways that contribute to an open, welcoming,
diverse, inclusive, and healthy community.

## Our Standards

Examples of behavior that contributes to a positive environment for our
community include:

* Demonstrating empathy and kindness toward other people
* Being respectful of differing opinions, viewpoints, and experiences
* Giving and gracefully accepting constructive feedback
* Accepting responsibility and apologizing to those affected by our mistakes,
  and learning from the experience
* Focusing on what is best not just for us as individuals, but for the overall
  community

Examples of unacceptable behavior include:

* The use of sexual language or imagery, and sexual attention or advances of
  any kind
* Trolling, insulting or derogatory comments, and personal or political attacks
* Public or private harassment
* Publishing others' private information, such as a physical or email address,
  without their explicit permission
* Other conduct which could reasonably be considered inappropriate in a
  professional setting

## Enforcement Responsibilities

Community leaders are responsible for clarifying and enforcing our standards of
acceptable behavior and will take appropriate and fair corrective action in
response to any behavior that they deem inappropriate, threatening, offensive,
or harmful.

Community leaders have the right and responsibility to remove, edit, or reject
comments, commits, code, wiki edits, issues, and other contributions that are
not aligned to this Code of Conduct, and will communicate reasons for moderation
decisions when appropriate.

## Scope

This Code of Conduct applies within all community spaces, and also applies when
an individual is officially representing the community in public spaces.
Examples of representing our community include using an official e-mail address,
posting via an official social media account, or acting as an appointed
representative at an online or offline event.

## Enforcement

Instances of abusive, harassing, or otherwise unacceptable behavior may be
reported to the community leaders responsible for enforcement via creating a Github issue with the REPORT title. You can use [KeyBase](https://keybase.io/encrypt) to make an encrypted message to conceal any private information. Please address it to [Dexter on KeyBase](https://keybase.io/dexter)
All complaints will be reviewed and investigated promptly and fairly.

All community leaders are obligated to respect the privacy and security of the
reporter of any incident.

## Enforcement Guidelines

Community leaders will follow these Community Impact Guidelines in determining
the consequences for any action they deem in violation of this Code of Conduct:

### 1. Correction

**Community Impact**: Use of inappropriate language or other behavior deemed
unprofessional or unwelcome in the community.

**Consequence**: A private, written warning from community leaders, providing
clarity around the nature of the violation and an explanation of why the
behavior was inappropriate. A public apology may be requested.

### 2. Warning

**Community Impact**: A violation through a single incident or series of
actions.

**Consequence**: A warning with consequences for continued behavior. No
interaction with the people involved, including unsolicited interaction with
those enforcing the Code of Conduct, for a specified period of time. This
includes avoiding interactions in community spaces as well as external channels
like social media. Violating these terms may lead to a temporary or permanent
ban.

### 3. Temporary Ban

**Community Impact**: A serious violation of community standards, including
sustained inappropriate behavior.

**Consequence**: A temporary ban from any sort of interaction or public
communication with the community for a specified period of time. No public or
private interaction with the people involved, including unsolicited interaction
with those enforcing the Code of Conduct, is allowed during this period.
Violating these terms may lead to a permanent ban.

### 4. Permanent Ban

**Community Impact**: Demonstrating a pattern of violation of community
standards, including sustained inappropriate behavior, harassment of an
individual, or aggression toward or disparagement of classes of individuals.

**Consequence**: A permanent ban from any sort of public interaction within the
community.

## Attribution

This Code of Conduct is adapted from the [Contributor Covenant][homepage],
version 2.1, available at
[https://www.contributor-covenant.org/version/2/1/code_of_conduct.html][v2.1].

Community Impact Guidelines were inspired by
[Mozilla's code of conduct enforcement ladder][Mozilla CoC].

For answers to common questions about this code of conduct, see the FAQ at
[https://www.contributor-covenant.org/faq][FAQ]. Translations are available at
[https://www.contributor-covenant.org/translations][translations].

[homepage]: https://www.contributor-covenant.org
[v2.1]: https://www.contributor-covenant.org/version/2/1/code_of_conduct.html
[Mozilla CoC]: https://github.com/mozilla/diversity
[FAQ]: https://www.contributor-covenant.org/faq
[translations]: https://www.contributor-covenant.org/translations