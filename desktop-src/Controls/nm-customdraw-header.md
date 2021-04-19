---
title: 'NM_CUSTOMDRAW (標頭) 通知碼 (Commctrl) '
description: 由標題控制項傳送，以通知其父視窗有關繪製作業。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 44dab54b-45ef-4fba-93b8-2a3e35cda23f
keywords:
- NM_CUSTOMDRAW (標頭) 通知碼 Windows 控制項
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
ms.openlocfilehash: 89d6b35503aebed221da6cec212c6dbf614061f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967576"
---
# <a name="nm_customdraw-header-notification-code"></a>NM \_ CUSTOMDRAW (標頭) 通知碼

由標題控制項傳送，以通知其父視窗有關繪製作業。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的指標，其中包含繪圖作業的相關資訊。 此結構的 **dwItemSpec** 成員包含所繪製專案的索引，而且此結構的 **lItemlParam** 成員包含該專案的 *lParam*。

</dd> </dl>

## <a name="return-value"></a>傳回值

您的應用程式可以傳回的值取決於目前的繪圖階段。 相關聯之 [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw)結構的 **dwDrawStage** 成員會保存指定繪圖階段的值。 您必須傳回下列其中一個值。



| 傳回碼                                                                                            | Description                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ DODEFAULT**</dt> </dl>         | 控制項將會自行繪製。 它不會針對此繪製迴圈傳送任何額外的 [NM \_ CUSTOMDRAW](nm-customdraw.md) 訊息。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                       |
| <dl> <dt>**CDRF \_ NOTIFYITEMDRAW**</dt> </dl>    | 控制項將會通知任何專案相關繪圖作業的父系。 它會 \_ 在繪製專案之前和之後傳送 NM CUSTOMDRAW 通知碼。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl>   | 控制項將會在清除專案之後通知父代。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                              |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl>   | 控制項將會在繪製專案之後通知父系。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                                             |
| <dl> <dt>**CDRF \_ NOTIFYSUBITEMDRAW**</dt> </dl> | [通用控制項版本](common-control-versions.md)。 當正在繪製清單視圖子項目時，控制項將會通知父代。 當 **dwDrawStage** 等於 CDDS PREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                    |
| <dl> <dt>**CDRF \_ NEWFONT**</dt> </dl>           | 您的應用程式已為專案指定新字型;控制項將會使用新的字型。 如需變更字型的詳細資訊，請參閱 [變更字型和色彩](custom-draw.md)。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/> |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>       | 您的應用程式會以手動方式繪製專案。 控制項不會繪製專案。 當 **dwDrawStage** 等於 CDDS ITEMPREPAINT 時，就會發生這種情況 \_ 。<br/>                                                                                                                                       |



 

## <a name="remarks"></a>備註

請參閱 [使用自訂繪製](custom-draw.md) 來進一步討論。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





