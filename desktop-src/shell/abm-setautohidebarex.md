---
description: 註冊或取消註冊螢幕指定邊緣的自動隱藏 appbar。 此訊息可 \_ 讓您指定特定的監視，以擴充 ABM SETAUTOHIDEBAR，以便在多個監視器的情況下使用。
title: 'ABM_SETAUTOHIDEBAREX 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104992455"
---
# <a name="abm_setautohidebarex-message"></a>ABM \_ SETAUTOHIDEBAREX 訊息

註冊或取消註冊螢幕指定邊緣的自動隱藏 appbar。 此訊息可讓您指定特定的監視，以擴充 [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) ，以便在多個監視器的情況下使用。


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。 將 **lParam** 成員設為 **TRUE** 以註冊 appbar 或 **FALSE** 將其取消註冊。 傳送此訊息時，您必須指定 **cbSize**、 **hWnd**、 **uEdge**、 **rc** 和 **lParam** 成員;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果發生錯誤，或如果已在指定的監視器上為指定的邊緣註冊自動隱藏 appbar，則傳回 **FALSE** 。

## <a name="remarks"></a>備註

系統只允許每個監視器的每個邊緣都有一個自動隱藏 appbar。 此監視器取決於 **rc** 成員，而邊緣是由 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的 **uEdge** 成員所決定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Shellapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> </dl>

 

 




