---
description: 如果此屬性為 true，表示裝置是共用裝置。
ms.assetid: d1da0747-ad07-49e5-8082-5f39bf0a84d8
title: IsShared
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f305381d43eb0d5f4305d2a838561883182a3855d63fcc23b97a128a5c0def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118467520"
---
# <a name="systemdevicesisshared"></a>IsShared

如果此屬性為 true，表示裝置是共用裝置。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8

```
propertyDescription
   name = System.Devices.IsShared
   shellPKey = PKEY_Devices_IsShared
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 84
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Shared
            value = #TRUE#
            text = Shared
            defineToken = ISSHAREDDEVICE_SHARED
         enum
            name = NotShared
            value = #FALSE#
            text = Not Shared
            defineToken = ISSHAREDDEVICE_NOTSHARED
```

## <a name="windows-7"></a>Windows 7

```
propertyDescription
   name = System.Devices.IsShared
   shellPKey = PKEY_Devices_IsSharedDevice
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 84
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Shared
            value = #TRUE#
            text = Shared
            defineToken = ISSHAREDDEVICE_SHARED
         enum
            name = NotShared
            value = #FALSE#
            text = Not Shared
            defineToken = ISSHAREDDEVICE_NOTSHARED
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

 

 
