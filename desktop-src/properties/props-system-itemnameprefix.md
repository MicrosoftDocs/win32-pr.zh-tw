---
description: 專案的前置詞，用於主體開頭為首碼 &0034; 的電子郵件訊息 \# 。Re： &\# 0034;。
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943626"
---
# <a name="systemitemnameprefix"></a>System. ItemNamePrefix

專案的前置詞，用於主體開頭為 "Re：" 前置詞的電子郵件訊息。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

如果專案是檔案，則此屬性的值為 VT \_ 空白。 如果專案是訊息，則這個屬性的值會是轉送或回復首碼 (包括分隔冒號，但不含空白字元) 或 VT 空白（如果沒有 \_ 前置詞）。

範例值：



| System. ItemNamePrefix | System.servicemodel  | System.ItemNameDisplay |
|-----------------------|------------------|------------------------|
| VT \_ 空白             | 「美好日」      | 「美好日」            |
| "Re："                 | 「美好日」      | 「Re：很棒的一天」        |
| "Fwd："               | 「每月預算」 | "Fwd：每月預算"  |
| VT \_ 空白             | accounts.xls     | accounts.xls           |



 

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

 

 
