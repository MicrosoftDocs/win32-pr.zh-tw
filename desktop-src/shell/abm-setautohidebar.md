---
description: 註冊或取消註冊螢幕指定邊緣的自動隱藏 appbar。 如果系統有多個監視器，則會使用包含主要工作列的監視器。
title: 'ABM_SETAUTOHIDEBAR 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972097"
---
# <a name="abm_setautohidebar-message"></a>ABM \_ SETAUTOHIDEBAR 訊息

註冊或取消註冊螢幕指定邊緣的自動隱藏 appbar。 如果系統有多個監視器，則會使用包含主要工作列的監視器。

> [!Note]  
> 若要在特定監視器上註冊或取消註冊自動隱藏 appbar，請使用 [**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)。

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。 將 **lParam** 成員設定為 **TRUE** ，即可註冊 appbar 或 **FALSE** 以將其取消註冊。 傳送此訊息時，您必須指定 **cbSize**、 **hWnd**、 **uEdge** 和 **lParam** 成員;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果發生錯誤，或如果已為指定的邊緣註冊自動隱藏 appbar，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

系統只允許畫面的每個邊緣都有一個自動隱藏 appbar。 當設定 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的成員 **uEdge** 時，就會決定這一點。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




