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
ms.openlocfilehash: b6f9740e0de413649b67cc8231d31425d212d2571dbc9a1b703f9f95c35e4981
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085758"
---
# <a name="date-and-time-picker-control-styles"></a>日期和時間選擇器控制項樣式

此處所列的視窗樣式是日期和時間選擇器控制項特有的樣式。



| 常數                                                                                                                                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DTS_APPCANPARSE"></span><span id="dts_appcanparse"></span><dl> <dt>**DTS \_ APPCANPARSE**</dt> </dl>                                  | 允許擁有者剖析使用者輸入並採取必要的動作。 當使用者按下 F2 鍵時，可讓使用者在控制項的工作區內進行編輯。 當使用者完成時，控制項會傳送 [DTN \_ USERSTRING](dtn-userstring.md) 通知碼。<br/>                                                                                                                                                                                                                                                                    |
| <span id="DTS_LONGDATEFORMAT"></span><span id="dts_longdateformat"></span><dl> <dt>**DTS \_ LONGDATEFORMAT**</dt> </dl>                         | 以完整格式顯示日期。 這種樣式的預設格式字串是由地區設定 \_ SLONGDATEFORMAT 所定義，它會產生像是「在1996年4月19日星期五」的輸出。 使用此樣式時，下拉式按鈕不會顯示圖示。<br/>                                                                                                                                                                                                                                                                                     |
| <span id="DTS_RIGHTALIGN"></span><span id="dts_rightalign"></span><dl> <dt>**DTS \_ RIGHTALIGN**</dt> </dl>                                     | 下拉式月曆將會靠右對齊控制項，而不是靠左對齊（預設值）。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHOWNONE"></span><span id="dts_shownone"></span><dl> <dt>**DTS \_ SHOWNONE**</dt> </dl>                                           | 目前無法在控制項中選取任何日期。 使用此樣式時，控制項會顯示每次挑選或輸入日期時都會自動選取的核取方塊。 如果後續核取方塊已取消選取，應用程式就無法從控制項取出日期，因為基本上，控制項沒有日期。 您可以使用 [**dtm \_ SETSYSTEMTIME**](dtm-setsystemtime.md) 訊息來設定核取方塊的狀態，或使用 [**dtm \_ GETSYSTEMTIME**](dtm-getsystemtime.md) 訊息來進行查詢。<br/> |
| <span id="DTS_SHORTDATEFORMAT"></span><span id="dts_shortdateformat"></span><dl> <dt>**DTS \_ SHORTDATEFORMAT**</dt> </dl>                      | 以簡短格式顯示日期。 此樣式的預設格式字串是由地區設定 SSHORTDATE 所定義 \_ ，它會產生 "4/19/96" 之類的輸出。<br/>                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DTS_SHORTDATECENTURYFORMAT"></span><span id="dts_shortdatecenturyformat"></span><dl> <dt>**DTS \_ SHORTDATECENTURYFORMAT**</dt> </dl> | **版本5.80。** 類似于 **DTS \_ SHORTDATEFORMAT** 樣式，不同之處在于年份是四位數的欄位。 此樣式的預設格式字串是根據地區設定 \_ SSHORTDATE。 輸出如下所示： "4/19/1996"。<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="DTS_TIMEFORMAT"></span><span id="dts_timeformat"></span><dl> <dt>**DTS \_ 時間格式**</dt> </dl>                                     | 顯示時間。 此樣式的預設格式字串是由地區設定 STIMEFORMAT 所定義 \_ ，它會產生像是 "5:31:42 PM" 的輸出。<br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="DTS_UPDOWN"></span><span id="dts_updown"></span><dl> <dt>**DTS \_ 上下按鈕**</dt> </dl>                                                 | 將上下按鈕控制項放在 DTP 控制項的右邊，以修改日期時間值。 這個樣式可以用來取代以預設樣式表示的下拉式月曆。<br/>                                                                                                                                                                                                                                                                                                                                                |



## <a name="remarks"></a>備註

\_無法合併定義顯示格式的 DTS XXXFORMAT 樣式。 如果沒有適用的格式樣式，請使用 [**DTM \_ SETFORMAT**](dtm-setformat.md) 訊息來定義自訂格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>CommCtrl。h</dt> </dl> |



 

 





