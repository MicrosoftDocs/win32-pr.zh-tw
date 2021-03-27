---
description: 針對所有選取的物件，抓取專案識別碼清單的指標陣列 (Pidl) 。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_GETSELECTEDOBJECTS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9639fbb6-d0ef-49b1-b3c5-e6a1dee0b7ad
api_name:
- SFVM_GETSELECTEDOBJECTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 056a9bd6bea78ef5093f6654b9935eb90e3759ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852580"
---
# <a name="sfvm_getselectedobjects-message"></a>SFVM \_ GETSELECTEDOBJECTS 訊息

針對所有選取的物件，抓取專案識別碼清單的指標陣列 (Pidl) 。 由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。


```C++
SFVM_GETSELECTEDOBJECTS 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppidl* \[擴展\]
</dt> <dd>目前所選物件之 Pidl 陣列的位址。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回陣列中的專案數。

## <a name="remarks"></a>備註

完成時，您應該在陣列的每個成員上呼叫 [**ILFree**](/windows/desktop/api/shlobj_core/nf-shlobj_core-ilfree) ，以釋放記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 




