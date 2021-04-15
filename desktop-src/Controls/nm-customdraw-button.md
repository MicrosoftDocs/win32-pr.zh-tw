---
title: 'NM_CUSTOMDRAW (按鈕) 通知碼 (Commctrl) '
description: 通知按鈕控制項的父視窗，有關按鈕上的自訂繪製作業。 按鈕控制項會以 WM 通知訊息的形式傳送此通知碼 \_ 。
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- NM_CUSTOMDRAW (按鈕) 通知碼 Windows 控制項
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
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467113"
---
# <a name="nm_customdraw-button-notification-code"></a>NM \_ CUSTOMDRAW (按鈕) 通知碼

通知按鈕控制項的父視窗，有關按鈕上的自訂繪製作業。

按鈕控制項會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送此通知碼。


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



| 傳回碼                                                                                          | Description                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CDRF \_ NOTIFYPOSTERASE**</dt> </dl> | 控制項將會在清除專案之後通知父代。 只有在 **dwDrawStage** 等於 CDDS PREERASE 時，才可以使用此 \_ 。<br/>                                  |
| <dl> <dt>**CDRF \_ NOTIFYPOSTPAINT**</dt> </dl> | 控制項將會在繪製專案之後通知父系。 只有在 **dwDrawStage** 等於 CDDS PREPAINT 時，才可以使用此 \_ 。<br/>                                 |
| <dl> <dt>**CDRF \_ SKIPDEFAULT**</dt> </dl>     | 應用程式會以手動方式繪製專案。 控制項不會繪製專案。 這可在 **dwDrawStage** 等於 CDDS \_ PREERASE 或 CDDS PREPAINT 時使用 \_ 。<br/> |



 

## <a name="remarks"></a>備註

如果按鈕控制項標示為 ownerdraw (BS \_ ownerdraw) ，則 \_ 不會傳送 NM CUSTOMDRAW 通知碼。

請參閱 [使用自訂繪製](custom-draw.md) 來進一步討論。

> [!Note]  
> 若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Commctrl (包含) 的 Windows。h </dt> </dl> |



 

 





