---
title: 'TBM_SETRANGEMIN 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的最小邏輯位置。
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- TBM_SETRANGEMIN message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933909"
---
# <a name="tbm_setrangemin-message"></a><span data-ttu-id="454c9-104">TBM \_ SETRANGEMIN 訊息</span><span class="sxs-lookup"><span data-stu-id="454c9-104">TBM\_SETRANGEMIN message</span></span>

<span data-ttu-id="454c9-105">設定捲軸中滑杆的最小邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="454c9-105">Sets the minimum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="454c9-106">參數</span><span class="sxs-lookup"><span data-stu-id="454c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="454c9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="454c9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="454c9-108">重繪旗標。</span><span class="sxs-lookup"><span data-stu-id="454c9-108">Redraw flag.</span></span> <span data-ttu-id="454c9-109">如果此參數為 **TRUE**，則訊息會在設定範圍之後重新繪製資訊區。</span><span class="sxs-lookup"><span data-stu-id="454c9-109">If this parameter is **TRUE**, the message redraws the trackbar after the range is set.</span></span> <span data-ttu-id="454c9-110">如果此參數為 **FALSE**，則訊息會設定範圍，但不會重新繪製這些。</span><span class="sxs-lookup"><span data-stu-id="454c9-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="454c9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="454c9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="454c9-112">滑杆的最小位置。</span><span class="sxs-lookup"><span data-stu-id="454c9-112">Minimum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="454c9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="454c9-113">Return value</span></span>

<span data-ttu-id="454c9-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="454c9-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="454c9-115">備註</span><span class="sxs-lookup"><span data-stu-id="454c9-115">Remarks</span></span>

<span data-ttu-id="454c9-116">如果目前滑杆的位置小於新的最小值， **TBM \_ SETRANGEMIN** 訊息會將滑杆位置設定為新的最小值。</span><span class="sxs-lookup"><span data-stu-id="454c9-116">If the current slider position is less than the new minimum, the **TBM\_SETRANGEMIN** message sets the slider position to the new minimum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="454c9-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="454c9-117">Requirements</span></span>



| <span data-ttu-id="454c9-118">需求</span><span class="sxs-lookup"><span data-stu-id="454c9-118">Requirement</span></span> | <span data-ttu-id="454c9-119">值</span><span class="sxs-lookup"><span data-stu-id="454c9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="454c9-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="454c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="454c9-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="454c9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="454c9-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="454c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="454c9-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="454c9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="454c9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="454c9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="454c9-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="454c9-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="454c9-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="454c9-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="454c9-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="454c9-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="454c9-128">**TBM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="454c9-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="454c9-129">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="454c9-129">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





