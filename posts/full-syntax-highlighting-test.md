---
title: full syntax highlighting test
date: '2012-10-03'
description:
categories:
---
<pre><code>
// hdu 1028. Ignatius and the Princess III
// yeoo
#include <code><</code>stdio.h<code>></code>
#include <code><stdio.h></code>

int main() {
	const int size = 121;
	int n,i,j,k;
	int c[size],d[size];
	while (scanf("%d", &n) != EOF){
		for (i = 0; i < size; i++){
			d[i] = 0;
			c[i] = 1;
		}
		for (i = 2; i <= n; i++){
			for (j = 0; j <= n; j++)
				for (k = 0; k + j <= n; k += i)
					d[k+j] += c[j];
			for (j = 0; j <= n; j++ ){
				c[j] = d[j];
				d[j] = 0;
			}
		}
		printf( "%d\n", c[n] );
	}
	return 0;
}
</code></pre>