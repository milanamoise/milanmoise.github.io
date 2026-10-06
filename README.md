# Milan Moise — Jekyll Portfolio

## Scope
This is an original Jekyll starter inspired by the reference site's introduction, profile links, project summaries, and project pages. It is not a verified visual replica. The Google Site blocked automated access, so its exact copy, photos, page structure, and videos have not been migrated. Project summaries use details previously provided in chat. Review all descriptions before publishing; remove any project you do not want included.

## Publish through GitHub's website
1. Create or open your public `YOURUSERNAME.github.io` repository.
2. Extract the ZIP. Upload the CONTENTS of the `portfolio` folder into the repository root, not the folder itself. Preserve folders beginning with underscores. GitHub's Upload files interface can accept folders dragged from your computer.
3. Replace your old `_config.yml` and homepage with these files. Delete an existing `index.md` if you use this `index.html`; keep only one homepage. Remove old theme settings and any `.nojekyll` file. These layouts provide their own styling, so no theme is needed.
4. Edit `_config.yml`: set `url` to `https://YOURUSERNAME.github.io`. Keep `baseurl: ""` for this user-site repository. Add your GitHub, LinkedIn, email, optional photo and resume paths. Blank values hide those links.
5. Commit changes to `main`.
6. Open Settings > Pages. Choose Deploy from a branch, select main and / (root), and Save. The branch publishing flow builds Jekyll on GitHub; Ruby does not need to be installed on your computer.
7. Check the Pages deployment in Actions. Open the site when it finishes. If it fails, read the failed build log.

If you use a repository named `portfolio` instead, set `baseurl: "/portfolio"`; the website will be at `https://YOURUSERNAME.github.io/portfolio/`.

## Customize
- `_config.yml`: name, introductory text, location, links, resume, photo.
- `index.html`: homepage structure and project list.
- `_layouts/default.html`: shared header, sidebar and footer.
- `_layouts/project.html`: project writeup structure.
- `assets/css/style.css`: colors, typography, spacing, mobile layout.
- `about.md`: background, education and experience.
- `_projects/*.md`: project descriptions and tags. Lower `order` appears first.
- `assets/images/`: your own photographs, diagrams and screenshots.
- `assets/files/`: your resume PDF.
- `404.html`: missing-page message.
- `Gemfile`: optional local preview dependencies.

## Add images and a resume
Upload `profile.jpg` to `assets/images/`, then set `avatar: "/assets/images/profile.jpg"` in `_config.yml`. Until then, the sidebar shows MM initials.
Upload `resume.pdf` to `assets/files/`, then set `resume_url: "/assets/files/resume.pdf"`.
To show a project thumbnail and its hero image, uncomment `image` and `image_alt` in that project's front matter and upload the matching image. Keep filenames lowercase without spaces.

## Add a project
Copy an existing `_projects/*.md` file to a new filename. Edit its title, order, tags, summary and body. Jekyll automatically creates its page and adds it to the homepage. You do not need a date in the filename because this uses a projects collection rather than blog posts.

## Optional local preview
With Ruby and Bundler installed, run `bundle install`, then `bundle exec jekyll serve` from the portfolio directory. Visit http://localhost:4000. Restart after editing `_config.yml`.

## Validation
The package's file structure and internal references were checked. A Jekyll build was not run in the authoring environment because Ruby/Bundler were unavailable. GitHub's deployment will provide the build result.
