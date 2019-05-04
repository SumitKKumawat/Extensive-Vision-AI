# Extensive-Vision-AI
Computer Vision | Deep Learning | EVA Phase 1

## What are Channels and Kernels (according to EVA)?
Channels : Channels are nothing but bucket or container of a same information

           We can add as many channels as we want.
           
           there is no relation to having a fix no. of channels.
           
           we can have n no. of channels for RGB colors.
           
           
           Ex. Fried Rice Recipie - we are having x different different ingredients or items to prepre the receipe which includes a bowl
           Rice, Salt, Garlic, oil, pepper, cutting pieces of carrots etc.
           so all the different different items are channels.
           
           Ex. LCD screen contains three channels Red, Green, Blue colors whereas a newspaper contains 4 channels which are CMYK—C for Cyan            (which usually means Blue), M for Magenta (Pink), Y for Yellow, and K for Black.
           

Kernals : It is a NxN matrix which can detect or extract a specific info. from an image source.
          It is also called feature extractors. Kernals usually convolve over the source image to extract the specific info and pass it to           next layer.
          
          Ex. 3x3 size kernal to extract or detects only vertical edge, below is for understanding purpose.
          [0 1 0]
          [0 1 0]
          [0 1 0]
          
          

## Why should we only (well mostly) use 3x3 Kernels?
Below are the couple of reasons why to stict only for 3x3 kernels.
1. 3x3 Kernels are small in size.
2. Contains middle row and column due to odd in manner.
3. Uses Less computation power or resources as compared to other 5x5 or 11x11 kernels.
4. More efficeient in use as recommended by many reserch fellows by their experience.

ex. if we use 3x3 kernal then we have 9 values however with the use of 5x5 we can have 25 values which are exceptionally high as compared to 3x3.



## How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)

we need to perform 99 times, 3x3 convolution operation to reach 1x1 from 199x199 as per below.

```
L000 Input 199x199 | L001 (3x3) 197X197 | L002 (3x3) 195X195 | L003 (3x3) 193X193 | L004 (3x3) 191X191 |
L005 (3x3) 189X189 | L006 (3x3) 187X187 | L007 (3x3) 185X185 | L008 (3x3) 183X183 | L009 (3x3) 181X181 |
L010 (3x3) 179X179 | L011 (3x3) 177X177 | L012 (3x3) 175X175 | L013 (3x3) 173X173 | L014 (3x3) 171X171 |
L015 (3x3) 169X169 | L016 (3x3) 167X167 | L017 (3x3) 165X165 | L018 (3x3) 163X163 | L009 (3x3) 161X161 |
L020 (3x3) 159X159 | L021 (3x3) 157X157 | L022 (3x3) 155X155 | L023 (3x3) 153X153 | L024 (3x3) 151X151 |
L025 (3x3) 149X149 | L026 (3x3) 147X147 | L027 (3x3) 145X145 | L028 (3x3) 143X143 | L029 (3x3) 141X141 |
L030 (3x3) 139X139 | L031 (3x3) 137X137 | L032 (3x3) 135X135 | L033 (3x3) 133X133 | L034 (3x3) 131X131 |
L035 (3x3) 129X129 | L036 (3x3) 127X127 | L037 (3x3) 125X125 | L038 (3x3) 123X123 | L039 (3x3) 121X121 |
L040 (3x3) 119X119 | L041 (3x3) 117X117 | L042 (3x3) 115X115 | L043 (3x3) 113X113 | L044 (3x3) 111X111 |
L045 (3x3) 109X109 | L046 (3x3) 107X107 | L047 (3x3) 105X105 | L048 (3x3) 103X103 | L049 (3x3) 101X101 |
L050 (3x3) 099x099 | L051 (3x3) 097X097 | L052 (3x3) 095X095 | L053 (3x3) 093X093 | L054 (3x3) 091X091 |
L055 (3x3) 089X089 | L056 (3x3) 087X087 | L057 (3x3) 085X085 | L058 (3x3) 083X083 | L059 (3x3) 081X081 |
L060 (3x3) 079X079 | L061 (3x3) 077X077 | L062 (3x3) 075X075 | L063 (3x3) 073X073 | L064 (3x3) 071X071 |
L065 (3x3) 069X069 | L066 (3x3) 067X067 | L067 (3x3) 065X065 | L068 (3x3) 063X063 | L069 (3x3) 061X061 |
L070 (3x3) 059X059 | L071 (3x3) 057X057 | L072 (3x3) 055X055 | L073 (3x3) 053X053 | L074 (3x3) 051X051 |
L075 (3x3) 049X049 | L076 (3x3) 047X047 | L077 (3x3) 045X045 | L078 (3x3) 043X043 | L079 (3x3) 041X041 |
L080 (3x3) 039X039 | L081 (3x3) 037X037 | L082 (3x3) 035X035 | L083 (3x3) 033X033 | L084 (3x3) 031X031 |
L085 (3x3) 029X029 | L086 (3x3) 027X027 | L087 (3x3) 025X025 | L088 (3x3) 023X023 | L089 (3x3) 021X021 |
L090 (3x3) 019X019 | L091 (3x3) 017X017 | L092 (3x3) 015X015 | L093 (3x3) 013X013 | L094 (3x3) 011X011 |
L195 (3x3) 009X009 | L096 (3x3) 007X007 | L097 (3x3) 005X005 | L098 (3x3) 003X003 | L099 (3x3) 001X001 |

```

