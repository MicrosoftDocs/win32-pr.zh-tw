---
title: 'NM_CUSTOMDRAW (的)  (Commctrl 通知碼) '
description: 由 [資料提示] 控制項傳送，以通知其父視窗關於繪圖作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b31d774d-e418-4162-aa2a-40fa49452d58
keywords:
- NM_CUSTOMDRAW (的程式碼段) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d863b180948676342a49615a526c8f6860905744aaf5269468807ad6dc04fa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109548"
---
# <a name="nm_customdraw-trackbar-notification-code"></a>NM \_ CUSTOMDRAW (的) 通知碼

由 [資料提示] 控制項傳送，以通知其父視窗關於繪圖作業。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。 此結構的 **dwItemSpec** 成員會包含其中一個 [自訂繪製值](custom-draw-values.md) ，指出正在繪製控制項的哪個部分。 [可見度] 控制項會將下列值插入此結構的 **dwItemSpec** 成員，以識別所繪製之控制項的部分：



| 值                                                                                                                                                      | 意義                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**TBCD \_ 通道**</dt> </dl> | 識別 [對齊程式] 控制項的 thumb 標記所投影的通道。 <br/>                           |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**TBCD \_ THUMB**</dt> </dl>       | 識別 [資料指標] 控制項的 [thumb] 標記。 這是使用者移動之控制項的部分。 <br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ TICS**</dt> </dl>          | 識別出現在 [側邊] 控制項邊緣的遞增刻度。 <br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

您的應用程式可以傳回的值取決於目前的繪圖階段。 相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。 您必須傳回下列其中一個值。



| 傳回碼                                                                                            | 描述                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | 控制項將會自行繪製。 它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | 控制項將會通知任何專案相關繪圖作業的父系。 它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                         |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | 控制項將會在清除專案之後通知父代。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | 控制項將會在繪製專案之後通知父系。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [版本 4.71](common-control-versions.md)。 當正在繪製清單視圖子項目時，控制項將會通知父代。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                               |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | 您的應用程式已為專案指定新字型;控制項將會使用新的字型。 如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | 您的應用程式會以手動方式繪製專案。 控制項不會繪製專案。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用自訂繪圖](custom-draw.md)
</dt> </dl>

 

 





