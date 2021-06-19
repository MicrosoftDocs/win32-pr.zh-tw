---
description: 閱讀有關 Print Schema Framework 中 ParameterRef 元素的資訊。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: ParameterRef 元素
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2935317bc4107e2071911ab1df826426b2bcec17
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396523"
---
# <a name="parameterref-elements"></a>ParameterRef 元素

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

ParameterRef 專案特別適用于 Option 元素，可讓該選項專案參考特定的 ParameterDef 元素。 針對這些選項元素，ScoredProperty 專案會將此選項的特性標示為不會以值的形式在 PrintCapabilities 檔中進行硬式編碼，但改為變數。 為了啟用此變異，這些 ScoredProperty 元素包含 ParameterRef 元素。 ScoredProperty 元素不可同時包含 Value 元素和 ParameterRef 元素。 包含一或多個 ParameterRef 元素的 Option 元素稱為參數化 Option 元素。

Print Schema Framework 可讓 Option 元素包含任意數目的 ScoredProperty 專案，這些專案會參考參數專案，以及包含值專案的任何數目的 ScoredProperty 元素。 此架構也可讓任意數目的功能元素包含參數化選項專案，而且每個功能元素都允許任何數目的參數化選項元素。 此外，相同的參數結構可由數個不同的選項專案所參考，也就是可以屬於相同或不同功能專案的選項元素。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



