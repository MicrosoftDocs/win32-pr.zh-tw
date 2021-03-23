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
# <a name="capability-querying"></a><span data-ttu-id="d28d6-103">功能查詢</span><span class="sxs-lookup"><span data-stu-id="d28d6-103">Capability querying</span></span>

<span data-ttu-id="d28d6-104">您的應用程式可以透過呼叫 [**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)，探索資源系結的支援層級 (以及許多其他功能) 的支援層級。</span><span class="sxs-lookup"><span data-stu-id="d28d6-104">Your application can discover the level of support for resource binding (as well as the level of support for many other features), with a call to [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>

## <a name="how-to-query-for-the-resource-binding-tier"></a><span data-ttu-id="d28d6-105">如何查詢資源系結層</span><span class="sxs-lookup"><span data-stu-id="d28d6-105">How to query for the resource binding tier</span></span>

<span data-ttu-id="d28d6-106">第一個範例著重于資源系結。</span><span class="sxs-lookup"><span data-stu-id="d28d6-106">This first example focuses on resource binding.</span></span> <span data-ttu-id="d28d6-107">每個資源系結層都是功能較低層級的超集合，因此在指定層上運作的程式碼在任何較高的層級上都不會變更。</span><span class="sxs-lookup"><span data-stu-id="d28d6-107">Each resource binding tier is a superset of lower tiers in functionality, so code that works on a given tier works unchanged on any higher tier.</span></span>

<span data-ttu-id="d28d6-108">資源系結層是 [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) 列舉中的常數。</span><span class="sxs-lookup"><span data-stu-id="d28d6-108">The resource binding tiers are constants in the [**D3D12_RESOURCE_BINDING_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_binding_tier) enumeration.</span></span>

<span data-ttu-id="d28d6-109">若要查詢資源系結層，請使用如下所示的程式碼。</span><span class="sxs-lookup"><span data-stu-id="d28d6-109">To query for the resource binding tier, use code such as this.</span></span> <span data-ttu-id="d28d6-110">這個程式碼範例會示範查詢各種功能支援類型的一般模式。</span><span class="sxs-lookup"><span data-stu-id="d28d6-110">This code example demonstrates the general pattern for querying for any of the various kinds of feature support.</span></span>

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

<span data-ttu-id="d28d6-111">請注意，在此情況下，您傳遞 ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)的任何列舉常數，) 都有對應的資料結構，可接收該功能或一組功能的相關資訊 ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)，在此案例中) 。</span><span class="sxs-lookup"><span data-stu-id="d28d6-111">Note that any enumerated constant that you pass ([**D3D12_FEATURE_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature), in this case) has a corresponding data structure that receives info about that feature or set of features ([**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options), in this case).</span></span> <span data-ttu-id="d28d6-112">一律傳遞符合您傳遞的列舉常數之結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d28d6-112">Always pass a pointer to the structure that matches the enumerated constant that you pass.</span></span>

## <a name="how-to-query-for-any-feature-level"></a><span data-ttu-id="d28d6-113">如何查詢任何功能等級</span><span class="sxs-lookup"><span data-stu-id="d28d6-113">How to query for any feature level</span></span>

<span data-ttu-id="d28d6-114">除了資源系結層之外，還有許多其他功能，您可以使用上述程式碼範例中所示的相同模式來查詢其支援層級。</span><span class="sxs-lookup"><span data-stu-id="d28d6-114">As well as the resource binding tier, there are many other features whose level of support you can query for using the same pattern shown in the code example above.</span></span> <span data-ttu-id="d28d6-115">您只需將不同的常數從 [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) 列舉傳遞給 [**ID3D12Device：： CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (，告訴 API 哪些功能要求) 上的支援資訊，然後將指標傳遞至相符結構 (的實例，以接收要求的資訊) 。</span><span class="sxs-lookup"><span data-stu-id="d28d6-115">You just pass a different constant from the [**D3D12_FEATURE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature) enumeration to [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) (to tell the API what feature to request support information on), and you pass a pointer to an instance of the matching structure (in which to receive the requested info).</span></span>

- <span data-ttu-id="d28d6-116">傳遞 **D3D12_FEATURE_ARCHITECTURE** 並 [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-116">Pass **D3D12_FEATURE_ARCHITECTURE** and [**D3D12_FEATURE_DATA_ARCHITECTURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture).</span></span>
- <span data-ttu-id="d28d6-117">傳遞 **D3D12_FEATURE_ARCHITECTURE1** 並 [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-117">Pass **D3D12_FEATURE_ARCHITECTURE1** and [**D3D12_FEATURE_DATA_ARCHITECTURE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture1).</span></span>
- <span data-ttu-id="d28d6-118">傳遞 **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** 並 [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-118">Pass **D3D12_FEATURE_COMMAND_QUEUE_PRIORITY** and [**D3D12_FEATURE_DATA_COMMAND_QUEUE_PRIORITY**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_command_queue_priority).</span></span>
- <span data-ttu-id="d28d6-119">傳遞 **D3D12_FEATURE_CROSS_NODE** 並 [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-119">Pass **D3D12_FEATURE_CROSS_NODE** and [**D3D12_FEATURE_DATA_CROSS_NODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_cross_node).</span></span>
- <span data-ttu-id="d28d6-120">傳遞 **D3D12_FEATURE_D3D12_OPTIONS** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-120">Pass **D3D12_FEATURE_D3D12_OPTIONS** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options).</span></span>
- <span data-ttu-id="d28d6-121">傳遞 **D3D12_FEATURE_D3D12_OPTIONS1** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-121">Pass **D3D12_FEATURE_D3D12_OPTIONS1** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options1).</span></span>
- <span data-ttu-id="d28d6-122">傳遞 **D3D12_FEATURE_D3D12_OPTIONS2** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-122">Pass **D3D12_FEATURE_D3D12_OPTIONS2** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS2**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options2).</span></span>
- <span data-ttu-id="d28d6-123">傳遞 **D3D12_FEATURE_D3D12_OPTIONS3** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-123">Pass **D3D12_FEATURE_D3D12_OPTIONS3** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS3**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3).</span></span>
- <span data-ttu-id="d28d6-124">傳遞 **D3D12_FEATURE_D3D12_OPTIONS4** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-124">Pass **D3D12_FEATURE_D3D12_OPTIONS4** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS4**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options4).</span></span>
- <span data-ttu-id="d28d6-125">傳遞 **D3D12_FEATURE_D3D12_OPTIONS5** 並 [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-125">Pass **D3D12_FEATURE_D3D12_OPTIONS5** and [**D3D12_FEATURE_DATA_D3D12_OPTIONS5**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options5).</span></span>
- <span data-ttu-id="d28d6-126">傳遞 **D3D12_FEATURE_EXISTING_HEAPS** 並 [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-126">Pass **D3D12_FEATURE_EXISTING_HEAPS** and [**D3D12_FEATURE_DATA_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_existing_heaps).</span></span>
- <span data-ttu-id="d28d6-127">傳遞 **D3D12_FEATURE_FEATURE_LEVELS** 並 [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-127">Pass **D3D12_FEATURE_FEATURE_LEVELS** and [**D3D12_FEATURE_DATA_FEATURE_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_feature_levels).</span></span>
- <span data-ttu-id="d28d6-128">傳遞 **D3D12_FEATURE_FORMAT_INFO** 並 [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-128">Pass **D3D12_FEATURE_FORMAT_INFO** and [**D3D12_FEATURE_DATA_FORMAT_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info).</span></span>
- <span data-ttu-id="d28d6-129">傳遞 **D3D12_FEATURE_FORMAT_SUPPORT** 並 [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-129">Pass **D3D12_FEATURE_FORMAT_SUPPORT** and [**D3D12_FEATURE_DATA_FORMAT_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support).</span></span>
- <span data-ttu-id="d28d6-130">傳遞 **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** 並 [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-130">Pass **D3D12_FEATURE_GPU_VIRTUAL_ADDRESS_SUPPORT** and [**D3D12_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support).</span></span>
- <span data-ttu-id="d28d6-131">傳遞 **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** 並 [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-131">Pass **D3D12_FEATURE_MULTISAMPLE_QUALITY_LEVELS** and [**D3D12_FEATURE_DATA_MULTISAMPLE_QUALITY_LEVELS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_multisample_quality_levels).</span></span>
- <span data-ttu-id="d28d6-132">傳遞 **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** 並 [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-132">Pass **D3D12_FEATURE_PROTECTED_RESOURCE_SESSION_SUPPORT** and [**D3D12_FEATURE_DATA_PROTECTED_RESOURCE_SESSION_SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_protected_resource_session_support).</span></span>
- <span data-ttu-id="d28d6-133">傳遞 **D3D12_FEATURE_ROOT_SIGNATURE** 並 [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-133">Pass **D3D12_FEATURE_ROOT_SIGNATURE** and [**D3D12_FEATURE_DATA_ROOT_SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature).</span></span>
- <span data-ttu-id="d28d6-134">傳遞 **D3D12_FEATURE_SERIALIZATION** 並 [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-134">Pass **D3D12_FEATURE_SERIALIZATION** and [**D3D12_FEATURE_DATA_SERIALIZATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_serialization).</span></span>
- <span data-ttu-id="d28d6-135">傳遞 **D3D12_FEATURE_SHADER_CACHE** 並 [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-135">Pass **D3D12_FEATURE_SHADER_CACHE** and [**D3D12_FEATURE_DATA_SHADER_CACHE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_cache).</span></span>
- <span data-ttu-id="d28d6-136">傳遞 **D3D12_FEATURE_SHADER_MODEL** 並 [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model)。</span><span class="sxs-lookup"><span data-stu-id="d28d6-136">Pass **D3D12_FEATURE_SHADER_MODEL** and [**D3D12_FEATURE_DATA_SHADER_MODEL**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_shader_model).</span></span>

## <a name="hardware-support-for-dxgi-formats"></a><span data-ttu-id="d28d6-137">DXGI 格式的硬體支援</span><span class="sxs-lookup"><span data-stu-id="d28d6-137">Hardware support for DXGI Formats</span></span>

<span data-ttu-id="d28d6-138">若要查看 DXGI 格式和硬體功能的表格，請參閱這些主題。</span><span class="sxs-lookup"><span data-stu-id="d28d6-138">To view tables of DXGI formats and hardware features, refer to these topics.</span></span>

- [<span data-ttu-id="d28d6-139">Direct3D 功能等級12.1 硬體的 DXGI 格式支援</span><span class="sxs-lookup"><span data-stu-id="d28d6-139">DXGI Format Support for Direct3D Feature Level 12.1 Hardware</span></span>](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-1-formats)
- [<span data-ttu-id="d28d6-140">Direct3D 功能等級12.0 硬體的 DXGI 格式支援</span><span class="sxs-lookup"><span data-stu-id="d28d6-140">DXGI Format Support for Direct3D Feature Level 12.0 Hardware</span></span>](/windows/desktop/direct3ddxgi/hardware-support-for-direct3d-12-0-formats)
- [<span data-ttu-id="d28d6-141">Direct3D 功能等級11.1 硬體的 DXGI 格式支援</span><span class="sxs-lookup"><span data-stu-id="d28d6-141">DXGI Format Support for Direct3D Feature Level 11.1 Hardware</span></span>](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-1-feature-level-hardware)
- [<span data-ttu-id="d28d6-142">Direct3D 功能等級11.0 硬體的 DXGI 格式支援</span><span class="sxs-lookup"><span data-stu-id="d28d6-142">DXGI Format Support for Direct3D Feature Level 11.0 Hardware</span></span>](/windows/desktop/direct3ddxgi/format-support-for-direct3d-11-0-feature-level-hardware)
- <span data-ttu-id="d28d6-143">[Direct3D 10Level9 格式的硬體支援](/previous-versions//ff471324(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d28d6-143">[Hardware Support for Direct3D 10Level9 Formats](/previous-versions//ff471324(v=vs.85))</span></span>
- <span data-ttu-id="d28d6-144">[Direct3D 10.1 格式的硬體支援](/previous-versions//cc627091(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d28d6-144">[Hardware Support for Direct3D 10.1 Formats](/previous-versions//cc627091(v=vs.85))</span></span>
- <span data-ttu-id="d28d6-145">[適用于 Direct3D 10 格式的硬體支援](/previous-versions//cc627090(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d28d6-145">[Hardware Support for Direct3D 10 Formats](/previous-versions//cc627090(v=vs.85))</span></span>

## <a name="related-topics"></a><span data-ttu-id="d28d6-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="d28d6-146">Related topics</span></span>

* [<span data-ttu-id="d28d6-147">Direct3D 12 中的資源繫結</span><span class="sxs-lookup"><span data-stu-id="d28d6-147">Resource binding in Direct3D 12</span></span>](resource-binding.md)
* [<span data-ttu-id="d28d6-148">硬體功能等級</span><span class="sxs-lookup"><span data-stu-id="d28d6-148">Hardware feature levels</span></span>](hardware-feature-levels.md)
* [<span data-ttu-id="d28d6-149">根簽章</span><span class="sxs-lookup"><span data-stu-id="d28d6-149">Root signatures</span></span>](root-signatures.md)