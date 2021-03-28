---
description: 允許回呼物件將按鈕加入至工具列。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_GETBUTTONINFO 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973485"
---
# <a name="sfvm_getbuttoninfo-message"></a>SFVM \_ GETBUTTONINFO 訊息

允許回呼物件將按鈕加入至工具列。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*ptbinfo* \[擴展\]
</dt> <dd>

[**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo)結構的位址，指定按鈕數目以及如何將其加入工具列。

</dd> </dl>

## <a name="remarks"></a>備註

您可以在標準系統資料夾 view 物件按鈕上附加或顯示按鈕，或顯示這些按鈕來取代標準按鈕。 此訊息後面會接著 [**SFVM \_ GETBUTTONS**](sfvm-getbuttons.md) 訊息，以抓取有關按鈕細節的資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
