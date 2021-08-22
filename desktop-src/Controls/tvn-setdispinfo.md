---
title: 'TVN_SETDISPINFO (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，它必須更新它針對某個專案所維護的資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 40fa61bc-c043-4001-ada9-b627d68bd737
keywords:
- TVN_SETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_SETDISPINFO
- TVN_SETDISPINFOA
- TVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88a9b5fed4260fa88f5f40431113456950d99985ad2f2e0e97c2e951dce96bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957767"
---
# <a name="tvn_setdispinfo-notification-code"></a>IZDEBSKI \_ SETDISPINFO 通知碼

通知樹狀檢視控制項的父視窗，它必須更新它針對某個專案所維護的資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_SETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

描述正在更新之專案的 [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) 結構指標。 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **hItem** 成員會指定要更新的專案，而 **遮罩** 成員會指定要更新專案的哪些屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

如果專案的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **PSZTEXT** 成員是 LPSTR \_ TEXTCALLBACK 值，控制項會傳送此通知來設定專案的文字。 在此情況下， *lParam* 的 **mask** 成員將會設定 TVIF \_ 文字旗標。

如果專案 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **iImage** 或 **iSelectedImage** 成員是 I \_ IMAGECALLBACK 值，控制項會傳送此通知，以取得要顯示之圖示影像的索引。 在此情況下， *lParam* 的 **mask** 成員將會設定 TVIF \_ IMAGE 或 TVIF \_ SELECTEDIMAGE 旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_SETDISPINFOW** (Unicode) 和 **izdebski \_ SETDISPINFOA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)
</dt> <dt>

[**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)
</dt> <dt>

[IZDEBSKI \_ GETDISPINFO](tvn-getdispinfo.md)
</dt> </dl>

 

 





