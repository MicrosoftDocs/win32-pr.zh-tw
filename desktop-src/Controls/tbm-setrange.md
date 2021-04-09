---
title: 'TBM_SETRANGE 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的最小和最大邏輯位置的範圍。
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- TBM_SETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024847"
---
# <a name="tbm_setrange-message"></a><span data-ttu-id="076b2-104">TBM \_ SETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="076b2-104">TBM\_SETRANGE message</span></span>

<span data-ttu-id="076b2-105">設定捲軸中滑杆的最小和最大邏輯位置的範圍。</span><span class="sxs-lookup"><span data-stu-id="076b2-105">Sets the range of minimum and maximum logical positions for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="076b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="076b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="076b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="076b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="076b2-108">重繪旗標。</span><span class="sxs-lookup"><span data-stu-id="076b2-108">Redraw flag.</span></span> <span data-ttu-id="076b2-109">如果此參數為 **TRUE**，則會在設定範圍之後重新繪製這些程式。</span><span class="sxs-lookup"><span data-stu-id="076b2-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="076b2-110">如果此參數為 **FALSE**，則訊息會設定範圍，但不會重新繪製這些。</span><span class="sxs-lookup"><span data-stu-id="076b2-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="076b2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="076b2-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="076b2-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定滑杆的最小位置，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定最大位置。</span><span class="sxs-lookup"><span data-stu-id="076b2-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum position for the slider, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="076b2-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="076b2-113">Return value</span></span>

<span data-ttu-id="076b2-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="076b2-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="076b2-115">備註</span><span class="sxs-lookup"><span data-stu-id="076b2-115">Remarks</span></span>

<span data-ttu-id="076b2-116">如果目前滑杆的位置超出新的範圍， **TBM \_ SETRANGE** 訊息會將滑杆位置設定為新的最大值或最小值。</span><span class="sxs-lookup"><span data-stu-id="076b2-116">If the current slider position is outside the new range, the **TBM\_SETRANGE** message sets the slider position to the new maximum or minimum value.</span></span>

<span data-ttu-id="076b2-117">因為此訊息採用 2 16 位不帶正負號的整數值，此訊息可以指定的最大範圍是從0到65535。</span><span class="sxs-lookup"><span data-stu-id="076b2-117">Because this message takes two 16-bit unsigned integer values, the maximum range that this message can specify is from 0 to 65,535.</span></span> <span data-ttu-id="076b2-118">若要指定較大的範圍值，請使用 [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md) 和 [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="076b2-118">To specify larger range values, use the [**TBM\_SETRANGEMIN**](tbm-setrangemin.md) and [**TBM\_SETRANGEMAX**](tbm-setrangemax.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="076b2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="076b2-119">Requirements</span></span>



| <span data-ttu-id="076b2-120">需求</span><span class="sxs-lookup"><span data-stu-id="076b2-120">Requirement</span></span> | <span data-ttu-id="076b2-121">值</span><span class="sxs-lookup"><span data-stu-id="076b2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="076b2-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="076b2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="076b2-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="076b2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="076b2-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="076b2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="076b2-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="076b2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="076b2-126">標頭</span><span class="sxs-lookup"><span data-stu-id="076b2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="076b2-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="076b2-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="076b2-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="076b2-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="076b2-129">**參考**</span><span class="sxs-lookup"><span data-stu-id="076b2-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="076b2-130">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="076b2-130">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> <dt>

[<span data-ttu-id="076b2-131">**TBM \_ SETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="076b2-131">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

