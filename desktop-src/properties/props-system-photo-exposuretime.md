---
description: 從交換影像檔案讀取之相片的曝光時間（以秒為單位） (EXIF) 資訊。
ms.assetid: 44f7e6d5-c4d9-4b41-b6c6-15145abb7983
title: ExposureTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2bc1c767344187efd0107d4efa7bcec23d6f099497d9a26f29b89153a73a2e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118723863"
---
# <a name="systemphotoexposuretime"></a>ExposureTime

從交換影像檔案讀取之相片的曝光時間（以秒為單位） (EXIF) 資訊。 這個屬性是從 [ExposureTimeNumerator](./props-system-photo-exposuretimenumerator.md) 和 [ExposureTimeDenominator](./props-system-photo-exposuretimedenominator.md)計算而來。

以下是從 EXIF 2.2 規格中取得的可能值清單。

-   30
-   15
-   8
-   4
-   2
-   1
-   1/2
-   1/4
-   1/8
-   1/15
-   1/30
-   1/60
-   1/125
-   1/250
-   1/500
-   1/1000
-   1/2000

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8、Windows 7、Windows Vista

```
propertyDescription
   name = System.Photo.ExposureTime
   shellPKey = PKEY_Photo_ExposureTime
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 33434
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

 

 
