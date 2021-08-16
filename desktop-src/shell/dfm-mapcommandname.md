---
description: 由預設內容功能表執行所傳送，以將名稱指派給功能表命令。
title: 'DFM_MAPCOMMANDNAME 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8aa764f7-d5d4-4a84-94d2-993265e1eb5a
api_name:
- DFM_MAPCOMMANDNAME
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e3dac1cdb3c04397a59b26a2212fe1c46b611ce72ba029aabd25e0b01c9000b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459974"
---
# <a name="dfm_mapcommandname-message"></a>DFM \_ MAPCOMMANDNAME 訊息

由預設內容功能表執行所傳送，以將名稱指派給功能表命令。


```C++
DFM_MAPCOMMANDNAME

    lParam = (LPARAM)(int*) defaultID;

    wparam = (WPARAM)(LPTSTR) pszCommandName;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*defaultID* \[in、out\]
</dt> <dd>

所選功能表命令的識別碼指標。

</dd> <dt>

*pszCommandName* \[在\]
</dt> <dd>

Unicode 字串的指標，其中包含命令的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

這則訊息會傳送至回呼函式或回呼物件（根據預設的內容功能表物件的執行方式而定）。 有兩個 Api 適用于其實 [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。

[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。 如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 




