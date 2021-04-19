---
title: '月曆控制項樣式 (CommCtrl .h) '
description: 當建立月曆控制項時，會使用下列樣式常數。
ms.assetid: 8d9b2239-fd13-4579-81a2-0385fd318e83
topic_type:
- apiref
api_name:
- MCS_DAYSTATE
- MCS_MULTISELECT
- MCS_WEEKNUMBERS
- MCS_NOTODAYCIRCLE
- MCS_NOTODAY
- MCS_NOTRAILINGDATES
- MCS_SHORTDAYSOFWEEK
- MCS_NOSELCHANGEONNAV
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45ccef4a3cc8e16851c0676b8b0dce8c53cfdd27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982584"
---
# <a name="month-calendar-control-styles"></a><span data-ttu-id="e1205-103">月曆控制項樣式</span><span class="sxs-lookup"><span data-stu-id="e1205-103">Month Calendar Control Styles</span></span>

<span data-ttu-id="e1205-104">當建立月曆控制項時，會使用下列樣式常數。</span><span class="sxs-lookup"><span data-stu-id="e1205-104">The following style constants are used when creating month calendar controls.</span></span>



| <span data-ttu-id="e1205-105">常數</span><span class="sxs-lookup"><span data-stu-id="e1205-105">Constant</span></span>                                                                                                                                                                           | <span data-ttu-id="e1205-106">描述</span><span class="sxs-lookup"><span data-stu-id="e1205-106">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <span data-ttu-id="e1205-107"><dt>**MCS \_ DAYSTATE**</dt></span><span class="sxs-lookup"><span data-stu-id="e1205-107"><dt>**MCS\_DAYSTATE**</dt></span></span> </dl>                         | <span data-ttu-id="e1205-108">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="e1205-108">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="e1205-109">月曆會傳送 [MCN \_ GETDAYSTATE](mcn-getdaystate.md) 通知，要求應以粗體顯示哪些天的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e1205-109">The month calendar sends [MCN\_GETDAYSTATE](mcn-getdaystate.md) notifications to request information about which days should be displayed in bold.</span></span><br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <span data-ttu-id="e1205-110"><dt>**MCS \_ 多重複選**</dt></span><span class="sxs-lookup"><span data-stu-id="e1205-110"><dt>**MCS\_MULTISELECT**</dt></span></span> </dl>                | <span data-ttu-id="e1205-111">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="e1205-111">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="e1205-112">月曆可讓使用者選取控制項內的日期範圍。</span><span class="sxs-lookup"><span data-stu-id="e1205-112">The month calendar enables the user to select a range of dates within the control.</span></span> <span data-ttu-id="e1205-113">根據預設，最大範圍是一周。</span><span class="sxs-lookup"><span data-stu-id="e1205-113">By default, the maximum range is one week.</span></span> <span data-ttu-id="e1205-114">您可以使用 [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) 訊息來變更可選取的最大範圍。</span><span class="sxs-lookup"><span data-stu-id="e1205-114">You can change the maximum range that can be selected by using the [**MCM\_SETMAXSELCOUNT**](mcm-setmaxselcount.md) message.</span></span> <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <span data-ttu-id="e1205-115"><dt>**MCS \_ WEEKNUMBERS**</dt></span><span class="sxs-lookup"><span data-stu-id="e1205-115"><dt>**MCS\_WEEKNUMBERS**</dt></span></span> </dl>                | <span data-ttu-id="e1205-116">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="e1205-116">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="e1205-117">月曆控制項會在每個資料列的左邊顯示 (1-52) 的周數。</span><span class="sxs-lookup"><span data-stu-id="e1205-117">The month calendar control displays week numbers (1-52) to the left of each row of days.</span></span> <span data-ttu-id="e1205-118">第1周定義為至少包含四天的第一周。</span><span class="sxs-lookup"><span data-stu-id="e1205-118">Week 1 is defined as the first week that contains at least four days.</span></span> <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <span data-ttu-id="e1205-119"><dt>**MCS \_ NOTODAYCIRCLE**</dt></span><span class="sxs-lookup"><span data-stu-id="e1205-119"><dt>**MCS\_NOTODAYCIRCLE**</dt></span></span> </dl>          | <span data-ttu-id="e1205-120">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="e1205-120">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="e1205-121">月曆控制項不會圈出「今天」的日期。</span><span class="sxs-lookup"><span data-stu-id="e1205-121">The month calendar control does not circle the "today" date.</span></span> <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <span data-ttu-id="e1205-122"><dt>**MCS \_ NOTODAY**</dt></span><span class="sxs-lookup"><span data-stu-id="e1205-122"><dt>**MCS\_NOTODAY**</dt></span></span> </dl>                            | <span data-ttu-id="e1205-123">[版本 4.70](common-control-versions.md)。月曆控制項不會在控制項底部顯示「今天」的日期。</span><span class="sxs-lookup"><span data-stu-id="e1205-123">[Version 4.70](common-control-versions.md).The month calendar control does not display the "today" date at the bottom of the control.</span></span> <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <span data-ttu-id="e1205-124"><dt>**MCS \_ NOTRAILINGDATES**</dt></span><span class="sxs-lookup"><span data-stu-id="e1205-124"><dt>**MCS\_NOTRAILINGDATES**</dt></span></span> </dl>    | <span data-ttu-id="e1205-125">**Windows Vista。**</span><span class="sxs-lookup"><span data-stu-id="e1205-125">**Windows Vista.**</span></span> <span data-ttu-id="e1205-126">上個月和下個月的日期，不會顯示在當月的日曆中。</span><span class="sxs-lookup"><span data-stu-id="e1205-126">Dates from the previous and next months are not displayed in the current month's calendar.</span></span><br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <span data-ttu-id="e1205-127"><dt>**MCS \_ SHORTDAYSOFWEEK**</dt></span><span class="sxs-lookup"><span data-stu-id="e1205-127"><dt>**MCS\_SHORTDAYSOFWEEK**</dt></span></span> </dl>    | <span data-ttu-id="e1205-128">**Windows Vista。**</span><span class="sxs-lookup"><span data-stu-id="e1205-128">**Windows Vista.**</span></span> <span data-ttu-id="e1205-129">簡短的日期名稱會顯示在標頭中。</span><span class="sxs-lookup"><span data-stu-id="e1205-129">Short day names are displayed in the header.</span></span><br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <span data-ttu-id="e1205-130"><dt>**MCS \_ NOSELCHANGEONNAV**</dt></span><span class="sxs-lookup"><span data-stu-id="e1205-130"><dt>**MCS\_NOSELCHANGEONNAV**</dt></span></span> </dl> | <span data-ttu-id="e1205-131">**Windows Vista。**</span><span class="sxs-lookup"><span data-stu-id="e1205-131">**Windows Vista.**</span></span> <span data-ttu-id="e1205-132">當使用者流覽日曆中的下一個或上一個時，不會變更選取專案。</span><span class="sxs-lookup"><span data-stu-id="e1205-132">The selection is not changed when the user navigates next or previous in the calendar.</span></span> <span data-ttu-id="e1205-133">這可讓使用者選取 [大於] 可見的範圍。</span><span class="sxs-lookup"><span data-stu-id="e1205-133">This allows the user to select a range larger than is visible.</span></span><br/>                                                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="e1205-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1205-134">Requirements</span></span>



| <span data-ttu-id="e1205-135">需求</span><span class="sxs-lookup"><span data-stu-id="e1205-135">Requirement</span></span> | <span data-ttu-id="e1205-136">值</span><span class="sxs-lookup"><span data-stu-id="e1205-136">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1205-137">標頭</span><span class="sxs-lookup"><span data-stu-id="e1205-137">Header</span></span><br/> | <dl> <span data-ttu-id="e1205-138"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1205-138"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





