---
description: 藉由將指標指向 (Pidl) 的專案識別碼清單，將指標傳遞至兩個指標的陣列，以更新物件。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_UPDATEOBJECT 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e3c4ee64583710e84af0d377999c389f6fe1bfa6876bb150789a5fd118f79f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452841"
---
# <a name="sfvm_updateobject-message"></a>SFVM \_ UPDATEOBJECT 訊息

藉由將指標指向 (Pidl) 的專案識別碼清單，將指標傳遞至兩個指標的陣列，以更新物件。 由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppidl* \[在\]
</dt> <dd>

兩個 Pidl 陣列的位址。 第一個 PIDL 是舊的 PIDL。 第二個是舊 PIDL 的複本，其中包含更新的資訊。 成功完成此呼叫後，對複製的存留期的控制權會屬於 view。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果更新成功，則傳回已更新物件的 listview 識別碼;否則，它會傳回-1。

## <a name="remarks"></a>備註

如果更新失敗，則呼叫端必須釋放記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 




