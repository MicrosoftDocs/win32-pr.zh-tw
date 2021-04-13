---
title: 畫筆旗標
description: 可以出現在 POINTER_PEN_INFO 結構的 penFlags 欄位中的值。
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: d7c28beaf58b6fa96bb8dd82b2dd650b2a7d6950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466129"
---
# <a name="pen-flags"></a><span data-ttu-id="7d13c-103">畫筆旗標</span><span class="sxs-lookup"><span data-stu-id="7d13c-103">Pen Flags</span></span>

<span data-ttu-id="7d13c-104">可以出現在 [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api)結構的 **penFlags** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="7d13c-104">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="7d13c-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="7d13c-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d13c-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7d13c-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="7d13c-107">沒有畫筆旗標。</span><span class="sxs-lookup"><span data-stu-id="7d13c-107">There is no pen flag.</span></span> <span data-ttu-id="7d13c-108">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="7d13c-108">This is the default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d13c-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span><span class="sxs-lookup"><span data-stu-id="7d13c-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d13c-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7d13c-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="7d13c-111">已按下 [圓筒] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="7d13c-111">The barrel button is pressed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d13c-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span><span class="sxs-lookup"><span data-stu-id="7d13c-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d13c-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7d13c-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="7d13c-114">畫筆已反轉。</span><span class="sxs-lookup"><span data-stu-id="7d13c-114">The pen is inverted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="7d13c-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span><span class="sxs-lookup"><span data-stu-id="7d13c-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d13c-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="7d13c-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="7d13c-117">已按下橡皮擦按鈕。</span><span class="sxs-lookup"><span data-stu-id="7d13c-117">The eraser button is pressed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d13c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d13c-118">Requirements</span></span>



| <span data-ttu-id="7d13c-119">需求</span><span class="sxs-lookup"><span data-stu-id="7d13c-119">Requirement</span></span> | <span data-ttu-id="7d13c-120">值</span><span class="sxs-lookup"><span data-stu-id="7d13c-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7d13c-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d13c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7d13c-122">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d13c-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7d13c-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d13c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7d13c-124">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d13c-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7d13c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7d13c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d13c-126"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="7d13c-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d13c-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d13c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d13c-128">常數</span><span class="sxs-lookup"><span data-stu-id="7d13c-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="7d13c-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="7d13c-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





