---
description: 這個屬性類似于 ItemNameDisplay，但它只會針對資料夾進行設定，而檔案將會是空的。
ms.assetid: 4517a4bf-3cc1-4835-b21b-03de5b33db0c
title: System. FolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60922054e80a6589bcb04c3962a4527ee62eaf7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980353"
---
# <a name="systemfoldernamedisplay"></a>System. FolderNameDisplay

這個屬性類似于 ItemNameDisplay，但它只會針對資料夾進行設定，而檔案將會是空的。 使用這個做為第一個排序索引鍵來分隔檔案和資料夾，這會很有用。 當使用 ItemDate 做為第二個排序索引鍵時，它會產生第一個依名稱排序的資料夾結果，然後依日期排序的檔案。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、1507版、Windows 8。1

```
propertyDescription
   name = System.FolderNameDisplay
   shellPKey = PKEY_FolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 25
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[>cultureinfo.numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
