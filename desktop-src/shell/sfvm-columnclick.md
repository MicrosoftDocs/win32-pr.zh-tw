---
description: 通知回呼物件，使用者已按一下資料行標頭，以排序資料夾檢視中的物件清單。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_COLUMNCLICK 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469344"
---
# <a name="sfvm_columnclick-message"></a>SFVM \_ COLUMNCLICK 訊息

通知回呼物件，使用者已按一下資料行標頭，以排序資料夾檢視中的物件清單。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*iColumn* \[在\]
</dt> <dd>

已按下之資料行的索引。

</dd> </dl>

## <a name="remarks"></a>備註

為了回應這項通知，您應該傳回 \_ [確定] 以自行重新排列清單。 若要讓系統資料夾 view 物件重新排列清單，請傳回 \_ FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
