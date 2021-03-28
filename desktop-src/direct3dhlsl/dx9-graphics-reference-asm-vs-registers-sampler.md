---
title: " (Direct3D 9 asm 的取樣器-vs) "
description: 取樣器是頂點著色器的輸入虛擬登錄，用來識別取樣階段。 有四個頂點著色器 s0 至 s3。 您可以在單一著色器階段中讀取四個材質表面。
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- '取樣器，輸入 (Direct3D 9 asm-vs) '
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382742"
---
# <a name="sampler-direct3d-9-asm-vs"></a> (Direct3D 9 asm 的取樣器-vs) 

取樣器是頂點著色器的輸入虛擬登錄，用來識別取樣階段。 有四個頂點著色器取樣器： s0 至 s3。 您可以在單一著色器階段中讀取四個材質表面。

 (Direct3D 9 asm-vs) s 的取樣器是虛擬暫存器，因為您無法直接讀取或寫入它們。

取樣單位會對應至材質取樣階段，封裝 [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)所提供的取樣特定狀態。 每個取樣器都會唯一識別單一材質介面，此介面會使用 [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)設定為對應的取樣器。 不過，您可以在多個取樣器設定相同的材質介面。

在繪圖時，紋理不能同時設定為轉譯目標和某個階段的材質。

由於有四個取樣器，因此在單一著色器階段中最多可以讀取四個材質表面。 取樣器可能會在材質載入指示中顯示為唯一的引數： [texldl-vs](texldl---vs.md)。

在 vs \_ 3 \_ 0 中，如果使用取樣器，則必須在著色器程式的開頭使用 samplerType 來宣告， [ \_ (sm3-vs asm) ](dcl-samplertype---vs.md) 指令。



| 頂點著色器版本 | 1\_1 | 2 \_ 0 | 2個 \_ sw | 2 \_ x | 3 \_ 0 | 3個 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| 取樣器                |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點著色器暫存器](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[Vs \_ 3 \_ 0 (DirectX HLSL) 的頂點紋理 ](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 