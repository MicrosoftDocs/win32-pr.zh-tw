---
description: 指出整體影像增益調整的程度。 從 PKEY \_ photo \_ GAINCONTROLNUMERATOR 和 PKEY \_ photo GainControlDenominator 計算 \_ 。
ms.assetid: 5076e03b-2c8a-4ef4-93d6-271a4bd697a6
title: GainControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8278120e5e65137eda491f52af7bc36f1c163c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944066"
---
# <a name="systemphotogaincontrol"></a>GainControl

指出整體影像增益調整的程度。 從 PKEY \_ photo \_ GAINCONTROLNUMERATOR 和 PKEY \_ photo GainControlDenominator 計算 \_ 。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.Photo.GainControl
   shellPKey = PKEY_Photo_GainControl
   formatID = FA304789-00C7-4D80-904A-1E4DCC7265AA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0.0
            text = None
            defineToken = PHOTO_GAINCONTROL_NONE
         enum
            name = LowGainUp
            value = 1.0
            text = Low gain up
            defineToken = PHOTO_GAINCONTROL_LOWGAINUP
         enum
            name = HighGainUp
            value = 2.0
            text = High gain up
            defineToken = PHOTO_GAINCONTROL_HIGHGAINUP
         enum
            name = LowGainDown
            value = 3.0
            text = Low gain down
            defineToken = PHOTO_GAINCONTROL_LOWGAINDOWN
         enum
            name = HighGainDown
            value = 4.0
            text = High gain down
            defineToken = PHOTO_GAINCONTROL_HIGHGAINDOWN
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.GainControl
   shellPKey = PKEY_Photo_GainControl
   formatID = FA304789-00C7-4D80-904A-1E4DCC7265AA
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0.0
            text = None
            defineName = PHOTO_GAINCONTROL_NONE
         enum
            value = 1.0
            text = Low gain up
            defineName = PHOTO_GAINCONTROL_LOWGAINUP
         enum
            value = 2.0
            text = High gain up
            defineName = PHOTO_GAINCONTROL_HIGHGAINUP
         enum
            value = 3.0
            text = Low gain down
            defineName = PHOTO_GAINCONTROL_LOWGAINDOWN
         enum
            value = 4.0
            text = High gain down
            defineName = PHOTO_GAINCONTROL_HIGHGAINDOWN
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

 

 
