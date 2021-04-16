---
title: 'LVN_GETINFOTIP (Commctrl 的通知碼) '
description: 由大型圖示視圖清單-view 控制項（具有 LVS) EX 提示的 \_ \_ 延伸樣式）傳送。
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509494"
---
# <a name="lvn_getinfotip-notification-code"></a>LVN \_ GETINFOTIP 通知碼

由大型圖示視圖清單-view 控制項（具有 [**lvs) \_ EX \_**](extended-list-view-styles.md) 提示的延伸樣式）傳送。 當清單視圖控制項要求要顯示在工具提示中的其他文字資訊時，就會傳送此通知碼。 它是以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa)結構的指標，其中包含此通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此通知的傳回值。

## <a name="remarks"></a>備註

此通知碼只會由具有 [**lvs) \_ EX \_**](extended-list-view-styles.md) 提示擴充樣式的清單視圖控制項所傳送。 LVN \_ GETINFOTIP 通知碼只會針對子項0傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVN \_GETINFOTIPW** (Unicode) 和 **LVN \_ GETINFOTIPA** (ANSI) <br/>             |



 

 





