---
title: " (Direct3D 11 圖形) 的著色器指定樣板參考值"
description: 啟用圖元著色器以輸出樣板參考值，而不是使用 API 指定的值，讓您能夠對樣板作業進行細微的控制。
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a089ec8ab56a1cf00021f97bb40cf86fe42f04
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104316979"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a> (Direct3D 11 圖形) 的著色器指定樣板參考值

啟用圖元著色器以輸出樣板參考值，而不是使用 API 指定的值，讓您能夠對樣板作業進行細微的控制。

著色器指定的值會取代該調用的 API 指定樣板 *參考值* ，這表示變更會影響樣板測試，而當樣板 op D3D11 樣板 \_ \_ op \_ 取代 (其中一個 D3D11 樣板 op 的成員時，會使用 [**樣板 \_ \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) 的成員將參考值寫入至樣板緩衝區。

在舊版的 D3D11 中，樣板參考值只能由 [**>id3d11devicecoNtext：： OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) 方法指定。 這表示此值只能在個別繪製的資料細微性上定義。 這項 D3D 11.3 功能可讓開發人員讀取和使用樣板參考值 (`SV_StencilRef`) 是圖元著色器的輸出，這表示可以針對每個圖元或每個取樣的資料細微性來指定。

這是 D3D 11.3 中的選擇性功能。 若要測試其支援，請 `PSSpecifiedStencilRefSupported` 使用 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)來檢查 [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2)的布林值欄位。

以下是 `SV_StencilRef` 在圖元著色器中使用的範例：

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11.3 功能](direct3d-11-3-features.md)
</dt> <dt>

[著色器模型5。1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
