---
title: AUTHOR 元素
description: AUTHOR 元素包含 Windows Media 中繼檔或媒體剪輯的作者名稱。
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- AUTHOR 元素 Windows Media Player
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995623"
---
# <a name="author-element"></a><span data-ttu-id="8f2f2-104">AUTHOR 元素</span><span class="sxs-lookup"><span data-stu-id="8f2f2-104">AUTHOR Element</span></span>

<span data-ttu-id="8f2f2-105">**Author** 元素包含 Windows Media 中繼檔或媒體剪輯的作者名稱。</span><span class="sxs-lookup"><span data-stu-id="8f2f2-105">The **AUTHOR** element contains the name of the author of a Windows Media metafile or media clip.</span></span>

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a><span data-ttu-id="8f2f2-106">屬性</span><span class="sxs-lookup"><span data-stu-id="8f2f2-106">Attributes</span></span>

<span data-ttu-id="8f2f2-107">這個元素沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="8f2f2-107">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="8f2f2-108">父/子項目</span><span class="sxs-lookup"><span data-stu-id="8f2f2-108">Parent/Child Elements</span></span>



| <span data-ttu-id="8f2f2-109">階層</span><span class="sxs-lookup"><span data-stu-id="8f2f2-109">Hierarchy</span></span>       | <span data-ttu-id="8f2f2-110">元素</span><span class="sxs-lookup"><span data-stu-id="8f2f2-110">Element</span></span>            |
|-----------------|--------------------|
| <span data-ttu-id="8f2f2-111">父元素</span><span class="sxs-lookup"><span data-stu-id="8f2f2-111">Parent elements</span></span> | <span data-ttu-id="8f2f2-112">**ASX**， **進入**</span><span class="sxs-lookup"><span data-stu-id="8f2f2-112">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="8f2f2-113">子元素</span><span class="sxs-lookup"><span data-stu-id="8f2f2-113">Child elements</span></span>  | <span data-ttu-id="8f2f2-114">無</span><span class="sxs-lookup"><span data-stu-id="8f2f2-114">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="8f2f2-115">備註</span><span class="sxs-lookup"><span data-stu-id="8f2f2-115">Remarks</span></span>

<span data-ttu-id="8f2f2-116">這個元素包含一個文字字串，代表 Windows Media 中繼檔或媒體剪輯的作者名稱。</span><span class="sxs-lookup"><span data-stu-id="8f2f2-116">This element contains a text string representing the name of the author of a Windows Media metafile or media clip.</span></span> <span data-ttu-id="8f2f2-117">您可以使用 **ASX** 元素內的 AUTHOR 元素，以及 **專案專案** 內的 **AUTHOR** 專案。</span><span class="sxs-lookup"><span data-stu-id="8f2f2-117">You can use the **AUTHOR** element within the **ASX** element and within **ENTRY** elements.</span></span>

<span data-ttu-id="8f2f2-118">如果此元素出現在 **ASX** 專案中，則文字會顯示為 [ **顯示** 資訊]。</span><span class="sxs-lookup"><span data-stu-id="8f2f2-118">If this element appears in the **ASX** element, the text is displayed as **Show** information.</span></span>

<span data-ttu-id="8f2f2-119">如果這個元素出現在 **ENTRY 專案** 中，文字就會顯示為剪輯作者。</span><span class="sxs-lookup"><span data-stu-id="8f2f2-119">If this element appears in an **ENTRY** element, the text is displayed as the clip author.</span></span>

<span data-ttu-id="8f2f2-120">每個父 **ASX** 和 **ENTRY** 元素最多隻能包含一個子 **作者** 元素。</span><span class="sxs-lookup"><span data-stu-id="8f2f2-120">Each parent **ASX** and **ENTRY** element should contain at most one child **AUTHOR** element.</span></span> <span data-ttu-id="8f2f2-121">第一個專案之後的多個 **AUTHOR** 元素將會被忽略，且不會顯示。</span><span class="sxs-lookup"><span data-stu-id="8f2f2-121">Multiple **AUTHOR** elements after the first will be ignored and will not be displayed.</span></span>

## <a name="examples"></a><span data-ttu-id="8f2f2-122">範例</span><span class="sxs-lookup"><span data-stu-id="8f2f2-122">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="8f2f2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f2f2-123">Requirements</span></span>



| <span data-ttu-id="8f2f2-124">需求</span><span class="sxs-lookup"><span data-stu-id="8f2f2-124">Requirement</span></span> | <span data-ttu-id="8f2f2-125">值</span><span class="sxs-lookup"><span data-stu-id="8f2f2-125">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="8f2f2-126">版本</span><span class="sxs-lookup"><span data-stu-id="8f2f2-126">Version</span></span><br/> | <span data-ttu-id="8f2f2-127">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="8f2f2-127">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f2f2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f2f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f2f2-129">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="8f2f2-129">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="8f2f2-130">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="8f2f2-130">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





