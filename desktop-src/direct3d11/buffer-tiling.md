---
title: 緩衝區拼貼
description: 緩衝資源分為 64KB 的磚，若大小不是 64 KB 的倍數，則最後一個磚會有某些空白空間。
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36352f492efb88bf220035d737b5767ef086e74ab91ffb4228d7734f838425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734240"
---
# <a name="buffer-tiling"></a>緩衝區拼貼

如果大小不是64KB 的倍數，則 [緩衝區](overviews-direct3d-11-resources-buffers.md) 資源會分割成64kb 個磚，並在最後一個磚中顯示一些空白空間。

結構化的緩衝區對於要並排顯示的分散必須無限制。 但若一開始就將其並排顯示，便可能失去利用 [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) 所達到的可能硬體效能最佳化。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚式資源的區域如何並排顯示](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 