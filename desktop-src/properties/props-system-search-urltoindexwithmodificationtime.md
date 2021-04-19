---
description: 這個屬性與 UrlToIndex 相同，不同之處在于它包含上次修改 URL 的時間。
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975866"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>UrlToIndexWithModificationTime

這個屬性與 [**UrlToIndex**](props-system-search-urltoindex.md) 相同，不同之處在于它包含上次修改 URL 的時間。 這是索引子的優化，因此不需要回呼至通訊協定處理常式來要求這項資訊，以判斷是否需要重新編制內容的索引。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a>備註

此 [UrlToIndexWithModificationTime]() 屬性與 [UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) 屬性相同，不同之處在于您也會傳入檔的上次修改時間。 如果上次修改時間相符，則索引子會假設檔已編制索引，並擲回通知。 這個屬性是具有兩個元素的向量，包含 URL 的 **vt \_ LPWSTR** 值，以及包含上次修改時間的 **vt \_ FILETIME** 值。

[UrlToIndexWithModificationTime]() \_ \_ \_ \_ 在舊版 WINDOWS 作業系統中的時間稱為 PID GTHR DIRLINK。

PKEY 值定義于 Propkey 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
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

 

 
