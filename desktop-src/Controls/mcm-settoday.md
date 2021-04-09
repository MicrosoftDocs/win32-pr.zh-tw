---
title: 'MCM_SETTODAY 訊息 (Commctrl .h) '
description: 設定 \ 0034; today \ 0034;月曆控制項的選取專案。 您可以使用 MonthCal SetToday 宏明確地傳送此訊息 \_ 。
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- MCM_SETTODAY message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686584"
---
# <a name="mcm_settoday-message"></a><span data-ttu-id="14e5d-105">MCM \_ SETTODAY 訊息</span><span class="sxs-lookup"><span data-stu-id="14e5d-105">MCM\_SETTODAY message</span></span>

<span data-ttu-id="14e5d-106">設定月曆控制項的 "today" 選項。</span><span class="sxs-lookup"><span data-stu-id="14e5d-106">Sets the "today" selection for a month calendar control.</span></span> <span data-ttu-id="14e5d-107">您可以使用 [**MonthCal \_ SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="14e5d-107">You can send this message explicitly or by using the [**MonthCal\_SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="14e5d-108">參數</span><span class="sxs-lookup"><span data-stu-id="14e5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e5d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14e5d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="14e5d-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="14e5d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="14e5d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14e5d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14e5d-112">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的指標，其中包含要設定為控制項「今天」選取專案的日期。</span><span class="sxs-lookup"><span data-stu-id="14e5d-112">Pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure that contains the date to be set as the "today" selection for the control.</span></span> <span data-ttu-id="14e5d-113">如果這個參數設定為 **Null**，控制項會返回預設設定。</span><span class="sxs-lookup"><span data-stu-id="14e5d-113">If this parameter is set to **NULL**, the control returns to the default setting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e5d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="14e5d-114">Return value</span></span>

<span data-ttu-id="14e5d-115">未使用此訊息的傳回值。</span><span class="sxs-lookup"><span data-stu-id="14e5d-115">The return value for this message is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="14e5d-116">備註</span><span class="sxs-lookup"><span data-stu-id="14e5d-116">Remarks</span></span>

<span data-ttu-id="14e5d-117">如果 "today" 選項設定為預設值以外的任何日期，則適用下列條件：</span><span class="sxs-lookup"><span data-stu-id="14e5d-117">If the "today" selection is set to any date other than the default, the following conditions apply:</span></span>

-   <span data-ttu-id="14e5d-118">當時間通過當日的午夜時，此控制項將不會自動更新「今天」選取範圍。</span><span class="sxs-lookup"><span data-stu-id="14e5d-118">The control will not automatically update the "today" selection when the time passes midnight for the current day.</span></span>
-   <span data-ttu-id="14e5d-119">控制項不會根據地區設定變更自動更新其顯示。</span><span class="sxs-lookup"><span data-stu-id="14e5d-119">The control will not automatically update its display based on locale changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="14e5d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="14e5d-120">Requirements</span></span>



| <span data-ttu-id="14e5d-121">需求</span><span class="sxs-lookup"><span data-stu-id="14e5d-121">Requirement</span></span> | <span data-ttu-id="14e5d-122">值</span><span class="sxs-lookup"><span data-stu-id="14e5d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14e5d-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14e5d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="14e5d-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14e5d-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14e5d-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14e5d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="14e5d-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14e5d-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14e5d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="14e5d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="14e5d-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="14e5d-128"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14e5d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14e5d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e5d-130">月曆控制項中的時間</span><span class="sxs-lookup"><span data-stu-id="14e5d-130">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

