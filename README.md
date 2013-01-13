Supersassious
=============
Learning SASS by following the [tutorial](http://sass-lang.com/tutorial.html).

Nesting
-------

    #header{
    	background-color:blue;
    	h1 {
    		font-size: 5em;
    		border: {
    			style: solid;				
    			left: {
    				width: 10px + $extend;
    				color: red;
    			}
    			right: {
    				width: 20px;
    				color: red;
    			}
    			bottom: {
    				width: 10px;
    				color: lighten($awesome,10%);
    			}
    		}
    	}
    }

### Parent References

    .concluding{
    	a.important{			
    		&:hover {
    			color: $awesome;			
    		}				
    	}
    }
    
Variables
---------

    $awesome: orange;
    $extend: 10px;

Operations &amp; Functions
--------------------------

     color: lighten($awesome,10%);

Interpolation
-------------

    $awesome-color: orange;
    
    #content{
    	.introducing-#{$awesome-color}{
    		background-color: $awesome-color;
    	}
    }

Mixins
------

    @mixin spin-me-right-round-baby {
    
    	-webkit-transition-duration: 0.8s;
    	-moz-transition-duration: 0.8s;
    	-o-transition-duration: 0.8s;
    	transition-duration: 0.8s;
         
    	-webkit-transition-property: -webkit-transform;
    	-moz-transition-property: -moz-transform;
    	-o-transition-property: -o-transform;
    	transition-property: transform;
    
    	&:hover {
    		transform:rotate(360deg);
    		-ms-transform:rotate(360deg); /* IE 9 */
    		-moz-transform:rotate(360deg); /* Firefox */
    		-webkit-transform:rotate(360deg); /* Safari and Chrome */
    		-o-transform:rotate(360deg); /* Opera */					
    	}
    }
    
    
    .concluding{
    	@include spin-me-right-round-baby;
    	a.important{			
    		&:hover {
    			color: $awesome-color;			
    		}				
    	}
    }   
