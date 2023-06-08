---
title: Structs in C language / සිංහල
date: 2022-11-12 
category: notes
image: https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/f68cf413-ab00-41fc-82fe-0a175144bf20/dfoguih-b630d9e3-21fa-4901-879a-36ab310d0ac2.png/v1/fill/w_1095,h_730,q_70,strp/ninja_rabbit_02_by_darkwhite2981_dfoguih-pre.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9ODU0IiwicGF0aCI6IlwvZlwvZjY4Y2Y0MTMtYWIwMC00MWZjLTgyZmUtMGExNzUxNDRiZjIwXC9kZm9ndWloLWI2MzBkOWUzLTIxZmEtNDkwMS04NzlhLTM2YWIzMTBkMGFjMi5wbmciLCJ3aWR0aCI6Ijw9MTI4MCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.u5-DDBhA9TYBaFQ5lM58TNm-3_3JgxaUjoWCbT4CBgU
alt : Structs in C language / සිංහල
imageCaption : Samurai rabbit 
showShare : true
comments: false
toc: false
tags:
    - C language 101 

keywords:
    - c programming in සිංහල   
    - Computer Science 

---

## Structs  ගැන , 

Structs , C language එකේ විශේෂ ස්ථානයක් ගන්නවා , එයට හේතුව  , අපි දන්නවා  අපිට programme එක තුල අවශ්‍ය දෙයක් computer memory එකේ තබා ගැනීමට අවශ්‍ය වූ විට සිදු කරන්නේ , variable එකක් create කරන එක. උදාහරණයක් විදියට ගත්තොත් .. 

`int x=20 , y=30;` ආකාරයට .
struct තුලින් කරන්නෙත් මේ හා සමාන ක්‍රියාවලියක් (ඒ කියන්නේ memory එකට acces කිරීමක්) . හැබැයි මෙහි වෙනස් කමක් දක්නට පුළුවන්, ඒ .. අපි variable එකක් create කරනකොට බාවිතා කරනවා data types කියලා ජාතියක් . int ,char ,short ,float ,long , double කියලා Data-types set එකක් අපි දැනටමත් දන්නවා , මේවට අපි කියනව pre-define data-types කියල, මොකද මේවා නිකන් standards වගේ එදා ඉදලා තිබ්බ දේවල් . 

හැබැයි structs නිර්මාණය කරලා තියෙන්නේ , මේ Pre-define data types සමග බැදුණු varible කිහිපයක් එක් කරගෙන අපිට නව data type එකක් නිර්ම්මාණය කර ගතහැකි අකාරයටයි. අර සෙට් එක bundle කරලා එකක් නිර්මාණය කර ගැනීමක් තමයි සිද්ද වෙන්නේ ,  අන්න ඒ හේතුව නිසා අපි structs කියන්නේ User-define data type එකක් විදියට සලකනවා .

අපි උදාහරණයක් අරන් බලමු ,

```c
#include <stdio.h>
int main(){
char *name; // pointer variable එකක් use කල එකට confused වෙන්න එපා , ඒ කොටසෙන් කියනවා 
char *district;
int student_count;
}
```
👆 ඉහත දක්වල තියෙන විදියට තමයි අපි normally code කරන්නේ  👆

හරි දැන් බලමු , අපි structs බාවිත කරමින් මේ සිදු කරන්නේ කොහොමද කියල .. 
```c
#include <stdio.h>

struct schools{
 char* name;
 char* district;
 int student_count;	
};

int main(){
	
}
```

මේක අපි ලියද්දි Global scope එකෙන් ලියන්නේ ( main එක උඩින්  ලියන්නේ) , එම නිසා globaly available වෙනවා නිකන්ම.
ඒවගේම තමයි මම කලින් කිව්වා වගේ ඔක්කොම bundle කරලා එකකට ගෙනාවට පස්සේ අලුතින් මේ නිර්මාණය වුනේ data type එකක් ( එය User-define data type එකක් කියලත් හදුන්වනවා ), ඉහත උදාහරණයට අනුව , මේකේ Data-type  එක වෙන්නේ struct school කියන එක 
**`🤠  // Data-type එක මොකක්ද කියලා ඇහුවොත් නිකන් school නෙවේ , struct school . 🤠`** 

හරි දැන් Data-type එක නිර්මාණය කර ගෙන අවසානයි. 
දැන් තියෙන්නේ අපිට මේකෙන් ප්‍රයෝජනයක් ගන්න , අපිට මෙය main එකට call කර ගන්න වෙනවා , එහෙමත් නැත්නම් අපි මේ අවස්තාවට කියනවා struct එකක් declare කරනව කියලා , නැතිනම් initialize කරනවා යනුවෙනුත් හදුන්වන්න පුළුවන්. 
struct එක declare කරන්නේ මෙහෙමයි ,

```c
#include <stdio.h>
struct schools{
   char* name;
   char* district;
   int student_count;
};
int main(){
	struct schools f_school;
return 0;
}
```
මේ ආකාරයට declare කර ගත්ත variable එක තවම initialize කළා කියන තැනට ඇවිල්ල නැහැ , එකට හේතුව අපි කිසිම Data එකක් දීල නැති එක , 
මෙන්න මේ ආකාරයට data අපි create කල variable එකට දෙමු ... **`( variable එක : f_school , data type එක : struct schools  )`**

```c
#include <stdio.h>
struct schools{
   char* name;
   char* district;
   int student_count;
};

int main(){
	struct schools f_school;
	f_school.name = "St.thomas College";
	f_school.district = "Matara";
	f_school.student_count = 6500;

    printf("%s \n",f_school.name);
    printf("%s \n",f_school.district);
    printf("%d \n",f_school.student_count);

    return 0;
}
```
__output එක :__

- St.thomas College
- Matara
- 6500

ඒ වගේම අපිට පුළුවන් ඉහත අකාරයට initialize කර ගතපු data , පහත ඇති ආකාරයටත් වෙනස් කර ගැනීමට හැක 

```c
#include <stdio.h>
struct schools{
   char* name;
   char* district;
   int student_count;
};

int main(){
	struct schools f_school = {
        .name = "St.thomas College",
        .district = "Matara",
        .student_count = 6500
    };

    printf("%s \n",f_school.name);
    printf("%s \n",f_school.district);
    printf("%d \n",f_school.student_count);

    return 0;
}

```

අදට එපමණයි , ජයවේවා !🤍
