---
description: Direct3D 應用程式可透過在多個轉譯階段套用各種紋理到基本類型，達到多項特效。
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Multipass (Direct3D 9) 的材質混合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109149"
---
# <a name="multipass-texture-blending-direct3d-9"></a>Multipass (Direct3D 9) 的材質混合

Direct3D 應用程式可透過在多個轉譯階段套用各種紋理到基本類型，達到多項特效。 針對此一行動的常用字詞為多階段紋理混色。 多重紋理混合的一般用途為藉由套用數種不同紋理的多重色彩，模擬複雜光源和著色模型的效果。 這類應用方式稱為光線對應。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質燈光對應 ](light-mapping-with-textures.md)。

> [!Note]  
> 某些裝置能夠在單一階段中將多個紋理套用至基本專案。 如需詳細資訊，請參閱 [ (Direct3D 9) 的材質混色 ](texture-blending.md)。

 

如果使用者的硬體不支援多重紋理混合，您的應用程式可以使用多重紋理混合來達到相同的視覺效果。 不過，當使用多重紋理混合時，應用程式無法維持可行的畫面播放速率。

在 C/c + + 應用程式中執行 multipass 材質混色。

1.  藉由呼叫 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 方法，設定材質階段0中的材質。
2.  使用 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 方法，選取想要的色彩和 Alpha 混合引數和作業。 預設值適用於多重紋理混合。
3.  在場景中呈現適當物件。
4.  在紋理階段 0 設定下一個紋理。
5.  設定 D3DRS \_ SRCBLEND 和 D3DRS \_ DESTBLEND 轉譯狀態，以視需要調整來源和目的地混合因素。 系統根據這些參數，在呈現目標表面中混合新紋理與現有像素。
6.  視需要盡量使用紋理重複步驟 3、4 及 5。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[材質混色](texture-blending.md)
</dt> </dl>

 

 
