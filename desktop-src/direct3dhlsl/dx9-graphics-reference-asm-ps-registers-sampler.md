---
title: " (Direct3D 9 asm-ps) 的取樣器"
description: 取樣器是圖元著色器的輸入虛擬註冊，用來識別取樣階段。
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- '取樣器，輸入 (Direct3D 9 asm-ps) '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023654"
---
# <a name="sampler-direct3d-9-asm-ps"></a> (Direct3D 9 asm-ps) 的取樣器

取樣器是圖元著色器的輸入虛擬註冊，用來識別取樣階段。 有16個圖元著色器取樣階段暫存器： s0 至 s15。 因此，您可以在單一著色器階段中讀取最多16個材質表面。 使用取樣器註冊的指示為 texld 和 texldp。

在搭配使用 [ \_ (sm2、sm3-ps asm) ](dcl-samplertype---ps.md) 指令的 dcl 之前，必須先宣告取樣器。



| 圖元著色器版本 | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| 取樣器               |      |      |      |      | x    | x     | x    | x    | x     |



 

取樣器是虛擬暫存器，因為您無法直接讀取或寫入它們。

取樣單位會對應至材質取樣階段，封裝 [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)所提供的取樣特定狀態。 每個取樣器都會唯一識別單一材質介面，此介面會使用 [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)設定為對應的取樣器。 不過，您可以在多個取樣器設定相同的材質介面。

在繪圖時，紋理不能同時設定為轉譯目標和某個階段的材質。

取樣器可能會顯示為材質載入指令中的唯一引數： [texldl-ps](texldl---ps.md)。

在 ps \_ 3 \_ 0 中，如果使用取樣器，則必須使用 [dcl \_ samplerType (sm2、sm3 ps asm) ](dcl-samplertype---ps.md) 指令，在著色器程式的開頭宣告它。

使用具有較高維度的材質來取樣紋理座標中的材質不合法。 以較低的維度來取樣紋理座標中的材質將會忽略額外的材質座標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[寄存 器](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 