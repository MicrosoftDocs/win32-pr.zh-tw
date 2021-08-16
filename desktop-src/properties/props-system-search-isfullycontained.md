---
description: 由容器的所有子專案發出為 TRUE (例如電子郵件或副檔名為 .zip 的壓縮檔案，) 會發出 IsClosedDirectory 為 TRUE。 這可確保子專案包含在搜尋索引中。
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce7f325be26abdb81dcb51da7018f6da786e6ec5f3a31111e4ae3823acf8c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864987"
---
# <a name="systemsearchisfullycontained"></a>IsFullyContained

由容器的所有子專案發出為 **true** (例如電子郵件或副檔名為 .zip 的壓縮檔案，) 會發出 [IsClosedDirectory](./props-system-search-iscloseddirectory.md) 為 **true**。 這可確保子專案包含在搜尋索引中。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8、Windows 7、Windows Vista

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

[IsClosedDirectory](./props-system-search-iscloseddirectory.md)屬性可讓索引子略過容器子專案的列舉，以協助優化索引子的效能。 不過，索引子會將這些子專案標示為未造訪，因此會從索引中刪除。 藉由發出 [IsFullyContained]() 為 **TRUE**，就不會從索引中刪除專案（儘管尚未造訪）。

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

 

 
