---
title: " (Direct3D 12 圖形) 的著色器指定樣板參考值"
description: 啟用圖元著色器以輸出樣板參考值，而不是使用 API 指定的值，讓您能夠對樣板作業進行細微的控制。
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a8b7697cc06594b3e2ffc717cbded9e6832129
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548411"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a> (Direct3D 12 圖形) 的著色器指定樣板參考值

啟用圖元著色器以輸出樣板參考值，而不是使用 API 指定的值，讓您能夠對樣板作業進行細微的控制。

樣板參考值通常是由 [**ID3D12GraphicsCommandList：： OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) 方法所指定。 這個方法會針對每個繪製的資料細微性設定樣板參考值。 不過，圖元著色器可以覆寫這個值。

這個 D3D12 (和 D3D 11.3) 功能，可讓開發人員讀取和使用樣板參考值 (*SV \_ StencilRef*) ，此值是圖元著色器的輸出，可啟用每圖元或每個取樣的資料細微性。

著色器指定的值會取代該調用的 API 指定參考值，這表示變更會影響樣板測試，以及當樣板作業 D3D12 樣板作業 \_ \_ \_ 取代 (D3D12 樣板) [**\_ \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) 的其中一個成員時，會使用它將參考值寫入至樣板緩衝區。

這項功能在 D3D12 和 D3D 11.3 中都是選擇性的。 若要測試其支援，請使用 [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)來檢查 [**D3D12 \_ 功能 \_ 資料 \_ D3D12 \_ 選項**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)的 *PSSpecifiedStencilRefSupported* 布林值欄位。

以下是在圖元著色器中使用 *SV \_ StencilRef* 的範例：

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯](rendering.md)
</dt> <dt>

[HLSL 中的資源系結](resource-binding-in-hlsl.md)
</dt> <dt>

[著色器模型5。1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[在 HLSL 中指定根簽章](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
