---
title: 'LVN_SETDISPINFO (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，它必須更新它為專案維護的資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659623d892f0f5a556f4890703d4e0dd725536b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934728"
---
# <a name="lvn_setdispinfo-notification-code"></a>LVN \_ SETDISPINFO 通知碼

通知清單視圖控制項的父視窗，它必須更新它為專案維護的資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)結構的指標，指定已變更之專案的資訊。 此結構的 **專案** 成員是 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構，其中包含已變更之專案的相關資訊。 **專案** 的 **pszText** 成員包含有效的值，不論是否在 \_ 此結構的 **遮罩** 成員中設定 LVIF 文字旗標。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

通知接收者會轉換 *lParam* 來取出 [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) 結構。 *WParam* 參數包含訊息碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVN \_SETDISPINFOW** (Unicode) 和 **LVN \_ SETDISPINFOA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[LVN \_ GETDISPINFO](lvn-getdispinfo.md)
</dt> </dl>

 

 





