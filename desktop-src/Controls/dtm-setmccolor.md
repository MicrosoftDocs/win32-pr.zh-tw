---
title: 'DTM_SETMCCOLOR 訊息 (Commctrl .h) '
description: 在日期和時間選擇器中，設定日曆指定部分的色彩， (DTP) 控制項。 您可以明確地傳送此訊息，或使用 DateTime \_ SetMonthCalColor 宏。
ms.assetid: cee72c1d-58da-4ee5-850e-a615ec6ad079
keywords:
- DTM_SETMCCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e496abb4dd28b040dd4a8035073ffa32a3f3847
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686173"
---
# <a name="dtm_setmccolor-message"></a><span data-ttu-id="1a7e0-105">DTM \_ SETMCCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="1a7e0-105">DTM\_SETMCCOLOR message</span></span>

<span data-ttu-id="1a7e0-106">在日期和時間選擇器中，設定日曆指定部分的色彩， (DTP) 控制項。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-106">Sets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="1a7e0-107">您可以明確地傳送此訊息，或使用 [**DateTime \_ SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) 宏。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a7e0-108">參數</span><span class="sxs-lookup"><span data-stu-id="1a7e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a7e0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a7e0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a7e0-110">**Int** 類型的值，指定要設定的月曆色彩。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-110">A value of type **int** specifying which month calendar color to set.</span></span> <span data-ttu-id="1a7e0-111">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="1a7e0-111">This value can be one of the following:</span></span>



| <span data-ttu-id="1a7e0-112">值</span><span class="sxs-lookup"><span data-stu-id="1a7e0-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="1a7e0-113">意義</span><span class="sxs-lookup"><span data-stu-id="1a7e0-113">Meaning</span></span>                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="1a7e0-114"><dt>**MCSC \_ 背景**</dt></span><span class="sxs-lookup"><span data-stu-id="1a7e0-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="1a7e0-115">設定在月份之間顯示的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-115">Set the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="1a7e0-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="1a7e0-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="1a7e0-117">設定在月份內顯示的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-117">Set the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="1a7e0-118"><dt>**MCSC \_ 文字**</dt></span><span class="sxs-lookup"><span data-stu-id="1a7e0-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="1a7e0-119">設定用來顯示一個月內文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-119">Set the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="1a7e0-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="1a7e0-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="1a7e0-121">設定日曆標題中顯示的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-121">Set the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="1a7e0-122"><dt>**MCSC \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="1a7e0-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="1a7e0-123">設定用來顯示行事曆標題內文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-123">Set the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="1a7e0-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="1a7e0-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="1a7e0-125">設定用來顯示頁首日和尾端日文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-125">Set the color used to display header day and trailing day text.</span></span> <span data-ttu-id="1a7e0-126">[頁首] 和 [結束日期] 是出現在當月日曆上的上個月和之後幾天。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1a7e0-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a7e0-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a7e0-128">**COLORREF** 值，表示將針對月曆的指定區域設定的色彩。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-128">A **COLORREF** value representing the color that will be set for the specified area of the month calendar.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a7e0-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a7e0-129">Return value</span></span>

<span data-ttu-id="1a7e0-130">傳回 **COLORREF** 值，表示如果成功，則表示月曆控制項指定部分的先前色彩設定。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-130">Returns a **COLORREF** value that represents the previous color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="1a7e0-131">否則，訊息會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-131">Otherwise, the message returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a7e0-132">備註</span><span class="sxs-lookup"><span data-stu-id="1a7e0-132">Remarks</span></span>

<span data-ttu-id="1a7e0-133">啟用視覺化樣式時，除了 *wParam* 為 MCSC 背景時，此訊息不會有任何作用 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1a7e0-133">When visual styles are enabled, this message has no effect except when *wParam* is MCSC\_BACKGROUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a7e0-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a7e0-134">Requirements</span></span>



| <span data-ttu-id="1a7e0-135">需求</span><span class="sxs-lookup"><span data-stu-id="1a7e0-135">Requirement</span></span> | <span data-ttu-id="1a7e0-136">值</span><span class="sxs-lookup"><span data-stu-id="1a7e0-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a7e0-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1a7e0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1a7e0-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a7e0-138">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a7e0-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1a7e0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1a7e0-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1a7e0-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a7e0-141">標頭</span><span class="sxs-lookup"><span data-stu-id="1a7e0-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a7e0-142"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a7e0-142"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





