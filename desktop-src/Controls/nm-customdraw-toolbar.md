---
title: 'NM_CUSTOMDRAW (工具列) 通知碼 (Commctrl) '
description: 由工具列傳送以通知其父視窗有關繪製作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e83a85f4-7955-411d-9a08-29f5b30158c5
keywords:
- NM_CUSTOMDRAW (工具列) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: c8d1a33e6b7e9a26237813ec3a90e560f05dd9ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509492"
---
# <a name="nm_customdraw-toolbar-notification-code"></a>NM \_ CUSTOMDRAW (工具列) 通知碼

由工具列傳送以通知其父視窗有關繪製作業。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_CUSTOMDRAW
        
    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[版本 4.70](common-control-versions.md)。 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。 此結構的 **dwItemSpec** 成員包含所繪製專案的命令識別碼。 此結構的 **lItemlParam** 成員包含所繪製專案的 **dwData** 值。

[版本 4.71](common-control-versions.md)。 [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。 此結構之 **nmcd** 成員的 **dwItemSpec** 成員包含所繪製專案的命令識別碼。 此結構之 **nmcd** 成員的 **lItemlParam** 成員包含所繪製專案的 **dwData** 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

您的應用程式可以傳回的值取決於目前的繪圖階段。 相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。 您必須傳回下列其中一個值。



| 傳回碼                                                                                            | Description                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | 控制項將會自行繪製。 它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | 控制項將會通知任何專案相關繪圖作業的父系。 它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                         |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | 控制項將會在清除專案之後通知父代。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | 控制項將會在繪製專案之後通知父系。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [版本 4.71](common-control-versions.md)。 當正在繪製清單視圖子項目時，控制項將會通知父代。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                               |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | 您的應用程式已為專案指定新字型;控制項將會使用新的字型。 如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | 您的應用程式會以手動方式繪製專案。 控制項不會繪製專案。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                       |
| <dl> <dt>**TBCDRF \_ BLENDICON**</dt> </dl>       | [版本 5.00](common-control-versions.md)。 將按鈕50百分比與背景混合。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                      |
| <dl> <dt>**TBCDRF \_ NOBACKGROUND**</dt> </dl>    | [版本 5.00](common-control-versions.md)。 不要繪製按鈕背景。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                        |
| <dl> <dt>**TBCDRF \_ NOEDGES**</dt> </dl>         | [版本 4.71](common-control-versions.md)。 不要繪製按鈕邊緣。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                             |
| <dl> <dt>**TBCDRF \_ HILITEHOTTRACK**</dt> </dl>  | [版本 4.71](common-control-versions.md)。 使用 [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw)結構的 **clrHighlightHotTrack** 成員來繪製熱追蹤專案的背景。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                        |
| <dl> <dt>**TBCDRF \_ NOOFFSET**</dt> </dl>        | [版本 4.71](common-control-versions.md)。 當按下時，請勿位移按鈕。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                |
| <dl> <dt>**TBCDRF \_ NOMARK**</dt> </dl>          | 請勿繪製 [**\_ 標示了 TBSTATE**](toolbar-button-states.md)之專案的預設反白顯示。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                              |
| <dl> <dt>**TBCDRF \_ NOETCHEDEFFECT**</dt> </dl>  | [版本 4.71](common-control-versions.md)。 請勿針對停用的專案繪製蝕刻效果。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                         |
| <dl> <dt>**TBCDRF \_ USECDCOLORS**</dt> </dl>     | [版本 6.00](common-control-versions.md)，僅限 **Windows Vista** 。 無論視覺化樣式為何，都可以使用自訂繪製色彩來轉譯文字。<br/>                                                                                                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用自訂繪圖](custom-draw.md)
</dt> </dl>

 

 





