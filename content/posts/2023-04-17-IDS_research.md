---
title: Intrusion Detection & Prevention Systems.
date: 2023-04-17 
category: notes
tags:
    - Networking 101
    - Infosec
image : https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/d0238b56-a644-497f-9172-d1cd75295d1b/daxn0cg-f67263f8-123a-4cd0-84fb-3dd679b9d1db.jpg/v1/fill/w_1095,h_730,q_70,strp/newtype_by_asgerd_art_daxn0cg-pre.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MTIwMCIsInBhdGgiOiJcL2ZcL2QwMjM4YjU2LWE2NDQtNDk3Zi05MTcyLWQxY2Q3NTI5NWQxYlwvZGF4bjBjZy1mNjcyNjNmOC0xMjNhLTRjZDAtODRmYi0zZGQ2NzliOWQxZGIuanBnIiwid2lkdGgiOiI8PTE4MDAifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uub3BlcmF0aW9ucyJdfQ.1pM5mFP_O30gBpOmMcExcDd87Tihue3zIaIrERa_RXs

alt : robottxt:) 
keywords:
    - ids
    - ips 
    - Computer Science
    - computer security 

---

C පාඩම් මාලාව පටන් ගන්න කලින් , මට නිකමට ලිපියක් ලියල  දාන්න හිතුන , ඇයි ඇත්තටම මේ (C) පරිගණක බාශාවම  ලිපි ටිකක් විදියට දාන්න හිතුන එක ගැන . මේකෙදි අපිට C වල අතීත කතා ව නොකිය ඉන්නම බැහැ , මොකද සරලවම C language එක බාවිතයට් ගෙන  තමයි අද අපි බාවිතා කරන Operating Systems , ඒ වගේම device drivers , network හා සම්බන්ද applications , Embedded Systems සහ Databases වැනි බොහොමයක් ලියල තියෙන්නේ .
ඉතින් 1972 දී , Dennis Richie මහතා  Belllabs සමග වැඩ කරන කාලේ තමයි C language එක නිර්මාණය කරන්නේ  , මෙතැනදී කියන්න ඕන අපි දැනට බාවිතා  කරන technology side එකේ දේවල් බොහොමයකට ආරම්බය  වෙලා  තියෙන්නේ bellabs සහ එහි සිටිය set එකේ පරිශ්‍රමය මත , හරි දැනට දල අදහසක් තියෙනවා  නේ අපි මේ code කරන්න බාවිත කරන බාශාව ගැන .. ! 
ඒවගේම දෙයක් තියෙනවා  C බාෂාව තවත් විශේෂ වෙන , ඒ තමයි C වලට හැකියාව පවතිනවා  Directly memory එක Access කරන්න , මේ දේ නිසා  අපිට Data structures ලියද්දි සහ අලුත් ඒවා  නිර්මාණය කරද්දී වටිනවා  .. අපි අනිවාර්යෙන්ම මේ සම්බන්දව Pointers ගැන කතා  කරනකොට , කතාකරමු .

දැන් code කරන්න වෙලාව හරි , මේකට අපිට CodeBLocks වගේ IDA එකක් යොදා  ගන්න පුළුවන් , නැත්නම් හොදම විදිය කියල මම හිතන්නේ Old School විදියට text editor එකේ type කරලා  compiler එකක් use කර ගෙන compile කර ගන්න එක . ( ඇත්තටම text editor එක බාවිත කරලා  ඉගෙන ගන්න වෙලාවේ code කරන එක මම පයුද්ගලිකව හිතනවා හොදයි කියල , under the hood වෙන දේවල් ඉගෙන ගන්න පුළුවන් මේ විදියෙන් , හැබැයි ලොකු systems මේ විදියට ලියන්නේ නැහැ  , ) , අනෙක් දේ තමයි Operating system එක , අපිට කැමති එකක ලියන්න පුළුවන් , හැබැයි Windows / Mac වලට වඩා  මේක ඉගෙන ගන්න වේලාවෙ මොනවා  හරි Linux/Unix based OS එකක ලියන එක වටිනවා  , එකට හේතුව තමයි windows සහ Mac වල restrictions වැඩි , ඒ වගේම අපිට c එක්ක ඉදිරියට වැඩ කරද්දී සහරා  system calls එහෙම programme ඇතුලේ call කරන්න වෙනවා , අන්න එනත්නදී ගැටළු එන්න පුළුවන් . ( මෙතැනදී Ubuntu වගේ එකක් use කරන එක හොදයි , හොද package manager එකකුත් තියෙන එකේ පහසුයි මේ වැඩෙ කරන් යන්න ) .  vm එකක Ubuntu install කරන ආකාරය මම ලිපියක් දන්නම්.

හරි දැන් අපි දැන් C වල අතීත විත්ති ටිකකුත් දන ගෙන , ගැලපෙන Os එකකුත් දා  ගන්න එකත් දැනගෙන ඉන්න අතරේ , ඊළඟට මේ වැඩේට අවශ්‍ය මොකක්ද කියන එක අපි බලන්න ඕන , ඔව් .. ඊළඟට ඕන compiler එකක් , compiler එක කියන්නෙත් එක්තරා  ආකාරයක application එකක් මේක බාවිතයට ගන්නේ අපි High level language එකක් බාවිතා  කරලා  ලියන programme එක machine code එක බවට පරිවර්තනය කර ගන්න .  ඉතින් මෙතැනදී අපි gcc compiler එක යොදා  ගන්නවා  අපේ c programme එක compile කර ගන්න , ඔයාලට වෙන දෙයක් test කරලා බලන්න ඕන නම් පොඩ්ඩක් google කරලා  බලන්න set එකක්ම තියෙනවා  .

අදට මම මේ ලිපිය මෙතැනින් ඉවර කරනවා  , ඊළඟ ලිපියේ අපි compiler එක install (Ubuntu වල gcc එකනම් inbuild එනවා  , අපි clang වගේ එකකුත් test කරලා  බලමු ) කරලා  code කරන්න පටන් ගමු , එහෙනම්  
ජයවේවා !

===========================================================================

අද තමයි මේකේ දෙවැනි කොටස , ඔක්තෝබර් පළවෙනිදා  පට්ට වැස්සක් අතරේ ලියන්නේ :)) , කලින් ලිපියෙන් පොඩි හැදින්වීමක් තමයි සිදු කලේ , මොකද කාට හරි හිතෙන්න පුළුවන් මේ කාලෙට C වගේ පරිගණක බාශාවක් ඉගෙන ගන්න එකේ ප්‍රයෝජනයක් තියේද , ඒ කාලය වෙන වැඩකට allocate කලොත් නරකද වගේ දේවල් හිතෙන්න පුළුවන් , ඉතින් ඒ වගේ ගතියක් තිබ්බ නම් මීට පෙර ලිපිය කියෙව්වම මම හිත්නේව අඩු වෙන්න ඇති කියල ;) , 

හරි දැන් අපි වැඩේට බහිමු , මම හිතව්නවා  මේක කියවන ඔබ Linux based , Os එකට හෝ  WSL වලටවත් මාරු වෙලා ඇති කියල , වැඩි කතා  අනවශ්‍යයි අපි c වලින් සරල programme එකක් ලියල බලමු ,

```c
#include <stdio.h>
int main(void){
printf("Hello world!");
return 0;
}
```

දැන් මොනවා  හරි notepad එකක් ඔපෙන් කරලා  මේ code එක type කරලා  කැමති නමක් එක්ක .c extension එකත් එක්ක save කරන්න . මම මේක first.c කියල save කර ගන්නම් 
මේක තමයි අපේ පලවෙනි prgramme එක , දැක්ක ගමන්ම පේනවා  උඩින්ම #include කියල එකක් තියෙනවා  එකට <> අතරට "stdio.h" කියල තියෙනවා  , ටිකක් බැලුව ගමන්ම confuse වෙනවා  . ඒ ගතිය යන්නත් එක්ක අපි code එක compile කරලා  බලමු , compile කරනවා  කියන්නේ සරලවම අපි මේ ඉංග්‍රීසියෙන් අපිට තේරෙන බාශාවෙන් ලියපු code එක පරිගණකයට තේරෙන්න convert කරන එක . කලින් ලිපියේ සදහන් කළා වගේ එකට අපි යොදා  ගන්නේ  gcc compiler එක , අපි compile කරන්න කලින් Ubuntu/WSL terminal එකේ gcc --version කියල ගහල බලමු .

ඉතින් දැන් අපි පලවෙනි programme එක ලියල save කරලා  ඉන්නේ , ඊළඟට අපි  තෙරුන් ගන්න ඕන මොනවද මේ ලියල තියෙන්නේ කියල ,  උඩින් #include කියල එකක් තියෙනවා  එකත් එක්කම <> ඇතුලේ "stdio.h" කියල එකක් තියෙනවා  , දැක්ක ගමන් confused වෙන එක හරිම සාමාන්‍ය දෙයක් , ඉතින් ඒ ගතිය යන්නත් එක්ක compile කරලා  බලලම , එකින් එක ගැට ලිහා  ගමු  . ඉතින්ක ලින් ලිපියේ සදහන් කළා වගේ එකට අපි යොදා  ගන්නේ  gcc compiler එක , අපි compile කරන්න කලින් Ubuntu/WSL terminal එකේ gcc --version කියල ගහල බලමු .


```shell

 gcc --version
 
```


```

gcc (Ubuntu 11.4.0-1ubuntu1~22.04) 11.4.0
Copyright (C) 2021 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

```

ඊළඟට මෙන්න මේ ආකාරයට type කරලා  , ඔයාගේ programme එකට අදාළ binnary file එක ලබා  ගන්න පුළුවන් . මෙතන -o තැනට කැමති නමක් දෙන්න පුළුවන් , source file එකේ නමම යොදන්න පුළුවන් නම් වැඩේ පිළිවෙලයි .

```shell

gcc -o first first.c

```


දැන් output එක විදියට first කියල binnary file එකක් create වෙලා ඇති  . මේක open කරලා  බැලුවට මේකේ symbols වගයක් පෙන්න පුළුවන් . ඊළඟට මේක run  කරලා  බලමු මේ අක්කරට  
```
./first
```


එතකොට Display වෙනවා  අපට අපි printf (); එක මැදට දුන්න "හෙල්ලෝ owrld " කියන ටික

දැන් අපි සාර්ථක ලෙස , අපේ පලවෙනි programme එක ලියල run කරලා  අවසානයි. අපි දැන් බලමු එකින් එකට code එකේ තියෙන syntax සහ ඒවගෙ තේරුම.

ඔයාල ට මුලින්ම බල ගන්න පුළුවන් #include<"stdio.h "> කියන syntax එක , මේකේ මුල තියෙන #include එක use කරන්නේ  අපිට code කරන් යද්දී , අපේ පහසුවට මොනවා හරි function එකක් call කලොත් අන්න ඒ function එකට අදාළ source code එක load කර ගැනීමක් තමයි මේ " #include  " syntax එක බාවිතයෙන් වෙන්නේ , දැන් මෙතැනදී අපි stdio කියන header file එක බාවිතයට අර ගෙන තියෙනවා . එතකොට මොකක්ද මේ header file එකක් කියල කියන්නේ . මම කලින් සදහන් කල නේ , අපි code කරන යද්දී අපිට සමහර functions, macros වගේම data structures නුත් use කරන්න වෙනවා  අපේ පහසුව උදෙසා  (macros ගැන මම ඉස්සරහට කියනවා  , data structures කියල කියන්නේ සරලව , අපිට programme එකේ data store කරන්න වගේම execute කරද්දීත් computer එකේ main memory එක ඕන වෙනවා නේ , ඉතින් මේ data structures use කරන්න memory එකේ data කාර්යක්ෂමව store කර ගන්න -: මේවා ගැන ඉදිරියට සවිස්තර කතා කරනවා), කාටහරි ප්‍රශ්නයක් එන්න පුළුවන් ඉතින් අපිට මේවා  ලියන්න පුළුවන් නේ කියල , ඔව් ලියන්න පුළුවන් , හැබැයි එක  අනවශ්‍ය විදියේ වෙලාව යන දෙයක් වෙන්න පුළුවන් enterprise level එකේදී , ඒ වගේම මේ libraries එහෙමත් නැත්නම් header files ඒ ඒ ඇදලා  engineers ල ලියල තියෙන්නේ ගොඩක් හිතල vulnerabilities උපරිම අඩු වෙන විදියට සහ උපරිම පලදායිතාවය ලබා  ගන්න පුළුවන් අකාරයට . එහෙම එකේ අපි අයේ ලියන්න ඕන කමක් නැහැ  (හැබැයි ඉගෙන ගන්න කාලේ dont reinvente the wheel කියන එක පොඩ්ඩක් කැඩුවට කමක් නැහැ  -- වෙලාව තියෙනවා  නම්).

ඉතින් දැන් අපේ code එකේ හැටියට , අපි stdio.h කියන header file එක add කර ගෙන තියෙන්නේ . දැන් අපි මේ standard input output header file එකේ තියෙන  variables , functions බාවිත කරන්න පුළුවන් අපේ data input output වැඩ වලට .

ඒ වගේමයි මේ stdio හෙඅදෙර් file එක වගේම system එකෙන් ලබා  දෙන header files අපිට කියවා ගන්න පුළුවන් , MS code text editir  එකේනම් right click කරලා  header file එකේ text එක click කරලා  go  to  difinition  දුන්නම බල ගන්න පුළුවන් අදාළ header file එකේ code එක , එහෙම නැත්නම් /usr/include directory එකට ගියාමත් අපිට os එකෙන් ලබා  දෙන header files ටික බල ගන්න පුළුවන් .

හරි දැන් ඊළඟට තියෙන්නේ  main function එක , මෙතන අපිට අවශ්‍ය  algorithms  ලියනවා වගේම , අපිට අවශ්‍ය functions call  කර ගන්න පුළුවන් . කලින් ඔයාල ලියපු programme එකෙත් printf(); function එක යොදා  ගෙන තියෙනවා  පේනවා  . main function එකත් අනීත් functions වගේම තමයි , අපි function එකක් create  කර ගන්නකොට යොදා  ගන්න පිළිවෙලවල් මේකෙත් තියෙනවා  , <function එකේ return type එක > <function name එක> () ඇතුලේ අපිට data share කර ගන්න පුළුවන් වගේම , අපි මේවට කියනවා  arguments කියල , උදාහරණෙ හැටියට නම් මෙතන void දල තියෙන්නේ , එතනට void නොදා  ලිව්වත් කමක් නැහැ  , හැබැයි එහෙම දාල ලියන එකෙන් compiler එක සතුටු වෙනවා . ඊළඟට return එක , මෙතන return එක 0 දීල තියෙන්නේ එකට හේතුව තමයි අපේ programme එක නිවැරදිව run උනා  නම් return කරන්නේ 0 ,  0 හැර වෙන මොනවා  හරි return කරනවා  නම් code එකේ කොතැනම හරි ප්‍රශ්නයක් තියෙන්නව . මේක බලන්න පුළුවන් , ඔයාලගේ terminal එකේ echo $? ට්ය්පේ කරලා , 0 return වෙනවා  කියන්නේ programme එක successfully run  වෙලා කියන එක 

// C program to demonstrate segmentation fault
// by modifying a string literal
#include <stdio.h>
```c

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


මේක fault එකක් තියෙන code උදාහරනෙකට මේක second.c කියල save කරලා  , compile කරමු , බැලූ බැල්මට compiluth වුනා . හරි දැන් රුන් කරමු , මෙන්න රුන් කලාම segmentation ඵුල්ට් එකක් වැටෙනවා  . මේ error එක ගැන අපි ඉස්සරහට කතා කරමු , දැන් කලින් කිව්වා  වගේ  echo  $? ගැහුවම return වෙන්නේ 0 නෙවේ , අන්න එකෙන් අදහසක් ගන්න පුළුවන් return 0 ගැන .

අදට මේ ලිපියෙන් මෙපමණයි ඉතින් , ඊළඟ එකෙන් සමුවෙමු ! ජයවේවා !