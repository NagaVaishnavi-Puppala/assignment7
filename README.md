
# InstaCart

Created a Grocery Delivery Website using Css/Html/Sass
## Authors

- Vaishnavi Puppala


## Feature Used

 1)for responsive banner section used css grid.
 2)for responsive category section used css grid.
 3)for responsive products section used css grid.
 4)for responsive about section used css flexbox.
 5)for responsive gallery section used css grid.
 6)for responsive review card section used css grid.
 7)for responsive blogs section used css grid.
 8)for responsive contact form section used css grid and flexbox.
 9)for responsive footer section used css grid.

### Variables-to store value color and fonts

$black:#222;
$white:#fff;

###  Custom properties

$light-color:#666;
$light-bg:#f3f3f3;
font-family: 'Poppins', sans-serif;
$border:.1rem solid rgba(0,0,0,.1);
$box-shadow:0 .5rem 1rem rgba(0,0,0,.1);

### Nesting 
 nesting-nesting child selector inside parent
.box{
      display: flex;
      align-items: center;
      gap:1.5rem;
      margin-bottom: 1.5rem;
      position: relative;

      .fa-times{
        position: absolute;
        top:50%; right:2rem;
        transform: translateY(-50%);
        font-size: 2rem;
        color:$light-color;
        cursor: pointer;

        &:hover{
          color:$green;
        }
      }
### Mixins
 mixin-We use them to group together multiple CSS declarations for reuse throughout our projects
 @mixin grid($val) {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax($val, 1fr));
  gap:1.5rem;
}
### Functions

@function set-text-color($color) {
  @if(lightness($color) > 70) {
      @return #000;
  } @else {
      @return #fff;
  }
}

// set the background and text color
@mixin set-background($color) {
  background-color: $color;
  color: set-text-color($color);
}
### Placeholder Selectors
%heading{
  text-shadow: 1px 1px 1px $primaryColor;

}

### interpolation
$spaceamounts: (1,2,3,4,5);

@each $space in $spaceamounts {
    .m-#{$space}{
        margin: #{$space}rem;
    }
    .my-#{$space}{
        margin: #{$space}rem 0; 
    }

    .p-#{$space}{
        padding: #{$space}rem;
    }
    .py-#{$space}{
        padding: #{$space}rem 0; 
    }
}
$color:$black;
$box-sizing:border-box;
$width1:35rem;
$width:100%;


Sass properties used: Variables, Custom properties, nesting, Interpolation, Placeholder selectors, mixins, functions.

Animation-@keyframe