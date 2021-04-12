---
title: 'TBM_SETRANGEMAX 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的最大邏輯位置。
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- TBM_SETRANGEMAX message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464253"
---
# <a name="tbm_setrangemax-message"></a><span data-ttu-id="1629d-104">TBM \_ SETRANGEMAX 訊息</span><span class="sxs-lookup"><span data-stu-id="1629d-104">TBM\_SETRANGEMAX message</span></span>

<span data-ttu-id="1629d-105">設定捲軸中滑杆的最大邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="1629d-105">Sets the maximum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="1629d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1629d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1629d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1629d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1629d-108">重繪旗標。</span><span class="sxs-lookup"><span data-stu-id="1629d-108">Redraw flag.</span></span> <span data-ttu-id="1629d-109">如果此參數為 **TRUE**，則會在設定範圍之後重新繪製這些程式。</span><span class="sxs-lookup"><span data-stu-id="1629d-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="1629d-110">如果此參數為 **FALSE**，則訊息會設定範圍，但不會重新繪製這些。</span><span class="sxs-lookup"><span data-stu-id="1629d-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="1629d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1629d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1629d-112">滑杆的最大位置。</span><span class="sxs-lookup"><span data-stu-id="1629d-112">Maximum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1629d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="1629d-113">Return value</span></span>

<span data-ttu-id="1629d-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="1629d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1629d-115">備註</span><span class="sxs-lookup"><span data-stu-id="1629d-115">Remarks</span></span>

<span data-ttu-id="1629d-116">如果目前滑杆的位置大於新的最大值， **TBM \_ SETRANGEMAX** 訊息會將滑杆位置設定為新的最大值。</span><span class="sxs-lookup"><span data-stu-id="1629d-116">If the current slider position is greater than the new maximum, the **TBM\_SETRANGEMAX** message sets the slider position to the new maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1629d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1629d-117">Requirements</span></span>



| <span data-ttu-id="1629d-118">需求</span><span class="sxs-lookup"><span data-stu-id="1629d-118">Requirement</span></span> | <span data-ttu-id="1629d-119">值</span><span class="sxs-lookup"><span data-stu-id="1629d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1629d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1629d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1629d-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1629d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1629d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1629d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1629d-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1629d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1629d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1629d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1629d-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1629d-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1629d-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1629d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="1629d-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="1629d-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1629d-128">**TBM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="1629d-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="1629d-129">**TBM \_ SETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="1629d-129">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

 





