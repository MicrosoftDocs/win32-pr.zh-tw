---
title: 'NM_CUSTOMDRAW (清單視圖) 通知碼 (Commctrl) '
description: 由清單視圖控制項傳送，以通知其父視窗關於繪圖作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 4e9b91e3-d042-4fd0-b063-a9e6ea9ad564
keywords:
- NM_CUSTOMDRAW (清單視圖) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: ba991f5af43ee5513ec0713208aed84319bd5a9a
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812677"
---
# <a name="nm_customdraw-list-view-notification-code"></a>NM \_ CUSTOMDRAW (清單視圖) 通知碼

由清單視圖控制項傳送，以通知其父視窗關於繪圖作業。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。 此結構（ **nmcd**）的第一個成員是指向 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) 結構的指標。 **Nmcd** 所指向之結構的 **dwItemSpec** 成員包含所繪製專案的識別碼，而 **lItemlParam** 成員包含其應用程式定義的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

您的應用程式可以傳回的值取決於目前的繪圖階段。 相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。 您必須傳回下列其中一個值。



| 傳回碼                                                                                            | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | 控制項將會自行繪製。 它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ DOERASE**</dt> </dl>           | Windows Vista。 控制項只會繪製背景。 <br/>                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | 控制項將會通知任何專案相關繪圖作業的父系。 它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | 控制項將會在清除專案之後通知父代。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | 控制項將會在繪製專案之後通知父系。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | 應用程式為專案指定了新的字型;控制項將會使用新的字型。 如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [版本4.71。](common-control-versions.md) 您的應用程式將會在 [ \_ ](nm-customdraw.md) \_ \| \_ 繪製每個清單視圖子集合之前，收到具有 dwDrawStage 設定為 CDDS ITEMPREPAINT CDDS 子工作的 NM CUSTOMDRAW 控制項程式碼。 然後，您可以分別為每個子項指定字型和色彩，或針對預設處理傳回 [**CDRF \_ DODEFAULT**](cdrf-constants.md) 。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | 應用程式會以手動方式繪製專案。 控制項不會繪製專案。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | Windows Vista。 控制項不會繪製焦點矩形。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>備註

[版本5.80。](common-control-versions.md) 如果您藉由傳回 [**CDRF \_ NEWFONT**](cdrf-constants.md)來變更字型，則清單視圖控制項可能會顯示已裁剪的文字。 這是與舊版通用控制項的回溯相容性所需的行為。 如果您想要變更清單視圖控制項的字型，則在將任何專案加入至控制項之前，如果您將 *wParam* 值設定為5，則會得到更 [**好的結果 \_**](ccm-setversion.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





