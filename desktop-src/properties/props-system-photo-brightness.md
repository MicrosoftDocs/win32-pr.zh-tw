---
description: 影像的亮度值（以頂點單位），通常在-99.99 到99.99 的範圍內。
ms.assetid: 533f6934-dec8-455a-937c-d4e144be4335
title: 系統相片。亮度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28d49464b5d5d081869e514a92fe892a95c1f5a2608412513a2a18b46a51f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033346"
---
# <a name="systemphotobrightness"></a>系統相片。亮度

影像的亮度值（以頂點單位），通常在-99.99 到99.99 的範圍內。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8、Windows 7、Windows Vista

```
propertyDescription
   name = System.Photo.Brightness
   shellPKey = PKEY_Photo_Brightness
   formatID = 1A701BF6-478C-4361-83AB-3701BB053C58
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

請參閱 EXIF 2.2 規格（附錄 C），以比較 [系統的亮度]() 數位和 Foot-Lambert 度量。 這個屬性是從 [BrightnessNumerator](./props-system-photo-brightnessnumerator.md) 和 [BrightnessDenominator](./props-system-photo-brightnessdenominator.md)計算而來。 如果已記錄值的分子為 FFFFFFFF。H，應指出「未知」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[數位相機的交換影像檔案格式： Exif 2.2 版](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

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

 

 
