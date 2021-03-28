---
title: Texture2D 和 Texture2DArray 子資源拼貼
description: 這些表格顯示了 Texture2D 和 Texture2DArray 子資源拼接的方式。
ms.assetid: 3CFA384D-2C49-4BB2-9A92-FC45B1A499B5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a7ded22fcb7e7e476a701c7db3063dfae33fda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375969"
---
# <a name="texture2d-and-texture2darray-subresource-tiling"></a>Texture2D 和 Texture2DArray 子資源拼貼

這些表格顯示 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 和 [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) 子資源的並排顯示方式。 這些表格中的數值並未計入結尾 mip 包裝。

下表顯示了 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 和多重採樣次數為 1 之 [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) 子資源拼接的方式。



| 位元數/像素 (1 個樣本/像素) | 磚的維度 (像素，寬 x 高) |
|-----------------------------|-------------------------------|
| 8                           | 256 x 256                       |
| 16                          | 256 x 128                       |
| 32                          | 128 x 128                       |
| 64                          | 128 x 64                        |
| 128                         | 64x64                         |
| BC1,4                       | 512 x 256                       |
| BC2,3,5,6,7                 | 256 x 256                       |



 

並排顯示的資源不支援格式位元數目為 96 bpp 格式、影片格式、DXGI \_ 格式 \_ R1 \_ UNORM、dxgi \_ 格式 \_ R8G8 \_ B8G8 \_ UNORM 和 dxgi \_ 格式 \_ R8R8 \_ G8B8 UNORM \_ 。

下表顯示了 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 和多重採樣次數超過 1 之 [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) 子資源拼接的方式。



| 多級取樣計數           |  (WxH 來分割上方的磚維度)  |
|-----------------------------|-------------------------------|
| 1                           | 1 x 1                           |
| 2                           | 2 x 1                           |
| 4                           | 2 x 2                           |
| 8                           | 4 x 2                           |
| 16                          | 4x4                           |



 

 (只需要取樣計數1和4，而且可讓磚的資源支援) 。 並排顯示的資源目前不支援2、8和16，但仍會顯示。

即使磚的資源不支援，您也可以選擇支援2、8及/或16個取樣的多重取樣消除鋸齒， (MSAA) 模式的非並排資源。

使用大於1的取樣計數來將資源並排顯示，無法使用 128 bpp 格式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚式資源的區域如何並排顯示](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 