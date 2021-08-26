---
title: 'WM_NEXTMENU 訊息 (Winuser .h) '
description: 當使用向右鍵或向左鍵切換至功能表列和系統功能表時，傳送至應用程式。
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 635ce19efbcfdfd8451f929affbbe0fe2b2c000bc4912977062f3fba2c54e9c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952078"
---
# <a name="wm_nextmenu-message"></a>WM \_ NEXTMENU 訊息

當使用向右鍵或向左鍵切換至功能表列和系統功能表時，傳送至應用程式。


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

金鑰的虛擬按鍵碼。 請參閱 [**虛擬金鑰代碼**](/windows/desktop/inputdev/virtual-key-codes)。

</dd> <dt>

*lParam* 
</dt> <dd>

[**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)結構的指標，其中包含要啟用之功能表的相關資訊。

</dd> </dl>

## <a name="remarks"></a>備註

回應此訊息時，應用程式可以在 [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)的 **hmenuNext** 成員中指定要切換的功能表，並在視窗中指定要在 **MDINEXTMENU** 結構的 **hwndNext** 成員中接收功能表通知訊息的功能表。 您必須設定這兩個成員，變更才會生效 (這些成員最初是 **Null**) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**概念**
</dt> <dt>

[功能表](menus.md)
</dt> </dl>

 

