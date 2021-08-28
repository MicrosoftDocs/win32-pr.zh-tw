---
description: 影像拍攝時的數位縮放比例。
ms.assetid: 1164e2c9-0864-4520-a3be-0c29a5b70ba4
title: DigitalZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47f98b4ff65f541160804c41f0b6bcd0218d04514a079f39374b222e15013cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598308"
---
# <a name="systemphotodigitalzoom"></a>DigitalZoom

影像拍攝時的數位縮放比例。 在檔案的交換影像檔案中讀取相機 (EXIF) 資訊。 這個屬性是從 [DigitalZoomNumerator](./props-system-photo-digitalzoomnumerator.md) 和 [DigitalZoomDenominator](./props-system-photo-digitalzoomdenominator.md)計算而來。 如果記錄值的分子為0，則不會使用數位縮放。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8、Windows 7、Windows Vista

```
propertyDescription
   name = System.Photo.DigitalZoom
   shellPKey = PKEY_Photo_DigitalZoom
   formatID = F85BF840-A925-4BC2-B0C4-8E36B598679E
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

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

 

 
