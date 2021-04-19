---
title: ENDMARKER 元素
description: ENDMARKER 元素會指定 Windows Media Player 將停止轉譯資料流程的標記。
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- ENDMARKER 元素 Windows Media Player
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996300"
---
# <a name="endmarker-element"></a><span data-ttu-id="d034a-104">ENDMARKER 元素</span><span class="sxs-lookup"><span data-stu-id="d034a-104">ENDMARKER Element</span></span>

<span data-ttu-id="d034a-105">**ENDMARKER** 元素會指定 Windows Media Player 將停止轉譯資料流程的標記。</span><span class="sxs-lookup"><span data-stu-id="d034a-105">The **ENDMARKER** element specifies a marker at which Windows Media Player will stop rendering the stream.</span></span>

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a><span data-ttu-id="d034a-106">屬性</span><span class="sxs-lookup"><span data-stu-id="d034a-106">Attributes</span></span>

<span data-ttu-id="d034a-107">**數量**</span><span class="sxs-lookup"><span data-stu-id="d034a-107">**NUMBER**</span></span>

<span data-ttu-id="d034a-108">索引中數值標記的數目。</span><span class="sxs-lookup"><span data-stu-id="d034a-108">The number of a numeric marker in the index.</span></span> <span data-ttu-id="d034a-109">預設值是內容的結尾。</span><span class="sxs-lookup"><span data-stu-id="d034a-109">The default value is the end of the content.</span></span>

<span data-ttu-id="d034a-110">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d034a-110">**NAME**</span></span>

<span data-ttu-id="d034a-111">索引中命名標記的名稱。</span><span class="sxs-lookup"><span data-stu-id="d034a-111">The name of a named marker in the index.</span></span> <span data-ttu-id="d034a-112">預設值是內容的結尾。</span><span class="sxs-lookup"><span data-stu-id="d034a-112">The default value is the end of the content.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="d034a-113">父/子項目</span><span class="sxs-lookup"><span data-stu-id="d034a-113">Parent/Child Elements</span></span>



| <span data-ttu-id="d034a-114">階層</span><span class="sxs-lookup"><span data-stu-id="d034a-114">Hierarchy</span></span>       | <span data-ttu-id="d034a-115">元素</span><span class="sxs-lookup"><span data-stu-id="d034a-115">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="d034a-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d034a-116">Parent elements</span></span> | <span data-ttu-id="d034a-117">**ENTRY**、 **REF**</span><span class="sxs-lookup"><span data-stu-id="d034a-117">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="d034a-118">子元素</span><span class="sxs-lookup"><span data-stu-id="d034a-118">Child elements</span></span>  | <span data-ttu-id="d034a-119">無</span><span class="sxs-lookup"><span data-stu-id="d034a-119">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="d034a-120">備註</span><span class="sxs-lookup"><span data-stu-id="d034a-120">Remarks</span></span>

<span data-ttu-id="d034a-121">這個元素會指定標記，其中 Windows Media Player 是用來停止轉譯在父 **專案** 或 **REF** 元素中定義的資料流程。</span><span class="sxs-lookup"><span data-stu-id="d034a-121">This element specifies the marker where Windows Media Player is to stop rendering the stream defined in the parent **ENTRY** or **REF** element.</span></span>

<span data-ttu-id="d034a-122">注意</span><span class="sxs-lookup"><span data-stu-id="d034a-122">Note</span></span>

<span data-ttu-id="d034a-123">使用具有 **NUMBER** 或 **NAME** 屬性的 **ENDMARKER** 元素，但不能同時使用兩者。</span><span class="sxs-lookup"><span data-stu-id="d034a-123">Use the **ENDMARKER** element with either the **NUMBER** or **NAME** attribute, but not both.</span></span>

<span data-ttu-id="d034a-124">在預覽模式中，即使 **PREVIEWDURATION** 元素所指定的時間尚未經過，到達結束標記也會停止預覽。</span><span class="sxs-lookup"><span data-stu-id="d034a-124">In preview mode, reaching an end marker stops the preview, even if the time specified by the **PREVIEWDURATION** element has not elapsed.</span></span> <span data-ttu-id="d034a-125">**ENDMARKER** 元素也優先于 **DURATION** 元素。</span><span class="sxs-lookup"><span data-stu-id="d034a-125">The **ENDMARKER** element also takes precedence over the **DURATION** element.</span></span>

<span data-ttu-id="d034a-126">在 **ref** 元素內定義的 **ENDMARKER** 元素優先于 **Ref** 元素的父 **專案專案** 內定義的 **ENDMARKER** 。</span><span class="sxs-lookup"><span data-stu-id="d034a-126">An **ENDMARKER** element defined within a **REF** element takes precedence over an **ENDMARKER** defined within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="d034a-127">如果 **ENDMARKER** 元素所指定的標記在資料流程中比 **STARTMARKER** 專案所定義的標記稍早出現，則不會播放任何內容，但不會產生任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="d034a-127">If the marker specified by an **ENDMARKER** element occurs earlier in the stream than the marker defined by a **STARTMARKER** element, no content plays, but no error is generated.</span></span>

## <a name="examples"></a><span data-ttu-id="d034a-128">範例</span><span class="sxs-lookup"><span data-stu-id="d034a-128">Examples</span></span>


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

```



## <a name="requirements"></a><span data-ttu-id="d034a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d034a-129">Requirements</span></span>



| <span data-ttu-id="d034a-130">需求</span><span class="sxs-lookup"><span data-stu-id="d034a-130">Requirement</span></span> | <span data-ttu-id="d034a-131">值</span><span class="sxs-lookup"><span data-stu-id="d034a-131">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="d034a-132">版本</span><span class="sxs-lookup"><span data-stu-id="d034a-132">Version</span></span><br/> | <span data-ttu-id="d034a-133">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="d034a-133">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d034a-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d034a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d034a-135">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="d034a-135">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d034a-136">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="d034a-136">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





