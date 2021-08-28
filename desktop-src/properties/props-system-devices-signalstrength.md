---
description: 裝置信號強度。
ms.assetid: 662d39a6-f2f5-4556-a6de-bbcc655b4adb
title: SignalStrength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8b93b51271b25e2bbb49d91b25b457ab55ea794c44e47107e20ee601566777b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119097157"
---
# <a name="systemdevicessignalstrength"></a>SignalStrength

裝置信號強度。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.Devices.SignalStrength
   shellPKey = PKEY_Devices_SignalStrength
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0
            text = No signal
            defineToken = SIGNALSTRENGTH_NONE
         enum
            name = Weak
            value = 1
            text = Weak signal
            defineToken = SIGNALSTRENGTH_WEAK
         enum
            name = Average
            value = 2
            text = Average signal
            defineToken = SIGNALSTRENGTH_AVERAGE
         enum
            name = Strong
            value = 3
            text = Strong signal
            defineToken = SIGNALSTRENGTH_STRONG
         enum
            name = Excellent
            value = 4
            text = Excellent signal
            defineToken = SIGNALSTRENGTH_EXCELLENT
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

 

 
