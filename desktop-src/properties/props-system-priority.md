---
description: System. Priority
ms.assetid: 43f81cb5-7f2e-4f8f-ad31-8aad71765f60
title: System. Priority
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66e6930c9746d61f181c88076d10677d5cfdd787
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091746"
---
# <a name="systempriority"></a>System. Priority

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.Priority
   shellPKey = PKEY_Priority
   formatID = 9C1FCF74-2D97-41BA-B4AE-CB2E3661A6E4
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Low
            value = 0
            text = Low
            defineToken = PRIORITY_PROP_LOW
         enum
            name = Normal
            value = 1
            text = Normal
            defineToken = PRIORITY_PROP_NORMAL
         enum
            name = High
            value = 2
            text = High
            defineToken = PRIORITY_PROP_HIGH
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Priority
   shellPKey = PKEY_Priority
   formatID = 9C1FCF74-2D97-41BA-B4AE-CB2E3661A6E4
   propID = 5
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Low
            defineName = PRIORITY_PROP_LOW
         enum
            value = 1
            text = Normal
            defineName = PRIORITY_PROP_NORMAL
         enum
            value = 2
            text = High
            defineName = PRIORITY_PROP_HIGH
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

 

 
