---
title: 具類型的未排序存取視圖 (UAV) 載入
description: 瞭解如何在 Direct3D 12 中 UAV) 具類型的載入 (未排序的存取視圖。 UAV 具型別的 Load 是可讓著色器從具有特定 DXGI_FORMAT 的 UAV 讀取的能力。
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bd45c1b2c14aa85ec9b9ab65cd6d6a9f33cb5e0995ac20b779b84aa7bed640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123475"
---
# <a name="typed-unordered-access-view-uav-loads"></a>具類型的未排序存取視圖 (UAV) 載入

未排序的存取視圖 (UAV) 具類型的負載，是可讓著色器從具有特定 [**DXGI \_ 格式**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)的 UAV 讀取的能力。

-   [概觀](#overview)
-   [支援的格式和 API 呼叫](#supported-formats-and-api-calls)
-   [從 HLSL 使用具類型的 UAV 載入](#using-typed-uav-loads-from-hlsl)
-   [使用 UNORM 和 SNORM 具類型的 UAV 從 HLSL 載入](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

未排序的存取視圖 (UAV) 是未排序存取資源 (的視圖，可包含緩衝區、紋理和材質陣列，但不需要多取樣) 。 UAV 可讓您從多個執行緒暫時未排序的讀取/寫入存取。 這表示此資源類型可以由多個執行緒同時讀取/寫入，而不會產生記憶體衝突。 這項同時存取是透過使用不可部分 [完成的函](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)式來處理。

D3D12 (和 D3D 11.3) 會在可與具類型 UAV 載入搭配使用的格式清單上展開。

## <a name="supported-formats-and-api-calls"></a>支援的格式和 API 呼叫

先前支援下列三種格式的 UAV 載入，並為 D3D 11.0 硬體所需。 所有 D3D 11.3 和 D3D12 硬體都支援它們。

-   R32 \_ 浮點數
-   R32 \_ UINT
-   R32 \_ 聖

以下是在 D3D12 或 D3D 11.3 硬體上支援的格式，因此，如果支援任何一種格式，則會支援所有的格式。

-   R32G32B32A32 \_ 浮點數
-   R32G32B32A32 \_ UINT
-   R32G32B32A32 \_ 聖
-   R16G16B16A16 \_ 浮點數
-   R16G16B16A16 \_ UINT
-   R16G16B16A16 \_ 聖
-   R8G8B8A8 \_ UNORM
-   R8G8B8A8 \_ UINT
-   R8G8B8A8 \_ 聖
-   R16 \_ 浮點數
-   R16 \_ UINT
-   R16 \_ 聖
-   R8 \_ UNORM
-   R8 \_ UINT
-   R8 \_ 聖

D3D12 和 D3D 11.3 硬體上可選擇性且個別支援下列格式，因此必須在每一種格式上進行單一查詢，以測試支援。

-   R16G16B16A16 \_ UNORM
-   R16G16B16A16 \_ SNORM
-   R32G32 \_ 浮點數
-   R32G32 \_ UINT
-   R32G32 \_ 聖
-   R10G10B10A2 \_ UNORM
-   R10G10B10A2 \_ UINT
-   R11G11B10 \_ 浮點數
-   R8G8B8A8 \_ SNORM
-   R16G16 \_ 浮點數
-   R16G16 \_ UNORM
-   R16G16 \_ UINT
-   R16G16 \_ SNORM
-   R16G16 \_ 聖
-   R8G8 \_ UNORM
-   R8G8 \_ UINT
-   R8G8 \_ SNORM
-   R8G8 \_ 聖
-   R16 \_ UNORM
-   R16 \_ SNORM
-   R8 \_ SNORM
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

若要判斷是否支援任何其他格式，請使用 [**D3D12 \_ 功能 \_ 資料 \_ D3D12 \_ 選項**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)結構來呼叫 [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) ，做為第一個參數 (參考) 的 [功能查詢](capability-querying.md)。 如果支援上述的「支援為集合」清單，則會設定 *TypedUAVLoadAdditionalFormats* 欄位。 使用 [**D3D12 \_ 功能 \_ 資料 \_ 格式 \_ 支援**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support)結構，對 **CheckFeatureSupport** 進行第二次呼叫， (檢查傳回的結構是否符合 \_ \_ \_ \_ \_ [**UAV \_ 格式 \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2)列舉) 的 D3D12 格式 SUPPORT2 SUPPORT2 具類型的載入成員，以判斷上述選擇性支援格式清單中的支援，例如：

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a>從 HLSL 使用具類型的 UAV 載入

針對具類型的 UAVs，HLSL 旗標為 D3D \_ 著色器， \_ 需要具 \_ 類型 \_ \_ 的 UAV 載入 \_ 其他 \_ 格式。

以下是處理具型別 UAV 負載的範例著色器程式碼：

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a>使用 UNORM 和 SNORM 具類型的 UAV 從 HLSL 載入

使用具類型的 UAV 載入以從 UNORM 或 SNORM 資源讀取時，您必須將 HLSL 物件的元素類型正確宣告為 `unorm` 或 `snorm` 。 它會指定為未定義的行為，以將 HLSL 中宣告的元素類型與基礎資源資料類型不相符。 例如，如果您在具有 R8 UNORM 資料的緩衝區資源上使用具類型的 UAV 載入 \_ ，則必須將元素類型宣告為 `unorm float` ：

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉譯](rendering.md)
</dt> <dt>

[資源系結](resource-binding.md)
</dt> <dt>

[HLSL 中的資源系結](resource-binding-in-hlsl.md)
</dt> <dt>

[著色器模型5。1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[在 HLSL 中指定根簽章](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 