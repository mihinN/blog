---
title: Compilation Process in C / සිංහල
date: 2023-10-15 
category: notes
image: https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/f239c046-c6e3-4e6d-a9d7-3c189be515d1/dgv260v-cf3ad109-df5f-4263-9245-81aa8bb5cf78.jpg/v1/fill/w_1014,h_788,q_70,strp/italian_connection_iii_by_luopioart_dgv260v-pre.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9OTk1IiwicGF0aCI6IlwvZlwvZjIzOWMwNDYtYzZlMy00ZTZkLWE5ZDctM2MxODliZTUxNWQxXC9kZ3YyNjB2LWNmM2FkMTA5LWRmNWYtNDI2My05MjQ1LTgxYWE4YmI1Y2Y3OC5qcGciLCJ3aWR0aCI6Ijw9MTI4MCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.gdGPY2zHhz15o7mlqI4vVyyGtWhvNDNGE4D0bDOAzsk
alt : Compilation Process / සිංහල
# imageCaption :  
showShare : true
comments: false
toc: false
tags:
    - C language 101 
    - 02 lesson

keywords:
    - c programming in සිංහල   
    - Computer Science
    - C
    - Compilation process 
    - new

---


## "C" compilation Process එක, 

කලින් ලිපියේ සදහන් කළා ඔයාලට මතක ඇති , අපි ලියපු programme එක compile කර ගැනීමේදී , එම compilation process එක steps කීපෙකට වෙන බව , ඉතින් අද අපි ඒ steps කීපය ගැන බලන්න තමයි යන්නේ . ඊට කලින් කවුරු හරි මේ ලිපියෙන් කියවන්න පටන් ගත්ත නම් ඒ අය සදහා මම පොඩි ආරම්බයක් විදියට අයෙත් මේ පොඩි විස්තරෙන්ම පටන් ගන්නම් .

  

සරලවම , අපි compiler එකක් බාවිතයට ගන්නේ අපි ලියන programme  එක machine code එක බවට convert කර ගැනීමට , මොකද පරිගණකයට තේරෙන්නේ 0,1 එහෙමත් නැත්නම් binaries නිසා , ඉතින් විවිද පරිගණක බාෂා ඒ ඒ බාශාවන්ට ගැලපෙන්න compilers නිර්මාණය කරලා තියෙනවා .

  

ඉතින් අපේ කතාව සිද්ද වෙන්නේ C බාශාවත් එක්ක නිසා gcc එහෙමත් නැත්නම් GNU C Compiler එක තමයි බාවිතයට ගන්නේ (C වලදී බාවිතා වන එකම compiler එක gcc පමණක් නොවේ .. Google කරලා බලන්න). 
ඉතින්  gcc compiler එක C පරිගණක බාශාවේ වගේම C++ සදහාත් බාවිතා වෙනවා . ඊට අමතරව Go වගේ language වලදීත් බාවිතා වෙනවා.

හරි මම හිතවා ආරම්බය විදියට මේ විස්තර ටික ඇති කියල , දැන් බලමු මොනවද මේ steps ටික කියල ,

C වල compilation process  එක steps 4කට සිද්ද වෙනවා , ඒ කියන්නේ ඔයා programme එක ලියල , gcc -o first first.c enter ගැහුව
ගමන් gcc programme එක, ඔයා ලිව්ව programme එක steps හතරක් හරහා ගෙනල්ලා තමයි ඔයා දකින ./first කියන executable file එක create කරන්නේ .

ඉතින් මොකක්ද මේ හතර ?

පිලිවෙලින් ,

1. Pre-processing

2. Compiling

3. Assembling

4. Linking

පලවෙනි එක තමයි ```pre-processing part``` එක , මෙතැනදී compiler එකෙන් ඔයාගේ programme එකේ තියෙන **header files , macros ටික extract කර ගන්නවා**.

ඉතින් මේක ඔයාටම බලා ගන්න පුළුවන් , ඔයාට තියෙන්නේ compiler එකට කියන්න compilation process එක pre-processing part එකෙන් පමණක් නවත්වන්න කියල , මේක කරන්නේ කොහොමද , හරි සරලයි ,

gcc  -o විදියට සදහන් කල flag (අපි මේවට flags කියල කියනවා) එක වෙනුවට ```gcc -E``` **flag** එක යොදා ගෙන compile කරලා බලමු .  ඔයාලට output එක බලාගන්න පුළුවන් මේ විදියට ,

  
  

```shell

gcc -E first.c

```

මේක පැහැදිලි වෙන්න මේ ටික text file එකක save කර ගමු මේ විදියට .

```shell

gcc -E first.c > first-pre.txt

```

text file එක open කර ගත්තට පස්සේ , ඔයාලටම බලා ගන්න පුළුවන් අපේ header files extract වෙලා තියෙන අපූරුව ✅✅

  

දැන් ඔයාල සාර්ථක ලෙස එකක් ඉවරයි , ඊළඟට ```compilation part``` එක , මෙතනදී වෙන්නේ **ඔයා extract කර ගත්තු code** එක ```assembly language එකට convert වෙන එක``` , assembly කියන්නේ **low -level language** එකක් **machine code එකට සමීප** , ඒ කලේ programmes බොහොමයක් ලියවුනේ මේ බාශාවෙන්. ඉතින් මේ වැඩේ අපිට කරන්න පුළුවන් කලින් වගේ gcc වලට ```-S``` කියන flag එක ලබා දීමෙන් , ඒවගේම .s කියන file type එකෙන් output එක ගන්න පුළුවන් .

  

```shell

gcc -S first.s first.c

```

  

දැන් ඔයාලට බලා ගන්න පුළුවන් assembly code එක.

ඊළඟ step එක තමයි මේ assembly code  එක binaries වලට convert කර ගන්න එක ,  මේකට අපි -c flag එක යොදා ගන්නවා.

```gcc -c first.s``` **ENTER** කල ගමන් අපිට first .o object file එක create වෙලා තියෙනවා ..

```shell

gcc -c first.s

```

  

මෙතනදී compiler එකෙන් warnings එහෙම දෙන්න පුළුවන් linking part එක වෙලා නැහැ කියල , අපි ඉතින් දන්නවා නේ තව step එකක් තියෙනවා කියල අන්තිම stage එකට එන්න.

හරි .. ඉතාමත් සාර්ථක අකාරයෙන් මේ ටික අවසන් කල ඔයා , ඊළඟට යන්නේ මේක compile කරලා අවසාන කර ගන්න. ඉතින් එකට අපි -o flag එක යොදා ගෙන,

පහත ආකාරයට compile කරලා අවසාන කරනවා ,

  

```shell

gcc -o first first.o

```

  

ඉතින් මෙතනදී වෙන්නේ Linking part එක , ඔයාගේ programme එකට අවශ්‍ය libraries තියෙනවා නම්, ඒ binaries සහ ඔයාගේ programme එකේ binaries එකට එකතු කිරීමක් තමයි මෙතනදී  වෙන්නේ.

  

තව විස්තර ඇතුව කිව්වොත් ,

  

අපි programme එකක් ලියද්දි , ඒ සදහා libraries එහෙමත් නැත්නම් header files කිහිපයක් යොදා ගන්නවා , ඒ වගේම system එකෙන් ලබා දෙන libraries  වලට අමතර අපිම ලියන , අපිට අවශ්‍ය පරිදි customize  කල libraries  අපිට යොදා ගන්න වෙනවා , අන්න එතනදී මේ linking part එකේ වැදගත් කම හොදටම දැනෙනවා

  

හරි , මේක තමයි compilation process එකේ කතාව , අදට නිමි එහෙනම්, ජයවේවා .....!! 🤍