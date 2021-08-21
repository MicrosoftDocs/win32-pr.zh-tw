---
description: 專案的使用者易記型別名稱。
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f145aa2491f3352c4691be95c0e8ae16a75e8e0880732904e983fbf02c167dbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553748"
---
# <a name="systemitemtypetext"></a>System. ItemTypeText

專案的使用者易記型別名稱。 此值不能以程式設計方式剖析。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8、Windows 7、Windows Vista

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

如果 [system.object](./props-system-itemtype.md) 是 vt \_ 空白，則這個屬性的值也是 vt \_ 空白。 如果專案是檔案，這個屬性的值就會與您將檔案的 system.string 值傳遞給 [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)時相同。

這個屬性不應該與 [system.object](./props-system-kind.md)混淆，因為這是高階、使用者易記的種類名稱。 例如，在 .doc 檔檔中，不同的屬性如下所示：



| 屬性                                               | 值                   |
|--------------------------------------------------------|-------------------------|
| [System.string](./props-system-kind.md)                 | 文件                |
| [System.servicemodel](./props-system-itemtype.md)         | .doc                    |
| [System. ItemTypeText]() | Microsoft Word文檔 |



 

範例值：



| 路徑                                   | ItemTypeText            |
|----------------------------------------|-------------------------|
| c： \\ mydir \\ bar \\hello.txt              | 文字檔               |
| \\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc | Microsoft Word文檔 |
| \\\\伺服器 \\ 共用 \\ 資料夾              | 檔案資料夾             |
| c： \\ MyDir \\ MyFolder                    | 檔案資料夾             |
| /Mailbox 帳戶/收件匣/' Re： Hello！ '    | Outlook電子郵件  |



 

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

 

 
