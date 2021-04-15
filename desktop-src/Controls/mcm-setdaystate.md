---
title: 'MCM_SETDAYSTATE 訊息 (Commctrl .h) '
description: 設定當月月曆控制項中目前可見的所有月份的日期狀態。 您可以使用 MonthCal SetDayState 宏明確地傳送此訊息 \_ 。
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- MCM_SETDAYSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466801"
---
# <a name="mcm_setdaystate-message"></a><span data-ttu-id="a76be-105">MCM \_ SETDAYSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="a76be-105">MCM\_SETDAYSTATE message</span></span>

<span data-ttu-id="a76be-106">設定當月月曆控制項中目前可見的所有月份的日期狀態。</span><span class="sxs-lookup"><span data-stu-id="a76be-106">Sets the day states for all months that are currently visible within a month calendar control.</span></span> <span data-ttu-id="a76be-107">您可以使用 [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a76be-107">You can send this message explicitly or by using the [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a76be-108">參數</span><span class="sxs-lookup"><span data-stu-id="a76be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a76be-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a76be-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a76be-110">值，指出 *lParam* 所指向陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="a76be-110">Value indicating how many elements are in the array that *lParam* points to.</span></span>

</dd> <dt>

<span data-ttu-id="a76be-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a76be-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a76be-112">[**MONTHDAYSTATE**](monthdaystate.md)值陣列的指標，定義月曆控制項在其顯示中每天的繪製方式。</span><span class="sxs-lookup"><span data-stu-id="a76be-112">Pointer to an array of [**MONTHDAYSTATE**](monthdaystate.md) values that define how the month calendar control will draw each day in its display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a76be-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a76be-113">Return value</span></span>

<span data-ttu-id="a76be-114">如果成功，則傳回非零，否則傳回零。</span><span class="sxs-lookup"><span data-stu-id="a76be-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a76be-115">備註</span><span class="sxs-lookup"><span data-stu-id="a76be-115">Remarks</span></span>

<span data-ttu-id="a76be-116">應用程式可以藉由傳送此訊息來明確設定日狀態資訊，但在行事曆的不同部分滾動查看時，狀態將不會保存。</span><span class="sxs-lookup"><span data-stu-id="a76be-116">An application can explicitly set day state information by sending this message, but the state will not persist when a different part of the calendar is scrolled into view.</span></span> <span data-ttu-id="a76be-117">日期狀態資訊通常是為了回應 [MCN \_ GETDAYSTATE](mcn-getdaystate.md) 通知碼而設定，每當控制項需要重新整理時，就會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="a76be-117">Day state information is usually set in response to the [MCN\_GETDAYSTATE](mcn-getdaystate.md) notification code, which is sent whenever the control needs to be refreshed.</span></span>

<span data-ttu-id="a76be-118">*LParam* 的陣列必須包含的元素數目，與下列宏所傳回的值相同：</span><span class="sxs-lookup"><span data-stu-id="a76be-118">The array at *lParam* must contain as many elements as the value returned by the following macro:</span></span>

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

<span data-ttu-id="a76be-119">請記住， *lParam* 中的陣列必須包含 [**MONTHDAYSTATE**](monthdaystate.md) 值，而這些值會對應到目前在控制項顯示中的所有月份（以時間順序排列）。</span><span class="sxs-lookup"><span data-stu-id="a76be-119">Keep in mind that the array at *lParam* must contain [**MONTHDAYSTATE**](monthdaystate.md) values that correspond with all months currently in the control's display, in chronological order.</span></span> <span data-ttu-id="a76be-120">這包括兩個月，可能會在第一個月之前和最後一個月之後部分顯示。</span><span class="sxs-lookup"><span data-stu-id="a76be-120">This includes the two months that may be partially displayed before the first month and after the last month.</span></span>

## <a name="requirements"></a><span data-ttu-id="a76be-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a76be-121">Requirements</span></span>



| <span data-ttu-id="a76be-122">需求</span><span class="sxs-lookup"><span data-stu-id="a76be-122">Requirement</span></span> | <span data-ttu-id="a76be-123">值</span><span class="sxs-lookup"><span data-stu-id="a76be-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a76be-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a76be-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a76be-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a76be-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a76be-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a76be-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a76be-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a76be-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a76be-128">標頭</span><span class="sxs-lookup"><span data-stu-id="a76be-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a76be-129"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a76be-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a76be-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a76be-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a76be-131">使用月曆控制項</span><span class="sxs-lookup"><span data-stu-id="a76be-131">Using Month Calendar Controls</span></span>](using-month-calendar-controls.md)
</dt> </dl>

 

 





