---
title: 磚式資源的區域如何並排顯示
description: 當您建立並排顯示的資源時，維度、格式元素大小，以及 mipmap 和（或）陣列配量的數目 (（如果適用的話）) 決定要備份整個介面區所需的磚數目。
ms.assetid: 834E317F-CFFD-460C-9F89-793081BA1853
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9ae1bf4ad1ca308fb3c93a36c4b3478aabdb0f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990979"
---
# <a name="how-a-tiled-resources-area-is-tiled"></a>磚式資源的區域如何並排顯示

當您建立並排顯示的資源時，維度、格式元素大小，以及 mipmap 和（或）陣列配量的數目 (（如果適用的話）) 決定要備份整個介面區所需的磚數目。 磚內像素/位元組的配置是由實作決定。 可放入磚的像素數目取決於格式項目大小，而且無論您是否使用標準 swizzle 都一樣。

特定表面大小和格式項目寬度所使用的磚數目會妥善定義，並且可根據下列區段中的表格預測。 對於包含 mipmap 的資源或表面維度未填滿磚的案例，某些條件約束存在，並在 [Mipmap 封裝](mipmap-packing.md)中討論。

您可以使用不同的格式，將不同的並排資源指向相同的記憶體，只要應用程式不依賴以某種格式寫入記憶體的結果，並以另一個格式讀取。 但在受限的情況下，應用程式可以依賴以一種格式寫入記憶體的結果，如果格式是相同的格式系列，則會以另一個格式讀取， (也就是說，它們具有相同的無類型父格式) 。 例如，DXGI \_ format \_ R8G8B8A8 \_ UNORM 和 dxgi \_ format \_ R8G8B8A8 UINT 彼此相容， \_ 但不能使用 dxgi \_ format \_ R16G16 \_ UNORM。 應用程式必須謹慎地比對所有資源屬性，才能在兩個材質之間重新解譯資料，因為磚模式非常謹慎地定義。 但很明顯地，格式較不嚴格。 這些格式只需要相容，如上所示。 有一個例外是已妥善定義洩出資料從一種格式更名為另一種：如果磚的所有位元都只包含 0，該磚就可以搭配將這些記憶體內容解譯為 0 的任何格式使用 (無論記憶體配置為何)。 因此，您可以使用格式為 DXGI 格式的 R8 UNORM 將磚清除為0x00， \_ \_ \_ 然後使用格式（例如 dxgi \_ 格式 \_ R32G32 \_ FLOAT），它會顯示內容仍 (0.0 f，0.0 f) 。

磚內的資料版面配置可能取決於資源屬性、其所在的 subresource，以及 subresource 中的磚位置。 主要的例外狀況如下所示：與其他資源屬性相等的相容格式，以及所有材質是否為相同的模式。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                             | 描述                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Texture2D 和 Texture2DArray 子資源拼貼](texture2d-and-texture2darray-subresource-tiling.md)<br/> | 這些表格顯示 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 和 [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) 子資源的並排顯示方式。 <br/>                                                                                                          |
| [Texture3D 子資源拼貼](texture3d-subresource-tiling.md)<br/>                                       | 下表說明 [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) 子資源如何並排顯示。 <br/>                                                                                                                                                                            |
| [緩衝區拼貼](buffer-tiling.md)<br/>                                                                     | 如果大小不是64KB 的倍數，則 [緩衝區](overviews-direct3d-11-resources-buffers.md) 資源會分割成64kb 個磚，並在最後一個磚中顯示一些空白空間。<br/>                                                                                                  |
| [Mipmap 封裝](mipmap-packing.md)<br/>                                                                   | 根據並排顯示資源的支援 [層級](tiled-resources-features-tiers.md) ，具有特定維度的 mipmap 不會遵循標準磚圖形，而且會被視為以不透明的方式將它們封裝在一起。 <br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立磚資源](creating-tiled-resources.md)
</dt> </dl>

 

