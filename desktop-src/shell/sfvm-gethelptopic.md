---
description: 允許回呼物件指定 HTML 說明檔及其內的主題。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_GETHELPTOPIC 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850663"
---
# <a name="sfvm_gethelptopic-message"></a>SFVM \_ GETHELPTOPIC 訊息

允許回呼物件指定 HTML 說明檔及其內的主題。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*phtd* \[擴展\]
</dt> <dd>

[**SFVM \_ HELPTOPIC \_ 資料**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data)結構的位址，指定 HTML 說明檔和主題。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
