---
title: 滑杆. useForegroundProgress
description: UseForegroundProgress 屬性會指定或抓取值，指出是否會使用前景進度列。
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- UseForegroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989722"
---
# <a name="slideruseforegroundprogress"></a><span data-ttu-id="dd3b3-104">滑杆. useForegroundProgress</span><span class="sxs-lookup"><span data-stu-id="dd3b3-104">SLIDER.useForegroundProgress</span></span>

<span data-ttu-id="dd3b3-105">**UseForegroundProgress** 屬性會指定或抓取值，指出是否會使用前景進度列。</span><span class="sxs-lookup"><span data-stu-id="dd3b3-105">The **useForegroundProgress** attribute specifies or retrieves a value indicating whether the foreground progress bar will be used.</span></span>

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="dd3b3-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="dd3b3-106">Possible Values</span></span>

<span data-ttu-id="dd3b3-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="dd3b3-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="dd3b3-108">值</span><span class="sxs-lookup"><span data-stu-id="dd3b3-108">Value</span></span> | <span data-ttu-id="dd3b3-109">描述</span><span class="sxs-lookup"><span data-stu-id="dd3b3-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="dd3b3-110">true</span><span class="sxs-lookup"><span data-stu-id="dd3b3-110">true</span></span>  | <span data-ttu-id="dd3b3-111">使用前景進度。</span><span class="sxs-lookup"><span data-stu-id="dd3b3-111">Use foreground progress.</span></span>                 |
| <span data-ttu-id="dd3b3-112">false</span><span class="sxs-lookup"><span data-stu-id="dd3b3-112">false</span></span> | <span data-ttu-id="dd3b3-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="dd3b3-113">Default.</span></span> <span data-ttu-id="dd3b3-114">請勿使用前景進度。</span><span class="sxs-lookup"><span data-stu-id="dd3b3-114">Do not use foreground progress.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="dd3b3-115">備註</span><span class="sxs-lookup"><span data-stu-id="dd3b3-115">Remarks</span></span>

<span data-ttu-id="dd3b3-116">這個屬性允許使用 **foregroundProgress** 屬性，此屬性主要用於追蹤媒體檔案的下載進度，同時使用 **value** 屬性來追蹤檔案目前的播放位置。</span><span class="sxs-lookup"><span data-stu-id="dd3b3-116">This attribute allows the use of the **foregroundProgress** attribute, which is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd3b3-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd3b3-117">Requirements</span></span>



| <span data-ttu-id="dd3b3-118">需求</span><span class="sxs-lookup"><span data-stu-id="dd3b3-118">Requirement</span></span> | <span data-ttu-id="dd3b3-119">值</span><span class="sxs-lookup"><span data-stu-id="dd3b3-119">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="dd3b3-120">版本</span><span class="sxs-lookup"><span data-stu-id="dd3b3-120">Version</span></span><br/> | <span data-ttu-id="dd3b3-121">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="dd3b3-121">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd3b3-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd3b3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd3b3-123">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="dd3b3-123">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="dd3b3-124">**滑杆. foregroundProgress**</span><span class="sxs-lookup"><span data-stu-id="dd3b3-124">**SLIDER.foregroundProgress**</span></span>](slider-foregroundprogress.md)
</dt> <dt>

[<span data-ttu-id="dd3b3-125">**滑杆。值**</span><span class="sxs-lookup"><span data-stu-id="dd3b3-125">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





