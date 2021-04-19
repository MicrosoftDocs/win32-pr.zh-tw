---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 071dc91f-3574-4e0e-b2ba-0e4a56ce4a28
title: 嵌套 ScoredProperty 實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f1bfed09c48bc0ac6e93e09f96dc8116e8b0a91
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106991400"
---
# <a name="nested-scoredproperty-instances"></a>嵌套 ScoredProperty 實例

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

請注意，您不會將 ScoredProperty 實例新增為選項實例的子項目。 ScoredProperty 實例也可以嵌套在其他 ScoredProperty 實例內。 當裝置屬性很複雜，且最適合由多個子屬性工作表示時，這會很有用。 將子屬性（Property）新增至現有的 (或公用) 屬性（Property）或 ScoredProperty 是增強選項的好方法，同時保留現有選項實例的可攜性。 例如，「媒體媒體」功能的標準選項實例包含 ScoredProperty，描述媒體的權數為淺色、中、大或 ExtraHeavy。 如果您想要更精確的權數描述，您可以在下列範例中新增子屬性 (GramsPer100Sheets) ，其中包含媒體的100工作表的實際權數)  (。 增強選項看起來可能如下列範例所示。

``` syntax
<!-- Note: The following ScoredProperty is not a Public Print Schema ScoredProperty -->
<!-- This example shows a nested ScoredProperty defined by a Private namespace-->
<!-- It is included for illustration purposes. -->

<psf:ScoredProperty name="FabrikamES500:PaperWeight">
  <psf:Value xsi:type="xs:string">Medium</psf:Value>
  <psf:ScoredProperty name="FabrikamES500:GramsPerSheet">
    <Value xsi:type="decimal">109.5</Value>
  </psf:ScoredProperty>
</psf:ScoredProperty>
```

比較原始和增強的選項實例會產生近乎完美的比對，因為增強的選項是原始的超集合，而且會保留每個原始 ScoredProperty 實例的位置和值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



