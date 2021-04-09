---
title: MOF 字串
description: 字串是包含字元字串的資料類型，通常是人們可讀取的文字。
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848629"
---
# <a name="mof-strings"></a>MOF 字串

字串是包含字元字串的資料類型，通常是人們可讀取的文字。 MOF 描述兩種類型的字串，用來保存單一或多個字元。 MOF 也有一系列的規則，描述如何在字串中使用引號。

下表列出 MOF 的字串資料類型。



| 資料類型  | Automation 類型 | Description                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| **char16** | **VT \_ I2**      | 通用字元集2中的單一16位 Unicode 字元 (UCS-2) 格式<br/> |
| **string** | **VT \_ BSTR**    | Unicode 字元字串<br/>                                                    |



 

撰寫 MOF 的字串時，請使用下列指導方針：

-   使用單引號來括住單一字元常數。

    如果您未搭配單一字元常數使用單引號，則必須使用 Unicode 字元值的整數表示。 您可以選擇性地使用 \\ 美國國家標準局 (ANSI) C 標準的 x escape 序列來指定字元，如下所示：

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    因為 MOF 是以 Unicode 為基礎，所以您也可以指定16位值。

    請注意，ANSI C 格式的單一字元常數會以雙引號括住。

-   將字元字串括在雙引號中。

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   使用一或多個空白字元串連連續的引號字串。

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   使用以反斜線開頭的 escape 序列，將引號內嵌至字串中。

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

下列範例說明如何初始化字串屬性和字串參數：

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




