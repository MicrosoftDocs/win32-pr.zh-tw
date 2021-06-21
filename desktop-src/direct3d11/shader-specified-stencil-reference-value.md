---
title: " (Direct3D 11 圖形) 的著色器指定樣板參考值"
description: 瞭解 Direct3D 11 圖形中的樣板參考值。 啟用圖元著色器以使用樣板參考值，可讓您更精確地控制樣板作業。
ms.assetid: 6E336623-9746-4872-ADC1-C5489F53D7AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e8a34d53bc7f30dc2a91fafabb561dff7a1e96
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408101"
---
# <a name="shader-specified-stencil-reference-value-direct3d-11-graphics"></a><span data-ttu-id="0208f-104"> (Direct3D 11 圖形) 的著色器指定樣板參考值</span><span class="sxs-lookup"><span data-stu-id="0208f-104">Shader Specified Stencil Reference Value (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="0208f-105">啟用圖元著色器以輸出樣板參考值，而不是使用 API 指定的值，讓您能夠對樣板作業進行細微的控制。</span><span class="sxs-lookup"><span data-stu-id="0208f-105">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="0208f-106">著色器指定的值會取代該調用的 API 指定樣板 *參考值* ，這表示變更會影響樣板測試，而當樣板 op D3D11 樣板 \_ \_ op \_ 取代 (其中一個 D3D11 樣板 op 的成員時，會使用 [**樣板 \_ \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) 的成員將參考值寫入至樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0208f-106">The shader specified value replaces the API-specified *Stencil Reference Value* for that invocation, which means the change affects both the stencil test, and when stencil op D3D11\_STENCIL\_OP\_REPLACE (one member of [**D3D11\_STENCIL\_OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="0208f-107">在舊版的 D3D11 中，樣板參考值只能由 [**>id3d11devicecoNtext：： OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) 方法指定。</span><span class="sxs-lookup"><span data-stu-id="0208f-107">In earlier versions of D3D11, the Stencil Reference Value can only be specified by the [**ID3D11DeviceContext::OMSetDepthStencilState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate) method.</span></span> <span data-ttu-id="0208f-108">這表示此值只能在個別繪製的資料細微性上定義。</span><span class="sxs-lookup"><span data-stu-id="0208f-108">This means that this value can only be defined on a per-draw granularity.</span></span> <span data-ttu-id="0208f-109">這項 D3D 11.3 功能可讓開發人員讀取和使用樣板參考值 (`SV_StencilRef`) 是圖元著色器的輸出，這表示可以針對每個圖元或每個取樣的資料細微性來指定。</span><span class="sxs-lookup"><span data-stu-id="0208f-109">This D3D11.3 feature enables developers to read and use the Stencil Reference Value (`SV_StencilRef`) that is output from a pixel shader, meaning that it can be specified on a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="0208f-110">這是 D3D 11.3 中的選擇性功能。</span><span class="sxs-lookup"><span data-stu-id="0208f-110">This feature is optional in D3D11.3.</span></span> <span data-ttu-id="0208f-111">若要測試其支援，請 `PSSpecifiedStencilRefSupported` 使用 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)來檢查 [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2)的布林值欄位。</span><span class="sxs-lookup"><span data-stu-id="0208f-111">To test for its support, check the `PSSpecifiedStencilRefSupported` boolean field of [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) using [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)</span></span>

<span data-ttu-id="0208f-112">以下是 `SV_StencilRef` 在圖元著色器中使用的範例：</span><span class="sxs-lookup"><span data-stu-id="0208f-112">Here is an example of the use of `SV_StencilRef` in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="0208f-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="0208f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0208f-114">Direct3D 11.3 功能</span><span class="sxs-lookup"><span data-stu-id="0208f-114">Direct3D 11.3 Features</span></span>](direct3d-11-3-features.md)
</dt> <dt>

[<span data-ttu-id="0208f-115">著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="0208f-115">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 
