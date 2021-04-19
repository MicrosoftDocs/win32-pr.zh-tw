---
title: 'CD3DX12_ROOT_PARAMETER 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根 \_ 參數結構。
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- CD3DX12_ROOT_PARAMETER 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981808"
---
# <a name="cd3dx12_root_parameter-structure"></a><span data-ttu-id="d7ace-104">CD3DX12 \_ 根 \_ 參數結構</span><span class="sxs-lookup"><span data-stu-id="d7ace-104">CD3DX12\_ROOT\_PARAMETER structure</span></span>

<span data-ttu-id="d7ace-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) 結構。</span><span class="sxs-lookup"><span data-stu-id="d7ace-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ace-106">語法</span><span class="sxs-lookup"><span data-stu-id="d7ace-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="d7ace-107">成員</span><span class="sxs-lookup"><span data-stu-id="d7ace-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7ace-108">**CD3DX12 \_ 根 \_ 參數 ()**</span><span class="sxs-lookup"><span data-stu-id="d7ace-108">**CD3DX12\_ROOT\_PARAMETER()**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-109">建立 CD3DX12 根參數的新、未初始化的 \_ 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d7ace-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-110">**明確 CD3DX12 的 \_ 根 \_ 參數 (const D3D12 \_ 根 \_ 參數 &o)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-110">**explicit CD3DX12\_ROOT\_PARAMETER(const D3D12\_ROOT\_PARAMETER &o)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-111">建立 CD3DX12 根參數的新實例 \_ \_ ，並使用另一個 [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="d7ace-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-112">**靜態內嵌 InitAsDescriptorTable (D3D12 \_ 根 \_ 參數 &ROOTPARAM、UINT numDescriptorRanges、const D3D12 \_ 描述項 \_ 範圍 \* pDescriptorRanges、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-113">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="d7ace-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="d7ace-114">[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="d7ace-114">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="d7ace-115">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="d7ace-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="d7ace-116">[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="d7ace-116">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="d7ace-117"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性</span><span class="sxs-lookup"><span data-stu-id="d7ace-117">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-118">**靜態內嵌 InitAsConstants (D3D12 \_ 根 \_ 參數 &ROOTPARAM、uint NUM32BITVALUES、UINT SHADERREGISTER、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-119">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="d7ace-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="d7ace-120">[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="d7ace-120">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="d7ace-121">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="d7ace-121">UINT num32BitValues</span></span>

<span data-ttu-id="d7ace-122">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="d7ace-122">UINT shaderRegister</span></span>

<span data-ttu-id="d7ace-123"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="d7ace-123">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="d7ace-124"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性</span><span class="sxs-lookup"><span data-stu-id="d7ace-124">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-125">**靜態內嵌 InitAsConstantBufferView (D3D12 \_ 根 \_ 參數 &ROOTPARAM、UINT SHADERREGISTER、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-126">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="d7ace-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="d7ace-127">[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="d7ace-127">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="d7ace-128">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="d7ace-128">UINT shaderRegister</span></span>

<span data-ttu-id="d7ace-129"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="d7ace-129">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="d7ace-130"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性</span><span class="sxs-lookup"><span data-stu-id="d7ace-130">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-131">**靜態內嵌 InitAsShaderResourceView (D3D12 \_ 根 \_ 參數 &ROOTPARAM、UINT SHADERREGISTER、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-131">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-132">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="d7ace-132">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="d7ace-133">[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="d7ace-133">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="d7ace-134">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="d7ace-134">UINT shaderRegister</span></span>

<span data-ttu-id="d7ace-135"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="d7ace-135">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="d7ace-136"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性</span><span class="sxs-lookup"><span data-stu-id="d7ace-136">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-137">**靜態內嵌 InitAsUnorderedAccessView (D3D12 \_ 根 \_ 參數 &ROOTPARAM、UINT SHADERREGISTER、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-137">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-138">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="d7ace-138">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="d7ace-139">[**D3D12 \_根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span><span class="sxs-lookup"><span data-stu-id="d7ace-139">[**D3D12\_ROOT\_PARAMETER**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootParam</span></span>

<span data-ttu-id="d7ace-140">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="d7ace-140">UINT shaderRegister</span></span>

<span data-ttu-id="d7ace-141"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="d7ace-141">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="d7ace-142"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性</span><span class="sxs-lookup"><span data-stu-id="d7ace-142">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-143">**內嵌 InitAsDescriptorTable (UINT numDescriptorRanges，const D3D12 \_ 描述項 \_ 範圍 \* pDescriptorRanges，D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-143">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-144">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="d7ace-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="d7ace-145">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="d7ace-145">UINT numDescriptorRanges</span></span>

<span data-ttu-id="d7ace-146">[**D3D12 \_描述項 \_ 範圍**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="d7ace-146">[**D3D12\_DESCRIPTOR\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range)\* pDescriptorRanges</span></span>

<span data-ttu-id="d7ace-147"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性</span><span class="sxs-lookup"><span data-stu-id="d7ace-147">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-148">**內嵌 InitAsConstants (UINT num32BitValues、UINT shaderRegister、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-148">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-149">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="d7ace-149">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="d7ace-150">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="d7ace-150">UINT num32BitValues</span></span>

<span data-ttu-id="d7ace-151">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="d7ace-151">UINT shaderRegister</span></span>

<span data-ttu-id="d7ace-152"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="d7ace-152">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="d7ace-153"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性</span><span class="sxs-lookup"><span data-stu-id="d7ace-153">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-154">**內嵌 InitAsConstantBufferView (UINT shaderRegister、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-154">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-155">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="d7ace-155">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="d7ace-156">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="d7ace-156">UINT shaderRegister</span></span>

<span data-ttu-id="d7ace-157"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="d7ace-157">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="d7ace-158"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性</span><span class="sxs-lookup"><span data-stu-id="d7ace-158">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-159">**內嵌 InitAsShaderResourceView (UINT shaderRegister、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-159">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-160">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="d7ace-160">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="d7ace-161">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="d7ace-161">UINT shaderRegister</span></span>

<span data-ttu-id="d7ace-162"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="d7ace-162">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="d7ace-163"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性</span><span class="sxs-lookup"><span data-stu-id="d7ace-163">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="d7ace-164">**內嵌 InitAsUnorderedAccessView (UINT shaderRegister、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="d7ace-164">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="d7ace-165">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="d7ace-165">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="d7ace-166">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="d7ace-166">UINT shaderRegister</span></span>

<span data-ttu-id="d7ace-167"> (opt) UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="d7ace-167">(opt) UINT registerSpace = 0</span></span>

<span data-ttu-id="d7ace-168"> (opt) [**D3D12 \_ 著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) 可見度 = D3D12 \_ 著色器 \_ 可見 \_ 性</span><span class="sxs-lookup"><span data-stu-id="d7ace-168">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7ace-169">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7ace-169">Requirements</span></span>



| <span data-ttu-id="d7ace-170">需求</span><span class="sxs-lookup"><span data-stu-id="d7ace-170">Requirement</span></span> | <span data-ttu-id="d7ace-171">值</span><span class="sxs-lookup"><span data-stu-id="d7ace-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ace-172">標頭</span><span class="sxs-lookup"><span data-stu-id="d7ace-172">Header</span></span><br/> | <dl> <span data-ttu-id="d7ace-173"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ace-173"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ace-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7ace-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ace-175">**D3D12 \_ 根 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="d7ace-175">**D3D12\_ROOT\_PARAMETER**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[<span data-ttu-id="d7ace-176">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="d7ace-176">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





