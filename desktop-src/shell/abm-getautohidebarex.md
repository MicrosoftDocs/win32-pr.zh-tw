---
description: 抓取與螢幕邊緣相關聯的自動隱藏 appbar 控制碼。 此訊息可 \_ 讓您指定特定的監視，以擴充 ABM GETAUTOHIDEBAR，以便在多個監視器的情況下使用。
title: 'ABM_GETAUTOHIDEBAREX 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9aecbc81e313c3d971b310cc35bd399b93cc18f2ef2a4f02a00d51a16745eb61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225237"
---
# <a name="abm_getautohidebarex-message"></a>ABM \_ GETAUTOHIDEBAREX 訊息

抓取與螢幕邊緣相關聯的自動隱藏 appbar 控制碼。 此訊息可讓您指定特定的監視，以擴充 [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) ，以便在多個監視器的情況下使用。


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標，指定螢幕邊緣和監視器。 傳送此訊息時，您必須指定 **cbSize**、 **uEdge** 和 **rc** 成員;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

將控制碼傳回到自動隱藏 appbar。 如果發生錯誤，或沒有自動隱藏 appbar 與指定監視器的指定邊緣相關聯，則傳回值為 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Shellapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




