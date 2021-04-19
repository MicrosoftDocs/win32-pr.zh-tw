---
title: 'MCM_SETRANGE 訊息 (Commctrl .h) '
description: 設定月曆控制項的最小和最大允許日期。 您可以使用 MonthCal SetRange 宏明確地傳送此訊息 \_ 。
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- MCM_SETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380e599da8cd4a054c02135bc64f57f29d2c81d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966336"
---
# <a name="mcm_setrange-message"></a><span data-ttu-id="4cb7e-105">MCM \_ SETRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="4cb7e-105">MCM\_SETRANGE message</span></span>

<span data-ttu-id="4cb7e-106">設定月曆控制項的最小和最大允許日期。</span><span class="sxs-lookup"><span data-stu-id="4cb7e-106">Sets the minimum and maximum allowable dates for a month calendar control.</span></span> <span data-ttu-id="4cb7e-107">您可以使用 [**MonthCal \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="4cb7e-107">You can send this message explicitly or by using the [**MonthCal\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4cb7e-108">參數</span><span class="sxs-lookup"><span data-stu-id="4cb7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cb7e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4cb7e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cb7e-110">旗標值，指定要設定的日期限制。</span><span class="sxs-lookup"><span data-stu-id="4cb7e-110">Flag values that specify which date limits are being set.</span></span> <span data-ttu-id="4cb7e-111">此值必須是下列其中一項或兩項：</span><span class="sxs-lookup"><span data-stu-id="4cb7e-111">This value must be one or both of the following:</span></span>



| <span data-ttu-id="4cb7e-112">值</span><span class="sxs-lookup"><span data-stu-id="4cb7e-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="4cb7e-113">意義</span><span class="sxs-lookup"><span data-stu-id="4cb7e-113">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="4cb7e-114"><dt>**GDTR \_ MAX**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb7e-114"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="4cb7e-115">已設定允許的最大日期。</span><span class="sxs-lookup"><span data-stu-id="4cb7e-115">The maximum allowable date is being set.</span></span> <span data-ttu-id="4cb7e-116">*LpSysTimeArray* 1 的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構 \[ \] 必須包含日期資訊。</span><span class="sxs-lookup"><span data-stu-id="4cb7e-116">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[1\] must contain date information.</span></span> <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="4cb7e-117"><dt>**GDTR \_ 分鐘**</dt></span><span class="sxs-lookup"><span data-stu-id="4cb7e-117"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="4cb7e-118">已設定允許的最小日期。</span><span class="sxs-lookup"><span data-stu-id="4cb7e-118">The minimum allowable date is being set.</span></span> <span data-ttu-id="4cb7e-119">位於 *lpSysTimeArray* 0 的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構 \[ \] 必須包含日期資訊。</span><span class="sxs-lookup"><span data-stu-id="4cb7e-119">The [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure at *lpSysTimeArray*\[0\] must contain date information.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="4cb7e-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4cb7e-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4cb7e-121">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的雙元素陣列的指標，其中包含日期限制。</span><span class="sxs-lookup"><span data-stu-id="4cb7e-121">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that contain the date limits.</span></span> <span data-ttu-id="4cb7e-122"> \[ 如果指定了 GDTR MAX，則上限必須在 lpSysTimeArray 1 中 \] \_ ，  \[ \] 如果指定了 GDTR MIN，則 lpSysTimeArray 0 必須包含最小限制 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4cb7e-122">The maximum limit must be in *lpSysTimeArray*\[1\] if GDTR\_MAX is specified, and *lpSysTimeArray*\[0\] must contain the minimum limit if GDTR\_MIN is specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cb7e-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="4cb7e-123">Return value</span></span>

<span data-ttu-id="4cb7e-124">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="4cb7e-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cb7e-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cb7e-125">Requirements</span></span>



| <span data-ttu-id="4cb7e-126">需求</span><span class="sxs-lookup"><span data-stu-id="4cb7e-126">Requirement</span></span> | <span data-ttu-id="4cb7e-127">值</span><span class="sxs-lookup"><span data-stu-id="4cb7e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb7e-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4cb7e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb7e-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cb7e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cb7e-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4cb7e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb7e-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4cb7e-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4cb7e-132">標頭</span><span class="sxs-lookup"><span data-stu-id="4cb7e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cb7e-133"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4cb7e-133"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cb7e-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cb7e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb7e-135">月曆控制項中的時間</span><span class="sxs-lookup"><span data-stu-id="4cb7e-135">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

