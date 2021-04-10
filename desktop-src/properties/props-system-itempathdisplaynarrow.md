---
description: 專案的使用者易記顯示路徑。
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194264"
---
# <a name="systemitempathdisplaynarrow"></a>System. ItemPathDisplayNarrow

專案的使用者易記顯示路徑。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

若要針對窄的視圖資料行進行優化，必須量身打造字串的格式，以便先取得名稱。

如果專案是檔案，則屬性值會排除副檔名，但會包含當地語系化名稱（如果有的話）。 如果專案是訊息，此值會包含 [ItemNamePrefix](./props-system-itemnameprefix.md)。 若要剖析專案路徑，請使用 [ItemUrl](./props-system-itemurl.md) 或 [ParsingPath](./props-system-parsingpath.md)。

範例值：



| 路徑                                   | ItemPathDisplayName                 |
|----------------------------------------|-------------------------------------|
| c： \\ mydir \\ bar \\hello.txt              | hello (c： \\ mydir \\ bar)               |
| \\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc | goodnews (\\ \\ server \\ share \\ mydir)  |
| \\\\伺服器 \\ 共用 \\ 資料夾              |  (\\ \\ server \\ 共用) 資料夾          |
| c： \\ MyDir \\ MyFolder                    | MyFolder (c： \\ mydir)                 |
| /Mailbox 帳戶/收件匣/' Re： Hello！ '    | Re：您好！  (/Mailbox 帳戶/收件匣)  |



 

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

 

 
