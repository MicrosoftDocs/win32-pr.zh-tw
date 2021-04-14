---
title: Texture3D 子資源拼貼
description: 下表顯示了 Texture3D 子資源的拼接方式。
ms.assetid: D0CDD652-AE8E-40A4-BA05-E743B0757AFA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7a668f499a2f6d3911716d5d7bad60df4cd9e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991026"
---
# <a name="texture3d-subresource-tiling"></a>Texture3D 子資源拼貼

下表說明 [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d) 子資源如何並排顯示。 此表格中的數值並未計入結尾 mip 包裝。

此表格利用了 [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) 拼接，將 x 及 y 維度各除以 4，並且增加了 16 層的深度。 所有第一個平面的磚 (2D 磚的平面定義了前 16 層深度) 都會在後續平面之前顯示。

> [!Note]  
> 磚資源的 [**Texture3D**](/windows/desktop/direct3dhlsl/sm5-object-texture3d)支援不會在初始的並排資源執行中公開，但所需的磚圖形會在此列出，因為未來版本中可能會考慮到支援。

 



| 位元數/像素 (1 個樣本/像素) | 磚尺寸 (像素，寬 x 高 x 深) |
|-----------------------------|---------------------------------|
| 8                           | 64 x 32 x 32                        |
| 16                          | 32 x 32 x 32                        |
| 32                          | 32 x 32 x 16                        |
| 64                          | 32 x 16 x 16                        |
| 128                         | 16 x 16 x 16                        |
| BC1,4                       | 128 x 64 x 16                       |
| BC2,3,5,6,7                 | 64 x 64 x 16                        |



 

並排顯示的資源不支援格式位元數目為 96 bpp 格式、影片格式、DXGI \_ 格式 \_ R1 \_ UNORM、dxgi \_ 格式 \_ R8G8 \_ B8G8 \_ UNORM 和 dxgi \_ 格式 \_ R8R8 \_ G8B8 UNORM \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚式資源的區域如何並排顯示](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 