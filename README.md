# Icons for the HOI4 Icon Search

This repository holds all the icons and definitions of the [HOI4 Icon Search website](https://wyandotte.github.io/hoi4-icon-search/), an application which lists the icons of [Hearts of Iron IV](http://www.heartsofirongame.com/) to easily find the goal or idea GFX you're looking for.

All rights of "vanilla" icons belong to Paradox Development Studio or Paradox Interactive. All "Kaiserreich" icons are created by the team of the [Kaiserreich mod](http://steamcommunity.com/sharedfiles/filedetails/?id=809903394).

## Adding new icons

1. Add the icons as **PNG** images to `images/goals` folder (or `ideas`, depending on the type.)
2. Create new items at the bottom of either `data/goals.yaml` or `ideas.yaml`, depending on the type.

An item has the following form:

```yaml
-
 name: GFX_goal_socialist_infrastructure
 image: GFX_goal_socialist_infrastructure.png
 tags:
  - Kaiserreich
  - KR
  - production
  - transportation
```
- **name**: The in-game name used in a focus tree or idea file, this name will be copied when a user clicks on the icon.
- **image**: The name of the PNG image (including .png!) that was added in the `images` folder.
- **tags**: Each tag needs to be on it's own line, indented by two spaces.

:exclamation: Make sure there is a dash (`-`) before each item (above the name), and that the `name`, `image` and `tag` are indented by one space.

3. If these changes are pushed to the `master` branch, they are immediately visible on the live site. If you do not see any images, there likely is a problem with your formatting. Roll back and/or consult the YAML file via the GitHub interface to see where the error is.
