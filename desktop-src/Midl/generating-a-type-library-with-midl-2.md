---
title: 使用 MIDL 產生類型程式庫
description: ODL 語法的最上層元素是程式庫語句 (程式庫區塊) 。
ms.assetid: e21a9e6e-4e10-4280-af8f-24534cb2ab90
keywords:
- Microsoft 介面定義語言 MIDL、工作、產生類型程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d9084631dc30eb1cff7f61f6f3f090f95bb92cff357b3902cb0959f2c4142f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013846"
---
# <a name="generating-a-type-library-with-midl"></a>使用 MIDL 產生類型程式庫

ODL 語法的最上層元素是程式庫語句 (程式庫區塊) 。 除了套用至程式庫語句的屬性之外，每個其他 ODL 語句都必須定義于程式庫區塊內。 當 MIDL 編譯器看到程式庫區塊時，它會產生類型程式庫，與 Mktyplib.exe 的方式大致相同。 除了 [MIDL 和 Mktyplib.exe 之間的差異](differences-between-midl-and-mktyplib.md)中所述的一些例外狀況，程式庫區塊內的語句應遵循與 ODL 語言和 mktyplib.exe 中相同的語法。

> [!Note]  
> Mktyplib.exe 工具已淘汰。 請改用 MIDL 編譯器。

 

您可以將 ODL 屬性套用至在程式庫區塊內部或外部定義的元素。 除非從程式庫區塊內參考所套用的元素，否則這些屬性不會在程式庫區塊之外生效。 程式庫區塊內的語句可以參考外部專案，方法是使用它作為基底類型、繼承自它，或在行上參考它，如下所示：

``` syntax
<some IDL definitions including definitions for interface IFace and struct bar>
[<some attributes>]
library a
{
    interface IFace;
    struct this_struct;
...
};
```

如果程式庫區塊內所定義的元素是在程式庫區塊內參考，則其定義會放入產生的類型程式庫中。 MIDL 編譯器會將程式庫區塊以外的語句視為一般的 IDL 檔案，並剖析這些語句，因為它一律已完成。 一般來說，這表示會為 RPC 應用程式產生 C 語言的存根。

如需 ODL 檔之一般語法的詳細資訊，請參閱 [ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)。

 

 