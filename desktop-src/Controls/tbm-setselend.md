---
title: 'TBM_SETSELEND 訊息 (Commctrl .h) '
description: 在 [選取區] 中設定目前選取範圍的結束邏輯位置。 如果 [ENABLESELRANGE] 沒有 [TB] 樣式，則會忽略此訊息 \_ 。
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- TBM_SETSELEND message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146446df4daf8e8ac7c0f3499149ba0f46940880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093811"
---
# <a name="tbm_setselend-message"></a><span data-ttu-id="12f57-105">TBM \_ SETSELEND 訊息</span><span class="sxs-lookup"><span data-stu-id="12f57-105">TBM\_SETSELEND message</span></span>

<span data-ttu-id="12f57-106">在 [選取區] 中設定目前選取範圍的結束邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="12f57-106">Sets the ending logical position of the current selection range in a trackbar.</span></span> <span data-ttu-id="12f57-107">如果 [ENABLESELRANGE] 沒有 [ [**tb] \_**](trackbar-control-styles.md) 樣式，則會忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="12f57-107">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="12f57-108">參數</span><span class="sxs-lookup"><span data-stu-id="12f57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12f57-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12f57-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12f57-110">重繪旗標。</span><span class="sxs-lookup"><span data-stu-id="12f57-110">Redraw flag.</span></span> <span data-ttu-id="12f57-111">如果此參數為 **TRUE**，則訊息會在設定選取範圍之後，重新繪製資訊區。</span><span class="sxs-lookup"><span data-stu-id="12f57-111">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="12f57-112">如果此參數為 **FALSE**，則訊息會設定選取範圍，但不會重繪這些選取範圍。</span><span class="sxs-lookup"><span data-stu-id="12f57-112">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="12f57-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12f57-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12f57-114">結束選取範圍的邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="12f57-114">Ending logical position of the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12f57-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="12f57-115">Return value</span></span>

<span data-ttu-id="12f57-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="12f57-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f57-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="12f57-117">Requirements</span></span>



| <span data-ttu-id="12f57-118">需求</span><span class="sxs-lookup"><span data-stu-id="12f57-118">Requirement</span></span> | <span data-ttu-id="12f57-119">值</span><span class="sxs-lookup"><span data-stu-id="12f57-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12f57-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12f57-120">Minimum supported client</span></span><br/> | <span data-ttu-id="12f57-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12f57-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12f57-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12f57-122">Minimum supported server</span></span><br/> | <span data-ttu-id="12f57-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12f57-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12f57-124">標頭</span><span class="sxs-lookup"><span data-stu-id="12f57-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="12f57-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="12f57-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12f57-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12f57-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="12f57-127">**參考**</span><span class="sxs-lookup"><span data-stu-id="12f57-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="12f57-128">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="12f57-128">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="12f57-129">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="12f57-129">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="12f57-130">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="12f57-130">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="12f57-131">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="12f57-131">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





