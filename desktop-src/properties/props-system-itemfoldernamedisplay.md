---
description: 專案之父資料夾的使用者易記顯示名稱。
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193740"
---
# <a name="systemitemfoldernamedisplay"></a>System. ItemFolderNameDisplay

專案之父資料夾的使用者易記顯示名稱。

這是衍生自 [ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md)。 如果該屬性為 VT \_ 空白，則此屬性應該也是。

如果資料夾是檔案資料夾，則如果有可用的當地語系化名稱，此值就會當地語系化。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

如果 [ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) 是 VT \_ 空白，則此屬性也應為空白。 否則，應該由 ItemFolderPathDisplay 中的資料來源適當地衍生。

範例：



| 指定的路徑                             | 資料夾顯示名稱 |
|----------------------------------------|---------------------|
| c： \\ MyFiles \\ 文字 \\hello.txt           | Text                |
| \\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc | mydir               |
| \\\\伺服器 \\ 共用 \\numbers.xls         | 分享               |
| c： \\ 資料夾 \\ MyFolder                  | 資料夾             |
| /Mailbox 帳戶/收件匣/' Re： Hello！ '    | Inbox               |



 

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

 

 
