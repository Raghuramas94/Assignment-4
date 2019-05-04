# Kernel
Kernel or a feature extrator (also called filter and 3 * 3 matrix) is used to extract various features from a particular image. When a kernel 
is run on an input image, the kernel first extracts edges and gradients, then parts of objects, then objects and later images.
Scenes are extracted from images later on.

# CHANNEL
A collection of several units of the same object to detect a feature is known as a Channel. For example, if we are looking at a collection of 
red balls among a collection of balls, the collection of all the red balls is known as a channel, specifically, the red channel.
This can be used to extract the red feature in the image or the red balls in the image.

## Why should we only (well mostly) use 3x3 Kernels?

There are several reasons for using 3 * 3 kernels, some of which are listed below:
* Faster
* Not a lot of information is lost
* makes the network deeper
* Most of the GPU's today are optimised to 3*3 kernels and hence we would get faster, better optimised computations.

## How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)

199x199 | 197x197 | 195x195 | 193X193 | 191X191| 189X189 | 187X187 | 185X185| 183X183 | 181X181 | 179X179 | 177x177 | 175x175 | 173x173|
171X171 | 169X169 | 167X167 | 165X165 | 163X163 | 161X161 | 159X159 | 157X157 | 155X155 | 153X153 | 151X151 | 149X149 | 147X147 | 145X145 |
143X143 | 141X141 | 139X139 | 137X137 | 135X135 | 133X133 | 131X131 | 129X129 | 127X127 | 125X125 | 123X123 | 121X121 | 119X119 | 117X117 |
115X115 | 113X113 | 111X111 | 109X109 | 107X107 | 105X105 | 103X103 | 101X101 | 99X99 | 97X97 | 95X95 | 93X93 | 91X91 | 89X89 | 87X87 | 
85X85 | 83X83 | 81X81 | 79X79 | 77X77 | 75X75 | 73X73 | 71X71 | 69X69 | 67X67 | 65X65 | 63X63 | 61X61 | 59X59 | 57X57 | 55X55 | 53X53 | 
51X51 | 49X49 | 47X47 | 45X45 | 43X43 | 41X41 | 39X39 | 37X37 | 35X35 | 33X33 | 31X31 | 29X29 | 27X27 | 25X25 | 23X23 | 21X21 | 19X19 | 
17X17 | 15X15 | 13X13 | 11X11 | 9X9 | 7X7 | 5X5 | 3X3 | 1X1
