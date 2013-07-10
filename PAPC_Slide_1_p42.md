i = 8
h = log n = 3

Matrix A = [A, B, C, D, E, F, G, H]

Step 1:
Matrix B  
	0	1	2	3
1	A
2	B
3	C
4	D
5	E
6	F
7	G
8	H


Step 2:
For-loop description
[	for h = 1:3
		h=1:	for j=1:4
		h=2:	for j=1:2
		h=3:	for j=1:1		]

For h=1, j = 1:4
Matrix B	
	0	1	2	3
1	A	A+B	
2	B	C+D
3	C	E+F
4	D	G+H
5	E
6	F
7	G
8	H

For h=2, i = 1:2
Matrix B	
	0	1	2	3
1	A	A+B	A+B+C+D	
2	B	C+D	E+F+G+H
3	C	E+F
4	D	G+H
5	E
6	F
7	G
8	H

For h=3, i=1:1
Matrix B	
	0	1	2	3
1	A	A+B	A+B+C+D	A+B+C+D+E+F+G+H
2	B	C+D	E+F+G+H
3	C	E+F
4	D	G+H
5	E
6	F
7	G
8	H

Step 3
For-loop description
[	for h = 3:0
		h=3:	for j=1:1
		h=2:	for j=1:2
		h=1:	for j=1:4		
		h=0:	for j=1:8		]

* rule 1, j even, data source = Matrix C
* rule 2, j = 1, data source = Matrix B
* rule 3, j = else, data source = Matrix B+C

for h=3, j=1:1
Matrix C
	0		1		2		3
1							A+B+C+D+E+F+G+H
2					
3	
4	
5	
6	
7	
8

for h=2, j=1:2
Matrix C
	0		1		2		3
1					A+B+C+D		A+B+C+D+E+F+G+H
2					A+B+C+D+E+F+G+H
3	
4	
5	
6	
7	
8

for h=1, j=1:4
Matrix C	
	0		1		2		3
1			A+B		A+B+C+D		A+B+C+D+E+F+G+H
2			A+B+C+D		A+B+C+D+E+F+G+H
3			A+B+C+D+E+F
4			A+B+C+D+E+F+G+H
5	
6	
7	
8	

for h=0, j=1:8
Matrix C	
	0		1		2		3
1	A		A+B		A+B+C+D		A+B+C+D+E+F+G+H
2	A+B		A+B+C+D		A+B+C+D+E+F+G+H
3	A+B+C		A+B+C+D+E+F
4	A+B+C+D		A+B+C+D+E+F+G+H
5	A+B+C+D+E
6	A+B+C+D+E+F
7	A+B+C+D+E+F+G
8	A+B+C+D+E+F+G+H

