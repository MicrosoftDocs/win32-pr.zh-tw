---
title: 'NM_GETCUSTOMSPLITRECT (Commctrl 的通知碼) '
description: 由按鈕控制項傳送至其父系，以取得分割按鈕的兩個矩形的度量。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ce72778d-3cca-46a4-9d05-40954a18681d
keywords:
- NM_GETCUSTOMSPLITRECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_GETCUSTOMSPLITRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b839540da7e07069fdf56ed656ed8772d029eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093828"
---
# <a name="nm_getcustomsplitrect-notification-code"></a>NM \_ GETCUSTOMSPLITRECT 通知碼

由按鈕控制項傳送至其父系，以取得分割按鈕的兩個矩形的度量。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_GETCUSTOMSPLITRECT
        
    nmCustomSplit = (NMCUSTOMSPLITRECTINFO *) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo)的指標，用來接收周框矩形的資訊。 **NMCUSTOMSPLITRECTINFO** 結構會隨著通知程式碼傳送，作為父代的要求，以針對分割按鈕的矩形提供度量。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [**CDRF \_ SKIPDEFAULT**](cdrf-constants.md) ，告知按鈕控制項使用 [**NMCUSTOMSPLITRECTINFO**](/windows/win32/api/commctrl/ns-commctrl-nmcustomsplitrectinfo) 結構中傳回的值，否則傳回 [**CDRF \_ DODEFAULT**](cdrf-constants.md)。

## <a name="remarks"></a>備註

此通知碼是由按鈕控制項在繪製前傳送。 此按鈕的樣式必須是 [**BS \_ SPLITBUTTON**](button-styles.md) 或 [**BS \_ DEFSPLITBUTTON**](button-styles.md)。 如果在 *lParam* 中傳回給控制項的矩形無效，則會忽略它們。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





