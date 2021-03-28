---
description: 將目前所選物件的點設定為複製和剪下命令上的資料物件。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_SETPOINTS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195327"
---
# <a name="sfvm_setpoints-message"></a>SFVM \_ SETPOINTS 訊息

將目前所選物件的點設定為 **複製** 和 **剪** 下命令上的資料物件。 由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdtobj* \[在\]
</dt> <dd>**複製** 和 **剪** 下命令之 <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a>的指標。</dd> </dl>

## <a name="return-value"></a>傳回值

永遠傳回零。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
