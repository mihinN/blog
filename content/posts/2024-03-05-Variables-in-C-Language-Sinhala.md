---
title: Variables in C Language / සිංහල
date: 2022-11-12 
category: notes
# image: https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/f68cf413-ab00-41fc-82fe-0a175144bf20/dfoguih-b630d9e3-21fa-4901-879a-36ab310d0ac2.png/v1/fill/w_1095,h_730,q_70,strp/ninja_rabbit_02_by_darkwhite2981_dfoguih-pre.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9ODU0IiwicGF0aCI6IlwvZlwvZjY4Y2Y0MTMtYWIwMC00MWZjLTgyZmUtMGExNzUxNDRiZjIwXC9kZm9ndWloLWI2MzBkOWUzLTIxZmEtNDkwMS04NzlhLTM2YWIzMTBkMGFjMi5wbmciLCJ3aWR0aCI6Ijw9MTI4MCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.u5-DDBhA9TYBaFQ5lM58TNm-3_3JgxaUjoWCbT4CBgU
alt : Variables in C Language / සිංහල / Sinhala
imageCaption : Samurai rabbit 
showShare : true
comments: false
toc: false
tags:
    - C language 101 
    - 04 lesson

keywords:
    - c programming in සිංහල   
    - Computer Science 

---

මේ  ලිපියෙන් කතා කරන්නෙ variables  ගැන , 

සරලව , අපි programme එකක් ලියද්දි variables යොදා ගන්නේ Computer memory එකේ අපිට අවශ්‍ය data store  ගැනීමට. පරිගනකෙයේ memory එක කිව්වම ඇවිල්ල විවිද type එකේ memory devices තියෙනවා , ඔයාල දන්නවා HARDDISK එක , RAM එක ඊළඟට ප්‍රමාණයෙන් පොඩි හැබැයි speed memory  කොටසක් වන memory registers . 
හැබැයි variable එකක් create කර ගැනීමෙන් computer එකේ main memory එක ,එහෙමත් නැත්නම් ram එකේ අපිට අවශ්‍ය data ස්ටෝරේ කර ගැනීමක් තමයි වෙන්නේ . 

අපි c වල variable එකක් create කරලා වැඩ පටන් ගන්න කලින් , C ගැන පොඩී දෙයක් දැනන්  ඕන , එක ඔයාට js python ruby ,php  වගේ background එකකින්  ආව නම් වැදගත් වෙනවා , 
අපි එක මෙහෙම කියමු , පරිගණක බාෂා නිර්මාණය කරල තියෙන විදිය හා  හැකියාවන් අනුව කොටස් වලට  තියෙනවා , උදාහරණයක් විදියට ගත්තොත් low level , high level functional languages සහා procedural language කියන එක . අන්න ඒ වගේම තව දෙයක් තමයි static type සහ dynamic type කියන්නෙත් .

ඉතින් මෙතැනදී static  type language waladi අපිට variable එකක් create කරද්දී memory එකේ කොච්චර ඉඩක් ගන්න ඕනද කියන එක ටිකක් සවිස්තරව කියන්න වෙනවා. ඒ වෙලාවට අපි දන්න pre-define data types list එකක් තියෙනවා නේ , අන්න ඒ ටික යොදා ගෙන variables create කර ගන්නවා .
