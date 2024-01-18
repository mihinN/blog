---
title: Hello World! in C Language 
date: 2023-04-17 
category: notes
tags:
    - C
    - Programming
    - computer science
image : https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/15102441-2d8e-4af8-a431-0d409e866e20/d9osclx-5ffc445c-5296-4370-92ce-dd6781e70c79.jpg/v1/fill/w_1024,h_655,q_75,strp/hidden_sanctuary_by_cristi_b_d9osclx-fullview.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9NjU1IiwicGF0aCI6IlwvZlwvMTUxMDI0NDEtMmQ4ZS00YWY4LWE0MzEtMGQ0MDllODY2ZTIwXC9kOW9zY2x4LTVmZmM0NDVjLTUyOTYtNDM3MC05MmNlLWRkNjc4MWU3MGM3OS5qcGciLCJ3aWR0aCI6Ijw9MTAyNCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.CdLNeFqqSQ5QPtzlf0KaJ29qReB0PzdcDa4YByV21G8
alt : robottxt:) 
keywords:
    - C language
    - Baremetal Programming in Sinhala 
    - Computer Science
    - Programming
    - Linux
    - Windows 

---

අද තමයි මේකේ දෙවැනි කොටස , ඔක්තෝබර් පළවෙනිදා  පට්ට වැස්සක් අතරේ ලියන්නේ :)) , කලින් ලිපියෙන් පොඩි හැදින්වීමක් සිදු කලේ , මොකද කාට හරි හිතෙන්න පුළුවන් මේ කාලෙට C වගේ පරිගණක බාශාවක් ඉගෙන ගන්න එකේ ප්‍රයෝජනයක් තියේද , ඒ කාලය වෙන වැඩකට allocate කලොත් නරකද වගේ දේවල් හිතෙන්න පුළුවන් , ඉතින් ඒ වගේ ගතියක් තිබ්බ නම් මීට පෙර ලිපිය කියෙව්වම මම හිතනවා  අඩු වෙන්න ඇති කියල ;) ,

හරි දැන් අපි වැඩේට බහිමු , මම හිතනවා  මේක කියවන ඔබ මොනවා හරි  Linux based Os එකට හෝ  WSL වලට වගේ   මාරු වෙලා ඇති කියල , වැඩි කතා  අනවශ්‍යයි අපි c වලින් සරල programm එකක් ලියල බලමු ,

```c
#include <stdio.h>
int main(void){
printf("Hello world!");
return 0;
}
```

දැන් ඔයා ලග තියෙන මොනම හරි text editor (Sublimetext , VScode  , Notepad ++ , vim  , emacs ) එකක් Open  කරලා
උඩ දාල තියෙන code එක type කරන්න . (මෙතැනදී IDE  එකක් බාවිතා කරන්න පුළුවන් , හැබැයි code suggestions , build tools නැතුව අමුවෙන්ම code කරන එක , ඉගෙන ගන්න time එකේ හොදයි කියල හිතනවා .)  ඊළඟට ලියා ගත්ත code එක .c  කියන extension එකෙන් save කර ගන්න මොකද මේ අපි දැන් create කර ගන්නේ C File  එකක් නිසා .
හරි , අපි සාර්ථක ලෙස code එක ලියා ගත්තට පස්සේ , ඊළඟට අපි  ලියපු program එක Compile  කර ගන්න ඕන , ඉතින් මේ compile කරනවා කියන්නේ මොකක්ද ??
compile කරන්නේ මොකෙන්ද ?? compile කරද්දී මොකක්ද වෙන්නේ ?? මේ වගේ දේවල් ඔලුවට එන්න පුළුවන් , ඉතින් අපි ඒ දේවල් එකින් එක බලමු .
අපි programඑකක් ලියද්දි අපේ පහසුවට ඉංග්‍රීසි බාෂාව තමයි බාවිතා කරන්නේ , ඉංග්‍රීසි බාෂවත් එක්ක විවිද ගණිතමය සංකේත සහ logical symbols නුත් බාවිතය ගන්නවා සාර්ථක programඑකක් ලියා අවසන් කර ගන්න . හැබැයි මේ අපි බාවිතා කරන බාශාව පරිගනයකයට තේරෙනවද ?? මේ තියෙන hardware වලට තේරෙනවද ?? කොහෙත්ම  තේරෙන්නේ  නැහැ  ..  පරිගණකය තේරෙන්නේ  Binaries එහෙමත් නැත්නම 0 සහ 1 විතරයි . ඉතින් මේ අපිට තේරෙන බාෂාවෙන් ලිව්ව programඑක පරිගණකයට තේරෙන්න convert කිරීමේ කාර්ය පැවරිලා තියෙන්නේ Compiler එකට .
ඔබ නිකමට google කරලා බැලුවොත් මේ වෙනකොට විවද පරිගණක බාෂාවන් සදහා ඊට අදාලව තියෙන compilers බලා ගන්න පුළුවන් , එකම පරිගණක බාශාවට විවිද නම් වලින් compilers බාවිත වෙනවා දකින්න පුළුවන් එතකොට , හැබැයි පරිගණක බාෂාවට අනුව මොන විදියේ architecture එකකට නිර්මාණය කල Compiler එකක් උනත් අවසානයේ සිදු කරන්නේ ඔයා ලියපු programඑක binaries වලට convert කරන එක තමයි.

හරි , දැන් අපිට compile කරනවා කියන එක තේරෙනවා , ඊළඟට අපි ලියපු code එක compile කරගෙන බලමු , ඉතින් මේකට අපි ගන්නේ gcc කියන compiler එක , මේක c language එකට වගේම c ++ වලටත් යොදා ගන්නවා .
ඔයාගේ පරිගණකයේ gcc  තියේද  කියල බලල එහෙම නැත්නම්  install කර ගන්න ඕන .

```shell
gcc --version
```
මේක ගහල enter කලාට පස්සේ මෙහෙම display  වෙනවා නම් , ඔයාගේ machine එකේ මේ වෙනකොට compiler එක තියෙනවා .

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiV5qz6ndCe-ooKnvPW-O-SgVZDiyEYwYqGr4dgVirFyhBdE007GRl21SeOHQ74ji17UWJ1AQsAI7-kGGgneweiljaF2dKczm3IJ_RQ-DRnp7mHHIpWSgNTJ9IyqJBRn030TN_Q-kLkOa3VT0yLf50TYs-bBbmrJqT_k1G9MOPjHl7J_16-eYqpRso043ZS/s16000-rw/Screenshot%202024-01-18%20154216.png)

 එහෙම නැත්නම් 

```shell
sudo apt update 
sudo apt install gcc  
```
මේ විදියට type කරලා install කර ගන්න පුළුවන් .. 

ඉතින් මෙතනදී ඔයාලට තේරෙනවා මේකත් එක computer programඑකක් කියල , ඒ වගේම තමයි අපි compile කරන්න මේ programඑකට දෙන file steps කීපයක් හරහා ගිහිල්ල තමයි අවසානයේ පරිගණකයට තේරෙන executable binary file එකක් බවට convert වෙන්නේ . සරලවම මේ compilation process එක steps කීපෙකට තමයි සිද්ද වෙන්නේ . ( ඒක ගැන මම වෙනම ලිපියක් දාන්නම් )

```shell
gcc -o first first.c
```

දැන් මේක ගැන කතා කරා ඇති , compile කරමු ,
උඩ තියෙන විදියට type කරලා enter කරන්න , කිසිම case එකක් නැතුව compile වෙලා ඉවර වෙනවා කියන්නේ ඔයා පලවෙනි programඑක හරියට ලියල compile  කරලා අවසානයි කියන එක . දැන් output එක විදියට first කියල binnary file එකක් create වෙලා ඇති  . මේක open කරලා  බැලුවට මේකේ symbols වගයක් පෙන්න පුළුවන් . ඊළඟට මේක run  කරලා  

```shell
gcc --version
```

කියල type කරලා Enter ඔබන්න ..
කිසිම case එකක් නැතුව compile වෙලා ඉවර වෙනවා කියන්නේ ඔයා පලවෙනි programඑක හරියට ලියල compile  කරලා අවසානයි කියන එක

දැන් output එක විදියට first කියල binary file එකක් create වෙලා ඇති  . මේක open කරලා  බැලුවට මේකේ symbols වගයක් පෙන්න පුළුවන් .

![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhHdorRh4aMZvhoFeHN2TVpRuboEE96ywcdHslIWvRUMtyXB9bs6rjIWABPQYmAAUEnAwTsaNSm2N59ZYxQpjfKdzt_W8nnlCMQWgXq8ldUcSJr4LO0IBqZa5RF7Iwxwy8OH-2buVjdBv6zFK_x7_vVSyemO3ok9X3YhQTTLbMfpQ4riOsVEZymMgNQ8qMh/w640-h142-rw/Screenshot%202024-01-18%20145759.png)

ඊළඟට මේක run  කරලා  බලමු මේ අක්කරට  

```shell
./first
```
![](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEixLSsSoDhuNqleMKmgyP7KNsjhyphenhyphenQPqQA4lgOo4l8aAv2zoVC_9EQ7evk84wc_Ds2GsTz6xVzPWgJvbvhsq4_lCGGs-tnwPLgOu_d0q1BuH1A1SqDNtQs4jdoQZ_NRCgSS4ut-yNs0uj996H3fKawm3SCmJJ2TdvLwFGrTyvnRByIMbnst8mRqWYuIxVvfk/s320-rw/Screenshot%202024-01-18%20145640.png)

දැන් අපි සාර්ථක ලෙස , අපේ පලවෙනි program එක ලියල run කරලා  අවසානයි. අපි දැන් බලමු එකින් එකට code එකේ තියෙන syntax සහ ඒවගෙ තේරුම.

ඔයාල ට මුලින්ම බල ගන්න පුළුවන් #include<"stdio.h "> කියන syntax එක , මේකේ මුල තියෙන #include එක use කරන්නේ  අපිට code කරන් යද්දී , අපේ පහසුවට මොනවා හරි function එකක් call කලොත් අන්න ඒ function එකට අදාළ source code එක load කර ගැනීමක් තමයි මේ " #include  " syntax එක බාවිතයෙන් වෙන්නේ , දැන් මෙතැනදී අපි stdio කියන header file එක බාවිතයට අර ගෙන තියෙනවා . එතකොට මොකක්ද මේ header file එකක් කියල කියන්නේ . මම කලින් සදහන් කල නේ , අපි code කරන යද්දී අපිට සමහර functions, macros වගේම data structures නුත් use කරන්න වෙනවා  අපේ පහසුව උදෙසා  (macros ගැන මම ඉස්සරහට කියනවා  , data structures කියල කියන්නේ සරලව , අපිට programඑකේ data store කරන්න වගේම execute කරද්දීත් computer එකේ main memory එක ඕන වෙනවා නේ , ඉතින් මේ data structures use කරන්න memory එකේ data කාර්යක්ෂමව store කර ගන්න -: මේවා ගැන ඉදිරියට සවිස්තර කතා කරනවා), කාටහරි ප්‍රශ්නයක් එන්න පුළුවන් ඉතින් අපිට මේවා  ලියන්න පුළුවන් නේ කියල , ඔව් ලියන්න පුළුවන් , හැබැයි එක  අනවශ්‍ය විදියේ වෙලාව යන දෙයක් වෙන්න පුළුවන් enterprise level එකේදී , ඒ වගේම මේ libraries එහෙමත් නැත්නම් header files ඒ ඒ ඇදලා  engineers ල ලියල තියෙන්නේ ගොඩක් හිතල vulnerabilities උපරිම අඩු වෙන විදියට සහ උපරිම පලදායිතාවය ලබා  ගන්න පුළුවන් අකාරයට . එහෙම එකේ අපි අයේ ලියන්න ඕන කමක් නැහැ  (හැබැයි ඉගෙන ගන්න කාලේ don't re'-invent the wheel කියන එක පොඩ්ඩක් කැඩුවට කමක් නැහැ  -- වෙලාව තියෙනවා  නම්).

ඉතින් දැන් අපේ code එකේ හැටියට , අපි stdio.h කියන header file එක add කර ගෙන තියෙන්නේ . දැන් අපි මේ standard input output header file එකේ තියෙන  variables , functions බාවිත කරන්න පුළුවන් අපේ data input output වැඩ වලට .

ඒ වගේමයි මේ stdio හෙඅදෙර් file එක වගේම system එකෙන් ලබා  දෙන header files අපිට කියවා ගන්න පුළුවන් , MS code text-Editor එකේනම් right click කරලා  header file එකේ text එක click කරලා  go  to  definition දුන්නම බල ගන්න පුළුවන් අදාළ header file එකේ code එක , එහෙම නැත්නම් /usr/include directory එකට ගියාමත් අපිට OS එකෙන් ලබා  දෙන header files ටික බල ගන්න පුළුවන් .

හරි දැන් ඊළඟට තියෙන්නේ  main function එක , මෙතන අපිට අවශ්‍ය  algorithms  ලියනවා වගේම , අපිට අවශ්‍ය functions call  කර ගන්න පුළුවන් . කලින් ඔයාල ලියපු program එකෙත් printf(); function එක යොදා  ගෙන තියෙනවා  පේනවා  . main function එකත් අනීත් functions වගේම තමයි , අපි function එකක් create  කර ගන්නකොට යොදා  ගන්න පිළිවෙලවල් මේකෙත් තියෙනවා  , <function එකේ return type එක > <function name එක> () ඇතුලේ අපිට data share කර ගන්න පුළුවන් වගේම , අපි මේවට කියනවා  arguments කියල , උදාහරණෙ හැටියට නම් මෙතන void දල තියෙන්නේ , එතනට void නොදා  ලිව්වත් කමක් නැහැ  , හැබැයි එහෙම දාල ලියන එකෙන් compiler එක සතුටු වෙනවා . ඊළඟට return එක , මෙතන return එක 0 දීල තියෙන්නේ එකට හේතුව තමයි අපේ program එක නිවැරදිව run උනා  නම් return කරන්නේ 0 ,  0 හැර වෙන මොනවා  හරි return කරනවා  නම් code එකේ කොතැනම හරි ප්‍රශ්නයක් තියෙන්නව . මේක බලන්න පුළුවන් , ඔයාලගේ terminal එකේ echo $? ට්ය්පේ කරලා , 0 return වෙනවා  කියන්නේ program එක successfully run  වෙලා කියන එක

```c
#include <stdio.h>
int main()
{
    char* str;

    // Stored in read only part of data segment //
    str = "GfG";

    // Problem: trying to modify read only memory //
    *(str + 1) = 'n';
    return 0;
}
```


මේක fault එකක් තියෙන code උදාහරනෙකට මේක second.c කියල save කරලා  , compile කරමු , බැලූ බැල්මට Complicated වුනා . හරි දැන් Run කරමු , මෙන්න Run කලාම segmentation fault එකක් වැටෙනවා  . මේ error එක ගැන අපි ඉස්සරහට කතා කරමු , දැන් කලින් කිව්වා  වගේ  echo  $? ගැහුවම return වෙන්නේ 0 නෙවේ , අන්න එකෙන් අදහසක් ගන්න පුළුවන් return 0 ගැන .

අදට මේ ලිපියෙන් මෙපමණයි ඉතින් , ඊළඟ එකෙන් සමුවෙමු ! ජයවේවා !



