# Compass Sprites

## Setup

1. Install Ruby. Gems comes with Ruby
2. Install compass in comand line: `gem install compass`. Sass is automatically installed along with compass.
3. `gem install chunky_png`
4. `compass create compass_sprites`
5. `cd compass_sprites`
6. `compass watch`

## config.rb

```rb
require 'compass/import-once/activate'
require 'chunky_png'

http_path = "/"
css_dir = "css"
sass_dir = "sass"
images_dir = "img"
```

## sass/sprite.scss

```scss
@import "compass/utilities/sprites";
@import "travel_icon/*.png";
@include all-travel_icon-sprites;	
```

## Results

### css/sprite.css

```css
/* line 72, travel_icon/*.png */
.travel_icon-sprite, .travel_icon-1, .travel_icon-2, .travel_icon-3, .travel_icon-4 {
  background-image: url('/img/travel_icon-s35a4a562e1.png');
  background-repeat: no-repeat;
}

/* line 84, ../../../../../RailsInstaller/Ruby2.0.0/lib/ruby/gems/2.0.0/gems/compass-core-1.0.3/stylesheets/compass/utilities/sprites/_base.scss */
.travel_icon-1 {
  background-position: 0 0;
}

/* line 84, ../../../../../RailsInstaller/Ruby2.0.0/lib/ruby/gems/2.0.0/gems/compass-core-1.0.3/stylesheets/compass/utilities/sprites/_base.scss */
.travel_icon-2 {
  background-position: 0 -960px;
}

/* line 84, ../../../../../RailsInstaller/Ruby2.0.0/lib/ruby/gems/2.0.0/gems/compass-core-1.0.3/stylesheets/compass/utilities/sprites/_base.scss */
.travel_icon-3 {
  background-position: 0 -1920px;
}

/* line 84, ../../../../../RailsInstaller/Ruby2.0.0/lib/ruby/gems/2.0.0/gems/compass-core-1.0.3/stylesheets/compass/utilities/sprites/_base.scss */
.travel_icon-4 {
  background-position: 0 -2880px;
}
```
