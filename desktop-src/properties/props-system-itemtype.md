---
description: 專案的標準型別。
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System.servicemodel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194820"
---
# <a name="systemitemtype"></a>System.servicemodel

專案的標準型別。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7、Windows Vista 版本

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

System.servicemodel 的值是要以程式設計方式剖析，而且可以是：

-   指向 ProgID 值的副檔名， (HKEY \_ 類別 \_ 根 \\ <ProgID>) 保留類型的顯示名稱。
-   ProgID 值 (HKEY \_ 類別 \_ RROOT \\ <ProgID>) ，其中包含類型的顯示名稱。

ProgID 的 FriendlyTypeName 元素應為應用程式名稱的當地語系化版本 (@winword.dll 、-42) ，而 progid 索引鍵的預設值為非當地語系化的名稱 (Word.Doc>ument. 12) 。

如果沒有標準型別，則此值為 VT \_ 空白。 如果專案是檔案 ([系統檔案名](./props-system-filename.md) 不是 VT \_ 空白) ，則值與 [FileExtension](./props-system-fileextension.md)相同。 當您想要在視圖中顯示類型給終端使用者時，請使用 [ItemTypeText](./props-system-itemtypetext.md) 。

> [!Note]  
> 如果專案是檔案，則傳遞 [system.string 值給]() [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) 會產生與 [ItemTypeText](./props-system-itemtypetext.md)相同的值。

 

範例值：



| 路徑                                   | ItemType         |
|----------------------------------------|------------------|
| c： \\ mydir \\ bar \\hello.txt              | .txt             |
| \\\\伺服器 \\ 共用 \\ mydir \\goodnews.doc | .doc             |
| \\\\伺服器 \\ 共用 \\ 資料夾              | 目錄        |
| c： \\ MyDir \\ MyFolder                    | 目錄        |
| \[desktop\]                            | 資料夾           |
| /Mailbox 帳戶/收件匣/' Re： Hello！ '    | MAPI/IPM。消息 |



 

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
</dt> <dt>

[程式設計識別碼](../shell/fa-progids.md)
</dt> </dl>

 

 
