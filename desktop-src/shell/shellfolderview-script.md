---
description: 包含此視圖的腳本物件。
ms.assetid: 63a4e42f-3d24-493f-8801-fc09a7477401
title: 'ShellFolderView： Script 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Script
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86926f2013dd78c2c6685163ae78f890c337a251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194435"
---
# <a name="shellfolderviewscript-property"></a>ShellFolderView。 Script 屬性

\[Windows XP 或更新版本不支援這個屬性。\]

包含此視圖的腳本物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
objScript = ShellFolderView.Script
```



## <a name="property-value"></a>屬性值

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，它會接收腳本物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 
