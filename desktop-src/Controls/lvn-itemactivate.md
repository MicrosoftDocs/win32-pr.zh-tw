---
title: 'LVN_ITEMACTI加值稅E (Commctrl 的通知碼) '
description: 由清單視圖控制項在使用者啟用專案時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTI加值稅E 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21b02406157a13d2fcf110c15e692211b26b3f9da31741489e317e6b2c68309
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105048"
---
# <a name="lvn_itemactivate-notification-code"></a>LVN \_ ITEMACTI加值稅E 通知碼

由清單視圖控制項在使用者啟用專案時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[版本 4.71](common-control-versions.md)。 [**NMITEMACTI加值稅E**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate)結構的指標，其中包含此通知碼的相關資訊。

[4.70 版](common-control-versions.md) 及更早版本。 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

接收此通知碼的應用程式必須傳回零。

## <a name="remarks"></a>備註

若要取得正在啟用的專案，接收應用程式應該使用 [**LVM \_ GETSELECTEDCOUNT**](lvm-getselectedcount.md)訊息來取出所選的專案數目，然後將已 **\_ 選取 LVNI** 的 [**lvm \_ GETNEXTITEM**](lvm-getnextitem.md)訊息傳送到所有的專案都已抓取為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





