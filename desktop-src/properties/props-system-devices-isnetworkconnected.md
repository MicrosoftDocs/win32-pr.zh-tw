---
description: 如果此屬性為 true，表示裝置已連線到網路。
ms.assetid: 4d0aa672-1ff8-4fb1-82d2-76553c2b0209
title: IsNetworkConnected
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c016b97dc3e966407582e0447ddeae1c4ffb86d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692891"
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

 

 
