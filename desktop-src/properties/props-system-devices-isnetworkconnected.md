---
description: 如果此屬性為 true，表示裝置已連線到網路。
ms.assetid: 4d0aa672-1ff8-4fb1-82d2-76553c2b0209
title: IsNetworkConnected
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde5dfb7738c46cf8797286ef5894b6e993c6aed9a43b0d6dea67fa15fdf7302
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885548"
---
# <a name="systemdevicesisnetworkconnected"></a>IsNetworkConnected

如果此屬性為 true，表示裝置已連線到網路。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8

```
propertyDescription
   name = System.Devices.IsNetworkConnected
   shellPKey = PKEY_Devices_IsNetworkConnected
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 85
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NetworkConnected
            value = #TRUE#
            text = Network Connected
            defineToken = ISNETWORKDEVICE_NETWORKDEVICE
         enum
            name = NotNetworkConnected
            value = #FALSE#
            text = Not Network Connected
            defineToken = ISNETWORKDEVICE_NOTNETWORKDEVICE
```

## <a name="windows-7"></a>Windows 7

```
propertyDescription
   name = System.Devices.IsNetworkConnected
   shellPKey = PKEY_Devices_IsNetworkDevice
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 85
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NetworkConnected
            value = #TRUE#
            text = Network Connected
            defineToken = ISNETWORKDEVICE_NETWORKDEVICE
         enum
            name = NotNetworkConnected
            value = #FALSE#
            text = Not Network Connected
            defineToken = ISNETWORKDEVICE_NOTNETWORKDEVICE
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

 

 
