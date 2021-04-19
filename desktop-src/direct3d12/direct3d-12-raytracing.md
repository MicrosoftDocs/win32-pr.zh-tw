---
title: Direct3D 12 Raytracing
description: 本文提供適用于 Direct3D raytracing 的檔案清單。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d7896153f37a776faeddd00d78fbe0c1f3a120
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965810"
---
# <a name="direct3d-12-raytracing"></a><span data-ttu-id="7dc37-103">Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="7dc37-103">Direct3D 12 Raytracing</span></span>

<span data-ttu-id="7dc37-104">本文提供適用于 Direct3D raytracing 的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="7dc37-104">This article provides a listing of the documentation that is available for Direct3D raytracing.</span></span>

## <a name="c-raytracing-reference"></a><span data-ttu-id="7dc37-105">C + + raytracing 參考</span><span class="sxs-lookup"><span data-stu-id="7dc37-105">C++ raytracing reference</span></span>

<span data-ttu-id="7dc37-106">本節連結至用來執行 Direct3D 12 raytracing 的 c + + Api。</span><span class="sxs-lookup"><span data-stu-id="7dc37-106">This section links to the C++ APIs used to implement Direct3D 12 raytracing.</span></span>

### <a name="c-raytracing-interfaces"></a><span data-ttu-id="7dc37-107">C + + raytracing 介面</span><span class="sxs-lookup"><span data-stu-id="7dc37-107">C++ raytracing interfaces</span></span>

* [<span data-ttu-id="7dc37-108">ID3D12Device5</span><span class="sxs-lookup"><span data-stu-id="7dc37-108">ID3D12Device5</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12device5)
* [<span data-ttu-id="7dc37-109">ID3D12GraphicsCommandList4</span><span class="sxs-lookup"><span data-stu-id="7dc37-109">ID3D12GraphicsCommandList4</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist4)
* [<span data-ttu-id="7dc37-110">ID3D12StateObject</span><span class="sxs-lookup"><span data-stu-id="7dc37-110">ID3D12StateObject</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12stateobject)
* [<span data-ttu-id="7dc37-111">ID3D12StateObjectProperties</span><span class="sxs-lookup"><span data-stu-id="7dc37-111">ID3D12StateObjectProperties</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12stateobjectproperties)


### <a name="c-raytracing-structures"></a><span data-ttu-id="7dc37-112">C + + raytracing 結構</span><span class="sxs-lookup"><span data-stu-id="7dc37-112">C++ raytracing structures</span></span>


* [<span data-ttu-id="7dc37-113">D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-113">D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_desc)
* [<span data-ttu-id="7dc37-114">D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS</span><span class="sxs-lookup"><span data-stu-id="7dc37-114">D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs)
* [<span data-ttu-id="7dc37-115">D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_TOOLS_VISUALIZATION_HEADER</span><span class="sxs-lookup"><span data-stu-id="7dc37-115">D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_TOOLS_VISUALIZATION_HEADER</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_tools_visualization_header)
* [<span data-ttu-id="7dc37-116">D3D12_DISPATCH_RAYS_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-116">D3D12_DISPATCH_RAYS_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_rays_desc)
* [<span data-ttu-id="7dc37-117">D3D12_DXIL_LIBRARY_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-117">D3D12_DXIL_LIBRARY_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dxil_library_desc)
* [<span data-ttu-id="7dc37-118">D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION</span><span class="sxs-lookup"><span data-stu-id="7dc37-118">D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dxil_subobject_to_exports_association)
* [<span data-ttu-id="7dc37-119">D3D12_EXISTING_COLLECTION_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-119">D3D12_EXISTING_COLLECTION_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_existing_collection_desc)
* [<span data-ttu-id="7dc37-120">D3D12_EXPORT_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-120">D3D12_EXPORT_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_existing_collection_desc)
* [<span data-ttu-id="7dc37-121">D3D12_GLOBAL_ROOT_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="7dc37-121">D3D12_GLOBAL_ROOT_SIGNATURE</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_global_root_signature)
* [<span data-ttu-id="7dc37-122">D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE</span><span class="sxs-lookup"><span data-stu-id="7dc37-122">D3D12_GPU_VIRTUAL_ADDRESS_AND_STRIDE</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_virtual_address_and_stride)
* [<span data-ttu-id="7dc37-123">D3D12_GPU_VIRTUAL_ADDRESS_RANGE</span><span class="sxs-lookup"><span data-stu-id="7dc37-123">D3D12_GPU_VIRTUAL_ADDRESS_RANGE</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_virtual_address_range)
* [<span data-ttu-id="7dc37-124">D3D12_GPU_VIRTUAL_ADDRESS_RANGE_AND_STRIDE</span><span class="sxs-lookup"><span data-stu-id="7dc37-124">D3D12_GPU_VIRTUAL_ADDRESS_RANGE_AND_STRIDE</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_virtual_address_range_and_stride)
* [<span data-ttu-id="7dc37-125">D3D12_HIT_GROUP_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-125">D3D12_HIT_GROUP_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_hit_group_desc)
* [<span data-ttu-id="7dc37-126">D3D12_LOCAL_ROOT_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="7dc37-126">D3D12_LOCAL_ROOT_SIGNATURE</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_local_root_signature)
* [<span data-ttu-id="7dc37-127">D3D12_NODE_MASK</span><span class="sxs-lookup"><span data-stu-id="7dc37-127">D3D12_NODE_MASK</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_node_mask)
* [<span data-ttu-id="7dc37-128">D3D12_RAYTRACING_AABB</span><span class="sxs-lookup"><span data-stu-id="7dc37-128">D3D12_RAYTRACING_AABB</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_aabb)
* [<span data-ttu-id="7dc37-129">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-129">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc)
* [<span data-ttu-id="7dc37-130">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-130">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc)
* [<span data-ttu-id="7dc37-131">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-131">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_desc)
* [<span data-ttu-id="7dc37-132">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION</span><span class="sxs-lookup"><span data-stu-id="7dc37-132">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc)
* [<span data-ttu-id="7dc37-133">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-133">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc)
* [<span data-ttu-id="7dc37-134">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO</span><span class="sxs-lookup"><span data-stu-id="7dc37-134">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info)
* [<span data-ttu-id="7dc37-135">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV</span><span class="sxs-lookup"><span data-stu-id="7dc37-135">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_srv)
* [<span data-ttu-id="7dc37-136">D3D12_RAYTRACING_GEOMETRY_AABBS_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-136">D3D12_RAYTRACING_GEOMETRY_AABBS_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc)
* [<span data-ttu-id="7dc37-137">D3D12_RAYTRACING_GEOMETRY_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-137">D3D12_RAYTRACING_GEOMETRY_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc)
* [<span data-ttu-id="7dc37-138">D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-138">D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc)
* [<span data-ttu-id="7dc37-139">D3D12_RAYTRACING_INSTANCE_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-139">D3D12_RAYTRACING_INSTANCE_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_instance_desc)
* [<span data-ttu-id="7dc37-140">D3D12_RAYTRACING_PIPELINE_CONFIG</span><span class="sxs-lookup"><span data-stu-id="7dc37-140">D3D12_RAYTRACING_PIPELINE_CONFIG</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_pipeline_config)
* [<span data-ttu-id="7dc37-141">D3D12_RAYTRACING_SHADER_CONFIG</span><span class="sxs-lookup"><span data-stu-id="7dc37-141">D3D12_RAYTRACING_SHADER_CONFIG</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config)
* [<span data-ttu-id="7dc37-142">D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="7dc37-142">D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_serialized_data_driver_matching_identifier)
* [<span data-ttu-id="7dc37-143">D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER</span><span class="sxs-lookup"><span data-stu-id="7dc37-143">D3D12_SERIALIZED_RAYTRACING_ACCELERATION_STRUCTURE_HEADER</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_serialized_raytracing_acceleration_structure_header)
* [<span data-ttu-id="7dc37-144">D3D12_STATE_OBJECT_CONFIG</span><span class="sxs-lookup"><span data-stu-id="7dc37-144">D3D12_STATE_OBJECT_CONFIG</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_state_object_config)
* [<span data-ttu-id="7dc37-145">D3D12_STATE_OBJECT_DESC</span><span class="sxs-lookup"><span data-stu-id="7dc37-145">D3D12_STATE_OBJECT_DESC</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_state_object_desc)
* [<span data-ttu-id="7dc37-146">D3D12_STATE_SUBOBJECT</span><span class="sxs-lookup"><span data-stu-id="7dc37-146">D3D12_STATE_SUBOBJECT</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_state_subobject)
* [<span data-ttu-id="7dc37-147">D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION</span><span class="sxs-lookup"><span data-stu-id="7dc37-147">D3D12_SUBOBJECT_TO_EXPORTS_ASSOCIATION</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subobject_to_exports_association)
 

### <a name="c-raytracing-enumerations"></a><span data-ttu-id="7dc37-148">C + + raytracing 列舉</span><span class="sxs-lookup"><span data-stu-id="7dc37-148">C++ raytracing enumerations</span></span>

* [<span data-ttu-id="7dc37-149">D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS</span><span class="sxs-lookup"><span data-stu-id="7dc37-149">D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_driver_matching_identifier_status)
* [<span data-ttu-id="7dc37-150">D3D12_ELEMENTS_LAYOUT</span><span class="sxs-lookup"><span data-stu-id="7dc37-150">D3D12_ELEMENTS_LAYOUT</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_elements_layout)
* [<span data-ttu-id="7dc37-151">D3D12_EXPORT_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7dc37-151">D3D12_EXPORT_FLAGS</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_export_flags)
* [<span data-ttu-id="7dc37-152">D3D12_HIT_GROUP_TYPE</span><span class="sxs-lookup"><span data-stu-id="7dc37-152">D3D12_HIT_GROUP_TYPE</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_hit_group_type)
* [<span data-ttu-id="7dc37-153">D3D12_RAY_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7dc37-153">D3D12_RAY_FLAGS</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_ray_flags)
* [<span data-ttu-id="7dc37-154">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7dc37-154">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAGS</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags)
* [<span data-ttu-id="7dc37-155">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE</span><span class="sxs-lookup"><span data-stu-id="7dc37-155">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode)
* [<span data-ttu-id="7dc37-156">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE</span><span class="sxs-lookup"><span data-stu-id="7dc37-156">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_type)
* [<span data-ttu-id="7dc37-157">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE</span><span class="sxs-lookup"><span data-stu-id="7dc37-157">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_type)
* [<span data-ttu-id="7dc37-158">D3D12_RAYTRACING_GEOMETRY_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7dc37-158">D3D12_RAYTRACING_GEOMETRY_FLAGS</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags)
* [<span data-ttu-id="7dc37-159">D3D12_RAYTRACING_GEOMETRY_TYPE</span><span class="sxs-lookup"><span data-stu-id="7dc37-159">D3D12_RAYTRACING_GEOMETRY_TYPE</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_type)
* [<span data-ttu-id="7dc37-160">D3D12_RAYTRACING_INSTANCE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="7dc37-160">D3D12_RAYTRACING_INSTANCE_FLAGS</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags)
* [<span data-ttu-id="7dc37-161">D3D12_RAYTRACING_TIER</span><span class="sxs-lookup"><span data-stu-id="7dc37-161">D3D12_RAYTRACING_TIER</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_tier)

## <a name="hlsl-raytracing-reference"></a><span data-ttu-id="7dc37-162">HLSL raytracing 參考</span><span class="sxs-lookup"><span data-stu-id="7dc37-162">HLSL raytracing reference</span></span>

<span data-ttu-id="7dc37-163">如需用來執行 Direct3D 12 raytracing 之 HLSL 結構的詳細資訊，請參閱 [Direct3D 12 RAYTRACING HLSL 參考](direct3d-12-raytracing-hlsl-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="7dc37-163">For information on the HLSL constructs used to implement Direct3D 12 raytracing, see [Direct3D 12 Raytracing HLSL Reference](direct3d-12-raytracing-hlsl-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7dc37-164">相關主題</span><span class="sxs-lookup"><span data-stu-id="7dc37-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dc37-165">核心參考</span><span class="sxs-lookup"><span data-stu-id="7dc37-165">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="7dc37-166">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="7dc37-166">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





