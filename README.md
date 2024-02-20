# Kagi Bangs

This is a repository of bangs used by [Kagi Search](https://kagi.com). It does not include unmodified DuckDuckGo bangs.

## Contribution Guidelines

Kagi Staff and maintainers of this repo have final say, but a good bang submission should follow some basic guidelines.

The website must be reasonably well-known and widely used.
For example, popular commerical services and forums are OK.
Low-traffic independent sites, such as startups, local businesses, or personal blogs, are not OK.

The trigger must be specific to the website, not a generic term or word.
For example, "amazon.com" can have "!amazon" but not "!groceries".

Each trigger must be unique.
You can test your trigger on Kagi to see if a bang already exists with that trigger.

You can use the Categories list below to find the Category and Subcategory that fits best.
If you cannot find one, it can be omitted, or we can consider adding a new one.

## Bang Format

```jsonc
[
  // ...
  {
    "s": "Metacritic",
    "d": "www.metacritic.com",
    "t": "mc",
    "u": "https://www.metacritic.com/search/{{{s}}}/",
    "c": "Online Services",
    "sc": "Search"
  }
]
```

Key   | Description  | Required | Notes
------|--------------|----------|------
`s`   | Website name | yes      |
`d`   | Domain       | yes      |
`t`   | Trigger      | yes      | Letters and numbers only, no spaces or special characters
`u`   | URL template | yes      | Use `{{{s}}}` for query placeholder.
`c`   | Category     | no       |
`sc`  | Subcategory  | no       |
`fmt` | Format flags | no       | See below.

### Format Flags

The `fmt` field exists to tweak the behavior of how the bang is executed.
For the majority of bangs, you do not need to specify this - we use defaults that work for 99.9% of bangs.
But, it can be useful depending on the behavior of the website.

Flag                       | Description
---------------------------|----------------------
`open_base_path`           | When the bang is invoked with no query, opens the base path of the URL (`/`) instead of any path given in the template (e.g., `/search`)
`url_encode_placeholder`   | URL encode the search terms. Some sites do not work with this, so it can be disabled by omitting this.
`url_encode_space_to_plus` | URL encodes spaces as `+`, instead of `%20`. Some sites only work correctly with one or the other.

By default, all of these are enabled.
If you specify `fmt`, you must exhaustively specify each options you would like enabled.

## Categories

This is a list of possible categories, with their corresponding subcategories.

#### Entertainment

<details>
<summary>Subcategories</summary>

  - Audio
  - Blogs
  - Blogs (intl)
  - Comics
  - Events
  - Forum
  - Games (Minecraft)
  - Games (Pokemon)
  - Games (WOW)
  - Games (general)
  - Games (offline)
  - Games (specific)
  - Misc
  - Movies
  - Music
  - Radio
  - Sports
  - TV

</details>

#### Man Page

<details>
<summary>Subcategories</summary>

  - Sysadmin

</details>

#### Multimedia

<details>
<summary>Subcategories</summary>

  - Books
  - Docs
  - Games (general)
  - General
  - Images
  - Movies
  - Music
  - Music (Folk)
  - Music (Lyrics)
  - Video

</details>

#### News

<details>
<summary>Subcategories</summary>

  - Aggregators
  - Broadcast
  - Business
  - International
  - Magazine
  - Magazine (car)
  - Magazine (fashion)
  - Newspaper
  - Newspaper (intl)
  - Online
  - Specialty
  - Weather

</details>

#### Online Services

<details>
<summary>Subcategories</summary>

  - Events
  - Google
  - Jobs
  - Maps
  - Search
  - Search (DDG)
  - Search (Private)
  - Search (Real-time)
  - Search (non-US)
  - Social
  - Social (intl)
  - Social news/links
  - Sysadmin
  - Tools
  - Tools (URLs)
  - Tools (fundraising)
  - Tracking

</details>

#### Research

<details>
<summary>Subcategories</summary>

  - Academic
  - Academic (biology)
  - Academic (math/cs)
  - Food
  - Government
  - Health
  - Law
  - Learning
  - Learning (intl)
  - Local
  - Real Estate
  - Reference
  - Reference (fun)
  - Reference (religion)
  - Reference (science)
  - Reference (words intl)
  - Reference (words)
  - Topical
  - Travel

</details>

#### Shopping

<details>
<summary>Subcategories</summary>

  - Big box/department
  - Online
  - Online (deals)
  - Online (intl)
  - Online (marketplace)
  - Services
  - Tech
  - Tech (domains)

</details>

#### Tech

<details>
<summary>Subcategories</summary>

  - Blogs
  - Blogs (intl)
  - Chakra
  - Companies
  - Cryptocurrency
  - Design
  - Domains
  - Downloads
  - Downloads (add-ons)
  - Downloads (apps)
  - Downloads (code)
  - Downloads (software)
  - Language (perl)
  - Languages (.net)
  - Languages (Crystal)
  - Languages (Mathematica)
  - Languages (Matlab)
  - Languages (c++)
  - Languages (clojure)
  - Languages (cocoa)
  - Languages (coldfusion)
  - Languages (csharp)
  - Languages (d)
  - Languages (erlang)
  - Languages (go)
  - Languages (haskell)
  - Languages (html)
  - Languages (java)
  - Languages (javascript)
  - Languages (latex)
  - Languages (lisp)
  - Languages (lua)
  - Languages (other)
  - Languages (perl)
  - Languages (php)
  - Languages (python)
  - Languages (r)
  - Languages (racket)
  - Languages (ruby)
  - Languages (scala)
  - Languages (scheme)
  - Languages (vala)
  - Libraries/Frameworks
  - Libraries/Frameworks (KDE)
  - Libraries/Frameworks (wordpress)
  - Programming
  - Search (DDG)
  - Startups
  - Sysadmin
  - Sysadmin (Arch)
  - Sysadmin (Fedora)
  - Sysadmin (FreeBSD)
  - Sysadmin (Gentoo)
  - Sysadmin (RedHat)
  - Sysadmin (Ubuntu)
  - Sysadmin (debian)
  - Sysadmin (man)
  - Sysadmin (network)
  - Sysadmin (packages)
  - Tools
  - Tools (URLs)

</details>

#### Translation

<details>
<summary>Subcategories</summary>

  - General
  - Google

</details>
