---
description: 將指定之 ShellFolderView 物件的事件轉送至對應的 ShellFolderViewOC 事件處理常式。
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: 'ShellFolderViewOC. SetFolderView 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973584"
---
# <a name="shellfolderviewocsetfolderview-method"></a>ShellFolderViewOC. SetFolderView 方法

將指定之 [**ShellFolderView**](shellfolderview.md) 物件的事件轉送至對應的 [**ShellFolderViewOC**](shellfolderviewoc-object.md) 事件處理常式。

## <a name="syntax"></a>語法


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*oShellFolderView* \[在\]
</dt> <dd>

類型： **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _

[_ *ShellFolderView* *](shellfolderview.md)物件。 它的 [**EnumDone**](shellfolderviewoc-enumdone.md) 和 [**SelectionChanged**](shellfolderview-selectionchanged.md) 事件將會轉送到對應的 [**ShellFolderViewOC**](shellfolderviewoc-object.md) 事件處理常式。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 
