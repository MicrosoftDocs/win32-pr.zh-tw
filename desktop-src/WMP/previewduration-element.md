---
title: PREVIEWDURATION 元素
description: PREVIEWDURATION 元素會定義剪輯在預覽模式中播放的時間長度。
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- PREVIEWDURATION 元素 Windows Media Player
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989734"
---
# <a name="previewduration-element"></a><span data-ttu-id="7ea2c-104">PREVIEWDURATION 元素</span><span class="sxs-lookup"><span data-stu-id="7ea2c-104">PREVIEWDURATION Element</span></span>

<span data-ttu-id="7ea2c-105">**PREVIEWDURATION** 元素會定義剪輯在預覽模式中播放的時間長度。</span><span class="sxs-lookup"><span data-stu-id="7ea2c-105">The **PREVIEWDURATION** element defines the length of time a clip plays in preview mode.</span></span>

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="7ea2c-106">屬性</span><span class="sxs-lookup"><span data-stu-id="7ea2c-106">Attributes</span></span>

<span data-ttu-id="7ea2c-107">**值** (必要) </span><span class="sxs-lookup"><span data-stu-id="7ea2c-107">**VALUE** (required)</span></span>

<span data-ttu-id="7ea2c-108">剪輯在預覽模式中播放的時間長度 (以小時、分鐘、秒和百分之一為單位的) 。</span><span class="sxs-lookup"><span data-stu-id="7ea2c-108">Length of time (in hours, minutes, seconds, and hundredths of a second) that the clip plays in preview mode.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="7ea2c-109">父/子項目</span><span class="sxs-lookup"><span data-stu-id="7ea2c-109">Parent/Child Elements</span></span>



| <span data-ttu-id="7ea2c-110">階層</span><span class="sxs-lookup"><span data-stu-id="7ea2c-110">Hierarchy</span></span>       | <span data-ttu-id="7ea2c-111">元素</span><span class="sxs-lookup"><span data-stu-id="7ea2c-111">Elements</span></span>                    |
|-----------------|-----------------------------|
| <span data-ttu-id="7ea2c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7ea2c-112">Parent elements</span></span> | <span data-ttu-id="7ea2c-113">**ASX**、 **ENTRY**、 **REF**</span><span class="sxs-lookup"><span data-stu-id="7ea2c-113">**ASX**, **ENTRY**, **REF**</span></span> |
| <span data-ttu-id="7ea2c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="7ea2c-114">Child elements</span></span>  | <span data-ttu-id="7ea2c-115">無</span><span class="sxs-lookup"><span data-stu-id="7ea2c-115">None</span></span>                        |



 

## <a name="remarks"></a><span data-ttu-id="7ea2c-116">備註</span><span class="sxs-lookup"><span data-stu-id="7ea2c-116">Remarks</span></span>

<span data-ttu-id="7ea2c-117">此元素定義剪輯在預覽模式中播放的時間長度。</span><span class="sxs-lookup"><span data-stu-id="7ea2c-117">This element defines the length of time that a clip plays in preview mode.</span></span> <span data-ttu-id="7ea2c-118">如果這個專案出現在 **ENTRY** 元素或 **REF** 元素內，則會套用至該元素所定義的剪輯。</span><span class="sxs-lookup"><span data-stu-id="7ea2c-118">If this element appears within an **ENTRY** element or a **REF** element, it applies to the clip defined by that element.</span></span> <span data-ttu-id="7ea2c-119">如果出現在 **ASX** 元素的範圍內，則會套用至中繼檔中的每個剪輯。</span><span class="sxs-lookup"><span data-stu-id="7ea2c-119">If it appears within the scope of an **ASX** element, it applies to every clip in the metafile.</span></span> <span data-ttu-id="7ea2c-120">**REF** 元素中的 **PREVIEWDURATION** 專案優先于 ENTRY 專案中的專案，而且會優先于 **ASX** **元素中** 的 **PREVIEWDURATION** 元素。</span><span class="sxs-lookup"><span data-stu-id="7ea2c-120">A **PREVIEWDURATION** element in a **REF** element takes precedence over one in an ENTRY **element**, and either takes precedence over a **PREVIEWDURATION** element in an **ASX** element.</span></span> <span data-ttu-id="7ea2c-121">如果未針對剪輯定義任何 **PREVIEWDURATION** 元素，則預設預覽時間為10秒。</span><span class="sxs-lookup"><span data-stu-id="7ea2c-121">If no **PREVIEWDURATION** element is defined for a clip, the default preview time is 10 seconds.</span></span>

<span data-ttu-id="7ea2c-122">如果剪輯有 **STARTTIME** 或 **STARTMARKER** 元素，Windows Media Player 會從下列其中一個專案所定義的點開始轉譯剪輯;否則，它會從剪輯的開頭呈現。</span><span class="sxs-lookup"><span data-stu-id="7ea2c-122">If there is a **STARTTIME** or **STARTMARKER** element for the clip, Windows Media Player renders the clip starting at the point defined by one of these elements; otherwise it renders from the beginning of the clip.</span></span> <span data-ttu-id="7ea2c-123">如果剪輯比 **PREVIEWDURATION** 元素所定義的時間短，則會正常停止。</span><span class="sxs-lookup"><span data-stu-id="7ea2c-123">The clip stops normally if it is shorter than the time defined by the **PREVIEWDURATION** element.</span></span>

<span data-ttu-id="7ea2c-124">**DURATION** 元素會覆寫 **PREVIEWDURATION** 元素。</span><span class="sxs-lookup"><span data-stu-id="7ea2c-124">The **DURATION** element overrides a **PREVIEWDURATION** element.</span></span>

## <a name="examples"></a><span data-ttu-id="7ea2c-125">範例</span><span class="sxs-lookup"><span data-stu-id="7ea2c-125">Examples</span></span>


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="7ea2c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ea2c-126">Requirements</span></span>



| <span data-ttu-id="7ea2c-127">需求</span><span class="sxs-lookup"><span data-stu-id="7ea2c-127">Requirement</span></span> | <span data-ttu-id="7ea2c-128">值</span><span class="sxs-lookup"><span data-stu-id="7ea2c-128">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="7ea2c-129">版本</span><span class="sxs-lookup"><span data-stu-id="7ea2c-129">Version</span></span><br/> | <span data-ttu-id="7ea2c-130">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="7ea2c-130">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7ea2c-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ea2c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ea2c-132">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="7ea2c-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="7ea2c-133">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="7ea2c-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





