---
title: 功能查詢
description: '您的應用程式可以透過呼叫 ID3D12Device CheckFeatureSupport，探索資源系結的支援層級以及許多其他功能 \: \: 。'
ms.assetid: ECBAF8EF-5D91-46D8-9D6E-A7FA4203B9F8
ms.date: 11/26/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: eaf451f91d51cfa6e900f328898c3418f0974a2d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548374"
---
# <a name="capability-querying"></a>功能查詢

您的應用程式可以透過呼叫 [**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)，探索資源系結的支援層級 (以及許多其他功能) 的支援層級。

## <a name="how-to-query-for-the-resource-binding-tier"></a>如何查詢資源系結層

第一個範例著重于資源系結。 每個資源系結層都是功能較低層級的超集合，因此在指定層上運作的程式碼在任何較高的層級上都不會變更。

資源系結層是 [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) 列舉中的常數。

若要查詢資源系結層，請使用如下所示的程式碼。 這個程式碼範例會示範查詢各種功能支援類型的一般模式。

```cppwinrt
D3D12_RESOURCE_BINDING_TIER get_resource_binding_tier(::ID3D12Device* pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &featureSupport, sizeof(featureSupport))
    );

    switch (featureSupport.ResourceBindingTier)
    {
    case D3D12_RESOURCE_BINDING_TIER_1:
        // Tier 1 is supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_2:
        // Tiers 1 and 2 are supported.
        break;

    case D3D12_RESOURCE_BINDING_TIER_3:
        // Tiers 1, 2, and 3 are supported.
        break;
    }

    return featureSupport.ResourceBindingTier;
}
```

請注意，在此情況下，您傳遞 ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)的任何列舉常數，) 都有對應的資料結構，可接收該功能或一組功能的相關資訊 ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)，在此案例中) 。 一律傳遞符合您傳遞的列舉常數之結構的指標。

## <a name="how-to-query-for-any-feature-level"></a>如何查詢任何功能等級

除了資源系結層之外，還有許多其他功能，您可以使用上述程式碼範例中所示的相同模式來查詢其支援層級。 您只需將不同的常數從 [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) 列舉傳遞給 [**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (，告訴 API 哪些功能要求) 上的支援資訊，然後將指標傳遞至相符結構 (的實例，以接收要求的資訊) 。

- 傳遞 **D3D12_FEATURE_ARCHITECTURE** 並 [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture)。
- 傳遞 **D3D12_FEATURE_ARCHITECTURE1** 並 [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1)。
- 傳遞 **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** 並 [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority)。
- 傳遞 **D3D12_FEATURE_CROSS_NODE** 並 [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node)。
- 傳遞 **D3D12_FEATURE_D3D12_OPTIONS** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)。
- 傳遞 **D3D12_FEATURE_D3D12_OPTIONS1** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1)。
- 傳遞 **D3D12_FEATURE_D3D12_OPTIONS2** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2)。
- 傳遞 **D3D12_FEATURE_D3D12_OPTIONS3** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3)。
- 傳遞 **D3D12_FEATURE_D3D12_OPTIONS4** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4)。
- 傳遞 **D3D12_FEATURE_D3D12_OPTIONS5** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5)。
- 傳遞 **D3D12_FEATURE_EXISTING_HEAPS** 並 [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps)。
- 傳遞 **D3D12_FEATURE_FEATURE_LEVELS** 並 [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels)。
- 傳遞 **D3D12_FEATURE_FORMAT_INFO** 並 [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)。
- 傳遞 **D3D12_FEATURE_FORMAT_SUPPORT** 並 [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support)。
- 傳遞 **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** 並 [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support)。
- 傳遞 **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** 並 [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels)。
- 傳遞 **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** 並 [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support)。
- 傳遞 **D3D12_FEATURE_ROOT_SIGNATURE** 並 [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature)。
- 傳遞 **D3D12_FEATURE_SERIALIZATION** 並 [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization)。
- 傳遞 **D3D12_FEATURE_SHADER_CACHE** 並 [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache)。
- 傳遞 **D3D12_FEATURE_SHADER_MODEL** 並 [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model)。

## <a name="hardware-support-for-dxgi-formats"></a>DXGI 格式的硬體支援

若要查看 DXGI 格式和硬體功能的表格，請參閱這些主題。

- [Direct3D 功能等級12.1 硬體的 DXGI 格式支援](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [Direct3D 功能等級12.0 硬體的 DXGI 格式支援](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [Direct3D 功能等級11.1 硬體的 DXGI 格式支援](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [Direct3D 功能等級11.0 硬體的 DXGI 格式支援](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- [Direct3D 10Level9 格式的硬體支援](/previous-versions//ff471324(v=vs.85))
- [Direct3D 10.1 格式的硬體支援](/previous-versions//cc627091(v=vs.85))
- [適用于 Direct3D 10 格式的硬體支援](/previous-versions//cc627090(v=vs.85))

## <a name="related-topics"></a>相關主題

* [Direct3D 12 中的資源繫結](resource-binding.md)
* [硬體功能等級](hardware-feature-levels.md)
* [根簽章](root-signatures.md)