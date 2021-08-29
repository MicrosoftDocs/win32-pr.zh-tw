---
description: 擴充 FolderItem 物件。 除了 FolderItem 支援的屬性和方法之外，ShellFolderItem 還有兩個額外的方法。
title: 'ShellFolderItem 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: 509a05a0c83918d969bc1d165289395b6fcb61c6ef0f1283350f3d1bf121b792
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676700"
---
# <a name="shellfolderitem-object"></a>ShellFolderItem 物件

擴充 [**FolderItem**](folderitem.md) 物件。 除了 **FolderItem** 支援的屬性和方法之外， **ShellFolderItem** 還有兩個額外的方法。

## <a name="members"></a>成員

**ShellFolderItem** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ShellFolderItem** 物件有這些方法。



| 方法                                                       | 描述                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExtendedProperty**](shellfolderitem-extendedproperty.md) | 從專案的屬性集取得屬性的值。 屬性可以依照名稱或屬性集的格式識別碼來指定 (FMTID) 和屬性識別碼 (PID) 。<br/> |
| [**InvokeVerbEx**](invokeverbex.md)                         | 在 Shell 專案上執行動詞命令。<br/>                                                                                                                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



 

 




