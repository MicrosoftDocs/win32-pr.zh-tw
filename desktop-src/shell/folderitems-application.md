---
description: 包含資料夾專案集合的應用程式物件。
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: 'FolderItems： Application 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3809d76576b69c53f6fc5f8a11ab954242e3a89c9a369ada2f4fa47c460f523f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032606"
---
# <a name="folderitemsapplication-property"></a>FolderItems。應用程式屬性

包含資料夾專案集合的 **應用程式** 物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a>屬性值

應用程式物件的物件參考。

## <a name="remarks"></a>備註

如果可以存取該物件， **應用程式** 屬性會傳回包含 WebBrowser 控制項之應用程式所支援的 automation 物件。 否則，此屬性會傳回 WebBrowser 控制項的 automation 物件。

使用這個屬性搭配 **Set** 和 **CreateObject** 命令，或使用 **GetObject** 命令來建立和操作 Windows Internet Explorer 應用程式的實例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 




