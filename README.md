# gitbook-plugin-ace

This page is implemented using the two plugins developed by me: ```gitbook-plugin-ace```. Please check the [Github repo](https://github.com/ymcatar/gitbook-plugin-ace) for the syntax and changelog of the plugin.

## Example 1

Here is the "Hello World" program of C language. The code editor in this section is set to be editable.

{%ace edit=true, lang='c_cpp'%}
#include <stdio.h>

int main(){
	int i;

	for(i=0; i<10; i++)
		printf("Hello World.");

	return 0;
}
{%endace%}

## Example 2

And a javascript code right here:

{%ace edit=false, lang='javascript'%}
var message = 'H e l l o W o r l d';
var split = message.split(' ').join('');
console.log(message);
console.log("testing {{test}}");
{%endace%}

## Example 3

And a piece of javascript code with wrong syntax, but with syntax validation disabled.

{%ace edit=false, lang='javascript', check=false%}
var test = [
	somethingIsWrong: 'withThis';
];
{%endace%}

## Example 4

Custom theme support is also added.

{%ace edit=false, lang='javascript', theme='monokai'%}
var test = a => (
    `ES6 is amazing. $${a}`
);
{%endace%}