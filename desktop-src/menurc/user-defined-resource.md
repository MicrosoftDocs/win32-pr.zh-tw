---
title: User-Defined 資源
description: 使用者定義的資源定義語句會定義包含應用程式特定資料的資源。
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- 使用者定義的資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909352c7f0643ed67b1d199fafba1ac8f15d2a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183439"
---
# <a name="user-defined-resource"></a>User-Defined 資源

使用者定義的資源定義語句會定義包含應用程式特定資料的資源。 資料可以具有任何格式，而且可以定義為指定檔案的內容 (如果指定 *檔案名* 參數) 或指定為一系列的數位和字串 (如果) 指定 *原始資料* 區塊。

``` syntax
nameID typeID filename
```

*檔案名* 會指定包含資源之二進位資料的檔案名。 檔案內容會包含在資源中。 RC 不會以任何方式解讀二進位資料。 程式設計人員必須負責確保目的電腦架構的資料已正確對齊。

您也可以使用下列語法，在資源腳本中完全定義使用者定義的資源：

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

識別資源的唯一名稱或16位不帶正負號的整數。

</dd> <dt>

<span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*
</dt> <dd>

識別資源類型的唯一名稱或16位不帶正負號的整數。 如果指定了數位，則它必須大於255。 數位1到255會保留給現有和未來重新定義的資源類型。

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

包含資源資料的檔案名。 參數必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。

</dd> <dt>

<span id="raw-data"></span><span id="RAW-DATA"></span>*原始資料*
</dt> <dd>

由一或多個整數或字元字串所組成的原始資料。 您可以用十進位、八進位或十六進位格式來指定整數。 為了與16位 Windows 相容，整數會儲存為文字值。 您可以使用 "L" 尾碼來限定整數，以將整數儲存為 DWORD 值。

字串會以引號括住。 RC 不會自動將終止的 null 字元附加至字串。 每個字串都是指定之 ANSI 字元的序列，除非您將它限定為具有 "L" 前置詞的寬字元字串。

資料區塊開始于 **DWORD** 界限，而 RC 不會在 *原始資料* 區塊內執行資料的填補或對齊。 程式設計人員必須負責確保區塊內適當的資料對齊。

</dd> </dl>

## <a name="example"></a>範例

下列範例會顯示數個使用者定義的語句：

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




