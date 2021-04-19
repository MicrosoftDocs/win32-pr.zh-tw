---
title: 'MCM_GETMONTHRANGE 訊息 (Commctrl .h) '
description: 使用代表月曆控制項顯示之最高和最低限制的 SYSTEMTIME 結構) ，抓取日期資訊 (。 您可以使用 MonthCal GetMonthRange 宏明確地傳送此訊息 \_ 。
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- MCM_GETMONTHRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965125"
---
# <a name="mcm_getmonthrange-message"></a><span data-ttu-id="3491a-105">MCM \_ GETMONTHRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="3491a-105">MCM\_GETMONTHRANGE message</span></span>

<span data-ttu-id="3491a-106">使用代表月曆控制項顯示之最高和最低限制的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構) ，抓取日期資訊 (。</span><span class="sxs-lookup"><span data-stu-id="3491a-106">Retrieves date information (using [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures) that represents the high and low limits of a month calendar control's display.</span></span> <span data-ttu-id="3491a-107">您可以使用 [**MonthCal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3491a-107">You can send this message explicitly or by using the [**MonthCal\_GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3491a-108">參數</span><span class="sxs-lookup"><span data-stu-id="3491a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3491a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3491a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3491a-110">值，指定要抓取範圍限制的範圍。</span><span class="sxs-lookup"><span data-stu-id="3491a-110">Value specifying the scope of the range limits to be retrieved.</span></span> <span data-ttu-id="3491a-111">此值必須是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="3491a-111">This value must be one of the following:</span></span>



| <span data-ttu-id="3491a-112">值</span><span class="sxs-lookup"><span data-stu-id="3491a-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="3491a-113">意義</span><span class="sxs-lookup"><span data-stu-id="3491a-113">Meaning</span></span>                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <span data-ttu-id="3491a-114"><dt>**GMR \_ DAYSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="3491a-114"><dt>**GMR\_DAYSTATE**</dt></span></span> </dl> | <span data-ttu-id="3491a-115">包含只部分顯示之可見範圍的前置和尾端月份。</span><span class="sxs-lookup"><span data-stu-id="3491a-115">Include preceding and trailing months of visible range that are only partially displayed.</span></span> <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <span data-ttu-id="3491a-116"><dt>**GMR \_ 可見**</dt></span><span class="sxs-lookup"><span data-stu-id="3491a-116"><dt>**GMR\_VISIBLE**</dt></span></span> </dl>    | <span data-ttu-id="3491a-117">只包含完全顯示的月份。</span><span class="sxs-lookup"><span data-stu-id="3491a-117">Include only those months that are entirely displayed.</span></span> <br/>                                    |



 

</dd> <dt>

<span data-ttu-id="3491a-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3491a-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3491a-119">[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標，會接收 *wParam* 所指定之範圍的下限和上限。</span><span class="sxs-lookup"><span data-stu-id="3491a-119">Pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures that will receive the lower and upper limits of the scope specified by *wParam*.</span></span> <span data-ttu-id="3491a-120">下限和上限分別放在 *lprgSysTimeArray* \[ 0 \] 和 *lprgSysTimeArray* \[ 1 中 \] 。</span><span class="sxs-lookup"><span data-stu-id="3491a-120">The lower and upper limits are placed in *lprgSysTimeArray*\[0\] and *lprgSysTimeArray*\[1\], respectively.</span></span> <span data-ttu-id="3491a-121">此參數必須是有效的位址，而且不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3491a-121">This parameter must be a valid address and cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3491a-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="3491a-122">Return value</span></span>

<span data-ttu-id="3491a-123">傳回 INT 值，代表 *lParam* 所傳回的兩項限制的範圍（以月為單位）。</span><span class="sxs-lookup"><span data-stu-id="3491a-123">Returns an INT value that represents the range, in months, spanned by the two limits returned at *lParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3491a-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3491a-124">Requirements</span></span>



| <span data-ttu-id="3491a-125">需求</span><span class="sxs-lookup"><span data-stu-id="3491a-125">Requirement</span></span> | <span data-ttu-id="3491a-126">值</span><span class="sxs-lookup"><span data-stu-id="3491a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3491a-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3491a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3491a-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3491a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3491a-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3491a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3491a-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3491a-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3491a-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3491a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3491a-132"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3491a-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3491a-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3491a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3491a-134">月曆控制項中的時間</span><span class="sxs-lookup"><span data-stu-id="3491a-134">Times in the Month Calendar Control</span></span>](month-calendar-controls.md)
</dt> </dl>

 

