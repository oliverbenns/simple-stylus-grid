# Simple Stylus Grid
A flexible, yet simple Stylus grid, inspired by Bootstrap. Using .grid- prefixed classes.

## Getting Started.

### 1. Download

To grab the files, you may download the [Zip File](https://github.com/oliverbenns/simple-stylus-grid/archive/master.zip). Alternatively, you may install it through the Bower Package Manager:

```
bower install simple-stylus-grid --save
```


### 2. Import

Once you've got the files, place the [grid folder](https://github.com/oliverbenns/simple-stylus-grid/tree/master/grid) in your main Stylus directory.

```
@import "grid"
```

With bower you'll preferably want to copy over the files to your css directory manually or using a build tool. Alternatively you can link to the bower_components directory from the stylesheet:

```
@import "../../bower_components/simple-stylus-grid/grid"
```


## Usage

For the sake of this run through, I'll be using **Jade**.

### Standard Columns

Always start with a `.wrapper`, followed by your grid classes.

```
.wrapper
	.grid-lg-8
		p My main content is here!
	.grid-lg-4
		p My sidebar is here!
```

### Nested Columns

When nesting columns inside other columns, always start with a `.row`

```
.wrapper
	.grid-lg-6
		.row
			.grid-lg-3
				p Thumbnail here!
			.grid-lg-3
				p Thumbnail here!

	.grid-lg-6
		p My sidebar is here!
```

### Utilities

Simple Stylus Grid also comes with some classes to help you hide elements on certain devices.

```
/* Hide on mobile */
.hide-xs

```

### Configuration

In [grid-variables.styl](https://github.com/oliverbenns/simple-stylus-grid/tree/master/grid/grid-variables.styl), you have access to various variables to adjust your grid accordingly.

| Variable  | Description |
| ------------- | ------------- |
| `$mobile-first`  | By making this true, you will start your grid using `-xs-` prefixed classes first. The grid uses min-width's to then detemine any desktop or tablet styles.  |
| `$grid-columns`  | The total number of columns you wish to have.  |
| `$grid-gutter`  | The gutter spacing between columns. Pixel value.  |
| `$screen-xs`, `$screen-md`, etc  | Your breakpoints. Pixel value. |
| `$wrapper-max-width`  | The max width of the .wrapper container. Stops desktop being full width.  |


## Contributing

- [Log an issue](https://github.com/oliverbenns/simple-stylus-grid/issues)
- [Open a PR](https://github.com/oliverbenns/simple-stylus-grid/pulls)

## License

[The MIT License (MIT)](https://github.com/oliverbenns/simple-stylus-grid/blob/master/LICENSE.md)

