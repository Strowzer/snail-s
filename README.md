#include <stdio.h>

void main() {
	int snail[5][5] = {0};
	int x=0, y=0, n=1;
	int i, j;
	int v[2] = { 0,1 };

	for (i=0;n<=25;i++) {
		if (x+y==4 && x<y)
		{
			v[0] = 1;
			v[1] = 0;
		}
		else if (x == y && x+y>4) {
			v[0] = 0;
			v[1] = -1;
		}
		else if (x+y==4 && x>y) {
			v[0] = -1;
			v[1] = 0;
		}
		else if (x-y==1 && x+y<4) {
			v[0] = 0;
			v[1] = 1;
		}
		snail[x][y] = n;
		x += v[0];
		y += v[1];
		n += 1;
		}
	for (i = 0; i < 5; i++) {
		for (j = 0; j < 5; j++) {
			printf("%2d", snail[i][j]);
		}
		printf("\n");
	}

}
