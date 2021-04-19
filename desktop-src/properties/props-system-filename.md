---
description: 檔案名，包括副檔名。
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System.string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991856"
---
# <a name="systemfilename"></a>System.string

檔案名，包括副檔名。 FileExtension 衍生自這個屬性。

專案可能不存在於檔案系統上 (也可能無法使用 CreateFile) 開啟。 但是，如果專案是以檔案表示，且其名稱遵循標準 Win32 檔案命名語法，則資料來源應該發出這個屬性。 如果專案不是檔案，則資料來源應該將此屬性發出為 VT \_ 空白。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

專案可能不存在於檔案系統上 (也就是說，它可能不會使用 CreateFile) 開啟，但如果專案是以邏輯意義的檔案表示，而且其名稱遵循標準 Win32 檔案命名語法，則資料來源應該發出這個屬性。 如果專案不是檔案，則此屬性的值為 VT \_ 空白。 請參閱 ItemNameDisplay。 針對 Shell 的檔案資料夾所提供的專案，其值與 ParsingName 相同。

下表列出 [路徑] 和 [檔案名] 屬性值的範例：



| 路徑                               | 屬性值 |
|------------------------------------|----------------|
| c： \\ files \\ personal \\hello.txt     | hello.txt      |
| \\\\伺服器 \\ 共用 \\ mydir \\news.doc | news.doc       |
| \\\\伺服器 \\ 共用 \\numbers.xls     | numbers.xls    |
| c： \\ 東西 \\ MyFolder                | MyFolder       |
| \[電子郵件訊息\]                  | VT \_ 空白      |
| \[song. 可攜式裝置上的 wma\]    | song       |



 

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

 

 
