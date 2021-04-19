---
title: STARTTIME 元素
description: STARTTIME 元素會定義時間索引，Windows Media Player 將從該索引開始轉譯資料流程。
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- STARTTIME 元素 Windows Media Player
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981340"
---
# <a name="starttime-element"></a><span data-ttu-id="e5c42-104">STARTTIME 元素</span><span class="sxs-lookup"><span data-stu-id="e5c42-104">STARTTIME Element</span></span>

<span data-ttu-id="e5c42-105">**STARTTIME** 元素會定義時間索引，Windows Media Player 將從該索引開始轉譯資料流程。</span><span class="sxs-lookup"><span data-stu-id="e5c42-105">The **STARTTIME** element defines a time index from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="e5c42-106">屬性</span><span class="sxs-lookup"><span data-stu-id="e5c42-106">Attributes</span></span>

<span data-ttu-id="e5c42-107">**值** (必要) </span><span class="sxs-lookup"><span data-stu-id="e5c42-107">**VALUE** (required)</span></span>

<span data-ttu-id="e5c42-108">時間索引 (時、分、秒和百分之一秒的) ，Windows Media Player 開始播放相關元素中定義的資料流程。</span><span class="sxs-lookup"><span data-stu-id="e5c42-108">The time index (in hours, minutes, seconds, and hundredths of a second) from which Windows Media Player starts playing a stream defined in the associated element.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="e5c42-109">父/子項目</span><span class="sxs-lookup"><span data-stu-id="e5c42-109">Parent/Child Elements</span></span>



| <span data-ttu-id="e5c42-110">階層</span><span class="sxs-lookup"><span data-stu-id="e5c42-110">Hierarchy</span></span>       | <span data-ttu-id="e5c42-111">元素</span><span class="sxs-lookup"><span data-stu-id="e5c42-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="e5c42-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e5c42-112">Parent elements</span></span> | <span data-ttu-id="e5c42-113">**ENTRY**、 **REF**</span><span class="sxs-lookup"><span data-stu-id="e5c42-113">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="e5c42-114">子元素</span><span class="sxs-lookup"><span data-stu-id="e5c42-114">Child elements</span></span>  | <span data-ttu-id="e5c42-115">無</span><span class="sxs-lookup"><span data-stu-id="e5c42-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="e5c42-116">備註</span><span class="sxs-lookup"><span data-stu-id="e5c42-116">Remarks</span></span>

<span data-ttu-id="e5c42-117">這個元素會在內容中定義一個時間索引，Windows Media Player 開始呈現資料流程。</span><span class="sxs-lookup"><span data-stu-id="e5c42-117">This element defines a time index into the content where Windows Media Player is to start rendering the stream.</span></span> <span data-ttu-id="e5c42-118">此元素只可用於已編制索引的預存、隨選內容。</span><span class="sxs-lookup"><span data-stu-id="e5c42-118">This element can be used only with stored, on-demand content that has been indexed.</span></span>

## <a name="examples"></a><span data-ttu-id="e5c42-119">範例</span><span class="sxs-lookup"><span data-stu-id="e5c42-119">Examples</span></span>


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="e5c42-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5c42-120">Requirements</span></span>



| <span data-ttu-id="e5c42-121">需求</span><span class="sxs-lookup"><span data-stu-id="e5c42-121">Requirement</span></span> | <span data-ttu-id="e5c42-122">值</span><span class="sxs-lookup"><span data-stu-id="e5c42-122">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="e5c42-123">版本</span><span class="sxs-lookup"><span data-stu-id="e5c42-123">Version</span></span><br/> | <span data-ttu-id="e5c42-124">Windows Media Player 70 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="e5c42-124">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e5c42-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5c42-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5c42-126">**Windows Media 中繼檔元素參考**</span><span class="sxs-lookup"><span data-stu-id="e5c42-126">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="e5c42-127">**Windows Media 中繼檔參考**</span><span class="sxs-lookup"><span data-stu-id="e5c42-127">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





