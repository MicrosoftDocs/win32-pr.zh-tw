---
description: 瞭解 DestLongitude 屬性如何表示目的地點的經度。
ms.assetid: 72a3fb10-4554-4a4d-bb73-ee515341b9c1
title: DestLongitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e7b3482a5e632f774f500bcfe254667c120a3b5ea653c3725a354cbf95025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117866401"
---
# <a name="systemgpsdestlongitude"></a>DestLongitude

表示目的地點的緯度。 這是三個值的陣列，如下所示：索引0是度數，索引1是分鐘，索引2是秒。 每個都是從 PKEY \_ gps \_ DESTLONGITUDENUMERATOR 和 PKEY \_ gps DestLongitudeDenominator 中的值計算而來 \_ 。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8、Windows 7、Windows Vista

```
propertyDescription
   name = System.GPS.DestLongitude
   shellPKey = PKEY_GPS_DestLongitude
   formatID = 47A96261-CB4C-4807-8AD3-40B9D9DBC6BC
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
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

 

 
