---
title: 'TCM_SETITEMSIZE 訊息 (Commctrl .h) '
description: 在固定寬度或主控描繪的索引標籤控制項中，設定索引標籤的寬度和高度。 您可以使用 TabCtrl SetItemSize 宏明確地傳送此訊息 \_ 。
ms.assetid: 3935d686-f8bc-41fb-b025-04120cf03f02
keywords:
- TCM_SETITEMSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETITEMSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e306af3f6462507a181de91104169c5ac7d6ce14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843048"
---
# <a name="tcm_setitemsize-message"></a><span data-ttu-id="62521-105">TCM \_ SETITEMSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="62521-105">TCM\_SETITEMSIZE message</span></span>

<span data-ttu-id="62521-106">在固定寬度或主控描繪的索引標籤控制項中，設定索引標籤的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="62521-106">Sets the width and height of tabs in a fixed-width or owner-drawn tab control.</span></span> <span data-ttu-id="62521-107">您可以使用 [**TabCtrl \_ SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="62521-107">You can send this message explicitly or by using the [**TabCtrl\_SetItemSize**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setitemsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="62521-108">參數</span><span class="sxs-lookup"><span data-stu-id="62521-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62521-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62521-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="62521-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="62521-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="62521-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62521-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62521-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是指定新寬度的 **INT** 值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="62521-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is an **INT** value that specifies the new width, in pixels.</span></span> <span data-ttu-id="62521-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是指定新高度的 **INT** 值（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="62521-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is an **INT** value that specifies the new height, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62521-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="62521-114">Return value</span></span>

<span data-ttu-id="62521-115">傳回舊的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="62521-115">Returns the old width and height.</span></span> <span data-ttu-id="62521-116">寬度是在傳回值的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中，而高度則在 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中。</span><span class="sxs-lookup"><span data-stu-id="62521-116">The width is in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the return value, and the height is in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="remarks"></a><span data-ttu-id="62521-117">備註</span><span class="sxs-lookup"><span data-stu-id="62521-117">Remarks</span></span>

<span data-ttu-id="62521-118">如果寬度設定為小於 [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)所設定的影像寬度，則索引標籤的寬度會設定為大於影像寬度的最小值。</span><span class="sxs-lookup"><span data-stu-id="62521-118">If the width is set to a value less than the image width set by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), the width of the tab is set to the lowest value that is greater than the image width.</span></span>

## <a name="requirements"></a><span data-ttu-id="62521-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="62521-119">Requirements</span></span>



| <span data-ttu-id="62521-120">需求</span><span class="sxs-lookup"><span data-stu-id="62521-120">Requirement</span></span> | <span data-ttu-id="62521-121">值</span><span class="sxs-lookup"><span data-stu-id="62521-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="62521-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62521-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62521-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62521-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="62521-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62521-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62521-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62521-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="62521-126">標頭</span><span class="sxs-lookup"><span data-stu-id="62521-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="62521-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="62521-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

