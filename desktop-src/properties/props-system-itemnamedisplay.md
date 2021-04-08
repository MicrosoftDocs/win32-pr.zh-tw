---
description: '&0034 中的顯示名稱 \# ; 最完整的&\# 0034; 形式。'
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691232"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

「最完整」表單中的顯示名稱。 它是最適合終端使用者的專案名稱唯一標記法。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

這個值是[ItemNamePrefix](./props-system-itemnameprefix.md) [和 system.servicemodel 的串連。](./props-system-itemname.md)

如果專案是檔案，這個屬性會包含顯示名稱，如檔案總管所示。 [當指定了 system.string，但](./props-system-filename.md)這個屬性的值完全不同時，會有可接受的情況。 電子郵件訊息是很好的範例。 如果專案是電子郵件訊息，則專案名稱通常是主旨。 在此情況下，此值必須是[ItemNamePrefix](./props-system-itemnameprefix.md) [和 system.servicemodel 的串連。](./props-system-itemname.md) 由於 ItemNamePrefix 的值會排除任何尾端空格，因此在產生 [ItemNameDisplay]()時，串連必須包含空格。 請注意，此屬性不一定是唯一的，但其設計目的是要升級最可能是唯一的候選項，而且對終端使用者來說也很合理。

例如， [如果是檔，則可以](./props-system-title.md) 使用 system.string 做為 [ItemNameDisplay]()，但實際上，檔的標題可能不太實用，也無法作為唯一的 ItemNameDisplay。 相反地，提供 [system.object](./props-system-filename.md) 作為 ItemNameDisplay 的值是較佳的選擇。 在 Windows Mail 中，電子郵件會以 .eml 檔案的形式儲存在檔案系統中。 這些檔案的檔案名不太方便，因為它們是 Guid。 在此範例中，將 [system.object](./props-system-subject.md) 升階為 ItemNameDisplay，會更有意義。

**相容性注意事項：**

-   Windows Vista 上的 Shell 資料夾執行： \_ 當您想要 Windows 檔案總管呼叫 [**IShellFolder：： GETDISPLAYNAMEOF**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) (SHGDN \_ NORMAL) 來取得名稱的值時，請使用 PKEY ItemNameDisplay 做為名稱資料行。 \_當您想要 Windows 檔案總管呼叫資料夾的屬性存放區或 [**IShellFolder2：： GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex)來取得名稱的值時，請使用另一個 PKEY，例如 PKEY 的名稱。
-   Windows XP 上的 Shell 資料夾執行：第一個資料行必須是 [名稱] 資料行，而 Windows 檔案總管會呼叫 [**IShellFolder：： GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 來取得名稱的值。 PKEY/SCID 並不重要。



| 項目類型     | 範例                   |
|---------------|---------------------------|
| 檔案          | hello.txt                 |
| 訊息       | Re：會議在哪裡？ |
| 裝置資料夾 | song                  |
| 資料夾        | 文件                 |



 

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

 

 
