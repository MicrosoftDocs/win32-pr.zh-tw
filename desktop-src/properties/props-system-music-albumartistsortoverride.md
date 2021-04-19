---
description: 這個選擇性的字串值允許覆寫 AlbumArtist 的標準排序次序。這對於正確排序日文的音樂檔案而言非常重要，因為在沒有此欄位的情況下，不能 becorrectly 按發音排列 (使用者預期的) 順序。它也可以用來自訂非東亞案例中的排序，例如允許使用者移除用於排序的文章。
ms.assetid: 67dda36c-8098-4758-a473-4f10730a158e
title: AlbumArtistSortOverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f80d9ef55a8ef797af2dec8136c4bb8764a076f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986903"
---
# <a name="systemmusicalbumartistsortoverride"></a>AlbumArtistSortOverride

這個選擇性的字串值允許覆寫 AlbumArtist 的標準排序次序。這對於正確排序日文的音樂檔案而言非常重要，因為在沒有此欄位的情況下，不能 becorrectly 按發音排列 (使用者預期的) 順序。它也可以用來自訂非東亞案例中的排序，例如允許使用者移除用於排序的文章。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10，1703版、Windows 10、1607版、Windows 10、1511版、Windows 10、version 1507、Windows 8.1、Windows 8

```
propertyDescription
   name = System.Music.AlbumArtistSortOverride
   shellPKey = PKEY_Music_AlbumArtistSortOverride
   formatID = F1FDB4AF-F78C-466C-BB05-56E92DB0B8EC
   propID = 103
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
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

 

 
