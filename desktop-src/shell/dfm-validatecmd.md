---
description: 傳送以確認功能表命令是否存在。
title: 'DFM_VALIDATECMD 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fd647d5cd6e171cc71e0968abb29d80e7aef5900d43fe4bd4b88f5f49bbdc7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721944"
---
# <a name="dfm_validatecmd-message"></a>DFM \_ VALIDATECMD 訊息

傳送以確認功能表命令是否存在。


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*idCmd* 
</dt> <dd>功能表命令識別碼位移。</dd> <dt>

*lParam* 
</dt> <dd>未使用。 必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果命令存在，則傳回 s OK， \_ 否則傳回 FALSE。

## <a name="remarks"></a>備註

這則訊息會根據預設內容功能表物件的建立方式，傳送至回呼函式或回呼物件。 有兩個 Api 適用于其結構： [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。

[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。 如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 




