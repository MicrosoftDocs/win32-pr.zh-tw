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
# <a name="comments-msfeedsh"></a><span data-ttu-id="70fab-105">批註 (Msfeeds .h) </span><span class="sxs-lookup"><span data-stu-id="70fab-105">Comments (Msfeeds.h)</span></span>

<span data-ttu-id="70fab-106">遵循可延伸標記語言 (XML)  (XML) 語法，將批註新增至中繼檔。</span><span class="sxs-lookup"><span data-stu-id="70fab-106">Add comments to metafiles by following Extensible Markup Language (XML) syntax.</span></span> <span data-ttu-id="70fab-107">批註的開頭為 " &lt; !--"，結尾為 "-- &gt; "。</span><span class="sxs-lookup"><span data-stu-id="70fab-107">Comments begin with "&lt;!--" and end with "--&gt;".</span></span>

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a><span data-ttu-id="70fab-108">備註</span><span class="sxs-lookup"><span data-stu-id="70fab-108">Remarks</span></span>

<span data-ttu-id="70fab-109">批註可以出現在專案內容 (的任何地方，但在專案的開啟和關閉標記之間， < >) 。</span><span class="sxs-lookup"><span data-stu-id="70fab-109">Comments can appear anywhere except within element content (between element open and close tags, < >).</span></span> <span data-ttu-id="70fab-110">它們不是檔字元資料的一部分，而且會在剖析中繼檔時被忽略。</span><span class="sxs-lookup"><span data-stu-id="70fab-110">They are not part of the document's character data and are ignored when the metafile is parsed.</span></span>

## <a name="examples"></a><span data-ttu-id="70fab-111">範例</span><span class="sxs-lookup"><span data-stu-id="70fab-111">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="70fab-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="70fab-112">Requirements</span></span>



| <span data-ttu-id="70fab-113">需求</span><span class="sxs-lookup"><span data-stu-id="70fab-113">Requirement</span></span> | <span data-ttu-id="70fab-114">值</span><span class="sxs-lookup"><span data-stu-id="70fab-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="70fab-115">標頭</span><span class="sxs-lookup"><span data-stu-id="70fab-115">Header</span></span><br/> | <dl> <span data-ttu-id="70fab-116"><dt>Msfeeds。h</dt></span><span class="sxs-lookup"><span data-stu-id="70fab-116"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70fab-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70fab-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70fab-118">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="70fab-118">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





