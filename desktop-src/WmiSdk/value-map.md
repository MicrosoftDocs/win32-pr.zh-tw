---
description: 值對應是連結至具有值和 ValueMap 限定詞之屬性的陣列。
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: ValueMap 和值限定詞
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987257"
---
# <a name="valuemap-and-value-qualifiers"></a>ValueMap 和值限定詞

值對應是連結至具有 **值** 和 **ValueMap** 限定詞之屬性的陣列。

屬性會作為陣列中的索引，並保留代表陣列中其中一個值的值。 使用 MOF 程式碼，您可以有下列類型的值對應：

-   整數的陣列對應。

    您可以定義具有 **值** 限定詞的陣列，並將陣列直接連結至整數屬性，如下列範例所示：

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    在此範例中， **Status** 屬性值是以 **value** 定義之字串陣列中的索引。 屬性只能採用對應至 **值** 陣列中序數位置的值減1。 例如，將 [ **狀態** ] 設定為 [1] 會對應至「錯誤」值。 索引屬性只能採用對應至 **值** 陣列中位置的值。 例如，如果陣列有10個專案，則索引屬性可以是第0到第9個的故事，而不是30或177。

-   對應至另一個對應至整數之陣列的陣列。

    如果您想要建立不使用序數系統計數的索引，請使用 **ValueMap** 辨識符號。 **ValueMap** 辨識符號會設定另一個陣列來保存任意的索引編號系統，如下列範例所示：

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    雖然您必須將 **ValueMap** 的值放在引號中，WMI 仍會將值視為整數。 因此，在此範例中，您可以將 [ **狀態** ] 屬性設定為 [ **ValueMap** 集合： 1]、[3]、[99] 或 [0] 中的整數。 WMI 會將 **ValueMap** 字串陣列中序數位置的每個整數對應至 **值** 陣列中的對應位置。 例如，將 **狀態** 設定為0會對應到「未知」。

-   對應至另一個陣列對應至字串的陣列。

    如果您不想要使用整數來編制陣列的索引，可以改為使用字串來保存陣列中的其中一個可能值。 若要這樣做，您必須定義同時包含字串的 **值** 和 **ValueMap** 陣列，如下列範例所示：

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    使用字串屬性時，屬性的實際可允許值為 **ValueMap** 陣列中的專案。 例如，您可以將 **狀態** 設定為「確定」或「未知」。

應用程式是由應用程式以實用的方式利用對應。 由提供者來強制執行合法的值範圍。

## <a name="remarks"></a>備註

在決定是否要使用 **ValueMap** / **值** 或 **點陣圖** / **BitValues** 限定詞時，判斷是否有任何指定的值可能會同時發生。 如果有多個並行值可以存在，您必須使用 **BitMap** / **BitValues**。 如果所有值都是互斥的，您應該使用 **ValueMap** / **值** 限定詞。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[點陣圖和 BitValues](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



