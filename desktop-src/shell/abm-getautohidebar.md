---
description: 抓取與螢幕邊緣相關聯的自動隱藏 appbar 控制碼。 如果系統有多個監視器，則會使用包含主要工作列的監視器。
title: 'ABM_GETAUTOHIDEBAR 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112364"
---
# <a name="abm_getautohidebar-message"></a>ABM \_ GETAUTOHIDEBAR 訊息

抓取與螢幕邊緣相關聯的自動隱藏 appbar 控制碼。 如果系統有多個監視器，則會使用包含主要工作列的監視器。

> [!Note]  
> 若要查詢特定監視器上的自動隱藏 appbar，請使用 [**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)。

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

指定螢幕邊緣之 [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) 結構的指標。 傳送此訊息時，您必須指定 **cbSize** 和 **uEdge** 成員;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

將控制碼傳回到自動隱藏 appbar。 如果發生錯誤，或如果沒有自動隱藏 appbar 與指定的邊緣相關聯，則傳回值為 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md)
</dt> <dt>

[**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md)
</dt> <dt>

[**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md)
</dt> </dl>

 

 




