---
description: 指出裝置是否為漫遊。
ms.assetid: d2382e96-7ca4-42e4-8e5b-89f1da736904
title: 系統。漫遊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f482bb306eeeed03592ae18bb7a8f63c109f2f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849378"
---
# <a name="systemdevicesroaming"></a>系統。漫遊

指出裝置是否為漫遊。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.Devices.Roaming
   shellPKey = PKEY_Devices_Roaming
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = NotRoaming
            minValue = 0
            setValue = 0
            text = Not roaming
            defineToken = ROAMING_NOT_ROAMING
         enumRange
            name = Roaming
            minValue = 1
            setValue = 1
            text = Roaming
            defineToken = ROAMING_ROAMING
         enumRange
            name = UnknownStatus
            minValue = 2
            setValue = 2
            text = Unknown roaming status
            defineToken = ROAMING_UNKNOWN_STATUS
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

 

 
