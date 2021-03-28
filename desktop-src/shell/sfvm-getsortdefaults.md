---
description: 允許回呼物件指定預設排序參數。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_GETSORTDEFAULTS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973813"
---
# <a name="sfvm_getsortdefaults-message"></a>SFVM \_ GETSORTDEFAULTS 訊息

允許回呼物件指定預設排序參數。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*iDirection* \[擴展\]
</dt> <dd>

預設的排序方向。 將此參數設定為正數值，以遞增順序排序。 將此參數設定為零或負數值，以遞減順序排序。

</dd> <dt>

*iColumn* \[擴展\]
</dt> <dd>

用於排序的資料行。 這會在其 *lParam* 值的較低16位中傳遞給 [**IShellFolder：： CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) 。

</dd> </dl>

## <a name="remarks"></a>備註

> [!Note]  
> ：系統資料夾 view 物件無法辨識 **SFVM \_ GETSORTDEFAULTS** 。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
