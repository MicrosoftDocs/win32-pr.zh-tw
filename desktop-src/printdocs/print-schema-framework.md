---
description: 這些文章提供有關列印架構元素類型之意義和使用方式的詳細資訊。
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Print Schema Framework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 986308ae2ce1308c7df090da295f8b5473efe99219339a906490299ec33b2ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718598"
---
# <a name="print-schema-framework"></a>Print Schema Framework

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

本節提供有關列印架構元素類型之意義和使用方式的詳細資訊。 列印架構架構初始版本的主要重點在於代表裝置屬性的設定和功能。 概括而言，此架構提供兩種不同的樣式來描述裝置屬性：做為功能/選項結構，或做為參數結構。 如果裝置屬性有少量的可用值或狀態，則屬性的特性應該是具有允許的值或狀態（稱為 Option 元素）的特徵。 相反地，如果裝置屬性有大量可用的值或狀態，而且您可以輕鬆地定義所有可能值的集合，而不需要使用明確列舉，則裝置屬性應該是參數的特性。  (參數是透過 ParameterDef 元素來定義，而參數實例則是透過 ParameterInit 專案來初始化。 ) 屬性專案會在功能/選項和參數結構內使用，以提供更細微的差異層級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



