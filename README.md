# respond-to
## SASS responsive mixin

## Usage

-Add .scss mixin and breakpoint variable files to your project
-Use with
```sass
	#myElement {
		@include respond-to($from: 'small', $to: 'medium') { margin-right: 20px }
	}
```

## Options
You can also include media type with $media-type.
```sass
	#myElement {
		@include respond-to($media-type: print) { display: none }
	}
```
The mixin supports Strings provided in the breakpoint map, or any css value. E.g.
```sass
	#myElement {
		@include respond-to($from: 10em, $to: 2000px) { margin-bottom: 20px }
	}
```
There is also support for just min-width or max-width media queries.
```sass
	#myElement {
		@include respond-to($from: 'large') { margin: 0 auto }
	}
	#myElement {
		@include respond-to($to: 'large') { margin: 0 }
	}
```
