---
description: System. OfflineAvailability
ms.assetid: 4d0c880b-923d-4f83-91da-dd99bf111f13
title: System. OfflineAvailability
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceeefaf33acfc07bba2d552761ecd418257e8485
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090016"
---
# <a name="systemofflineavailability"></a>System. OfflineAvailability

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、1507版、Windows 8。1

```
propertyDescription
   name = System.OfflineAvailability
   shellPKey = PKEY_OfflineAvailability
   formatID = A94688B6-7D9F-4570-A648-E3DFC0AB2B3F
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailable
            value = 0
            text = Online-only
            defineToken = OFFLINEAVAILABILITY_NOT_AVAILABLE
         enum
            name = Available
            value = 1
            text = Available
            defineToken = OFFLINEAVAILABILITY_AVAILABLE
         enum
            name = AlwaysAvailable
            value = 2
            text = Available offline
            defineToken = OFFLINEAVAILABILITY_ALWAYS_AVAILABLE
```

## <a name="windows-8-windows-7"></a>Windows 8，Windows 7

```
propertyDescription
   name = System.OfflineAvailability
   shellPKey = PKEY_OfflineAvailability
   formatID = A94688B6-7D9F-4570-A648-E3DFC0AB2B3F
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotAvailable
            value = 0
            text = Not available
            defineToken = OFFLINEAVAILABILITY_NOT_AVAILABLE
         enum
            name = Available
            value = 1
            text = Available
            defineToken = OFFLINEAVAILABILITY_AVAILABLE
         enum
            name = AlwaysAvailable
            value = 2
            text = Always available
            defineToken = OFFLINEAVAILABILITY_ALWAYS_AVAILABLE
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.OfflineAvailability
   shellPKey = PKEY_OfflineAvailability
   formatID = A94688B6-7D9F-4570-A648-E3DFC0AB2B3F
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Not available
            defineName = OFFLINEAVAILABILITY_NOT_AVAILABLE
         enum
            value = 1
            text = Available
            defineName = OFFLINEAVAILABILITY_AVAILABLE
         enum
            value = 2
            text = Always available
            defineName = OFFLINEAVAILABILITY_ALWAYS_AVAILABLE
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

 

 
