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
# <a name="month-calendar-control-styles"></a>月曆控制項樣式

當建立月曆控制項時，會使用下列樣式常數。



| 常數                                                                                                                                                                           | 描述                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_DAYSTATE"></span><span id="mcs_daystate"></span><dl> <dt>**MCS \_ DAYSTATE**</dt> </dl>                         | [版本 4.70](common-control-versions.md)。 月曆會傳送 [MCN \_ GETDAYSTATE](mcn-getdaystate.md) 通知，要求應以粗體顯示哪些天的相關資訊。<br/>                                                                                                          |
| <span id="MCS_MULTISELECT"></span><span id="mcs_multiselect"></span><dl> <dt>**MCS \_ 多重複選**</dt> </dl>                | [版本 4.70](common-control-versions.md)。 月曆可讓使用者選取控制項內的日期範圍。 根據預設，最大範圍是一周。 您可以使用 [**MCM \_ SETMAXSELCOUNT**](mcm-setmaxselcount.md) 訊息來變更可選取的最大範圍。 <br/> |
| <span id="MCS_WEEKNUMBERS"></span><span id="mcs_weeknumbers"></span><dl> <dt>**MCS \_ WEEKNUMBERS**</dt> </dl>                | [版本 4.70](common-control-versions.md)。 月曆控制項會在每個資料列的左邊顯示 (1-52) 的周數。 第1周定義為至少包含四天的第一周。 <br/>                                                                                              |
| <span id="MCS_NOTODAYCIRCLE"></span><span id="mcs_notodaycircle"></span><dl> <dt>**MCS \_ NOTODAYCIRCLE**</dt> </dl>          | [版本 4.70](common-control-versions.md)。 月曆控制項不會圈出「今天」的日期。 <br/>                                                                                                                                                                                                |
| <span id="MCS_NOTODAY"></span><span id="mcs_notoday"></span><dl> <dt>**MCS \_ NOTODAY**</dt> </dl>                            | [版本 4.70](common-control-versions.md)。月曆控制項不會在控制項底部顯示「今天」的日期。 <br/>                                                                                                                                                                   |
| <span id="MCS_NOTRAILINGDATES"></span><span id="mcs_notrailingdates"></span><dl> <dt>**MCS \_ NOTRAILINGDATES**</dt> </dl>    | **Windows Vista。** 上個月和下個月的日期，不會顯示在當月的日曆中。<br/>                                                                                                                                                                                              |
| <span id="MCS_SHORTDAYSOFWEEK"></span><span id="mcs_shortdaysofweek"></span><dl> <dt>**MCS \_ SHORTDAYSOFWEEK**</dt> </dl>    | **Windows Vista。** 簡短的日期名稱會顯示在標頭中。<br/>                                                                                                                                                                                                                                            |
| <span id="MCS_NOSELCHANGEONNAV"></span><span id="mcs_noselchangeonnav"></span><dl> <dt>**MCS \_ NOSELCHANGEONNAV**</dt> </dl> | **Windows Vista。** 當使用者流覽日曆中的下一個或上一個時，不會變更選取專案。 這可讓使用者選取 [大於] 可見的範圍。<br/>                                                                                                                                  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





