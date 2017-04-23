# (P)reset

A simple, lightweight LESS Framework.

[![npm version](https://badge.fury.io/js/p-reset.svg)](https://badge.fury.io/js/p-reset)
[![Bower version](https://badge.fury.io/bo/p-reset.svg)](https://badge.fury.io/bo/p-reset)

(More info and better docs soon)

### Vars

| Var | Function |
|------|----------|
| **Fonts** | |
| @bodyfont | Font used in general text.
| @titlefont | Font for titles (h1 / h3 / h5).
| **Shades** | |
| @white / @lightgray / @gray / @black | |
| @background | Background color.
| @color | Text color.
| **Colors** | |
| @accent | The main color. Used in buttons/inputs, .info/.message boxes and titles. |
| @compl | Complementary color. |
| @success / @error / @warn | Colors for .info/.message boxes and buttons/inputs. |
| **Sizes** | |
| @basefont | General font size. |
| @baseline | General |
| @navheight | Height for the nav menu. |
| @pagePadding | @baseline * 6; |
| @pagePadding--tablet | @baseline; |
| @pagePadding--phone | @baseline / 2; |
| **Others** | |
| @laptop / @tablet / @phone | Media Query Breakpoints. |
| @cubic-bezier | Main easing function. |
| @brad | Main border-radius. Used in buttons/inputs and .info/.message boxes. |

### Columns / Grid

So, columns.

All you need is an element with a `.row-(n)` class (in this case, the default is `.row-12`), and inside, the `.col-(n)` elements.
In case you need gutters, wrap it all inside a `.gutt`.


#### Default Breakpoints

| Var     | Class         | Media Query |
|---------|---------------|-------------|
|         | `.col-(n)`    |             |
| @tablet | `.col-sm-(n)` | max-width: 900px |
| @phone  | `.col-xs-(n)` | max-width: 600px |


#### Examples

**Without Gutters**

	<div class="row-12">
		<div class="col-sm-12 col-4">
			I'm full-width on tablets and phones, and 1/3 on bigger screens.
		</div>
		<div class="col-xs-12 col-sm-6 col-4">
			We're full-width on phones, 1/2 on tablets, and 1/3 on bigger screens.
		</div>
		<div class="col-xs-12 col-sm-6 col-4">
			We're full-width on phones, 1/2 on tablets, and 1/3 on bigger screens.
		</div>
	</div>


**With Gutters**

	<div class="gutt">
		<div class="row-12">
			<div class="col-sm-12 col-4">
				I'm full-width on tablets and phones, and 1/3 on bigger screens.
			</div>
			<div class="col-xs-12 col-sm-6 col-4">
				We're full-width on phones, 1/2 on tablets, and 1/3 on bigger screens.
			</div>
			<div class="col-xs-12 col-sm-6 col-4">
				We're full-width on phones, 1/2 on tablets, and 1/3 on bigger screens.
			</div>
		</div>
	</div>


Note that the idea behind (P)Reset is to **tweak it to better serve your needs**.

So if, for example:
- 12 columns are not enough;
- The gutters are not the size you wanted;
- You could use one or two more breakpoints, or change when the current ones are triggered;
- ... feel free to change it! ([Cool, but ... How?](#useful-tweaks))

Also, keep in mind that, unlike other frameworks (i.e. Bootstrap), this grid layout is **not mobile-first**.
So only the `col-` size is required, instead of the mobile (col-xs-) size.

### Classes

| Class | Function |
|-------|----------|
| .shadow | Adds a box shadow to the element. |
| .input | Styles an element like an input. |
| **.button / .btn** | Styles an element like a button. |
| .big | Make the button bigger. |
| .hover | Style the button as it was hovered. |
| .no-shadow | Removes shadow from the button. |
| .active | Style the button as it was active. |
| **Colors** | |
| .border-(color) | Change the border color of an element. (i.e. '.border-black') |
| .color-(color) | Change the text color of an element. (i.e. '.color-white') |
| .bg-(color) | Change the background color of an element. (i.e. '.color-acc') |
| **Fonts** | |
| .font-title | Change the element's font to the @titlefont. |
| .font-body | Change the element's font to the @bodyfont. |
| **Text Aligns** | |
| .talignleft | Align the elements text to the left. |
| .taligncenter | Align the elements text to the center. |
| .talignright | Align the elements text to the right. |
| **Margins / Paddings** | |
| .page-padding | |
| .page-margin | |
| .no-padding | Removes all padding from an element. |
| .no-margin | Removes all margins from an element. |
| .padding | Adds a padding of @baseline to the element. |
| .padding-half | Adds a padding of (@baseline / 2) to the element. |
| .padding-sides | Adds a padding of @baseline to the left and right sides of the element. |
| .padding-ends | Adds a padding of @baseline to the top and bottom sides of the element. |
| **Media Hides** | |
| .laptop-hide | Hide the element on laptops (and above). |
| .tablet-hide | Hide the element on tablets (and below). |
| .phone-hide | Hide the element on phones. |
| **Width** | |
| .full-width / .width-100 | Set the element's width to 100%. |
| .half-width / .width-50 | Set the element's width to 50%. |
| **Border Radius** | |
| .brad / .b-rad | Set the element's border-radius to the value defined in `vars.less` |
| **Info / Message** | |
| .info / .message | |
| .warn / .warning | |
| .yes / .accept / .success / .succ | |
| .no / .cancel / .error / .err | |


### Useful Tweaks


---


#### TODO
- Footer - Always on bootom fix
- Add tooltips
- Add saturation var to .shadow()
- Add [:valid] input state (BUG inputs with no extra attr turning green)
	- Test [:focus] combo
- Test something like ~'(min-width: @tablet + 1)'
- Change table styles
- Change the god damn .info class to something else
- Fix button .big modifier
- Consider adding
	a, a:link, a:visited, a:focus, a:hover, a:active{ color: inherit; }
	:not(nav){
		a, a:link, a:visited, a:focus, a:hover, a:active{
			text-decoration: none;
		}
	}
- Add WordPress Gallery Support