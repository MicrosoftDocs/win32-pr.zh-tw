---
title: 'MCM_GETCOLOR 訊息 (Commctrl .h) '
description: 抓取月曆控制項指定部分的色彩。 您可以使用 MonthCal GetColor 宏明確地傳送此訊息 \_ 。
ms.assetid: 6c30ad0d-7584-402a-9c27-3c12c49c87f3
keywords:
- MCM_GETCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 932b457bd1ddd870fd84facdb540e31188825504
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105456"
---
# <a name="mcm_getcolor-message"></a><span data-ttu-id="be45a-105">MCM \_ GETCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="be45a-105">MCM\_GETCOLOR message</span></span>

<span data-ttu-id="be45a-106">抓取月曆控制項指定部分的色彩。</span><span class="sxs-lookup"><span data-stu-id="be45a-106">Retrieves the color for a given portion of a month calendar control.</span></span> <span data-ttu-id="be45a-107">您可以使用 [**MonthCal \_ GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="be45a-107">You can send this message explicitly or by using the [**MonthCal\_GetColor**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="be45a-108">參數</span><span class="sxs-lookup"><span data-stu-id="be45a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be45a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be45a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be45a-110">**Int** 類型的值，指定要取出的月曆色彩。</span><span class="sxs-lookup"><span data-stu-id="be45a-110">Value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="be45a-111">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="be45a-111">This value can be one of the following:</span></span>



| <span data-ttu-id="be45a-112">值</span><span class="sxs-lookup"><span data-stu-id="be45a-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="be45a-113">意義</span><span class="sxs-lookup"><span data-stu-id="be45a-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="be45a-114"><dt>**MCSC \_ 背景**</dt></span><span class="sxs-lookup"><span data-stu-id="be45a-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="be45a-115">取得顯示在月份之間的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="be45a-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="be45a-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="be45a-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="be45a-117">取得在月份內顯示的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="be45a-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="be45a-118"><dt>**MCSC \_ 文字**</dt></span><span class="sxs-lookup"><span data-stu-id="be45a-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="be45a-119">取得用來在一個月內顯示文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="be45a-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="be45a-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="be45a-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="be45a-121">取出日曆標題中顯示的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="be45a-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="be45a-122"><dt>**MCSC \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="be45a-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="be45a-123">抓取用來顯示行事曆標題內文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="be45a-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="be45a-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="be45a-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="be45a-125">抓取用來顯示頁首日和尾端日文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="be45a-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="be45a-126">[頁首] 和 [結束日期] 是出現在當月日曆上的上個月和之後幾天。</span><span class="sxs-lookup"><span data-stu-id="be45a-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="be45a-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be45a-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="be45a-128">必須為零。</span><span class="sxs-lookup"><span data-stu-id="be45a-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be45a-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="be45a-129">Return value</span></span>

<span data-ttu-id="be45a-130">如果成功，則傳回代表月曆控制項指定部分之色彩設定的 **COLORREF** 值。</span><span class="sxs-lookup"><span data-stu-id="be45a-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="be45a-131">否則，此訊息會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="be45a-131">Otherwise, this message returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="be45a-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="be45a-132">Requirements</span></span>



| <span data-ttu-id="be45a-133">需求</span><span class="sxs-lookup"><span data-stu-id="be45a-133">Requirement</span></span> | <span data-ttu-id="be45a-134">值</span><span class="sxs-lookup"><span data-stu-id="be45a-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be45a-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be45a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="be45a-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be45a-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be45a-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be45a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="be45a-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be45a-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be45a-139">標頭</span><span class="sxs-lookup"><span data-stu-id="be45a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="be45a-140"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="be45a-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





