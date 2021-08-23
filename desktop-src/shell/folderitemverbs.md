---
description: 表示 Shell 資料夾中專案的動詞集合。 此物件包含屬性和方法，可讓您取得集合的相關資訊。
title: 'FolderItemVerbs 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 31badb4b-b89e-4294-9dd7-bda716e163b2
ms.openlocfilehash: a710f8a1362ea54e98d76056b3b911ef4882cf522d200626e3479baf6d770af9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593258"
---
# <a name="folderitemverbs-object"></a>FolderItemVerbs 物件

表示 Shell 資料夾中專案的動詞集合。 此物件包含屬性和方法，可讓您取得集合的相關資訊。

## <a name="members"></a>成員

**FolderItemVerbs** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**FolderItemVerbs** 物件有這些方法。



| 方法                                        | 描述                                                                                                      |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitemverbs--newenum.md) | 建立並傳回新的 **FolderItemVerbs** 物件，該物件為這個 FolderItemVerbs 物件的複本。<br/>   |
| [**項目**](folderitemverbs-item.md)          | 抓取集合中指定之專案的 [**FolderItemVerb**](folderitemverb.md) 物件。<br/> |



 

### <a name="properties"></a>屬性

**FolderItemVerbs** 物件具有這些屬性。



| 屬性                                                      | 存取類型          | 描述                                                |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Application**](folderitemverbs-application.md)<br/> | 唯讀<br/> | 未實作。<br/>                                |
| [**計數**](folderitemverbs-count.md)<br/>             | 唯讀<br/> | 包含集合中的專案數。<br/> |
| [**父代**](folderitemverbs-parent.md)<br/>           | 唯讀<br/> | 未實作。<br/>                                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 




