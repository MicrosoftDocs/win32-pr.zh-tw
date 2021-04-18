---
title: 'MCM_SETCURSEL 訊息 (Commctrl .h) '
description: 針對月曆控制項設定目前選取的日期。 如果指定的日期不在 view 中，控制項會更新顯示，使其變成可供觀看。 您可以使用 MonthCal SetCurSel 宏明確地傳送此訊息 \_ 。
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- MCM_SETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965115"
---
# <a name="mcm_setcursel-message"></a><span data-ttu-id="dc697-106">MCM \_ SETCURSEL 訊息</span><span class="sxs-lookup"><span data-stu-id="dc697-106">MCM\_SETCURSEL message</span></span>

<span data-ttu-id="dc697-107">針對月曆控制項設定目前選取的日期。</span><span class="sxs-lookup"><span data-stu-id="dc697-107">Sets the currently selected date for a month calendar control.</span></span> <span data-ttu-id="dc697-108">如果指定的日期不在 view 中，控制項會更新顯示，使其變成可供觀看。</span><span class="sxs-lookup"><span data-stu-id="dc697-108">If the specified date is not in view, the control updates the display to bring it into view.</span></span> <span data-ttu-id="dc697-109">您可以使用 [**MonthCal \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="dc697-109">You can send this message explicitly or by using the [**MonthCal\_SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc697-110">參數</span><span class="sxs-lookup"><span data-stu-id="dc697-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc697-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc697-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dc697-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="dc697-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="dc697-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc697-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc697-114">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的指標，其中包含要設定為目前選取範圍的日期。</span><span class="sxs-lookup"><span data-stu-id="dc697-114">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the current selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc697-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc697-115">Return value</span></span>

<span data-ttu-id="dc697-116">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="dc697-116">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="dc697-117">如果套用至使用 [**MCS \_ 多重選**](month-calendar-control-styles.md) 樣式的月曆控制項，此訊息將會失敗。</span><span class="sxs-lookup"><span data-stu-id="dc697-117">This message will fail if applied to a month calendar control that uses the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc697-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc697-118">Requirements</span></span>



| <span data-ttu-id="dc697-119">需求</span><span class="sxs-lookup"><span data-stu-id="dc697-119">Requirement</span></span> | <span data-ttu-id="dc697-120">值</span><span class="sxs-lookup"><span data-stu-id="dc697-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc697-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc697-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dc697-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc697-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc697-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc697-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dc697-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc697-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc697-125">標頭</span><span class="sxs-lookup"><span data-stu-id="dc697-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc697-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc697-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc697-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc697-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc697-128">月曆控制項中的時間</span><span class="sxs-lookup"><span data-stu-id="dc697-128">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

