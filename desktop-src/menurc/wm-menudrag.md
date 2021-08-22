---
title: 'WM_MENUDRAG 訊息 (Winuser .h) '
description: 當使用者拖曳功能表項目時，傳送至拖放功能表的擁有者。
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG 訊息功能表和其他資源
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22792c7606bb001b72b7c4751d14129bca02c5b4a5b337e0349a9a9a2120b62a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971797"
---
# <a name="wm_menudrag-message"></a>WM \_ MENUDRAG 訊息

當使用者拖曳功能表項目時，傳送至拖放功能表的擁有者。


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

拖曳作業開始的專案位置。

</dd> <dt>

*lParam* 
</dt> <dd>

包含專案之功能表的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

應用程式應該會傳回下列其中一個值。



| 傳回碼/值                                                                                                                                   | 描述                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**MND \_繼續**</dt> <dt>0</dt> </dl> | 功能表應維持使用中狀態。 如果放開滑鼠，則應該予以忽略。<br/> |
| <dl> <dt>**MND \_ENDMENU**</dt> <dt>1</dt> </dl>  | 應結束功能表。<br/>                                                      |



 

## <a name="remarks"></a>備註

應用程式可以呼叫 [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) 函式來回應此訊息。

若要建立拖放功能表，請使用 **MNS \_ System.windows.dragdrop.drop>** 呼叫 [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) 。

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

[**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

**概念**
</dt> <dt>

[功能表](menus.md)
</dt> </dl>

 

