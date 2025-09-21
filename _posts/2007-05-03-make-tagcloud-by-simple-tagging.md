---
id: 40
title: WordPress如何生成標簽云？
date: '2007-05-03T22:36:16+00:00'
author: Westbank
layout: post
guid: 'http://scottie.cn/?p=87'
permalink: /2007/05/03/make-tagcloud-by-simple-tagging/
bot_views:
    - '7496'
views:
    - '2505'
latest_home_img:
    - wp.jpg
duoshuo_thread_id:
    - '1246078726781796392'
post_views_count:
    - '320'
categories:
    - 一地鸡毛
tags:
    - plugins
    - wordpress
---

居然有人向我問起WP的技術問題！我真的是菜鳥啊。在側邊欄(sidebar)生成一片花花世界算是我使用wp的一個小小的夢想吧。之前瀏覽了一些相關技術文章，可能我很笨，反正試驗都失敗了。這一次偶然來到一老外的網站software guide，標簽云突然就這樣做成功了。以下是我的經驗：(本文只針對和我一樣的wordpress的入門學員)

1. 在后臺停用原來裝載的 Utimate Tag Worrior 或Jerome's Keywords，可能不少人都裝有這兩個插件，停用當然是為了避免插件沖突。

2. 下載兩個新的Tag插件，simple-tagging (Download 1) 和 simpletagging-widget (Download 2), 解壓得到這兩個文件（插件）

3. 用FTP工具將這兩個插件上傳到wordpress的plugins目錄，在后臺激活。

4. 登錄后臺後，你可以看到在設置項后面多了一個Tags項，點擊進入。下面有4個小項（看來這個插件的功能相當強大，其他功能我沒來得及去研究），你在第一個 Tag Options 里面可以做一些調整，比如在include categories in tag cloud 后面打勾，這樣你原來博客做的分類將全部進入標簽云；還有在Tag cloud sort order 選擇 natural, 這樣標簽云的排列將會按照英文字母排列，中文和英文的標簽就可以分開，當然如果你全是使用的中文標簽，那就無所謂了。其余項目可以按照缺省值而不去管了。 

5. 將simpletagging-widget 在后臺的sidebar中鼠標拖移到你認為合適的地方，保存。

6. 在后臺撰寫日志，文章尾端的地方用逗號添加tags，發布。怎么樣，重新打開瀏覽器，你是不是看到了側邊欄上出現了標簽云，下面有你剛才輸入的標簽以及你原來設定的categories.

7. 可惜，這個時候你看到的標簽云排列是豎列的！！！要做到橫向排列，還差最后一步！將以下代碼放置到你使用模板的style (層疊樣式表文檔，也就是style.css)當中，一般是位于那個末端的

code {
font: 13px 'Courier New', Courier, Verdana, Arial, sans-serif;
color: #666;
padding: 2px;
}

代碼之后，拷貝以下代碼：

ul#tagcloud { padding:0; margin:0; text-align:center;
 list-style:none; }
ul#tagcloud li { display:inline; font-size:70%; color:#ccc;
 background: none; padding: 0;}
ul#tagcloud li a, ul#tagcloud li a:link { text-decoration:none; }
ul#tagcloud li a:hover { text-decoration:underline; }
ul#tagcloud li.t1 a { color:#797979; font-size: 120%; }
ul#tagcloud li.t2 a { color:#6d6d6d; font-size: 160%; }
ul#tagcloud li.t3 a { color:#616161; font-size: 190%; }
ul#tagcloud li.t4 a { color:#555555; font-size: 210%; }
ul#tagcloud li.t5 a { color:#484848; font-size: 230%; }
ul#tagcloud li.t6 a { color:#3c3c3c; font-size: 250%; }
ul#tagcloud li.t7 a { color:#303030; font-size: 270%; }
ul#tagcloud li.t8 a { color:#242424; font-size: 290%; }
ul#tagcloud li.t9 a { color:#181818; font-size: 310%; }
ul#tagcloud li.t10 a { color:#0c0c0c; font-size: 330%; }



8. 保存。OKAY，終于搞定了標簽云。最后要注意的是，模板必須支持sidebar才能實現標簽云的功能。而且你每次到要到后臺手動輸入文章的各個標簽，以英語輸入法狀態下的逗號(,)進行各個標簽的分隔。具體效果請見本博的側邊欄。希望以上說明對各位設置tag cloud有所幫助。

Del.icio.us : wordpress, 標簽云
