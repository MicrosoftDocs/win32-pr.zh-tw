---
description: 色彩的 Alpha 值會控制其透明度。 啟用 Alpha 混色可將介面上的色彩、材質和材質混合成另一個表面的透明度。
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: " (Direct3D 9) 的 Alpha 混色狀態"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4bd012340fae9e7597479d846d18db37c32d6f95a42118ba7444ad63a2e1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045206"
---
# <a name="alpha-blending-state-direct3d-9"></a> (Direct3D 9) 的 Alpha 混色狀態

色彩的 Alpha 值會控制其透明度。 啟用 Alpha 混色可將介面上的色彩、材質和材質混合成另一個表面的透明度。

如需詳細資訊，請參閱 [ (direct3d 9 的 Alpha 材質混合) ](alpha-texture-blending.md) 和 [材質混合 (direct3d 9) ](texture-blending.md)。

以 c + + 撰寫的應用程式會使用 [**D3DRS \_ ALPHABLENDENABLE**](./d3drenderstatetype.md) 轉譯狀態來啟用 Alpha 透明度混合。 Direct3D API 允許多種類型的 Alpha 混色。 不過，請務必注意，使用者的3D 硬體可能不支援 Direct3D 所允許的所有混合狀態。

完成的 Alpha 混色類型取決於 [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) 和 **D3DRS \_ DESTBLEND** 轉譯狀態。 來源和目的地 blend 狀態會成對使用。 下列程式碼範例示範如何將來源 blend 狀態設定為 D3DBLEND \_ SRCCOLOR，並將目的地 blend 狀態設定為 D3DBLEND \_ INVSRCCOLOR。


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



改變來源和目的地 blend 狀態可提供霧或塵封大氣中放射物件的外觀。 比方說，如果您的應用程式模型點火、強制欄位、等離子字形狀或類似的 radiant 物件在霧環境中，請將來源和目的地 blend 狀態設定為 D3DBLEND \_ 一。

Alpha 混合的另一個應用是在3D 場景中控制光源，也稱為「光線對應」。 將 [來源 blend 狀態] 設定為 [D3DBLEND \_ 0]，並將 [目的地 blend 狀態] 設定為 [D3DBLEND SRCALPHA] 會 \_ 根據來源 Alpha 資訊來變暗場景。 來源基本型別會用來做為淺色地圖，以調整框架緩衝區的內容，並在適當時將它變得更簡。 這會產生單色燈光對應。

您可以藉由將來源 Alpha 混色狀態設為 D3DBLEND \_ 0，並將目的地 blend 狀態設定為 D3DBLEND SRCCOLOR，來達到色燈對應 \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯狀態](render-states.md)
</dt> </dl>

 

 
