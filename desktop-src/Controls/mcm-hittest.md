---
title: 'MCM_HITTEST 訊息 (Commctrl .h) '
description: 判斷月曆控制項的哪個部分位於螢幕上的指定點。 您可以使用 MonthCal System.windows.media.visualtreehelper.hittest 宏明確地傳送此訊息 \_ 。
ms.assetid: 51e74b07-4ed7-488d-ad5d-116f046577fc
keywords:
- MCM_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3670ac8ab663ceda1786f7136a50c4da255a76c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685604"
---
# <a name="mcm_hittest-message"></a>MCM \_ system.windows.media.visualtreehelper.hittest 訊息

判斷月曆控制項的哪個部分位於螢幕上的指定點。 您可以使用 [**MonthCal \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_hittest) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo)結構的指標。 傳送訊息時， **cbSize** 成員必須設定為 **MCHITTESTINFO** 結構的大小，且 **pt** 必須設定為您想要點擊測試的時間點。

</dd> </dl>

## <a name="return-value"></a>傳回值

設定的成員中的值。



| 傳回碼                                                                                           | Description                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MCHT 行事 \_ 曆**</dt> </dl>         | 指定的點在行事曆內。<br/>                                                                                                                                                                                                                       |
| <dl> <dt>**MCHT \_ CALENDARBK**</dt> </dl>       | 指定的點在行事曆的背景中。<br/>                                                                                                                                                                                                              |
| <dl> <dt>**MCHT \_ CALENDARDATE**</dt> </dl>     | 指定的點在行事曆內的特定日期。 位於 *lParam >st* 的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構會設定為指定點的日期。<br/>                                                                                    |
| <dl> <dt>**MCHT \_ CALENDARDATENEXT**</dt> </dl> | 給定的點是在下個月的日期之後 (部分顯示在目前顯示的月份) 的結尾。 如果使用者按一下這裡，月曆會將其顯示滾動到下個月或一組月份。<br/>                                 |
| <dl> <dt>**MCHT \_ CALENDARDATEPREV**</dt> </dl> | 給定的點是上個月的日期， (部分顯示在目前顯示的月份) 的結尾。 如果使用者按一下這裡，月曆將會將其顯示滾動到上個月或一組月份。<br/>                         |
| <dl> <dt>**MCHT \_ CALENDARDAY**</dt> </dl>      | 指定的點超過一天的縮寫 ( "週五"，例如) 。 位於 *lParam >st* 的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構會設定為頂端資料列中的對應日期。<br/>                                                                      |
| <dl> <dt>**MCHT \_ CALENDARWEEKNUM**</dt> </dl>  | 給定的點是在一周內 ([**MCS \_ WEEKNUMBERS**](month-calendar-control-styles.md) 樣式) 。 位於 *lParam >st* 的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構會設定為最左邊資料行中的對應日期。<br/> |
| <dl> <dt>**MCHT \_ 下一步**</dt> </dl>             | 給定的點位於將導致月曆將其顯示滾動到下個月或一組月份的區域中。 此旗標是用來修改其他點擊測試旗標。<br/>                                                                                   |
| <dl> <dt>**MCHT \_ 地方**</dt> </dl>          | 給定的點不在月曆控制項上，或是在控制項的非作用中部分。<br/>                                                                                                                                                        |
| <dl> <dt>**MCHT \_ 上一步**</dt> </dl>             | 給定的點會在一個區域中，讓月曆將其顯示滾動到上個月或一組月份。 此旗標是用來修改其他點擊測試旗標。<br/>                                                                               |
| <dl> <dt>**MCHT \_ 標題**</dt> </dl>            | 指定的點超過一個月的標題。<br/>                                                                                                                                                                                                                      |
| <dl> <dt>**MCHT \_ TITLEBK**</dt> </dl>          | 給定的點是在月份標題的背景上。<br/>                                                                                                                                                                                                    |
| <dl> <dt>**MCHT \_ TITLEBTNNEXT**</dt> </dl>     | 指定的點是在控制項右上角的按鈕上方。 如果使用者按一下這裡，月曆會將其顯示滾動到下個月或一組月份。 <br/>                                                                           |
| <dl> <dt>**MCHT \_ TITLEBTNPREV**</dt> </dl>     | 指定的點是在控制項左上角的按鈕上方。 如果使用者按一下這裡，月曆將會將其顯示滾動到上個月或一組月份。 <br/>                                                                        |
| <dl> <dt>**MCHT \_ TITLEMONTH**</dt> </dl>       | 指定的點在月份的標題列中，超過一個月的名稱。<br/>                                                                                                                                                                                                 |
| <dl> <dt>**MCHT \_ TITLEYEAR**</dt> </dl>        | 給定的點在月份的標題列中，超過年份值。<br/>                                                                                                                                                                                               |
| <dl> <dt>**MCHT \_ TODAYLINK**</dt> </dl>        | 指定的點是在月曆控制項底部的「今天」連結。<br/> *LParam* 中 [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo)結構的 **uHit** 成員會等於傳回值。 <br/>                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

