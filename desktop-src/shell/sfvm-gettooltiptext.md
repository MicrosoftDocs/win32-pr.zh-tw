---
description: 允許回呼物件指定功能表項目或工具列按鈕的工具提示文字字串。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: 'SFVM_GETTOOLTIPTEXT 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3350d1f772cd78c97f7b57b47084c761808583dfe5396fafcdad336291a3a717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858220"
---
# <a name="sfvm_gettooltiptext-message"></a>SFVM \_ GETTOOLTIPTEXT 訊息

允許回呼物件指定功能表項目或工具列按鈕的工具提示文字字串。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

中的 *idCmd \_ cchMax* \[\]
</dt> <dd>

此參數的低序位字組會保存命令識別碼。 高序位單字會保存 *pszText* 緩衝區中的字元數。

</dd> <dt>

*pszText* \[擴展\]
</dt> <dd>

包含解說文字且以 null 終止的字串。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
