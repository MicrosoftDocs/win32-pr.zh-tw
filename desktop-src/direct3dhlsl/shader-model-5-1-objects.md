---
title: 著色器模型5.1 物件
description: 下列物件已新增至著色器模型5.1。
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c56fbe035f63bd8f25a8b34377c333c2ce9946c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993855"
---
# <a name="shader-model-51-objects"></a>著色器模型5.1 物件

下列物件已新增至著色器模型5.1。

針對 (D3D 11.3 和 D3D12) 提供的轉譯器 [順序視圖](/windows/desktop/direct3d11/rasterizer-order-views) ，下列物件是新的，而且只能在圖元著色器中使用。 請注意，其支援的方法與對應的 UAV 物件相同。



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| 轉譯器物件                  | UAV 物件                                                    |
| RasterizerOrderedBuffer            | [**RWBuffer**](sm5-object-rwbuffer.md)                       |
| RasterizerOrderedByteAddressBuffer | [**RWByteAddressBuffer**](sm5-object-rwbyteaddressbuffer.md) |
| RasterizerOrderedStructuredBuffer  | [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md)   |
| RasterizerOrderedTexture1D         | [**RWTexture1D**](sm5-object-rwtexture1d.md)                 |
| RasterizerOrderedTexture1DArray    | [**RWTexture1DArray**](sm5-object-rwtexture1darray.md)       |
| RasterizerOrderedTexture2D         | [**RWTexture2D**](sm5-object-rwtexture2d.md)                 |
| RasterizerOrderedTexture2DArray    | [**RWTexture2DArray**](sm5-object-rwtexture2darray.md)       |
| RasterizerOrderedTexture3D         | [**RWTexture3D**](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型5。1](shader-model-5-1.md)
</dt> <dt>

[適用于 Direct3D 12 的 HLSL 著色器模型5.1 功能](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 
