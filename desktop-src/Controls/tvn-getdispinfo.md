---
title: 'TVN_GETDISPINFO (Commctrl 的通知碼) '
description: 要求樹狀檢視控制項的父視窗提供顯示或排序專案所需的資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2dfe41d8-1164-481b-ac07-8faba43c562a
keywords:
- TVN_GETDISPINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_GETDISPINFO
- TVN_GETDISPINFOA
- TVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59728c816ee3fe7dac46c12d7e62da6c18cfdad8387f03d3861e63792d9c8f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059908"
---
# <a name="tvn_getdispinfo-notification-code"></a>IZDEBSKI \_ GETDISPINFO 通知碼

要求樹狀檢視控制項的父視窗提供顯示或排序專案所需的資訊。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_GETDISPINFO 

    lptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa)結構的指標。 **專案** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其 **mask**、 **hItem**、 **state** 和 **lParam** 成員會指定所需的資訊類型。 您必須以適當的資訊填入結構的成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

此通知碼會在下列情況下傳送：

-   如果專案的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **PSZTEXT** 成員是 LPSTR \_ TEXTCALLBACK 值，控制項會傳送此通知碼以取得專案的文字。 在此情況下， *lParam* 的 **mask** 成員將會設定 TVIF \_ 文字旗標。
-   如果專案 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **iImage** 或 **iSelectedImage** 成員是 I \_ IMAGECALLBACK 值，控制項會傳送此通知碼，以抓取控制項影像清單中專案圖示的索引。 在此情況下，如果選取專案， *lParam* 的 **mask** 成員將會 \_ 設定 TVIF SELECTEDIMAGE 旗標。 如果未選取此專案， *lParam* 的 **mask** 成員將會 \_ 設定 TVIF 影像旗標。
-   如果專案的 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構的 **cChildren** 成員是 I \_ CHILDRENCALLBACK 值，控制項會傳送此通知碼以取得指出專案是否有子專案的值。 在此情況下， *lParam* 的 **mask** 成員將會設定 TVIF \_ 子旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_GETDISPINFOW** (Unicode) 和 **izdebski \_ GETDISPINFOA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IZDEBSKI \_ SETDISPINFO](tvn-setdispinfo.md)
</dt> </dl>

 

 





