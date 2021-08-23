---
description: 評等系統，其使用介於0和5之間的整數值範圍。
ms.assetid: 50353ba9-86dd-4172-91b4-1898c8fc5522
title: System. SimpleRating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e13d7f65fb335aea6362509c20845bd1324b6e99d48f14cd9746f0237661f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598138"
---
# <a name="systemsimplerating"></a>System. SimpleRating

評等系統，其使用介於0和5之間的整數值範圍。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8、Windows 7、Windows Vista

```
propertyDescription
   name = System.SimpleRating
   shellPKey = PKEY_SimpleRating
   formatID = A09F084E-AD41-489F-8076-AA5BE3082BCA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

為了與 Windows Vista Shell 分級系統相容，您的屬性處理常式也應該將對應填入[system. 評](./props-system-rating.md)等屬性，如該屬性所述。

您可以使用下表，從 [系統的評](./props-system-rating.md) 等轉換為 [SimpleRating]()。



| 系統評分 | System. SimpleRating |
|---------------|---------------------|
| 0             | 0                   |
| 1-12          | 1                   |
| 13-37         | 2                   |
| 38-62         | 3                   |
| 63-87         | 4                   |
| 88-99         | 5                   |



 

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

 

 
