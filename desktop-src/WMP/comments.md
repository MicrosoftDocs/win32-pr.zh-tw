---
title: '批註 (Msfeeds .h) '
description: 遵循可延伸標記語言 (XML)  (XML) 語法，將批註新增至中繼檔。 批註的開頭為 \ 0034;--\ 0034;並以 \ 0034;--\ 0034; 結尾。
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- 批註 Windows Media Player
topic_type:
- apiref
api_name:
- Comments
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701f456cae9f1432ed42235a3a6e13af555b2b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984889"
---
# <a name="comments-msfeedsh"></a>批註 (Msfeeds .h) 

遵循可延伸標記語言 (XML)  (XML) 語法，將批註新增至中繼檔。 批註的開頭為 " &lt; !--"，結尾為 "-- &gt; "。

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>備註

批註可以出現在專案內容 (的任何地方，但在專案的開啟和關閉標記之間， < >) 。 它們不是檔字元資料的一部分，而且會在剖析中繼檔時被忽略。

## <a name="examples"></a>範例


```XML
<ASX version = "3.0">
<!-- This information is only visible when editing a metafile file. -->
<!--<BANNER HREF="c:\wmsdk\wmssdk\samples\dhtml\asfbutton3.gif">
    </BANNER>-->
    <ENTRY>
        <REF HREF = "mms://proseware.com/pubpt/filename.asf" />
    </ENTRY>

    <ENTRY>
        <TITLE>WMA Port na Pucai</TITLE>
        <!--<DURATION VALUE="00:00:15"/>-->
        <REF href="c:\asfroot\Port na Pucai.wma"/>
    </ENTRY></ASX>

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Msfeeds。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Windows Media 中繼檔元素參考**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





