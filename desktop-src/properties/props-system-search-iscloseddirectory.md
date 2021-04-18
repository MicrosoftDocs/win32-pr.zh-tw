---
description: 由容器專案發出為 TRUE，表示如果容器專案自上次增量索引驗證編目之後未變更，索引子就不需要列舉其子專案。
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: IsClosedDirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971558"
---
# <a name="systemsearchiscloseddirectory"></a>IsClosedDirectory

由容器專案發出為 **TRUE** ，表示如果容器專案自上次增量索引驗證編目之後未變更，索引子就不需要列舉其子專案。 這有助於優化索引子效能。 在這些容器案例中 (範例是包含附件的電子郵件，或副檔名為 .zip 的壓縮檔) ，子專案會從其父專案分不開。 例如，如果包含專案的 [DateModified](./props-system-datemodified.md) 屬性變更，則容器的 DateModified 值會變更為 [符合]。 此外，如果刪除父代專案，也會一併刪除所有子專案。 因此，如果容器未變更，索引子就會知道其中沒有任何專案已變更，且不需要開啟容器來個別檢查內容。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

> [!IMPORTANT]
> 如果專案在這個屬性中發出 **TRUE** ，每個子專案都必須發出 [IsFullyContained](./props-system-search-isfullycontained.md) 屬性為 **true** ，以防止從索引中刪除這些專案。

 

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

 

 
