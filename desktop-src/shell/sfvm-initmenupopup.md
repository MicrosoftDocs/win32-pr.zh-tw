---
description: 允許回呼物件在顯示 Windows 檔案總管快顯功能表之前加以修改。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_INITMENUPOPUP 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: fd69d19f753c1c72c1e0c143a0aface2cdb234cb2ace8c87d559834b97bbf0f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592314"
---
# <a name="sfvm_initmenupopup-message"></a>SFVM \_ INITMENUPOPUP 訊息

允許回呼物件在顯示 Windows 檔案總管快顯功能表之前加以修改。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

中的 *idCmd \_ nIndex* \[\]
</dt> <dd>

此參數的低序位字組會保留為用戶端命令保留的第一個命令識別碼的值。 高序位單字會保存功能表的索引。

</dd> <dt>

*hmenu* \[in、out\]
</dt> <dd>

功能表的控制碼。

</dd> </dl>

## <a name="remarks"></a>備註

當您選取功能表時，但在顯示之前，系統資料夾 view 物件會傳送此訊息。 舉例來說，如果您需要啟用或停用功能表命令，請處理此訊息。 快顯功能表可以是：

-   [檔案]、[編輯] 或 [流覽] 功能表。
-   用戶端所定義的最上層功能表。
-   用戶端定義的子功能表。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SFVM \_ MERGEMENU**](sfvm-mergemenu.md)
</dt> </dl>

 

 
