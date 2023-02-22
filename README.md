# Template for a simple personal website

Adapted from [jasonlai](`https://www.wslai.net/`).

Disclaimer: I do not own any of the images. They are free resources online.

## How to use
1. Clone this repo
1. Modify the desired values
1. Push changes to your cloned repo
1. Deploy this as your github-page
1. Profit

## Customisable values

### Header
Values displayed in the header section are basically extracted from `_config.yml`.

![](screenshots/header.png)

1. Profile picture: Update `profile-photo`. Absolute paths and relative paths, e.g., `assets/img/photo.png`, should both work.
2. Name: Update `name`. This name is also displayed in the footer.
3. Short description: Update `description`. Technically speaking, it does not need to be short, but this is supposed to be a headline and the longer content is left in the `about` section below.
4. Link to resume: Update `resume`. Absolute paths and relative paths, e.g., `./resume.pdf`, should both work.
5. Link to GitHub profile: Update `github_username`. Put only your username.
6. Link to LinkedIn profile: Update `linkedin_username`. The value should be the last part of your LinkedIn URL, i.e., `https://linkedin.com/in/<your name here>`.
7. Link to blog: Update `blog`. Absolute paths and relative paths, e.g., `/blog`, should both work, though relative paths need to be handled with extra care since this template does not include a blog.
8. Link to email address: Update `email`.
9. Background image: Update `background-img`. Absolute paths and relative paths, e.g., `assets/img/photo.png`, should both work.

### About me

The content in this section is extracted from a markdown file `about.md`. Just put whatever you want in that file.

### Timeline

![](screenshots/timeline.png)

Items are rendered based on `_data/experiences.yml`. In this file is a list of experiences with attributes as follows:
* `company`: Info about the company/institute/whatever. It has the following attributes:
	* `name`: Name of the company. As displayed at `2`
	* `link`: Link to the company. `name` becomes clickable if `link` is given. Optional.
	* `logo`: Logo of the company. As displayed at `1`. `logo` becomes clickable if `link` is given. Optional.
* `title`: Your title (or whatever you want to write) when in that company. As displayed at `3`.
* `start`: Start date. As displayed at `4`. It needs to be in the format `YYYY-MM-DD`. `DD` doesn't matter. This field is used to sort the experiences.
* `end`: End date. As displayed at `5`. It needs to be in the format `YYYY-MM-DD`. `DD` doesn't matter. Can be Something else like `Present` as well.

A sample experience may look like:
```yaml
- company:
    name: Google
    link: https://google.com/
    logo: assets/img/google.svg
  title: Software engineer
  start: 2019-07-01
  end: 2021-01-01
```

### Publications

![](screenshots/pub.png)

Items are rendered based on `_data/publications.yml`. In this file is a list of publications with attributes as follows:
* `title`: Title of that paper. As displayed at `2`.
* `screenshot`: Screenshot of your demo. As displayed at `1`. Can be `.gif` as well.
* `authors`: Authors of that paper. An author has the following attributes:
	* `name`: Name of the author. As displayed at `3` If the name matches yours, the name is displayed in bold.
	* `link`: Link to the author. `name` becomes clickable if `link` is given. Optional.
* `published_at`: Where the paper was published. Can be something like `To appear` as well. As displayed at `4`.
* `year`: When the paper was published. As displayed at `4`.
* `paper`: Link to the paper. As displayed at `5`.
* `site`: Link to the project website or demo. As displayed at `6`. Optional.

A sample publication may look like:
```yaml
- title: Face distortion aftereffects evoked by featureless first-order stimulus configurations 
  screenshot: assets/img/science-magic.gif
  authors:
    - name: Pál Vakli
      link: https://pubmed.ncbi.nlm.nih.gov/?term=Vakli+P&cauthor_id=23403400
    - name: Kornél Németh
    - name: Márta Zimmer
    - name: Stefan R Schweinberger
    - name: Gyula Kovács
    - name: James Clerk Maxwell
  published_at: Front Psychol
  year: 2012
  paper: https://pubmed.ncbi.nlm.nih.gov/23403400/
  site: https://pubmed.ncbi.nlm.nih.gov/23403400/
```
