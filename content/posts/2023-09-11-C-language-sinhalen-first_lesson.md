---
title: Getting started in C / සිංහල
date: 2023-09-11 
category: notes
image: https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/3a029f5b-07fb-4df6-a114-9ecf9f56f66c/dg8i3u5-e90bc730-f6eb-4ae8-b63f-73c05dda544b.jpg/v1/fill/w_1194,h_669,q_70,strp/dwarven_workshop_by_bouzuki_dg8i3u5-pre.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9NzE4IiwicGF0aCI6IlwvZlwvM2EwMjlmNWItMDdmYi00ZGY2LWExMTQtOWVjZjlmNTZmNjZjXC9kZzhpM3U1LWU5MGJjNzMwLWY2ZWItNGFlOC1iNjNmLTczYzA1ZGRhNTQ0Yi5qcGciLCJ3aWR0aCI6Ijw9MTI4MCJ9XV0sImF1ZCI6WyJ1cm46c2VydmljZTppbWFnZS5vcGVyYXRpb25zIl19.Z5b9zTsoQJIu0NKLtMFV_tQxupoukn1AlU0CfngvXJQ
alt : Getting started in C / සිංහල
# imageCaption : https://www.deviantart.com/bouzuki/art/Dwarven-workshop-981740525
showShare : true
comments: false
toc: false
tags:
    - C language 101 

keywords:
    - c programming in සිංහල   
    - Computer Science 

---
# "පුරෝකථනයක්" 
**"C"** පාඩම් මාලාව පටන් ගන්න කලින් , මට නිකමට ලිපියක් ලියල  දාන්න හිතුන , ඇයි ඇත්තටම මේ (C) පරිගණක බාශාවම  ලිපි ටිකක් විදියට දාන්න හිතුන එක ගැන . මේකෙදි අපිට C වල අතීත කතාව නොකිය ඉන්නම බැහැ , මොකද සරලවම C language එක බාවිතයට් ගෙන  තමයි අද අපි බාවිතා කරන Operating Systems , ඒ වගේම device drivers , network හා සම්බන්ද applications , Embedded Systems සහ Databases වැනි බොහොමයක් ලියල තියෙන්නේ .
ඉතින් 1972 දී , Dennis Richie මහතා  Bell labs සමග වැඩ කරන කාලේ තමයි C language එක නිර්මාණය කරන්නේ , මෙතැනදී කියන්න ඕන අපි දැනට බාවිතා  කරන technology side එකේ දේවල් බොහොමයකට ආරම්බය  වෙලා  තියෙන්නේ bell labs සහ එහි සිටිය set එකේ පරිශ්‍රමය මත.. හරි දැනට දල අදහසක් තියෙනවා  නේ අපි මේ code කරන්න බාවිත කරන බාශාව ගැන .. ! 
ඒවගේම දෙයක් තියෙනවා  C බාෂාව තවත් විශේෂ වෙන , ඒ තමයි C වලට හැකියාව පවතිනවා  Directly memory එක Access කරන්න , මේ දේ නිසා  අපිට Data structures ලියද්දි සහ අලුත් ඒවා  නිර්මාණය කරද්දී වටිනවා  .. අපි අනිවාර්යෙන්ම මේ සම්බන්දව Pointers ගැන කතා  කරනකොට , කතාකරමු .

![Dennis Richie](http://2.bp.blogspot.com/-9b8ZD8nw9cE/UZfxNrVi09I/AAAAAAAABlc/KEOcnLhPbpQ/s1600/DennisRichie.jpg "Dennis Richie")

දැන් code කරන්න වෙලාව හරි , මේකට අපිට CodeBLocks වගේ IDE එකක් යොදා  ගන්න පුළුවන් , නැත්නම් හොදම විදිය කියල මම හිතන්නේ Old School විදියට text editor එකේ type කරලා  compiler එකක් use කර ගෙන compile කර ගන්න එක . ( ඇත්තටම text editor එක බාවිත කරලා  ඉගෙන ගන්න වෙලාවේ code කරන එක මම පුද්ගලිකව හිතනවා හොදයි කියල , under the hood වෙන දේවල් ඉගෙන ගන්න පුළුවන් මේ විදියෙන් , හැබැයි ලොකු systems මේ විදියට ලියන්නේ නැහැ  ) , අනෙක් දේ තමයි Operating system එක , අපිට කැමති එකක ලියන්න පුළුවන් , හැබැයි Windows / Mac වලට වඩා  මේක ඉගෙන ගන්න වේලාවෙ මොනවා  හරි Linux/Unix based OS එකක ලියන එක වටිනවා  , එකට හේතුව තමයි windows සහ Mac වල restrictions වැඩි , ඒ වගේම අපිට c එක්ක ඉදිරියට වැඩ කරද්දී සමහර system calls එහෙම programme ඇතුලේ call කරන්න වෙනවා , අන්න එනත්නදී ගැටළු එන්න පුළුවන් . ( මෙතැනදී Ubuntu වගේ එකක් use කරන එක හොදයි , හොද package manager එකකුත් තියෙන එකේ පහසුයි මේ වැඩෙ කරන් යන්න ) .  vm එකක Ubuntu install කරන ආකාරය මම ලිපියක් දාන්නම්.

හරි දැන් අපි දැන් C වල අතීත විත්ති ටිකකුත් දැන ගෙන , ගැලපෙන Os එකකුත් දා  ගන්න එකත් දැනගෙන ඉන්න අතරේ , ඊළඟට මේ වැඩේට අවශ්‍ය මොකක්ද කියන එක අපි බලන්න ඕන , ඔව් .. ඊළඟට ඕන compiler එකක් , compiler එක කියන්නෙත් එක්තරා  ආකාරයක application එකක්, මේක බාවිතයට ගන්නේ අපි High level language එකක් බාවිතා  කරලා  ලියන programme එක machine code එක බවට පරිවර්තනය කර ගන්න .  ඉතින් මෙතැනදී අපි gcc compiler එක යොදා  ගන්නවා  අපේ c programme එක compile කර ගන්න , ඔයාලට වෙන දෙයක් test කරලා බලන්න ඕන නම් පොඩ්ඩක් google කරලා  බලන්න, set එකක්ම තියෙනවා  .

ඉතින් , අදට මම මේ ලිපිය මෙතැනින් ඉවර කරනවා  , ඊළඟ ලිපියේ අපි compiler එක install කරලා  code කරන්න පටන් ගමු (Ubuntu වල gcc එකනම් inbuild එනවා  , අපි clang වගේ එකකුත් test කරලා  බලමු ) , එහෙනම්  
ජයවේවා !