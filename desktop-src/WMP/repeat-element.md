---
title: REPEAT 元素
description: REPEAT 元素會定義 Windows Media Player 重複一或多個 ENTRY 或 ENTRYREF 元素的次數。
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- 重複元素 Windows Media Player
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978460"
---
# <a name="repeat-element"></a><span data-ttu-id="b6ad6-104">REPEAT 元素</span><span class="sxs-lookup"><span data-stu-id="b6ad6-104">REPEAT Element</span></span>

<span data-ttu-id="b6ad6-105">**REPEAT** 元素會定義 Windows Media Player 重複一或多個 **ENTRY** 或 **ENTRYREF** 元素的次數。</span><span class="sxs-lookup"><span data-stu-id="b6ad6-105">The **REPEAT** element defines the number of times Windows Media Player repeats one or more **ENTRY** or **ENTRYREF** elements.</span></span>

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a><span data-ttu-id="b6ad6-106">屬性</span><span class="sxs-lookup"><span data-stu-id="b6ad6-106">Attributes</span></span>

<span data-ttu-id="b6ad6-107">**COUNT**</span><span class="sxs-lookup"><span data-stu-id="b6ad6-107">**COUNT**</span></span>

<span data-ttu-id="b6ad6-108">整數，代表 Windows Media Player 重複此專案範圍內的 **專案** 與 **ENTRYREF** 元素的次數。</span><span class="sxs-lookup"><span data-stu-id="b6ad6-108">Integer representing the number of times Windows Media Player repeats the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="b6ad6-109">父/子項目</span><span class="sxs-lookup"><span data-stu-id="b6ad6-109">Parent/Child Elements</span></span>



| <span data-ttu-id="b6ad6-110">階層</span><span class="sxs-lookup"><span data-stu-id="b6ad6-110">Hierarchy</span></span>       | <span data-ttu-id="b6ad6-111">元素</span><span class="sxs-lookup"><span data-stu-id="b6ad6-111">Elements</span></span>                |
|-----------------|-------------------------|
| <span data-ttu-id="b6ad6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b6ad6-112">Parent elements</span></span> | <span data-ttu-id="b6ad6-113">**.ASX**</span><span class="sxs-lookup"><span data-stu-id="b6ad6-113">**ASX**</span></span>                 |
| <span data-ttu-id="b6ad6-114">子元素</span><span class="sxs-lookup"><span data-stu-id="b6ad6-114">Child elements</span></span>  | <span data-ttu-id="b6ad6-115">**ENTRY**、 **ENTRYREF**</span><span class="sxs-lookup"><span data-stu-id="b6ad6-115">**ENTRY**, **ENTRYREF**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b6ad6-116">備註</span><span class="sxs-lookup"><span data-stu-id="b6ad6-116">Remarks</span></span>

<span data-ttu-id="b6ad6-117">這個元素會定義 Windows Media Player 重複或迴圈的次數，以及此專案範圍內的 **ENTRY** 和 **ENTRYREF** 元素所定義的剪輯。</span><span class="sxs-lookup"><span data-stu-id="b6ad6-117">This element defines the number of times Windows Media Player repeats, or loops through, the clips defined by the **ENTRY** and **ENTRYREF** elements within this element's scope.</span></span> <span data-ttu-id="b6ad6-118">只有中繼檔中的第一個 **重複** 元素是有效的;後續的 **重複** 元素會被忽略。</span><span class="sxs-lookup"><span data-stu-id="b6ad6-118">Only the first **REPEAT** element in a metafile is valid; subsequent **REPEAT** elements are ignored.</span></span>

<span data-ttu-id="b6ad6-119">如果未定義 **COUNT** 屬性，相關聯的專案和 ENTRYREF **專案** 中的內容就會重複一次無限的次數。</span><span class="sxs-lookup"><span data-stu-id="b6ad6-119">If no **COUNT** attribute is defined, the content in the associated **ENTRY** and **ENTRYREF** elements repeats an infinite number of times.</span></span> <span data-ttu-id="b6ad6-120">值為零會導致 Windows Media Player 忽略 **重複** 專案並播放一次內容。</span><span class="sxs-lookup"><span data-stu-id="b6ad6-120">A value of zero causes Windows Media Player to ignore the **REPEAT** element and play the content once.</span></span>

## <a name="examples"></a><span data-ttu-id="b6ad6-121">範例</span><span class="sxs-lookup"><span data-stu-id="b6ad6-121">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
</ASX>
```



## <a name="requirements"></a><span data-ttu-id="b6ad6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b6ad6-122">Requirements</span></span>



| <span data-ttu-id="b6ad6-123">需求</span><span class="sxs-lookup"><span data-stu-id="b6ad6-123">Requirement</span></span> | <span data-ttu-id="b6ad6-124">值</span><span class="sxs-lookup"><span data-stu-id="b6ad6-124">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="b6ad6-125">版本</span><span class="sxs-lookup"><span data-stu-id="b6ad6-125">Version</span></span><br/> | <span data-ttu-id="b6ad6-126">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="b6ad6-126">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6ad6-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b6ad6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6ad6-128">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="b6ad6-128">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="b6ad6-129">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="b6ad6-129">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





