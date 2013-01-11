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

