---
description: 閱讀 ItemFolderPathDisplay 屬性，其代表專案之父資料夾的使用者易記顯示路徑。
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12909b29790ea2c016154cea9fccf7c53e45630
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403931"
---
# <a name="systemitemfolderpathdisplay"></a>System. ItemFolderPathDisplay

專案之父資料夾的使用者易記顯示路徑。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

如果 [ItemPathDisplay](./props-system-itempathdisplay.md) 是 VT \_ 空白，則此屬性也應為空白。 否則，應該由 ItemPathDisplay 中的資料來源適當地衍生。

範例值：



| 路徑                                   | ItemFolderPathDisplay    |
|----------------------------------------|--------------------------|
| c： \\ files \\ personal \\hello.txt         | c： \\ \\ 個人檔案      |
| \\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc | \\\\伺服器 \\ 共用 \\ mydir |
| \\\\伺服器 \\ 共用 \\numbers.xls         | \\\\伺服器 \\ 共用        |
| c： \\ 食物 \\ MyFolder                     | c： \\ 食物                 |
| /Mailbox 帳戶/收件匣/' Re： Hello！ '    | /Mailbox 帳戶/收件匣   |



 

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

 

 
