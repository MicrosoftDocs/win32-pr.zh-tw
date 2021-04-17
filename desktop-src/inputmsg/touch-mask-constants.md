---
title: 觸控遮罩
description: 可以出現在 POINTER_TOUCH_INFO 結構的 touchMask 欄位中的值。
ms.assetid: 23AD50C8-C769-48D6-9F27-DB2755C03D5C
topic_type:
- apiref
api_name:
- TOUCH_MASK_NONE
- TOUCH_MASK_CONTACTAREA
- TOUCH_MASK_ORIENTATION
- TOUCH_MASK_PRESSURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5ac389894d9096b389af127685feb9a2d81756ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466665"
---
# <a name="touch-mask"></a><span data-ttu-id="10f33-103">觸控遮罩</span><span class="sxs-lookup"><span data-stu-id="10f33-103">Touch Mask</span></span>

<span data-ttu-id="10f33-104">可以出現在 [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)結構的 **touchMask** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="10f33-104">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="10f33-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="10f33-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f33-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="10f33-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="10f33-107">預設值。</span><span class="sxs-lookup"><span data-stu-id="10f33-107">Default.</span></span> <span data-ttu-id="10f33-108">沒有任何選用欄位都有效。</span><span class="sxs-lookup"><span data-stu-id="10f33-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="10f33-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span><span class="sxs-lookup"><span data-stu-id="10f33-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f33-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="10f33-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="10f33-111">[**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)結構的 **rcContact** 是有效的。</span><span class="sxs-lookup"><span data-stu-id="10f33-111">**rcContact** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="10f33-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span><span class="sxs-lookup"><span data-stu-id="10f33-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f33-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="10f33-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="10f33-114">[**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)結構的 **方向** 是有效的。</span><span class="sxs-lookup"><span data-stu-id="10f33-114">**orientation** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="10f33-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="10f33-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f33-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="10f33-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="10f33-117">[**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api)結構的 **壓力** 是有效的。</span><span class="sxs-lookup"><span data-stu-id="10f33-117">**pressure** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10f33-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="10f33-118">Requirements</span></span>



| <span data-ttu-id="10f33-119">需求</span><span class="sxs-lookup"><span data-stu-id="10f33-119">Requirement</span></span> | <span data-ttu-id="10f33-120">值</span><span class="sxs-lookup"><span data-stu-id="10f33-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10f33-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10f33-121">Minimum supported client</span></span><br/> | <span data-ttu-id="10f33-122">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10f33-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="10f33-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10f33-123">Minimum supported server</span></span><br/> | <span data-ttu-id="10f33-124">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10f33-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="10f33-125">標頭</span><span class="sxs-lookup"><span data-stu-id="10f33-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="10f33-126"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="10f33-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10f33-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10f33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f33-128">常數</span><span class="sxs-lookup"><span data-stu-id="10f33-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="10f33-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="10f33-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





