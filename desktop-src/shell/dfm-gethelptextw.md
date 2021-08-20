---
description: DFM_GETHELPTEXTW 訊息-可讓回呼物件指定解說文字字串。
title: 'DFM_GETHELPTEXTW 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6a7a5c47fcdb81accf4c2370aa14fa5f477be50b718b326631b20847db528151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860923"
---
# <a name="dfm_gethelptextw-message"></a>DFM \_ GETHELPTEXTW 訊息

允許回呼物件指定解說文字字串。


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

中的 *idCmd \_ cchMax* \[\]
</dt> <dd>

此參數的低序位字組會保存命令識別碼。 高序位單字會保存 *pszText* 緩衝區中的字元數。

</dd> <dt>

*pszText* \[擴展\]
</dt> <dd>

包含解說文字且以 null 終止的 Unicode 字串。

</dd> </dl>

## <a name="remarks"></a>備註

這則訊息會根據預設內容功能表物件的建立方式，傳送至回呼函式或回呼物件。 有兩個 Api 適用于其結構： [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。

[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。 如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **DFM \_GETHELPTEXTW** (Unicode) <br/>                                          |



 

 




