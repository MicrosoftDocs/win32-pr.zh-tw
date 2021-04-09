---
title: 'TBM_SETSEL 訊息 (Commctrl .h) '
description: 設定在 [選取區] 中可用選取範圍的開始和結束位置。
ms.assetid: 71f5b9f8-4850-44a8-8acf-adca9bda84c3
keywords:
- TBM_SETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edebc6b6dcf3b0b93e3047a39aac74c34d121bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685508"
---
# <a name="tbm_setsel-message"></a><span data-ttu-id="7e49d-104">TBM \_ SETSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="7e49d-104">TBM\_SETSEL message</span></span>

<span data-ttu-id="7e49d-105">設定在 [選取區] 中可用選取範圍的開始和結束位置。</span><span class="sxs-lookup"><span data-stu-id="7e49d-105">Sets the starting and ending positions for the available selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e49d-106">參數</span><span class="sxs-lookup"><span data-stu-id="7e49d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e49d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e49d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e49d-108">重繪旗標。</span><span class="sxs-lookup"><span data-stu-id="7e49d-108">Redraw flag.</span></span> <span data-ttu-id="7e49d-109">如果此參數為 **TRUE**，則訊息會在設定選取範圍之後，重新繪製資訊區。</span><span class="sxs-lookup"><span data-stu-id="7e49d-109">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="7e49d-110">如果此參數為 **FALSE**，則訊息會設定選取範圍，但不會重繪這些選取範圍。</span><span class="sxs-lookup"><span data-stu-id="7e49d-110">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="7e49d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e49d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e49d-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定選取範圍的開始邏輯位置，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定結束的邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="7e49d-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the starting logical position for the selection range, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the ending logical position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e49d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e49d-113">Return value</span></span>

<span data-ttu-id="7e49d-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="7e49d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e49d-115">備註</span><span class="sxs-lookup"><span data-stu-id="7e49d-115">Remarks</span></span>

<span data-ttu-id="7e49d-116">如果 [ENABLESELRANGE] 沒有 [ [**tb] \_**](trackbar-control-styles.md) 樣式，則會忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="7e49d-116">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

<span data-ttu-id="7e49d-117">**TBM \_SETSEL** 可讓您將指標限制為僅可供進度列使用的部分範圍。</span><span class="sxs-lookup"><span data-stu-id="7e49d-117">**TBM\_SETSEL** allows you to restrict the pointer to only a portion of the range available to the progress bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e49d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e49d-118">Requirements</span></span>



| <span data-ttu-id="7e49d-119">需求</span><span class="sxs-lookup"><span data-stu-id="7e49d-119">Requirement</span></span> | <span data-ttu-id="7e49d-120">值</span><span class="sxs-lookup"><span data-stu-id="7e49d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e49d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e49d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7e49d-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e49d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e49d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e49d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7e49d-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e49d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e49d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="7e49d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e49d-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e49d-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e49d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e49d-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e49d-128">**參考**</span><span class="sxs-lookup"><span data-stu-id="7e49d-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7e49d-129">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="7e49d-129">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="7e49d-130">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="7e49d-130">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="7e49d-131">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="7e49d-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="7e49d-132">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="7e49d-132">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

