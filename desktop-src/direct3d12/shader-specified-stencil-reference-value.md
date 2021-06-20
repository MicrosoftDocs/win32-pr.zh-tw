---
title: " (Direct3D 12 圖形) 的著色器指定樣板參考值"
description: 瞭解 Direct3D 12 圖形中的樣板參考值。 啟用圖元著色器以使用樣板參考值，可讓您更精確地控制樣板作業。
ms.assetid: F58B1930-F12E-4FA4-A15C-A3C2B8705033
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee212d7c2573402ad38bc19040e5c60a89c090
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408311"
---
# <a name="shader-specified-stencil-reference-value-direct3d-12-graphics"></a><span data-ttu-id="13e91-104"> (Direct3D 12 圖形) 的著色器指定樣板參考值</span><span class="sxs-lookup"><span data-stu-id="13e91-104">Shader Specified Stencil Reference Value (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="13e91-105">啟用圖元著色器以輸出樣板參考值，而不是使用 API 指定的值，讓您能夠對樣板作業進行細微的控制。</span><span class="sxs-lookup"><span data-stu-id="13e91-105">Enabling pixel shaders to output the Stencil Reference Value, rather than using the API-specified one, enables a very fine granular control over stencil operations.</span></span>

<span data-ttu-id="13e91-106">樣板參考值通常是由 [**ID3D12GraphicsCommandList：： OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) 方法所指定。</span><span class="sxs-lookup"><span data-stu-id="13e91-106">The Stencil Reference Value is normally specified by the [**ID3D12GraphicsCommandList::OMSetStencilRef**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref) method.</span></span> <span data-ttu-id="13e91-107">這個方法會針對每個繪製的資料細微性設定樣板參考值。</span><span class="sxs-lookup"><span data-stu-id="13e91-107">This method sets the stencil reference value on a per-draw granularity.</span></span> <span data-ttu-id="13e91-108">不過，圖元著色器可以覆寫這個值。</span><span class="sxs-lookup"><span data-stu-id="13e91-108">However, this value can be overwritten by the pixel shader.</span></span>

<span data-ttu-id="13e91-109">這個 D3D12 (和 D3D 11.3) 功能，可讓開發人員讀取和使用樣板參考值 (*SV \_ StencilRef*) ，此值是圖元著色器的輸出，可啟用每圖元或每個取樣的資料細微性。</span><span class="sxs-lookup"><span data-stu-id="13e91-109">This D3D12 (and D3D11.3) feature enables developers to read and use the Stencil Reference Value (*SV\_StencilRef*) that is output from a pixel shader, enabling a per-pixel or per-sample granularity.</span></span>

<span data-ttu-id="13e91-110">著色器指定的值會取代該調用的 API 指定參考值，這表示變更會影響樣板測試，以及當樣板作業 D3D12 樣板作業 \_ \_ \_ 取代 (D3D12 樣板) [**\_ \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) 的其中一個成員時，會使用它將參考值寫入至樣板緩衝區。</span><span class="sxs-lookup"><span data-stu-id="13e91-110">The shader specified value replaces the API-specified reference value for that invocation, which means the change affects both the stencil test, and when the stencil operation D3D12\_STENCIL\_OP\_REPLACE (one member of [**D3D12\_STENCIL\_OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op)) is used to write the reference value to the stencil buffer.</span></span>

<span data-ttu-id="13e91-111">這項功能在 D3D12 和 D3D 11.3 中都是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="13e91-111">This feature is optional in both D3D12 and D3D11.3.</span></span> <span data-ttu-id="13e91-112">若要測試其支援，請使用 [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)來檢查 [**D3D12 \_ 功能 \_ 資料 \_ D3D12 \_ 選項**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)的 *PSSpecifiedStencilRefSupported* 布林值欄位。</span><span class="sxs-lookup"><span data-stu-id="13e91-112">To test for its support, check the *PSSpecifiedStencilRefSupported* boolean field of [**D3D12\_FEATURE\_DATA\_D3D12\_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) using [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

<span data-ttu-id="13e91-113">以下是在圖元著色器中使用 *SV \_ StencilRef* 的範例：</span><span class="sxs-lookup"><span data-stu-id="13e91-113">Here is an example of the use of *SV\_StencilRef* in a pixel shader:</span></span>

``` syntax
uint main2(float4 c : COORD) : SV_StencilRef
{
    return uint(c.x);
}
```

## <a name="related-topics"></a><span data-ttu-id="13e91-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="13e91-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13e91-115">轉譯</span><span class="sxs-lookup"><span data-stu-id="13e91-115">Rendering</span></span>](rendering.md)
</dt> <dt>

[<span data-ttu-id="13e91-116">HLSL 中的資源系結</span><span class="sxs-lookup"><span data-stu-id="13e91-116">Resource Binding in HLSL</span></span>](resource-binding-in-hlsl.md)
</dt> <dt>

[<span data-ttu-id="13e91-117">著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="13e91-117">Shader Model 5.1</span></span>](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[<span data-ttu-id="13e91-118">在 HLSL 中指定根簽章</span><span class="sxs-lookup"><span data-stu-id="13e91-118">Specifying Root Signatures in HLSL</span></span>](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 
