---
title: 非對應磚的 SRV 行為
description: 著色器資源檢視 (SRV) 涉及非對應磚的讀取行為取決於硬體支援程度。
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182974"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a>非對應磚的 SRV 行為

著色器資源檢視 (SRV) 涉及非對應磚的讀取行為取決於硬體支援程度。 如需要求的明細，請參閱並排顯示 [資源功能層](tiled-resources-features-tiers.md)的讀取行為。 本節摘要[第 2 層](tier-2.md)需要的理想行為。

請考慮可讀取 SRV 中的一組紋素的紋理篩選操作。 在格式的所有非遺失元件中，落在非對應磚的紋素貢獻 0（如果是遺失元件則為預設值）到整體篩選作業，對應紋素的貢獻在旁邊。 紋素全部都會加權和結合在一起，不受資料是來自對應或非對應磚的影響。

某些第一 [層層](tier-2.md) 級的硬體不符合這項規格需求，如果任何材質 (的非零權數) 落在非對應的磚上，則會傳回0，並以上述的預設值作為整體篩選結果。 不允許任何其他硬體錯過將所有（非零加權）紋素包含在篩選中的需求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源的管線存取](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




