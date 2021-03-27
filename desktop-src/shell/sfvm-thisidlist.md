---
description: SFVM \_ THISIDLIST 可能已變更或無法使用。
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: 'SFVM_THISIDLIST 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695439"
---
# <a name="sfvm_thisidlist-message"></a>SFVM \_ THISIDLIST 訊息

\[**SFVM \_THISIDLIST** 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

允許回呼物件指定 (PIDL) 之專案識別碼清單的視圖指標。 只有當 [**IPersistIDList：： SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) 和 [**IPersistFolder2：： GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) 失敗時，才會使用這個。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*pidl* \[擴展\]
</dt> <dd>

視圖 PIDL 的位址。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 用戶端支援結束<br/>    | Windows XP 含 SP2<br/>                                                      |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
