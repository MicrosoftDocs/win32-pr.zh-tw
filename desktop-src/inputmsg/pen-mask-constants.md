---
title: 畫筆遮罩
description: 可以出現在 POINTER_PEN_INFO 結構的 penMask 欄位中的值。
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bd181b5eafbe1cf6de56c95886deb04e5bd6d2b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104562"
---
# <a name="pen-mask"></a><span data-ttu-id="81d42-103">畫筆遮罩</span><span class="sxs-lookup"><span data-stu-id="81d42-103">Pen Mask</span></span>

<span data-ttu-id="81d42-104">可以出現在 [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)結構的 **penMask** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="81d42-104">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="81d42-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="81d42-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d42-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="81d42-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="81d42-107">預設值。</span><span class="sxs-lookup"><span data-stu-id="81d42-107">Default.</span></span> <span data-ttu-id="81d42-108">沒有任何選用欄位都有效。</span><span class="sxs-lookup"><span data-stu-id="81d42-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d42-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="81d42-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d42-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="81d42-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="81d42-111">[**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)結構的 **壓力** 是有效的。</span><span class="sxs-lookup"><span data-stu-id="81d42-111">**pressure** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d42-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span><span class="sxs-lookup"><span data-stu-id="81d42-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d42-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="81d42-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="81d42-114">[**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)結構的 **旋轉** 有效。</span><span class="sxs-lookup"><span data-stu-id="81d42-114">**rotation** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d42-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span><span class="sxs-lookup"><span data-stu-id="81d42-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d42-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="81d42-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="81d42-117">[**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)結構的 **tiltX** 是有效的。</span><span class="sxs-lookup"><span data-stu-id="81d42-117">**tiltX** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="81d42-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span><span class="sxs-lookup"><span data-stu-id="81d42-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81d42-119">0x00000008</span><span class="sxs-lookup"><span data-stu-id="81d42-119">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="81d42-120">[**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)結構的 **tiltY** 是有效的。</span><span class="sxs-lookup"><span data-stu-id="81d42-120">**tiltY** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81d42-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="81d42-121">Requirements</span></span>



| <span data-ttu-id="81d42-122">需求</span><span class="sxs-lookup"><span data-stu-id="81d42-122">Requirement</span></span> | <span data-ttu-id="81d42-123">值</span><span class="sxs-lookup"><span data-stu-id="81d42-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="81d42-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="81d42-124">Minimum supported client</span></span><br/> | <span data-ttu-id="81d42-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81d42-125">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="81d42-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="81d42-126">Minimum supported server</span></span><br/> | <span data-ttu-id="81d42-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="81d42-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="81d42-128">標頭</span><span class="sxs-lookup"><span data-stu-id="81d42-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="81d42-129"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="81d42-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81d42-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81d42-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d42-131">常數</span><span class="sxs-lookup"><span data-stu-id="81d42-131">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="81d42-132">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="81d42-132">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





