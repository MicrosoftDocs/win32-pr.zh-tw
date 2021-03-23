---
title: 直接在根簽章中使用描述項
description: 應用程式可以直接將描述項放在根簽章中，以避免需要經過描述元堆積。
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd97a7d68f5c9b51b6d15d3b71c6e30d04bb36e5
ms.sourcegitcommit: 83afb2f3e9e5d37f3f5a11e975515e9ed8b044ff
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/15/2020
ms.locfileid: "104548454"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>直接在根簽章中使用描述項

應用程式可以直接將描述項放在根簽章中，以避免需要經過描述元堆積。 這些描述項會在根簽章中佔用大量空間 (請參閱) 的根簽章限制一節，讓應用程式必須謹慎使用它們。

使用方式的範例是將常數緩衝區視圖 (CBV，以在根配置中變更每個繪圖的) ，如此一來，應用程式就不需要配置描述元堆積空間，如此一來，應用程式就不需要為每個 (繪圖配置描述中繼資料表，然後將描述中繼資料表指向描述項堆積) 的新位置。 藉由將某個內容放在根簽章中，應用程式只會將版本控制責任交給驅動程式，但這是它們已經有的基礎結構。

如果是使用極少資源的轉譯，則如果所有所需的描述項都可以直接放在根簽章中，就可能完全不需要描述項資料表/堆積用途。

根簽章中唯一支援的描述項類型為：
- CBVs.
- 著色器資源檢視 (SRVs) /Unordered 存取權視圖 (UAVs) 緩衝區資源，其中 SRV/UAV 格式只包含32位 FLOAT/UINT/聖中的元件 (沒有格式轉換) 。
- 在本機或全域根簽章中，raytracing 加速結構的 SRVs。 

根目錄中的 UAVs 不能有與其相關聯的計數器。 根簽章中的描述項會顯示為個別個別的描述元， &mdash; 但無法動態建立索引。

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

在上述範例中， `mySceneData` 無法宣告為數組，例如， `cbuffer mySceneData[2]` 如果它會對應至根簽章中的描述元，則在根簽章中不支援跨描述元編制索引。 應用程式可以定義個別的個別常數緩衝區，並在需要時將它們定義為根簽章中的個別專案。 請注意，在上述的範圍中 `mySceneData` ，有一個陣列 `bar[2]` 。 常數緩衝區內的動態索引是有效的-根簽章中的描述項的行為就像是透過描述元堆積存取相同的描述項。 這與直接在根簽章中的內嵌常數不同，它也像常數緩衝區一樣出現，但條件約束不允許內嵌常數內的動態索引編制，因此不允許這種情況 `bar[2]` 。

下列 (自 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面的 api) 適用于直接在根簽章上設定描述項：

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!Note]  
> Direct3D 12 沒有「根描述元陣列」的概念。 描述項陣列只在描述元堆積中受到支援。

## <a name="related-topics"></a>相關主題

[根簽章](root-signatures.md)
