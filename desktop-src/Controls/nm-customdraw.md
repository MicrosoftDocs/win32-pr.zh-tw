---
title: 'NM_CUSTOMDRAW (Commctrl 的通知碼) '
description: 通知控制項的父視窗有關自訂繪圖作業的相關資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2ca51ee0-4431-45c0-880c-a8b74318d8a9
keywords:
- NM_CUSTOMDRAW 通知碼 Windows 控制項
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
ms.openlocfilehash: d5f91f5197c7ecaf0ae4356fe00c48221a83ebd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464268"
---
# <a name="nm_customdraw-notification-code"></a>NM \_ CUSTOMDRAW 通知碼

通知控制項的父視窗有關自訂繪圖作業的相關資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_CUSTOMDRAW

#ifdef LIST_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMLVCUSTOMDRAW) lParam;

#elif TOOL_TIPS_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTTCUSTOMDRAW) lParam;

#elif TREE_VIEW_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTVCUSTOMDRAW) lParam;

#elif TOOL_BAR_CUSTOM_DRAW

    lpNMCustomDraw = (LPNMTBCUSTOMDRAW) lParam;

#else

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;

#endif
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

自訂繪圖相關結構的指標，其中包含繪圖作業的相關資訊。 下列清單指定控制項及其相關聯的結構。



| 控制                     | 自訂繪圖結構                    |
|-----------------------------|------------------------------------------|
| Rebar、標題和標頭 | [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)     |
| 清單檢視                   | [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) |
| 工具提示                     | [**NMTTCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmttcustomdraw) |
| 樹狀檢視                   | [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) |
| 工具列                     | [**NMTBCUSTOMDRAW**](/windows/desktop/api/Commctrl/ns-commctrl-nmtbcustomdraw) |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

您的應用程式可以傳回的值取決於目前的繪圖階段。 相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。 您必須傳回下列其中一個值。



| 傳回碼                                                                                            | Description                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | 控制項將會自行繪製。 它不會為此繪製迴圈傳送額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 此旗標不可與任何其他旗標一起使用。 <br/>                                                                                                                                                                                                                                 |
| <dl> <dt>**CDRF \_ DOERASE**</dt> </dl>           | 控制項只會繪製背景。<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | 您的應用程式已為專案指定新字型;控制項將會使用新的字型。 如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                        |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | 控制項將會通知任何專案相關繪圖作業的父系。 它會在繪製專案之前和之後傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                                                |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | 控制項將會在清除專案之後通知父代。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | 當整個控制項的繪製迴圈完成時，控制項將傳送 [NM \_ CUSTOMDRAW](nm-customdraw.md) 通知碼。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                                                                                    |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | 您的應用程式將會在[ \_ ](nm-customdraw.md)  \_ \| \_ 繪製每個清單視圖子集合之前，收到 CUSTOMDRAW 通知碼，其中 dwDrawStage 設定為 CDDS ITEMPREPAINT CDDS 子。 然後，您可以分別為每個子項指定字型和色彩，或針對預設處理傳回 [**CDRF \_ DODEFAULT**](cdrf-constants.md) 。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | 您的應用程式會以手動方式繪製專案。 控制項不會繪製專案。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**CDRF \_ SKIPPOSTPAINT**</dt> </dl>     | 控制項不會在專案周圍繪製焦點矩形。<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>備註

目前，下列控制項支援自訂繪製功能：標頭、清單視圖、Rebar、工具列、工具提示、標題和樹狀檢視。 如果您有應用程式資訊清單，以確保 Comctl32.dll 版本6可供使用，則按鈕控制項也支援自訂繪製。

如果在對話程式中處理此訊息，您必須先將傳回值設定為視窗資料的一部分，然後再傳回 **TRUE**。 如需詳細資訊，請參閱 [**DialogProc**](/windows/desktop/api/winuser/nc-winuser-dlgproc)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**概念**
</dt> <dt>

[自訂繪圖](custom-draw.md)
</dt> </dl>

 

