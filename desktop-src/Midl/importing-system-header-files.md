---
title: 匯入系統標頭檔
description: 雖然通常可以使用-include 指示詞在 IDL 檔案中包含標頭檔，但並不建議這麼做。
ms.assetid: ff524965-424d-416d-97cd-c2780ebf69ef
keywords:
- 匯入 MIDL、系統標頭檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26df7ca983fa21ae8e604446f0221c302c73099
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696342"
---
# <a name="importing-system-header-files"></a>匯入系統標頭檔

雖然通常可以使用 **\# include** 指示詞將標頭檔包含在 IDL 檔案中，但不建議您這樣做。 MIDL 編譯器會針對正在編譯的 IDL 檔案中定義的所有函式產生存根。 通常，標頭檔會包含您不需要或不想要包含在存根檔案中的一些原型，而且會將所有這些定義有效地放入 **\# 您的主要** IDL 檔案中。 此外，如果標頭檔中有定義不可遠端處理類型，IDL 檔案可能不會編譯。

有兩種方式可將標頭檔中的類型定義包含在 IDL 檔案中：

-   使用匯 [**入**](import.md) 指示詞來包含標頭檔中定義的資料類型。 與 C 語言 **\# include** 指示詞不同，匯 **入** 指示詞只會挑選型別和常數定義，並忽略程式原型。 只要您的主要 IDL 檔案未參考標頭檔中定義的任何不可遠端處理類型，這個方法就會運作。
-   使用包含標頭檔的虛擬介面建立 helper IDL 檔案。 然後，使用匯 [**入**](import.md) 指示詞來包含 helper 檔案。 如此一來，只有 [**typedef**](typedef.md)才會出現在已編譯的存根中。 例如：

```syntax
//in helper.idl:
interface dummy
{ 
   #include "kitchensink.h"
   #include "system.h"
}

//in main.idl:
import "helper.idl";
```
