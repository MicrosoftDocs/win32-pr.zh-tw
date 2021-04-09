---
title: 'LVM_APPROXIMATEVIEWRECT 訊息 (Commctrl .h) '
description: 計算顯示指定專案數目所需的大約寬度和高度。 您可以明確地傳送此訊息，或使用 ListView \_ ApproximateViewRect 宏。
ms.assetid: a14331a8-217d-48c6-9489-fb90c4d31b91
keywords:
- LVM_APPROXIMATEVIEWRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_APPROXIMATEVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be929d34acad46b75a53a9e0cc8825ec9801e998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933927"
---
# <a name="lvm_approximateviewrect-message"></a><span data-ttu-id="355d2-105">LVM \_ APPROXIMATEVIEWRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="355d2-105">LVM\_APPROXIMATEVIEWRECT message</span></span>

<span data-ttu-id="355d2-106">計算顯示指定專案數目所需的大約寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="355d2-106">Calculates the approximate width and height required to display a given number of items.</span></span> <span data-ttu-id="355d2-107">您可以明確地傳送此訊息，或使用 [**ListView \_ ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) 宏。</span><span class="sxs-lookup"><span data-stu-id="355d2-107">You can send this message explicitly or use the [**ListView\_ApproximateViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_approximateviewrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="355d2-108">參數</span><span class="sxs-lookup"><span data-stu-id="355d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="355d2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="355d2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="355d2-110">要在控制項中顯示的專案數目。</span><span class="sxs-lookup"><span data-stu-id="355d2-110">The number of items to be displayed in the control.</span></span> <span data-ttu-id="355d2-111">如果此參數設定為-1，則訊息會使用控制項中的總專案數。</span><span class="sxs-lookup"><span data-stu-id="355d2-111">If this parameter is set to -1, the message uses the total number of items in the control.</span></span>

</dd> <dt>

<span data-ttu-id="355d2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="355d2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="355d2-113">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是控制項的建議 x 維度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="355d2-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the proposed x-dimension of the control, in pixels.</span></span> <span data-ttu-id="355d2-114">這個參數可以設定為-1，以允許訊息使用目前的寬度值。</span><span class="sxs-lookup"><span data-stu-id="355d2-114">This parameter can be set to -1 to allow the message to use the current width value.</span></span>

<span data-ttu-id="355d2-115">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是控制項的建議 y 維度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="355d2-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the proposed y-dimension of the control, in pixels.</span></span> <span data-ttu-id="355d2-116">這個參數可以設定為-1，以允許訊息使用目前的高度值。</span><span class="sxs-lookup"><span data-stu-id="355d2-116">This parameter can be set to -1 to allow the message to use the current height value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="355d2-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="355d2-117">Return value</span></span>

<span data-ttu-id="355d2-118">傳回 **DWORD** 值，此值會將大約寬度 (保存在 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) 所需的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) 和高度 (（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="355d2-118">Returns a **DWORD** value that holds the approximate width (in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))) and height (in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))) needed to display the items, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="355d2-119">備註</span><span class="sxs-lookup"><span data-stu-id="355d2-119">Remarks</span></span>

<span data-ttu-id="355d2-120">根據此訊息所提供的維度來設定清單視圖控制項的大小，可以優化重繪並減少閃爍。</span><span class="sxs-lookup"><span data-stu-id="355d2-120">Setting the size of the list-view control based on the dimensions provided by this message can optimize redraw and reduce flicker.</span></span>

## <a name="requirements"></a><span data-ttu-id="355d2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="355d2-121">Requirements</span></span>



| <span data-ttu-id="355d2-122">需求</span><span class="sxs-lookup"><span data-stu-id="355d2-122">Requirement</span></span> | <span data-ttu-id="355d2-123">值</span><span class="sxs-lookup"><span data-stu-id="355d2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="355d2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="355d2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="355d2-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="355d2-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="355d2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="355d2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="355d2-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="355d2-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="355d2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="355d2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="355d2-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="355d2-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

