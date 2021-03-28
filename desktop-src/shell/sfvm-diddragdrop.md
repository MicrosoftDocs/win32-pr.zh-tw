---
description: SFVM \_ DIDDRAGDROP 可能已變更或無法使用。
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: 'SFVM_DIDDRAGDROP 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991682"
---
# <a name="sfvm_diddragdrop-message"></a>SFVM \_ DIDDRAGDROP 訊息

\[**SFVM \_DIDDRAGDROP** 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。\]

通知回呼函式已開始拖放作業。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwEffect* \[在\]
</dt> <dd>

來自 [**DROPEFFECT**](../com/dropeffect-constants.md) 列舉的 drop 效果規範。 這是藉由呼叫 [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop)來取得。

</dd> <dt>

*pIdo* \[在\]
</dt> <dd>

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)實例的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                |
| 用戶端支援結束<br/>    | Windows XP 含 SP2<br/>                                                      |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
