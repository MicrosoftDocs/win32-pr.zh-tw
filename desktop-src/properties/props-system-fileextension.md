---
description: 識別以檔案為基礎之專案的副檔名，包括前置句點。
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983470"
---
# <a name="systemfileextension"></a>System. FileExtension

識別以檔案為基礎之專案的副檔名，包括前置句點。 這個屬性是衍生自 System.object。 如果 system.string 沒有副檔名或 VT \_ 空白，則此屬性的值應該是 vt \_ 空白。

若要取得任何專案的類型 (包括非檔案) 的專案，請使用 system.servicemodel。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

如果 [system.string](./props-system-filename.md) 是 VT \_ 空白，這個屬性也應該是空的。 否則，這個屬性應該由 system.string 中的資料來源適當地衍生。 如果 system.string 不包含副檔名， [FileExtension]() 應該是 VT \_ 空白。 若要取得任何專案的類型 (包括非檔案) 的專案，[請使用 system.servicemodel。](./props-system-itemtype.md)

路徑和副檔名屬性範例。 

| 路徑                               | 副檔名 |
|------------------------------------|----------------|
| c： \\ files \\ personal \\hello.txt     | .txt           |
| \\\\伺服器 \\ 共用 \\ mydir \\news.doc | .doc           |
| \\\\伺服器 \\ 共用 \\numbers.xls     | .xls           |
| \\\\伺服器 \\ 共用 \\ 資料夾          | VT \_ 空白      |
| c： \\ 東西 \\ MyFolder                | VT \_ 空白      |
| \[desktop\]                        | VT \_ 空白      |



 

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

 

 
