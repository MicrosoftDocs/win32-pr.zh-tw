---
title: 具類型的未排序存取視圖載入
description: 瞭解在 Direct3D 11 中 UAV) 具類型的載入 (未排序的存取視圖。 UAV 具型別的 Load 是可讓著色器從具有特定 DXGI_FORMAT 的 UAV 讀取的能力。
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7389ba850c68129509ca6b6a835f949dd92f5541382d9fdc2243611d409ca2a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124056"
---
# <a name="typed-unordered-access-view-loads"></a>具類型的未排序存取視圖載入

未排序的存取視圖 (UAV) 具類型的負載，是可讓著色器從具有特定 DXGI 格式的 UAV 讀取的能力 \_ 。

-   [概觀](#overview)
-   [支援的格式和 API 呼叫](#supported-formats-and-api-calls)
-   [從 HLSL 使用具類型的 UAV 載入](#using-typed-uav-loads-from-hlsl)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

未排序的存取視圖 (UAV) 是未排序存取資源 (的視圖，可包含緩衝區、紋理和材質陣列，但不需要多取樣) 。 UAV 可讓您從多個執行緒暫時未排序的讀取/寫入存取。 這表示此資源類型可以由多個執行緒同時讀取/寫入，而不會產生記憶體衝突。 這項同時存取是透過使用不可部分 [完成的函](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)式來處理。

D3D12 和 D3D 11.3 會展開可搭配具類型 UAV 載入的格式清單。

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
-   8G8 \_ 聖
-   R16 \_ UNORM
-   R16 \_ SNORM
-   R8 \_ SNORM
-   A8 \_ UNORM
-   B5G6R5 \_ UNORM
-   B5G5R5A1 \_ UNORM
-   B4G4R4A4 \_ UNORM

若要判斷是否支援任何其他格式，請使用 [**D3D11 \_ 功能 \_ 資料 \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2)結構來呼叫 [**ID3D11Device：： CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)做為第一個參數。 `TypedUAVLoadAdditionalFormats`如果支援上述的「支援為集合」清單，則會設定位。 使用 [**D3D11 \_ 功能 \_ 資料 \_ 格式 \_ SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2)結構，對 **CheckFeatureSupport** 進行第二次呼叫， (檢查傳回的結構是否針對 \_ \_ \_ \_ \_ [**SUPPORT2 \_ 格式 \_ UAV**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)列舉) 的 D3D12 格式 D3D11 SUPPORT2 具類型的載入成員，以判斷上述選擇性支援格式清單中的支援，例如：

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
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

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 11.3 功能](direct3d-11-3-features.md)
</dt> <dt>

[著色器模型5。1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 