---
title: 直接在根簽章中使用描述項
description: 若要避免需要經過描述項堆積，您可以直接將描述項放入根簽章中。
ms.assetid: 033E3D8F-3003-42F7-BF77-68A7D62802E5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff9d459f3195a4cf722ea210edbe63e5c1bf3cc8
ms.sourcegitcommit: 170bc12e9724d00cecbb96d57c7226c51e135dee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113489170"
---
# <a name="using-descriptors-directly-in-the-root-signature"></a>直接在根簽章中使用描述項

若要避免需要經過描述項堆積，您可以直接將描述項放入根簽章中。 這些描述項會佔用根簽章中的大量空間 (請參閱) 的根簽章 [限制](/windows/win32/direct3d12/root-signature-limits) ，因此建議您謹慎使用。

使用方式的範例是在根配置中放置一個常數緩衝區視圖， (CBV) 變更每個繪製。 如此一來，就不需要由應用程式每次繪製來配置描述元堆積空間 (並將描述項資料表指向描述項堆積) 的新位置。 藉由將某個內容放在根簽章中，應用程式只會將版本控制責任交給驅動程式;但那就是驅動程式已經有的基礎結構。

如果是使用極少資源的轉譯，則如果所有所需的描述項都可以直接放在根簽章中，就可能完全不需要描述項資料表/堆積用途。

這些是根簽章中唯一支援的描述項類型。

- 常數緩衝區視圖 (CBVs) 。
- 著色器資源檢視 (SRVs) /未排序的存取權視圖 (UAVs 不需要格式轉換的緩衝區資源)  (不具類型的緩衝區) 。 可以與根描述元系結的不具類型緩衝區的一些範例包括 `StructuredBuffer<type>` 、 `RWStructuredBuffer<type>` `ByteAddressBuffer` 和 `RWByteAddressBuffer` 。 具類型的緩衝區（例如 `Buffer<uint>` 和） `Buffer<float2>` 不能。
- 在本機或全域根簽章中，raytracing 加速結構的 SRVs。 

根目錄中的 UAV 不能有與其相關聯的計數器。 根簽章中的描述項會顯示為個別個別的描述元， &mdash; 但無法動態建立索引。

``` syntax
struct SceneData
{
   uint foo;
   float bar[2];
   int moo;
};
ConstantBuffer<SceneData> mySceneData : register(b6);
```

在上述範例中， `mySceneData` 不能宣告為數組， `cbuffer mySceneData[2]` 如果它將會對應到根簽章中的描述元。 這是因為根簽章不支援跨描述元索引。 如有需要，您可以定義不同的個別常數緩衝區，並將它們定義為根簽章中的個別專案。 請注意，在上述的範圍中 `mySceneData` ，有一個陣列 `bar[2]` 。 在常數緩衝區內的動態索引是有效的，因為根簽章中的描述元所 &mdash; 表現的行為，就像是透過描述元堆積存取相同的描述項一樣。 這與直接在根簽章中的內嵌常數（也像常數緩衝區一樣）相同，但不允許在內嵌常數內動態編制索引的條件約束，因此不允許這種情況 `bar[2]` 。

從 [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面 (的這些 api) 適用于直接在根簽章上設定描述項。

-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetGraphicsRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootconstantbufferview)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetGraphicsRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootshaderresourceview)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetGraphicsRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootunorderedaccessview)

> [!NOTE]  
> Direct3D 12 沒有 *根描述元陣列* 的概念。 描述項陣列只在描述元堆積中受到支援。

## <a name="related-topics"></a>相關主題

* [根簽章](root-signatures.md)
