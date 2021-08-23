---
description: GraphEdit 檔案格式
ms.assetid: 84c2de05-6c8f-45f1-b789-04a24cfa3ea1
title: GraphEdit 檔案格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbce90247e710772b75ad31593ce72a1fd4c8f9bd9fabf1be786b1e7bdc5e74d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015596"
---
# <a name="graphedit-file-format"></a>GraphEdit 檔案格式

當 GraphEdit 公用程式儲存 DirectShow 篩選圖形時，它會建立副檔名為 grf 的儲存體檔案。 儲存體檔案包含名為 ActiveMovieGraph 的單一資料流程。 此資料流程包含所有篩選、篩選名稱、檔案名、連接等等的相關資訊。

下列文法會使用修改過的 BNF (巴克斯格式) 語法來描述資料流程中的圖形語法：


```C++
<graph> ::= 
0003\r\n<filters><connections><clock>
END | 
0002\r\n<filters><connections>
END
<filters> ::= 
FILTERS<b> 
[<filter list><b>
]
<filter list> ::= <filter><b> 
[<filter list>
]
<filter> ::= <filter id><b><name><b><class id><b>
[<file>
]<length><b1><filter data>
<class id> ::= <guid>
<file> ::= 
SOURCE <name><b> | 
SINK <name><b>
<connections> ::= 
CONNECTIONS<b> 
{<connection><b>
}
<connection> ::= <filter id><b><pin id><b><filter id><b><pin id><b><media type>
<filter id> ::= <id>
<pin id> ::= <name>
<media type> ::= <sample size><major type><b><subtype><b><flags><format>
<major type> ::= <guid>
<subtype> ::= <guid>
<flags> ::= <fixed sample size><b><temporal compression><b>
<fixed sample size> ::= 1 
| 0
<temporal compression> ::= 1 
| 0
<format> ::= <length><b1><format type><b><length><b1><format data>
<format type> ::= <guid>
<format data> ::= 
{ binary_data 
}
<clock> ::= 
CLOCK <b><required><b><clockid>
\r\n
<required> ::= 1 
| 0
<clockid> ::= <filter id> 
| <class id>
<name> ::= quote_symbol 
{ any_non_quote_character 
} quote_symbol
<length> ::= unsigned decimal number (as a string), indicating the number 
             of bytes of data in the following token.
<guid> ::= GUID in string format. for example: {CF49D4E0-1115-11CE-B03A-0020AF0BA770}
<b> ::= 
{ space_character 
} 
{ \t 
} 
{ \r 
} 
{ \n 
} { <b> 
}
<b1> ::= space_character
<id> ::= integer (as a string), such as 0001
```



輸出時，會有新的一行 ( " \\ r \\ n" ) 每個篩選器，每個連接一個，另一個用於每個關鍵字篩選和連接。 的每個其他案例 <b> 都是單一空格。 關鍵字篩選、連接和結束都無法當地語系化。 另外也請注意，篩選資料和格式資料是二進位，因此可能包含不正確的分行符號、null 值等等。 資料流程會使用寬字元。

下圖顯示典型的圖形。 為了清楚起見， (連接線已中斷，並省略二進位資料。 ) 


```C++
003
FILTERS
0001 "C:\SomeFile.avi" {E436EBB5-524F-11CE-9F53-0020AF0BA770} SOURCE "C:\SomeFile.avi" 0000000000 
0002 "AVI Splitter" {1B544C20-FD0B-11CE-8C63-00AA0044B51E} 0000000000 
0003 "AVI Decompressor" {CF49D4E0-1115-11CE-B03A-0020AF0BA770} 0000000000
0004 "Video Renderer" {70E102B0-5556-11CE-97C0-00AA0055595A} 0000000000
CONNECTIONS
0001 "Output" 0002 "input pin" 0000000288 
   {E436EB83-524F-11CE-9F53-0020AF0BA770} 
   {E436EB88-524F-11CE-9F53-0020AF0BA770} 1 0 0000000001 
   {00000000-0000-0000-0000-000000000000} 0000000000  
0002 "Stream 00" 0003 "In" 0000000376 
   {73646976-0000-0010-8000-00AA00389B71} 
   {64697663-0000-0010-8000-00AA00389B71} 0 0 0000000001 
   {05589F80-C356-11CE-BF01-00AA0055595A} 0000000088 <binary data>
0003 "Out" 0004 "In" 0000000376 
    {73646976-0000-0010-8000-00AA00389B71} 
    {E436EB7D-524F-11CE-9F53-0020AF0BA770} 1 0 0000129600 
    {05589F80-C356-11CE-BF01-00AA0055595A} 0000000088 <binary data> 
CLOCK 1 0000
END
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 GraphEdit 模擬 Graph 建立](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



