---
title: 'DTM_GETMCCOLOR 訊息 (Commctrl .h) '
description: 取得日期和時間選擇器中的月曆指定部分的色彩， (DTP) 控制項。 您可以明確地傳送此訊息，或使用 DateTime \_ GetMonthCalColor 宏。
ms.assetid: 892e8c23-f0d0-4fd6-98ed-39592c4d316f
keywords:
- DTM_GETMCCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETMCCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690c461c5bccbd050fb3d698d1a41c6d1e513944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467126"
---
# <a name="dtm_getmccolor-message"></a><span data-ttu-id="a88bf-105">DTM \_ GETMCCOLOR 訊息</span><span class="sxs-lookup"><span data-stu-id="a88bf-105">DTM\_GETMCCOLOR message</span></span>

<span data-ttu-id="a88bf-106">取得日期和時間選擇器中的月曆指定部分的色彩， (DTP) 控制項。</span><span class="sxs-lookup"><span data-stu-id="a88bf-106">Gets the color for a given portion of the month calendar within a date and time picker (DTP) control.</span></span> <span data-ttu-id="a88bf-107">您可以明確地傳送此訊息，或使用 [**DateTime \_ GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) 宏。</span><span class="sxs-lookup"><span data-stu-id="a88bf-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalColor**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a88bf-108">參數</span><span class="sxs-lookup"><span data-stu-id="a88bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a88bf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a88bf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a88bf-110">**Int** 類型的值，指定要取出的月曆色彩。</span><span class="sxs-lookup"><span data-stu-id="a88bf-110">A value of type **int** specifying which month calendar color to retrieve.</span></span> <span data-ttu-id="a88bf-111">這個值可以是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="a88bf-111">This value can be one of the following:</span></span>



| <span data-ttu-id="a88bf-112">值</span><span class="sxs-lookup"><span data-stu-id="a88bf-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="a88bf-113">意義</span><span class="sxs-lookup"><span data-stu-id="a88bf-113">Meaning</span></span>                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCSC_BACKGROUND"></span><span id="mcsc_background"></span><dl> <span data-ttu-id="a88bf-114"><dt>**MCSC \_ 背景**</dt></span><span class="sxs-lookup"><span data-stu-id="a88bf-114"><dt>**MCSC\_BACKGROUND**</dt></span></span> </dl>       | <span data-ttu-id="a88bf-115">取得顯示在月份之間的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="a88bf-115">Retrieve the background color displayed between months.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_MONTHBK"></span><span id="mcsc_monthbk"></span><dl> <span data-ttu-id="a88bf-116"><dt>**MCSC \_ MONTHBK**</dt></span><span class="sxs-lookup"><span data-stu-id="a88bf-116"><dt>**MCSC\_MONTHBK**</dt></span></span> </dl>                | <span data-ttu-id="a88bf-117">取得在月份內顯示的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="a88bf-117">Retrieve the background color displayed within the month.</span></span><br/>                                                                                                                                    |
| <span id="MCSC_TEXT"></span><span id="mcsc_text"></span><dl> <span data-ttu-id="a88bf-118"><dt>**MCSC \_ 文字**</dt></span><span class="sxs-lookup"><span data-stu-id="a88bf-118"><dt>**MCSC\_TEXT**</dt></span></span> </dl>                         | <span data-ttu-id="a88bf-119">取得用來在一個月內顯示文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="a88bf-119">Retrieve the color used to display text within a month.</span></span><br/>                                                                                                                                      |
| <span id="MCSC_TITLEBK"></span><span id="mcsc_titlebk"></span><dl> <span data-ttu-id="a88bf-120"><dt>**MCSC \_ TITLEBK**</dt></span><span class="sxs-lookup"><span data-stu-id="a88bf-120"><dt>**MCSC\_TITLEBK**</dt></span></span> </dl>                | <span data-ttu-id="a88bf-121">取出日曆標題中顯示的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="a88bf-121">Retrieve the background color displayed in the calendar's title.</span></span><br/>                                                                                                                             |
| <span id="MCSC_TITLETEXT"></span><span id="mcsc_titletext"></span><dl> <span data-ttu-id="a88bf-122"><dt>**MCSC \_ TITLETEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="a88bf-122"><dt>**MCSC\_TITLETEXT**</dt></span></span> </dl>          | <span data-ttu-id="a88bf-123">抓取用來顯示行事曆標題內文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="a88bf-123">Retrieve the color used to display text within the calendar's title.</span></span><br/>                                                                                                                         |
| <span id="MCSC_TRAILINGTEXT"></span><span id="mcsc_trailingtext"></span><dl> <span data-ttu-id="a88bf-124"><dt>**MCSC \_ TRAILINGTEXT**</dt></span><span class="sxs-lookup"><span data-stu-id="a88bf-124"><dt>**MCSC\_TRAILINGTEXT**</dt></span></span> </dl> | <span data-ttu-id="a88bf-125">抓取用來顯示頁首日和尾端日文字的色彩。</span><span class="sxs-lookup"><span data-stu-id="a88bf-125">Retrieve the color used to display header day and trailing day text.</span></span> <span data-ttu-id="a88bf-126">[頁首] 和 [結束日期] 是出現在當月日曆上的上個月和之後幾天。</span><span class="sxs-lookup"><span data-stu-id="a88bf-126">Header and trailing days are the days from the previous and following months that appear on the current month calendar.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a88bf-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a88bf-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a88bf-128">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a88bf-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a88bf-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="a88bf-129">Return value</span></span>

<span data-ttu-id="a88bf-130">如果成功，則傳回代表月曆控制項指定部分之色彩設定的 **COLORREF** 值。</span><span class="sxs-lookup"><span data-stu-id="a88bf-130">Returns a **COLORREF** value that represents the color setting for the specified portion of the month calendar control if successful.</span></span> <span data-ttu-id="a88bf-131">如果失敗，訊息會傳回-1。</span><span class="sxs-lookup"><span data-stu-id="a88bf-131">The message returns -1 if unsuccessful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a88bf-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="a88bf-132">Requirements</span></span>



| <span data-ttu-id="a88bf-133">需求</span><span class="sxs-lookup"><span data-stu-id="a88bf-133">Requirement</span></span> | <span data-ttu-id="a88bf-134">值</span><span class="sxs-lookup"><span data-stu-id="a88bf-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a88bf-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a88bf-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a88bf-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a88bf-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a88bf-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a88bf-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a88bf-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a88bf-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a88bf-139">標頭</span><span class="sxs-lookup"><span data-stu-id="a88bf-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a88bf-140"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a88bf-140"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





