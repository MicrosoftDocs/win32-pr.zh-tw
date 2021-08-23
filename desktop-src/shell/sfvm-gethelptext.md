---
description: 允許回呼物件指定功能表項目或工具列按鈕的解說文字字串。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_GETHELPTEXT 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c015c1999cbd60174da1994d92766b4f334630294767ee390be21340aef97cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661018"
---
# <a name="sfvm_gethelptext-message"></a>SFVM \_ GETHELPTEXT 訊息

允許回呼物件指定功能表項目或工具列按鈕的解說文字字串。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_GETHELPTEXT 

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



 

 
