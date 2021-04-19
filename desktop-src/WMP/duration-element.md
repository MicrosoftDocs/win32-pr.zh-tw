---
title: DURATION 元素
description: DURATION 元素會定義 Windows Media Player 將呈現相關聯的播放清單專案的時間長度。
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- DURATION 元素 Windows Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994837"
---
# <a name="duration-element"></a><span data-ttu-id="66908-104">DURATION 元素</span><span class="sxs-lookup"><span data-stu-id="66908-104">DURATION Element</span></span>

<span data-ttu-id="66908-105">**DURATION** 元素會定義 Windows Media Player 將呈現相關聯的播放清單專案的時間長度。</span><span class="sxs-lookup"><span data-stu-id="66908-105">The **DURATION** element defines the length of time Windows Media Player will render the associated playlist entry.</span></span>

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="66908-106">屬性</span><span class="sxs-lookup"><span data-stu-id="66908-106">Attributes</span></span>

<span data-ttu-id="66908-107">**值** (必要) </span><span class="sxs-lookup"><span data-stu-id="66908-107">**VALUE** (required)</span></span>

<span data-ttu-id="66908-108">Windows Media Player 呈現專案的時間長度（以小時、分鐘、秒和百分之一秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="66908-108">The length of time, in hours, minutes, seconds, and hundredths of a second, that an entry is rendered by Windows Media Player.</span></span> <span data-ttu-id="66908-109">預設值是專案的整個長度。</span><span class="sxs-lookup"><span data-stu-id="66908-109">The default value is the entire length of the entry.</span></span> <span data-ttu-id="66908-110">如果專案是圖形檔案，則必須指定持續時間值。</span><span class="sxs-lookup"><span data-stu-id="66908-110">If the entry is a graphic file, a duration value must be specified.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="66908-111">父/子項目</span><span class="sxs-lookup"><span data-stu-id="66908-111">Parent/Child Elements</span></span>



| <span data-ttu-id="66908-112">階層</span><span class="sxs-lookup"><span data-stu-id="66908-112">Hierarchy</span></span>       | <span data-ttu-id="66908-113">元素</span><span class="sxs-lookup"><span data-stu-id="66908-113">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="66908-114">父元素</span><span class="sxs-lookup"><span data-stu-id="66908-114">Parent elements</span></span> | <span data-ttu-id="66908-115">**ENTRY**、 **REF**</span><span class="sxs-lookup"><span data-stu-id="66908-115">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="66908-116">子元素</span><span class="sxs-lookup"><span data-stu-id="66908-116">Child elements</span></span>  | <span data-ttu-id="66908-117">無</span><span class="sxs-lookup"><span data-stu-id="66908-117">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="66908-118">備註</span><span class="sxs-lookup"><span data-stu-id="66908-118">Remarks</span></span>

<span data-ttu-id="66908-119">這個元素會定義要轉譯資料流程的時間長度。</span><span class="sxs-lookup"><span data-stu-id="66908-119">This element defines the length of time a stream is to be rendered.</span></span> <span data-ttu-id="66908-120">如果 **VALUE** 屬性超過內容資料流程的長度，資料流程就會在其正常端點終止。</span><span class="sxs-lookup"><span data-stu-id="66908-120">If the **VALUE** attribute exceeds the length of the content stream, the stream terminates at its normal end-point.</span></span>

<span data-ttu-id="66908-121">這個元素可以出現在 **REF** 元素或 **ENTRY** 元素內。</span><span class="sxs-lookup"><span data-stu-id="66908-121">This element can appear either within a **REF** element or within an **ENTRY** element.</span></span> <span data-ttu-id="66908-122">不過，在 **ref** 元素內定義的 DURATION 元素，會覆寫在 **ref** 元素的父 **專案專案** 中顯示的 **DURATION** 元素。</span><span class="sxs-lookup"><span data-stu-id="66908-122">However, a **DURATION** element defined within a **REF** element overrides one that appears within the **REF** element's parent **ENTRY** element.</span></span>

<span data-ttu-id="66908-123">**DURATION** 元素會覆寫 **PREVIEWDURATION** 元素。</span><span class="sxs-lookup"><span data-stu-id="66908-123">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="66908-124">範例</span><span class="sxs-lookup"><span data-stu-id="66908-124">Examples</span></span>


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a><span data-ttu-id="66908-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="66908-125">Requirements</span></span>



| <span data-ttu-id="66908-126">需求</span><span class="sxs-lookup"><span data-stu-id="66908-126">Requirement</span></span> | <span data-ttu-id="66908-127">值</span><span class="sxs-lookup"><span data-stu-id="66908-127">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="66908-128">版本</span><span class="sxs-lookup"><span data-stu-id="66908-128">Version</span></span><br/> | <span data-ttu-id="66908-129">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="66908-129">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66908-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66908-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66908-131">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="66908-131">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="66908-132">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="66908-132">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





