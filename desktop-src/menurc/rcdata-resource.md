---
title: RCDATA 資源
description: 定義應用程式的原始資料資源。 原始資料資源允許直接在可執行檔中包含二進位資料。
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- RCDATA 資源功能表與其他資源
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932748"
---
# <a name="rcdata-resource"></a>RCDATA 資源

定義應用程式的原始資料資源。 原始資料資源允許直接在可執行檔中包含二進位資料。

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

識別資源的唯一名稱或16位不帶正負號的整數值。

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*選用語句*
</dt> <dd>

這個參數可以是零或多個下列語句。



| 陳述式                                                        | 描述                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**特性**](characteristics-statement.md) *dword*     | 有關可供讀取和寫入資源檔的工具使用之資源的使用者定義資訊。 如需詳細資訊，請參閱 [**特性**](characteristics-statement.md)。 |
| [**語言**](language-statement.md)*語言*、*語言* | 資源的語言。 如需詳細資訊，請參閱 [**語言**](language-statement.md)。                                                                                            |
| [**版本**](version-statement.md) *dword*                     | 資源的使用者定義版本號碼，可供讀取和寫入資源檔的工具使用。 如需詳細資訊，請參閱 [**版本**](version-statement.md)。              |



 

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*原始資料*
</dt> <dd>

由一或多個整數或字元字串所組成的原始資料。 您可以用十進位、八進位或十六進位格式來指定整數。 為了與16位 Windows 相容，整數會儲存為 **文字** 值。 您可以使用 "L" 尾碼來限定整數，以將整數儲存為 **DWORD** 值。

字串會以引號括住。 RC 不會自動將終止的 null 字元附加至字串。 每個字串都是指定之 ANSI 字元的序列，除非您將它限定為具有 L 前置詞的寬字元字串。

資料區塊開始于 **DWORD** 界限，而 RC 不會在 *原始資料* 區塊內執行資料的填補或對齊。 您必須負責確保區塊內適當的資料對齊。

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="examples"></a>範例

下列範例示範如何使用 **RCDATA** 語句：

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加速器**](accelerators-resource.md)
</dt> <dt>

[**特徵**](characteristics-statement.md)
</dt> <dt>

[**語言**](language-statement.md)
</dt> <dt>

[**功能表**](menu-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**版本**](version-statement.md)
</dt> </dl>

 

 




