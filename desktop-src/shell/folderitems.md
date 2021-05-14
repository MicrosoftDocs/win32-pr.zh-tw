---
description: 表示 Shell 資料夾中的專案集合。 此物件包含屬性和方法，可讓您取得集合的相關資訊。
title: 'FolderItems 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840649"
---
# <a name="folderitems-object"></a>FolderItems 物件

表示 Shell 資料夾中的專案集合。 此物件包含屬性和方法，可讓您取得集合的相關資訊。

## <a name="members"></a>成員

**FolderItems** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**FolderItems** 物件有這些方法。



| 方法                                    | 描述                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitems--newenum.md) | 未實作。<br/>                                                                              |
| [**項目**](folderitems-item.md)          | 抓取集合中指定之專案的 [**FolderItem**](folderitem.md) 物件。<br/> |



 

### <a name="properties"></a>屬性

**FolderItems** 物件具有這些屬性。



| 屬性                                                  | 存取類型          | 描述                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitems-application.md)<br/> | 唯讀<br/> | 包含資料夾專案集合的 [**應用程式**](folderitems-application.md) 物件。<br/> |
| [**計數**](folderitems-count.md)<br/>             | 唯讀<br/> | 包含集合中的專案數。<br/>                                                    |
| [**父代**](folderitems-parent.md)<br/>           | 唯讀<br/> | 未實作。<br/>                                                                                   |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 




