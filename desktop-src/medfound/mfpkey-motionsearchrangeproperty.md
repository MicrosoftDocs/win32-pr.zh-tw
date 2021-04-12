---
description: 指定用於移動搜尋的範圍。
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: 'MFPKEY_MOTIONSEARCHRANGE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192253"
---
# <a name="mfpkey_motionsearchrange-property"></a><span data-ttu-id="066b2-103">MFPKEY \_ MOTIONSEARCHRANGE 屬性</span><span class="sxs-lookup"><span data-stu-id="066b2-103">MFPKEY\_MOTIONSEARCHRANGE Property</span></span>

<span data-ttu-id="066b2-104">指定用於移動搜尋的範圍。</span><span class="sxs-lookup"><span data-stu-id="066b2-104">Specifies the range used in motion searches.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="066b2-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="066b2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="066b2-106">g \_ wszWMVCMotionSearchRange</span><span class="sxs-lookup"><span data-stu-id="066b2-106">g\_wszWMVCMotionSearchRange</span></span>

## <a name="data-type"></a><span data-ttu-id="066b2-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="066b2-107">Data Type</span></span>

<span data-ttu-id="066b2-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="066b2-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="066b2-109">預設值</span><span class="sxs-lookup"><span data-stu-id="066b2-109">Default Value</span></span>

<span data-ttu-id="066b2-110">0</span><span class="sxs-lookup"><span data-stu-id="066b2-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="066b2-111">備註</span><span class="sxs-lookup"><span data-stu-id="066b2-111">Remarks</span></span>

<span data-ttu-id="066b2-112">這個屬性可以設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="066b2-112">This property may be set to one of the following values.</span></span> <span data-ttu-id="066b2-113">H 表示水準範圍，V 表示垂直範圍。</span><span class="sxs-lookup"><span data-stu-id="066b2-113">H denotes horizontal range and V denotes vertical range.</span></span> <span data-ttu-id="066b2-114">所有範圍都會以圖元為單位。</span><span class="sxs-lookup"><span data-stu-id="066b2-114">All ranges are given in pixels.</span></span>



| <span data-ttu-id="066b2-115">值</span><span class="sxs-lookup"><span data-stu-id="066b2-115">Value</span></span> | <span data-ttu-id="066b2-116">範圍</span><span class="sxs-lookup"><span data-stu-id="066b2-116">Range</span></span>                                |
|-------|--------------------------------------|
| <span data-ttu-id="066b2-117">0</span><span class="sxs-lookup"><span data-stu-id="066b2-117">0</span></span>     | <span data-ttu-id="066b2-118">+ 63.75/-64.0 H、+ 31.75/-32.0 V</span><span class="sxs-lookup"><span data-stu-id="066b2-118">+63.75/-64.0 H, +31.75/-32.0 V</span></span>       |
| <span data-ttu-id="066b2-119">1</span><span class="sxs-lookup"><span data-stu-id="066b2-119">1</span></span>     | <span data-ttu-id="066b2-120">+127.75/-128.0 H, +63.75/-64.0 V</span><span class="sxs-lookup"><span data-stu-id="066b2-120">+127.75/-128.0 H, +63.75/-64.0 V</span></span>     |
| <span data-ttu-id="066b2-121">2</span><span class="sxs-lookup"><span data-stu-id="066b2-121">2</span></span>     | <span data-ttu-id="066b2-122">+ 511.75/-512.0 H、+ 127.75/-128.0 V</span><span class="sxs-lookup"><span data-stu-id="066b2-122">+511.75/-512.0 H, +127.75/-128.0 V</span></span>   |
| <span data-ttu-id="066b2-123">3</span><span class="sxs-lookup"><span data-stu-id="066b2-123">3</span></span>     | <span data-ttu-id="066b2-124">+ 1023.75/-1024.0 H、+ 255.75/-256.0 V</span><span class="sxs-lookup"><span data-stu-id="066b2-124">+1023.75/-1024.0 H, +255.75/-256.0 V</span></span> |
| <span data-ttu-id="066b2-125">-1</span><span class="sxs-lookup"><span data-stu-id="066b2-125">-1</span></span>    | <span data-ttu-id="066b2-126">巨大區塊-自動調整 (自動) </span><span class="sxs-lookup"><span data-stu-id="066b2-126">Macroblock-adaptive (automatic)</span></span>      |



 

<span data-ttu-id="066b2-127">這個屬性會控制編解碼器將搜尋可能在畫面格之間呈現動作之元素的框架區域大小。</span><span class="sxs-lookup"><span data-stu-id="066b2-127">This property controls the size of the frame area that the codec will search for an element that may have exhibited motion between frames.</span></span> <span data-ttu-id="066b2-128">較大的搜尋視窗將有助於找出更快速的動作，但需要較多的 CPU 時間。</span><span class="sxs-lookup"><span data-stu-id="066b2-128">A larger search window will help find faster motion but will require more CPU time.</span></span> <span data-ttu-id="066b2-129">CPU 需求大約是每個層級的兩倍。</span><span class="sxs-lookup"><span data-stu-id="066b2-129">The CPU requirements are approximately doubled at each level.</span></span>

<span data-ttu-id="066b2-130">自動模式 (-1) 會動態選取最有效率的模式。</span><span class="sxs-lookup"><span data-stu-id="066b2-130">The automatic mode (-1) will dynamically select the most efficient mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="066b2-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="066b2-131">Requirements</span></span>



| <span data-ttu-id="066b2-132">需求</span><span class="sxs-lookup"><span data-stu-id="066b2-132">Requirement</span></span> | <span data-ttu-id="066b2-133">值</span><span class="sxs-lookup"><span data-stu-id="066b2-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="066b2-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="066b2-134">Minimum supported client</span></span><br/> | <span data-ttu-id="066b2-135">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="066b2-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="066b2-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="066b2-136">Minimum supported server</span></span><br/> | <span data-ttu-id="066b2-137">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="066b2-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="066b2-138">標頭</span><span class="sxs-lookup"><span data-stu-id="066b2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="066b2-139"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="066b2-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="066b2-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="066b2-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="066b2-141">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="066b2-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




