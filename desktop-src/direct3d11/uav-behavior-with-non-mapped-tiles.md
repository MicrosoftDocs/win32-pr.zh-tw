---
title: 非對應磚的 UAV 行為
description: 未排序存取檢視 (UAV) 讀取和寫入的行為取決於硬體支援程度。
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed676403e5eb1fdc838ac080b8be530b5004e6734fedc5674664f4d75304ee37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857658"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a>非對應磚的 UAV 行為

未排序存取檢視 (UAV) 讀取和寫入的行為取決於硬體支援程度。 如需要求的明細，請參閱並排顯示的 [資源功能層](tiled-resources-features-tiers.md)的整體讀取和寫入行為。 本節摘要理想的行為。

讀取 UAV 非對應磚的著色器作業，對於格式的所有非遺失元件會傳回 0，對遺失元件則傳回預設值。

嘗試寫入到非對應磚的著色器作業，會導致無法寫入到非對應的區域（而繼續寫入到對應的區域）。 [第 2 層](tier-2.md)不需要此寫入處理的理想定義；對非對應磚的寫入最後可能會在快取，後續讀取可能會收取此資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源的管線存取](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




