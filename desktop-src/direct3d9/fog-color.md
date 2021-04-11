---
description: 圖元和頂點霧化的霧化色彩是透過 D3DRS FOGCOLOR 轉譯狀態來設定 \_ 。 轉譯狀態值可以是任何 RGB 色彩，以指定為 RGBA 色彩。 Alpha 元件會被忽略。
ms.assetid: 76366496-553d-4dbf-868d-d58b5377d36a
title: " (Direct3D 9) 的霧化色彩"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85c9ae217a26ab38be5e3f232fb9dfcd4c2977f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025601"
---
# <a name="fog-color-direct3d-9"></a> (Direct3D 9) 的霧化色彩

圖元和頂點霧化的霧化色彩是透過 D3DRS FOGCOLOR 轉譯狀態來設定 \_ 。 轉譯狀態值可以是任何 RGB 色彩，以指定為 RGBA 色彩。 Alpha 元件會被忽略。

下列 c + + 範例會將霧化色彩設定為白色。


```
/* For this example, the d3dDevice variable is
* a valid pointer to an IDirect3DDevice9 interface.
*/
HRESULT hr;
hr = d3dDevice->SetRenderState(
                    D3DRS_FOGCOLOR,
                    0x00FFFFFF); // Highest 8 bits are not used.
if(FAILED(hr))
    return hr;
```



固定函式管線和可程式化管線會以不同的方式套用霧化。

1.  如果驅動程式支援 D3DPMISCCAPS \_ FOGANDSPECULARALPHA：
    -   如果使用固定函式管線，且 \_ 已設定 D3DRS FOGCOLOR，則圖元著色器中的 v1. w () 等於在霧化 renderstate 中設定的值。
    -   如果使用可程式化管線，則在圖元著色器中 (v1. w) 等於0，即使 oD1 是在頂點著色器中明確寫入。
2.  如果驅動程式不支援 D3DPMISCCAPS \_ FOGANDSPECULARALPHA：
    -   如果使用固定函式管線，並 \_ 設定 D3DRS FOGCOLOR，則圖元著色器中的 v1. w () 等於在霧化 renderstate 中設定的值。
    -   如果 oFog 是在頂點著色器中明確寫入，則在圖元著色器中為 v1. w () 等於 oFog，壓制介於0和1之間。
    -   如果上述兩個案例都不適用，則在圖元著色器中的 v1. w () 等於0，即使 oD1 是在頂點著色器中明確寫入。

如需詳細資訊，請參閱 [D3DPMISCCAPS](d3dpmisccaps.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[霧化類型](fog-types.md)
</dt> </dl>

 

 



