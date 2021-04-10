---
description: 專案的使用者易記顯示路徑。
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115457"
---
# <a name="systemitempathdisplay"></a>System. ItemPathDisplay

專案的使用者易記顯示路徑。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

如果專案是檔案或資料夾，則這個屬性會在所有情況下都包含副檔名，而且如果有可用的當地語系化名稱，則會當地語系化。 如果是其他專案，這會是相當方便使用的專案，前提是該專案存在於階層式儲存體中。

不同于 [ItemUrl](./props-system-itemurl.md)，此屬性值不包含 URL 配置。 若要剖析專案路徑，請使用 ItemUrl 或 [ParsingPath](./props-system-parsingpath.md)。 若要使用 Shell Api 參考 Shell 命名空間專案，請使用 ParsingPath。

範例值：



| 路徑                                   | ItemPathDisplay                        |
|----------------------------------------|----------------------------------------|
| c： \\ mydir \\ bar \\hello.txt              | c： \\ mydir \\ bar \\hello.txt              |
| \\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc | \\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc |
| \\\\伺服器 \\ 共用 \\numbers.xls         | \\\\伺服器 \\ 共用 \\numbers.xls         |
| c： \\ mydir \\ MyFolder                    | c： \\ mydir \\ MyFolder                    |
| /Mailbox 帳戶/收件匣/' Re： Hello！ '    | /Mailbox 帳戶/收件匣/' Re： Hello！ '    |



 

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

 

 
