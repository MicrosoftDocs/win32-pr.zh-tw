---
description: 允許回呼物件提供要加入所選取物件之屬性工作表中的頁面。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_ADDPROPERTYPAGES 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991666"
---
# <a name="sfvm_addpropertypages-message"></a>SFVM \_ ADDPROPERTYPAGES 訊息

允許回呼物件提供要加入所選取物件之 **屬性** 表中的頁面。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*.pdata* \[擴展\]
</dt> <dd>

[**SFVM \_ PROPPAGE \_ 資料**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data)結構的位址。

</dd> </dl>

## <a name="remarks"></a>備註

此訊息基本上與 [**IShellPropSheetExt：： AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)有相同的功能。 如需進一步討論，請參閱 [建立屬性工作表處理常式](propsheet-handlers.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
