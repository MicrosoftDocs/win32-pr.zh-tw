---
description: 瞭解 DestLatitude 屬性如何表示目的地點的緯度。
ms.assetid: 63d8a3a3-76ec-4121-b48b-eb5034117d04
title: DestLatitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ff03532d4f377eb0b8d890c88a2dca5f7b17911132faae7a0b9b5cae806e39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119096857"
---
# <a name="systemgpsdestlatitude"></a>DestLatitude

表示目的地點的緯度。 這是三個值的陣列，如下所示：索引0是度數，索引1是分鐘，索引2是秒。 每個都是從 PKEY \_ gps \_ DESTLATITUDENUMERATOR 和 PKEY \_ gps DestLatitudeDenominator 中的值計算而來 \_ 。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8、Windows 7、Windows Vista

```
propertyDescription
   name = System.GPS.DestLatitude
   shellPKey = PKEY_GPS_DestLatitude
   formatID = 9D1D7CC5-5C39-451C-86B3-928E2D18CC47
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

 

 
