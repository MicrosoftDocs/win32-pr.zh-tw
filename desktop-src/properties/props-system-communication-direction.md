---
description: 指出通訊是否為傳入或傳出。
ms.assetid: b41f185b-f8b3-433b-9aed-8e71d59e4602
title: 系統。方向
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ed91eb7d6b771dcddd99aeff7aa249e9bc4bfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983412"
---
# <a name="systemcommunicationdirection"></a>系統。方向

指出通訊是否為傳入或傳出

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507"></a>Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、1507版

```
propertyDescription
   name = System.Communication.Direction
   shellPKey = PKEY_Communication_Direction
   formatID = 8E531030-B960-4346-AE0D-66BC9A86FB94
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Unknown
            value = 0
            text = Unknown
            defineToken = COMMUNICATION_DIRECTION_UNKNOWN
         enum
            name = Incoming
            value = 1
            text = Incoming
            defineToken = COMMUNICATION_DIRECTION_INCOMING
         enum
            name = Outgoing
            value = 2
            text = Outgoing
            defineToken = COMMUNICATION_DIRECTION_OUTGOING
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

 

 
