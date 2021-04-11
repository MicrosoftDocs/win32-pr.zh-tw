---
description: MOF 編譯器接受針對 nonfloating 點屬性指定的浮點值。 此值會向上或向下舍入，並儲存為 nonfloating 點數位。 這種情況可能會導致某些非預期的結果。
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: 使用 Floating-Point 值編譯 MOF 程式碼
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193873"
---
# <a name="compiling-mof-code-with-floating-point-values"></a>使用 Floating-Point 值編譯 MOF 程式碼

MOF 編譯器接受針對 nonfloating 點屬性指定的浮點值。 此值會向上或向下舍入，並儲存為 nonfloating 點數位。 這種情況可能會導致某些非預期的結果。

下列 MOF 程式碼範例會在名為 "Test" 的命名空間中，定義名為 **abc** 的類別。 這個 MOF 程式碼會進行編譯而不會發生錯誤，但是您無法在此程式碼所建立的實例中，查詢針對屬性 **exampleUint16** 所定義的浮點值。

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

如果您發出下列查詢，則會收到指出無效查詢的錯誤碼。


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



但是，下列查詢會尋找指定的實例。


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[編譯 MOF 檔案](compiling-mof-files.md)
</dt> <dt>

[**mofcomp.exe**](mofcomp.md)
</dt> <dt>

[預處理器命令](preprocessor-commands.md)
</dt> </dl>

 

 



