---
title: '日期和時間選擇器控制項樣式 (CommCtrl .h) '
description: 此處所列的視窗樣式是日期和時間選擇器控制項特有的樣式。
ms.assetid: d3b95521-75ef-4cca-b801-94c6f749aa47
topic_type:
- apiref
api_name:
- DTS_APPCANPARSE
- DTS_LONGDATEFORMAT
- DTS_RIGHTALIGN
- DTS_SHOWNONE
- DTS_SHORTDATEFORMAT
- DTS_SHORTDATECENTURYFORMAT
- DTS_TIMEFORMAT
- DTS_UPDOWN
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d24e7543e4e843fc70e0ccacdab670e18e46cf3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989575"
---
# <a name="date-and-time-picker-control-styles"></a><span data-ttu-id="c4c4b-103">日期和時間選擇器控制項樣式</span><span class="sxs-lookup"><span data-stu-id="c4c4b-103">Date and Time Picker Control Styles</span></span>

<span data-ttu-id="c4c4b-104">此處所列的視窗樣式是日期和時間選擇器控制項特有的樣式。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-104">The window styles listed here are specific to date and time picker controls.</span></span>



| <span data-ttu-id="c4c4b-105">常數</span><span class="sxs-lookup"><span data-stu-id="c4c4b-105">Constant</span></span>                                                                                                                                                                                             | <span data-ttu-id="c4c4b-106">描述</span><span class="sxs-lookup"><span data-stu-id="c4c4b-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DTS_APPCANPARSE"></span><span id="dts_appcanparse"></span><dl> <span data-ttu-id="c4c4b-107"><dt>**DTS \_ APPCANPARSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c4b-107"><dt>**DTS\_APPCANPARSE**</dt></span></span> </dl>                                  | <span data-ttu-id="c4c4b-108">允許擁有者剖析使用者輸入並採取必要的動作。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-108">Allows the owner to parse user input and take necessary action.</span></span> <span data-ttu-id="c4c4b-109">當使用者按下 F2 鍵時，可讓使用者在控制項的工作區內進行編輯。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-109">It enables users to edit within the client area of the control when they press the F2 key.</span></span> <span data-ttu-id="c4c4b-110">當使用者完成時，控制項會傳送 [DTN \_ USERSTRING](dtn-userstring.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-110">The control sends [DTN\_USERSTRING](dtn-userstring.md) notification codes when users are finished.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <span id="DTS_LONGDATEFORMAT"></span><span id="dts_longdateformat"></span><dl> <span data-ttu-id="c4c4b-111"><dt>**DTS \_ LONGDATEFORMAT**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c4b-111"><dt>**DTS\_LONGDATEFORMAT**</dt></span></span> </dl>                         | <span data-ttu-id="c4c4b-112">以完整格式顯示日期。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-112">Displays the date in long format.</span></span> <span data-ttu-id="c4c4b-113">這種樣式的預設格式字串是由地區設定 \_ SLONGDATEFORMAT 所定義，它會產生像是「在1996年4月19日星期五」的輸出。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-113">The default format string for this style is defined by LOCALE\_SLONGDATEFORMAT, which produces output like "Friday, April 19, 1996".</span></span> <span data-ttu-id="c4c4b-114">使用此樣式時，下拉式按鈕不會顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-114">When this style is used, the dropdown button does not display an icon.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="DTS_RIGHTALIGN"></span><span id="dts_rightalign"></span><dl> <span data-ttu-id="c4c4b-115"><dt>**DTS \_ RIGHTALIGN**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c4b-115"><dt>**DTS\_RIGHTALIGN**</dt></span></span> </dl>                                     | <span data-ttu-id="c4c4b-116">下拉式月曆將會靠右對齊控制項，而不是靠左對齊（預設值）。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-116">The drop-down month calendar will be right-aligned with the control instead of left-aligned, which is the default.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHOWNONE"></span><span id="dts_shownone"></span><dl> <span data-ttu-id="c4c4b-117"><dt>**DTS \_ SHOWNONE**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c4b-117"><dt>**DTS\_SHOWNONE**</dt></span></span> </dl>                                           | <span data-ttu-id="c4c4b-118">目前無法在控制項中選取任何日期。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-118">It is possible to have no date currently selected in the control.</span></span> <span data-ttu-id="c4c4b-119">使用此樣式時，控制項會顯示每次挑選或輸入日期時都會自動選取的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-119">With this style, the control displays a check box that is automatically selected whenever a date is picked or entered.</span></span> <span data-ttu-id="c4c4b-120">如果後續核取方塊已取消選取，應用程式就無法從控制項取出日期，因為基本上，控制項沒有日期。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-120">If the check box is subsequently deselected, the application cannot retrieve the date from the control because, in essence, the control has no date.</span></span> <span data-ttu-id="c4c4b-121">您可以使用 [**dtm \_ SETSYSTEMTIME**](dtm-setsystemtime.md) 訊息來設定核取方塊的狀態，或使用 [**dtm \_ GETSYSTEMTIME**](dtm-getsystemtime.md) 訊息來進行查詢。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-121">The state of the check box can be set with the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message or queried with the [**DTM\_GETSYSTEMTIME**](dtm-getsystemtime.md) message.</span></span><br/> |
| <span id="DTS_SHORTDATEFORMAT"></span><span id="dts_shortdateformat"></span><dl> <span data-ttu-id="c4c4b-122"><dt>**DTS \_ SHORTDATEFORMAT**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c4b-122"><dt>**DTS\_SHORTDATEFORMAT**</dt></span></span> </dl>                      | <span data-ttu-id="c4c4b-123">以簡短格式顯示日期。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-123">Displays the date in short format.</span></span> <span data-ttu-id="c4c4b-124">此樣式的預設格式字串是由地區設定 SSHORTDATE 所定義 \_ ，它會產生 "4/19/96" 之類的輸出。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-124">The default format string for this style is defined by LOCALE\_SSHORTDATE, which produces output like "4/19/96".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHORTDATECENTURYFORMAT"></span><span id="dts_shortdatecenturyformat"></span><dl> <span data-ttu-id="c4c4b-125"><dt>**DTS \_ SHORTDATECENTURYFORMAT**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c4b-125"><dt>**DTS\_SHORTDATECENTURYFORMAT**</dt></span></span> </dl> | <span data-ttu-id="c4c4b-126">**版本5.80。**</span><span class="sxs-lookup"><span data-stu-id="c4c4b-126">**Version 5.80.**</span></span> <span data-ttu-id="c4c4b-127">類似于 **DTS \_ SHORTDATEFORMAT** 樣式，不同之處在于年份是四位數的欄位。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-127">Similar to the **DTS\_SHORTDATEFORMAT** style, except the year is a four-digit field.</span></span> <span data-ttu-id="c4c4b-128">此樣式的預設格式字串是根據地區設定 \_ SSHORTDATE。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-128">The default format string for this style is based on LOCALE\_SSHORTDATE.</span></span> <span data-ttu-id="c4c4b-129">輸出如下所示： "4/19/1996"。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-129">The output looks like: "4/19/1996".</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DTS_TIMEFORMAT"></span><span id="dts_timeformat"></span><dl> <span data-ttu-id="c4c4b-130"><dt>**DTS \_ 時間格式**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c4b-130"><dt>**DTS\_TIMEFORMAT**</dt></span></span> </dl>                                     | <span data-ttu-id="c4c4b-131">顯示時間。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-131">Displays the time.</span></span> <span data-ttu-id="c4c4b-132">此樣式的預設格式字串是由地區設定 STIMEFORMAT 所定義 \_ ，它會產生像是 "5:31:42 PM" 的輸出。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-132">The default format string for this style is defined by LOCALE\_STIMEFORMAT, which produces output like "5:31:42 PM".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="DTS_UPDOWN"></span><span id="dts_updown"></span><dl> <span data-ttu-id="c4c4b-133"><dt>**DTS \_ 上下按鈕**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c4b-133"><dt>**DTS\_UPDOWN**</dt></span></span> </dl>                                                 | <span data-ttu-id="c4c4b-134">將上下按鈕控制項放在 DTP 控制項的右邊，以修改日期時間值。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-134">Places an up-down control to the right of the DTP control to modify date-time values.</span></span> <span data-ttu-id="c4c4b-135">這個樣式可以用來取代以預設樣式表示的下拉式月曆。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-135">This style can be used in place of the drop-down month calendar, which is the default style.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="c4c4b-136">備註</span><span class="sxs-lookup"><span data-stu-id="c4c4b-136">Remarks</span></span>

<span data-ttu-id="c4c4b-137">\_無法合併定義顯示格式的 DTS XXXFORMAT 樣式。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-137">The DTS\_XXXFORMAT styles that define the display format cannot be combined.</span></span> <span data-ttu-id="c4c4b-138">如果沒有適用的格式樣式，請使用 [**DTM \_ SETFORMAT**](dtm-setformat.md) 訊息來定義自訂格式。</span><span class="sxs-lookup"><span data-stu-id="c4c4b-138">If none of the format styles are suitable, use a [**DTM\_SETFORMAT**](dtm-setformat.md) message to define a custom format.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c4b-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4c4b-139">Requirements</span></span>



| <span data-ttu-id="c4c4b-140">需求</span><span class="sxs-lookup"><span data-stu-id="c4c4b-140">Requirement</span></span> | <span data-ttu-id="c4c4b-141">值</span><span class="sxs-lookup"><span data-stu-id="c4c4b-141">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c4b-142">標頭</span><span class="sxs-lookup"><span data-stu-id="c4c4b-142">Header</span></span><br/> | <dl> <span data-ttu-id="c4c4b-143"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4c4b-143"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





