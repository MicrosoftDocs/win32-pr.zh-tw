---
title: STARTMARKER 元素
description: STARTMARKER 元素會指定 Windows Media Player 將開始呈現資料流程的標記。
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- STARTMARKER 元素 Windows Media Player
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995443"
---
# <a name="startmarker-element"></a><span data-ttu-id="47191-104">STARTMARKER 元素</span><span class="sxs-lookup"><span data-stu-id="47191-104">STARTMARKER Element</span></span>

<span data-ttu-id="47191-105">**STARTMARKER** 元素會指定 Windows Media Player 將開始呈現資料流程的標記。</span><span class="sxs-lookup"><span data-stu-id="47191-105">The **STARTMARKER** element specifies a marker from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="47191-106">屬性</span><span class="sxs-lookup"><span data-stu-id="47191-106">Attributes</span></span>

<span data-ttu-id="47191-107">**數量**</span><span class="sxs-lookup"><span data-stu-id="47191-107">**NUMBER**</span></span>

<span data-ttu-id="47191-108">索引中數值標記的數目。</span><span class="sxs-lookup"><span data-stu-id="47191-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="47191-109">預設值是即時資料流中的隨選內容或目前位置的開始位置。</span><span class="sxs-lookup"><span data-stu-id="47191-109">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

<span data-ttu-id="47191-110">**名稱**</span><span class="sxs-lookup"><span data-stu-id="47191-110">**NAME**</span></span>

<span data-ttu-id="47191-111">索引中命名標記的名稱。</span><span class="sxs-lookup"><span data-stu-id="47191-111">The name of a named marker in the index.</span></span> <span data-ttu-id="47191-112">預設值是即時資料流中的隨選內容或目前位置的開始位置。</span><span class="sxs-lookup"><span data-stu-id="47191-112">The default value is the beginning of on-demand content or the current position in a real-time stream.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="47191-113">父/子項目</span><span class="sxs-lookup"><span data-stu-id="47191-113">Parent/Child Elements</span></span>



| <span data-ttu-id="47191-114">階層</span><span class="sxs-lookup"><span data-stu-id="47191-114">Hierarchy</span></span>       | <span data-ttu-id="47191-115">元素</span><span class="sxs-lookup"><span data-stu-id="47191-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="47191-116">父元素</span><span class="sxs-lookup"><span data-stu-id="47191-116">Parent elements</span></span> | <span data-ttu-id="47191-117">**ENTRY**、 **REF**</span><span class="sxs-lookup"><span data-stu-id="47191-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="47191-118">子元素</span><span class="sxs-lookup"><span data-stu-id="47191-118">Child elements</span></span>  | <span data-ttu-id="47191-119">無</span><span class="sxs-lookup"><span data-stu-id="47191-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="47191-120">備註</span><span class="sxs-lookup"><span data-stu-id="47191-120">Remarks</span></span>

<span data-ttu-id="47191-121">這個元素會指定 Windows Media Player 用來開始轉譯父 **專案** 或 **REF** 元素中定義之資料流程的標記。</span><span class="sxs-lookup"><span data-stu-id="47191-121">This element specifies the marker from which Windows Media Player is to start rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="47191-122">**注意**</span><span class="sxs-lookup"><span data-stu-id="47191-122">**Note**</span></span>

<span data-ttu-id="47191-123">您可以使用 **數位** 或 **名稱** 屬性來使用此元素，但不能同時使用兩者。</span><span class="sxs-lookup"><span data-stu-id="47191-123">Use this element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="47191-124">在 **ref** 元素內定義的 **STARTMARKER** 元素優先于 **Ref** 元素的父 **專案專案** 中所定義的 **STARTMARKER** 元素。</span><span class="sxs-lookup"><span data-stu-id="47191-124">A **STARTMARKER** element defined within a **REF** element takes precedence over a **STARTMARKER** element defined within the **REF** element's parent **ENTRY** element.</span></span> <span data-ttu-id="47191-125">**STARTMARKER** 元素也優先于 **STARTTIME** 元素。</span><span class="sxs-lookup"><span data-stu-id="47191-125">A **STARTMARKER** element also takes precedence over a **STARTTIME** element.</span></span>

<span data-ttu-id="47191-126">如果 **STARTMARKER** 元素所指定的標記在資料流程中的後面比 **ENDMARKER** 專案所定義的標記還新，則不會播放任何內容，但不會產生任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="47191-126">If the marker specified by a **STARTMARKER** element occurs later in the stream than the marker defined by an **ENDMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="47191-127">範例</span><span class="sxs-lookup"><span data-stu-id="47191-127">Examples</span></span>


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
```



## <a name="requirements"></a><span data-ttu-id="47191-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="47191-128">Requirements</span></span>



| <span data-ttu-id="47191-129">需求</span><span class="sxs-lookup"><span data-stu-id="47191-129">Requirement</span></span> | <span data-ttu-id="47191-130">值</span><span class="sxs-lookup"><span data-stu-id="47191-130">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="47191-131">版本</span><span class="sxs-lookup"><span data-stu-id="47191-131">Version</span></span><br/> | <span data-ttu-id="47191-132">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="47191-132">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="47191-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47191-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47191-134">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="47191-134">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="47191-135">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="47191-135">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





