---
description: 通知容器網站的回呼物件。 只有當不支援 IObjectWithSite：： SetSite 且使用 SHCreateShellFolderViewEx 時，才會使用這個。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: 'SFVM_SETISFV 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d9ad3e9b1b8302089da8a59a8d5502a04392da77c6fc5276725b144efa026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660798"
---
# <a name="sfvm_setisfv-message"></a>SFVM \_ SETISFV 訊息

\[這項通知是透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 支援。 Windows 的後續版本中可能不支援此功能。\]

通知容器網站的回呼物件。 只有當不支援 [**IObjectWithSite：： SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) 且使用 [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) 時，才會使用這個。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*網站* \[在\]
</dt> <dd>

容器網站的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
