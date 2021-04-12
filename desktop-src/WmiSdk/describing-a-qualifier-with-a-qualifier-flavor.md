---
description: 限定詞類別是描述限定詞詳細資訊的旗標。
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: 描述限定詞類別的辨識符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192199"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a>描述限定詞類別的辨識符號

[*限定詞*](gloss-q.md)類別是描述限定詞詳細資訊的旗標。 例如，限制的辨識符號類別指出 WMI 不應將相關聯的辨識符號傳播至任何衍生的類別或實例。 您可以使用 MOF 程式碼或以程式設計方式設定類別。 雖然您可以使用各種不同的方式來描述各種效果，但類別旗標的主要目的是要定義 WMI 如何透過繼承來傳播限定詞。

WMI 會定義數個限定詞類別，您可以附加至任何辨識符號，而不論辨識符號的來源為何。 不過，有些類別並非適用于所有的辨識符號類型。 例如， **ToSubClass** 類別僅適用于為類別定義的限定詞。 您無法將 **ToSubClass** 附加至用來描述實例的辨識符號。

您可以使用 [類別] 來描述辨識符號的各種不同效果。 例如，[類別] 可以指出是否可以當地語系化限定詞。 不過，限定詞類別的主要用途之一，就是描述父類別是否可以將限定詞傳遞給子類別或類別實例。 您也可以使用「類別」（class）來判斷類別屬性（property）是否會將限定詞傳遞給實例屬性（property）。 最後，使用 [類別] 來陳述子類別是否可以覆寫繼承的辨識符號的原始值。 不過，您為類別或實例宣告的限定詞不會傳播至該類別或實例的屬性。 此外，建立覆寫許可權的類別只有在您同時設定 **ToInstance** 或 **ToSubClass** 類別時才有效。

您可以使用下列語法，將類別全域指派給整個 MOF 檔案的辨識符號，其中，當指定多個類別時，泛空白字元會作為分隔符號。

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

全域類別適用于 MOF 檔案中所有後續的辨識符號用法。 全域類別語句可能會發生在物件宣告區塊之外的檔案中的任何位置。 在類別、實例或屬性層級重新定義的類別，會覆寫該物件範圍的全域類別宣告。

您無法定義新的類別。 雖然您可以建立新的辨識符號，但只使用現有的 [限定詞](qualifier-flavors.md) 類別來描述新的辨識符號。

**在 MOF 中定義限定詞類別**

-   宣告用來描述限定詞名稱之後，限定詞括弧之間指定限定詞的類別。 使用空白字元做為多個類別之間的分隔符號。

    下列範例顯示附加預先定義之限定詞的模式。

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

您只能以程式設計的方式，在 c + + 中新增限定詞類別。 雖然您可以藉由呼叫 [**SWbemQualifierSet**](swbemqualifierset-add.md)加入新的辨識符號，但無法在適用于 [WMI 的腳本 API](scripting-api-for-wmi.md)中使用這項作業。

**使用 c + + 指派風格**

-   呼叫 [**IWbemQualifierSet：:P**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) lFlavor 參數，並將參數設定為針對方法定義的其中一個常數。

 

 



