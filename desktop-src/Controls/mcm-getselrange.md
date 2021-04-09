---
title: 'MCM_GETSELRANGE 訊息 (Commctrl .h) '
description: 抓取代表使用者目前所選取日期範圍上限和下限的日期資訊。 您可以使用 MonthCal GetSelRange 宏明確地傳送此訊息 \_ 。
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- MCM_GETSELRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934199"
---
# <a name="mcm_getselrange-message"></a><span data-ttu-id="2fff1-105">MCM \_ GETSELRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="2fff1-105">MCM\_GETSELRANGE message</span></span>

<span data-ttu-id="2fff1-106">抓取代表使用者目前所選取日期範圍上限和下限的日期資訊。</span><span class="sxs-lookup"><span data-stu-id="2fff1-106">Retrieves date information that represents the upper and lower limits of the date range currently selected by the user.</span></span> <span data-ttu-id="2fff1-107">您可以使用 [**MonthCal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2fff1-107">You can send this message explicitly or by using the [**MonthCal\_GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2fff1-108">參數</span><span class="sxs-lookup"><span data-stu-id="2fff1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fff1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2fff1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2fff1-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="2fff1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2fff1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2fff1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2fff1-112">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標，會接收使用者選取範圍的下限和上限。</span><span class="sxs-lookup"><span data-stu-id="2fff1-112">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the user's selection.</span></span> <span data-ttu-id="2fff1-113">下限和上限分別放在 *lprgSysTimeArray* \[ 0 \] 和 *lprgSysTimeArray* \[ 1 中 \] 。</span><span class="sxs-lookup"><span data-stu-id="2fff1-113">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="2fff1-114">此參數必須是有效的位址，而且不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2fff1-114">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fff1-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2fff1-115">Return value</span></span>

<span data-ttu-id="2fff1-116">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="2fff1-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="2fff1-117">**MCM \_** 如果套用至不使用 [**MCS \_ 多重選**](month-calendar-control-styles.md)樣式的月曆控制項，GETSELRANGE 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="2fff1-117">**MCM\_GETSELRANGE** will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fff1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fff1-118">Requirements</span></span>



| <span data-ttu-id="2fff1-119">需求</span><span class="sxs-lookup"><span data-stu-id="2fff1-119">Requirement</span></span> | <span data-ttu-id="2fff1-120">值</span><span class="sxs-lookup"><span data-stu-id="2fff1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fff1-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2fff1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2fff1-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fff1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2fff1-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2fff1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2fff1-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2fff1-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2fff1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="2fff1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fff1-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2fff1-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fff1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fff1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fff1-128">月曆控制項中的時間</span><span class="sxs-lookup"><span data-stu-id="2fff1-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

