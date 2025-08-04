{\rtf1\ansi\ansicpg1252\cocoartf2822
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\fnil\fcharset0 Menlo-Regular;\f2\fnil\fcharset0 HelveticaNeue;
}
{\colortbl;\red255\green255\blue255;\red202\green204\blue151;\red23\green23\blue23;\red202\green202\blue202;
\red255\green255\blue255;\red29\green36\blue59;\red70\green137\blue204;\red152\green209\blue251;\red98\green136\blue72;
\red184\green128\blue103;\red172\green196\blue154;\red194\green126\blue101;\red174\green113\blue176;\red213\green213\blue157;
}
{\*\expandedcolortbl;;\cssrgb\c83137\c83137\c65490;\cssrgb\c11765\c11765\c11765;\cssrgb\c83137\c83137\c83137;
\cssrgb\c100000\c100000\c100000;\cssrgb\c14902\c19216\c29804;\cssrgb\c33725\c61176\c83922;\cssrgb\c65490\c85490\c98824;\cssrgb\c45490\c59608\c35294;
\cssrgb\c77647\c57647\c47843;\cssrgb\c72941\c80392\c66667;\cssrgb\c80784\c56863\c47059;\cssrgb\c74118\c53333\c74510;\cssrgb\c86667\c86275\c67843;
}
\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 // 
\f1\fs28 \cf2 \cb3 \expnd0\expndtw0\kerning0
\outl0\strokewidth0 \strokec2 zigzagTraverse\cf4 \cb1 \strokec4 \
\
- 
\f2\fs34 \cf5 \cb6 \strokec5 a zigzag traversal of a grid in JavaScript, mimicking the navigation of library bookshelves. Start at the bottom-right corner, move upwards in the last column, then downwards in the previous column, alternating directions. Traverse each column in this zigzag pattern and collect the items. Good luck!\
\
```js\
\
	
\f1\fs28 \cf7 \cb3 \strokec7 function\cf4 \strokec4  \cf2 \cb3 \strokec2 zigzagTraverse\cf4 \cb3 \strokec4 (\cf8 \strokec8 grid\cf4 \strokec4 ) \{\cf4 \cb1 \strokec4 \
\pard\pardeftab720\partightenfactor0
\cf4 \cb3 \strokec4     \cf9 \strokec9 // \cf7 \strokec7 TODO\cf9 \strokec9 : Determine the number of rows and columns in 'grid'\cf4 \cb1 \strokec4 \
\cb3     \cb1 \
\cb3     \cf7 \strokec7 const\cf4 \strokec4  \cf8 \strokec8 traversalPath\cf4 \strokec4  = [];\cb1 \
\cb3     \cf7 \strokec7 const\cf4 \strokec4  \cf8 \strokec8 rows\cf4 \strokec4  = \cf8 \strokec8 grid\cf4 \strokec4 .\cf10 \strokec10 length\cf4 \strokec4  ;\cb1 \
\cb3     \cf7 \strokec7 const\cf4 \strokec4  \cf8 \strokec8 cols\cf4 \strokec4  = \cf8 \strokec8 grid\cf4 \strokec4 [\cf11 \strokec11 0\cf4 \strokec4 ].\cf10 \strokec10 length\cf4 \strokec4  ;\cb1 \
\cb3     \cf7 \strokec7 let\cf4 \strokec4  \cf8 \strokec8 row\cf4 \strokec4  = \cf8 \strokec8 rows\cf4 \strokec4  - \cf11 \strokec11 1\cf4 \strokec4 ;\cb1 \
\cb3     \cf7 \strokec7 let\cf4 \strokec4  \cf8 \strokec8 col\cf4 \strokec4  = \cf8 \strokec8 cols\cf4 \strokec4  - \cf11 \strokec11 1\cf4 \strokec4 ;\cb1 \
\cb3     \cf7 \strokec7 let\cf4 \strokec4  \cf8 \strokec8 index\cf4 \strokec4  = \cf11 \strokec11 0\cf4 \strokec4 ;\cb1 \
\cb3     \cf7 \strokec7 let\cf4 \strokec4  \cf8 \strokec8 direction\cf4 \strokec4  = \cf12 \strokec12 "up"\cf4 \strokec4 ;\cb1 \
\cb3     \cb1 \
\cb3     \cf13 \strokec13 while\cf4 \strokec4 (\cf8 \strokec8 index\cf4 \strokec4  < \cf8 \strokec8 rows\cf4 \strokec4  * \cf8 \strokec8 cols\cf4 \strokec4 )\{\cb1 \
\cb3      \cf8 \strokec8 traversalPath\cf4 \strokec4 [\cf8 \strokec8 index\cf4 \strokec4 ] = \cf8 \strokec8 grid\cf4 \strokec4 [\cf8 \strokec8 row\cf4 \strokec4 ][\cf8 \strokec8 col\cf4 \strokec4 ];\cb1 \
\
\cb3         \cf13 \strokec13 if\cf4 \strokec4  (\cf8 \strokec8 direction\cf4 \strokec4  === \cf12 \strokec12 "up"\cf4 \strokec4 ) \{\cb1 \
\cb3             \cf13 \strokec13 if\cf4 \strokec4  (\cf8 \strokec8 row\cf4 \strokec4  - \cf11 \strokec11 1\cf4 \strokec4  < \cf11 \strokec11 0\cf4 \strokec4 ) \{\cb1 \
\cb3                 \cf8 \strokec8 direction\cf4 \strokec4  = \cf12 \strokec12 "down"\cf4 \strokec4 ;\cb1 \
\cb3                 \cf8 \strokec8 col\cf4 \strokec4  -= \cf11 \strokec11 1\cf4 \strokec4 ;\cb1 \
\cb3             \} \cf13 \strokec13 else\cf4 \strokec4  \{\cb1 \
\cb3                 \cf8 \strokec8 row\cf4 \strokec4  -= \cf11 \strokec11 1\cf4 \strokec4 ;\cb1 \
\cb3             \}\cb1 \
\cb3         \} \cf13 \strokec13 else\cf4 \strokec4  \{\cb1 \
\cb3             \cf13 \strokec13 if\cf4 \strokec4  (\cf8 \strokec8 row\cf4 \strokec4  + \cf11 \strokec11 1\cf4 \strokec4  === \cf8 \strokec8 rows\cf4 \strokec4 ) \{\cb1 \
\cb3                 \cf8 \strokec8 direction\cf4 \strokec4  = \cf12 \strokec12 "up"\cf4 \strokec4 ;\cb1 \
\cb3                 \cf8 \strokec8 col\cf4 \strokec4  -= \cf11 \strokec11 1\cf4 \strokec4 ;\cb1 \
\cb3             \} \cf13 \strokec13 else\cf4 \strokec4  \{\cb1 \
\cb3                 \cf8 \strokec8 row\cf4 \strokec4  += \cf11 \strokec11 1\cf4 \strokec4 ;\cb1 \
\cb3             \}\cb1 \
\cb3             \}\cb1 \
\cb3        \cb1 \
\
\
\
\cb3         \cf8 \strokec8 index\cf4 \strokec4 ++\cb1 \
\cb3     \}\cb1 \
\cb3     \cb1 \
\cb3     \cb1 \
\cb3     \cf9 \strokec9 // \cf7 \strokec7 TODO\cf9 \strokec9 : Traverse 'grid' in a zigzag pattern starting from the bottom right\cf4 \cb1 \strokec4 \
\cb3     \cb1 \
\cb3     \cf13 \strokec13 return\cf4 \strokec4  \cf8 \strokec8 traversalPath\cf4 \strokec4 ;\cb1 \
\cb3 \}\cb1 \
\
\cf7 \cb3 \strokec7 const\cf4 \strokec4  \cf8 \strokec8 grid\cf4 \strokec4  = [\cb1 \
\cb3     [\cf11 \strokec11 101\cf4 \strokec4 , \cf11 \strokec11 102\cf4 \strokec4 , \cf11 \strokec11 103\cf4 \strokec4 , \cf11 \strokec11 104\cf4 \strokec4 ],\cb1 \
\cb3     [\cf11 \strokec11 201\cf4 \strokec4 , \cf11 \strokec11 202\cf4 \strokec4 , \cf11 \strokec11 203\cf4 \strokec4 , \cf11 \strokec11 204\cf4 \strokec4 ]\cb1 \
\cb3 ];\cb1 \
\
\cf7 \cb3 \strokec7 const\cf4 \strokec4  \cf8 \strokec8 zigzagGrid\cf4 \strokec4  = \cf8 \strokec8 zigzagTraverse\cf4 \strokec4 (\cf8 \strokec8 grid\cf4 \strokec4 )\cb1 \
\
\cf7 \cb3 \strokec7 console\cf4 \strokec4 .\cf14 \strokec14 log\cf4 \strokec4 (\cf8 \strokec8 zigzagGrid\cf4 \strokec4 )\cb1 \
\
\cf9 \cb3 \strokec9 // \cf7 \strokec7 TODO\cf9 \strokec9 : Print the zigzag traversal path of items in 'grid'\cf4 \cb1 \strokec4 \
\
\
\cf9 \cb3 \strokec9 // 0,3,6,9,12\cf4 \cb1 \strokec4 \
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f2\fs34 \cf5 \cb6 \strokec5 \
\
```}