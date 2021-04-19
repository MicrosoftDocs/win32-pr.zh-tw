---
title: 'CD3DX12_ROOT_PARAMETER1 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 \_ 根 \_ PARAMETER1 結構。
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- CD3DX12_ROOT_PARAMETER1 結構
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989223"
---
# <a name="cd3dx12_root_parameter1-structure"></a><span data-ttu-id="b1219-104">CD3DX12 \_ 根 \_ PARAMETER1 結構</span><span class="sxs-lookup"><span data-stu-id="b1219-104">CD3DX12\_ROOT\_PARAMETER1 structure</span></span>

<span data-ttu-id="b1219-105">協助程式結構，可讓您輕鬆地初始化 [**D3D12 \_ 根 \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) 結構。</span><span class="sxs-lookup"><span data-stu-id="b1219-105">A helper structure to enable easy initialization of a [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1219-106">語法</span><span class="sxs-lookup"><span data-stu-id="b1219-106">Syntax</span></span>


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a><span data-ttu-id="b1219-107">成員</span><span class="sxs-lookup"><span data-stu-id="b1219-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b1219-108">**CD3DX12 \_ ROOT \_ PARAMETER1 ()**</span><span class="sxs-lookup"><span data-stu-id="b1219-108">**CD3DX12\_ROOT\_PARAMETER1()**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-109">建立新的、未初始化的 CD3DX12 \_ 根 PARAMETER1 實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b1219-109">Creates a new, uninitialized, instance of a CD3DX12\_ROOT\_PARAMETER1.</span></span>

</dd> <dt>

<span data-ttu-id="b1219-110">**明確 CD3DX12 \_ 根 \_ PARAMETER1 (const D3D12 \_ root \_ PARAMETER1 &o)**</span><span class="sxs-lookup"><span data-stu-id="b1219-110">**explicit CD3DX12\_ROOT\_PARAMETER1(const D3D12\_ROOT\_PARAMETER1 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-111">建立 CD3DX12 根 PARAMETER1 的新實例 \_ \_ ，並以另一個 [**D3D12 \_ 根 \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) 結構的內容進行初始化。</span><span class="sxs-lookup"><span data-stu-id="b1219-111">Creates a new instance of a CD3DX12\_ROOT\_PARAMETER1, initialized with the contents of another [**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b1219-112">**靜態內嵌 InitAsDescriptorTable (D3D12 \_ 根 \_ PARAMETER1 &ROOTPARAM、UINT numDescriptorRanges、const D3D12 \_ 描述項 \_ RANGE1 \* pDescriptorRanges、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="b1219-112">**static inline InitAsDescriptorTable(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-113">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="b1219-113">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b1219-114">[**D3D12 \_ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="b1219-114">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="b1219-115">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="b1219-115">UINT numDescriptorRanges</span></span>

<span data-ttu-id="b1219-116">const [**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="b1219-116">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="b1219-117">[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="b1219-117">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b1219-118">**靜態內嵌 InitAsConstants (D3D12 \_ 根 \_ PARAMETER1 &ROOTPARAM、UINT NUM32BITVALUES、UINT SHADERREGISTER、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="b1219-118">**static inline InitAsConstants(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-119">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="b1219-119">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b1219-120">[**D3D12 \_ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="b1219-120">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="b1219-121">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="b1219-121">UINT num32BitValues</span></span>

<span data-ttu-id="b1219-122">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="b1219-122">UINT shaderRegister</span></span>

<span data-ttu-id="b1219-123">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b1219-123">UINT registerSpace = 0</span></span>

<span data-ttu-id="b1219-124">[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="b1219-124">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b1219-125">**靜態內嵌 InitAsConstantBufferView (D3D12 \_ 根 \_ PARAMETER1 &ROOTPARAM，UINT SHADERREGISTER，UINT registerSpace = 0，D3D12 \_ 根目錄描述元旗標 \_ \_ 旗標 = D3D12 \_ 根目錄 \_ 描述項旗標 \_ \_ 無，D3D12 \_ 著色器可見 \_ 性 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="b1219-125">**static inline InitAsConstantBufferView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-126">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="b1219-126">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b1219-127">[**D3D12 \_ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="b1219-127">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="b1219-128">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="b1219-128">UINT shaderRegister</span></span>

<span data-ttu-id="b1219-129">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b1219-129">UINT registerSpace = 0</span></span>

<span data-ttu-id="b1219-130">[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="b1219-130">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b1219-131">[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="b1219-131">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b1219-132">**靜態內嵌 InitAsShaderResourceView (D3D12 \_ 根 \_ PARAMETER1 &ROOTPARAM，UINT SHADERREGISTER，UINT registerSpace = 0，D3D12 \_ 根目錄描述元旗標 \_ \_ 旗標 = D3D12 \_ 根目錄 \_ 描述項旗標 \_ \_ 無，D3D12 \_ 著色器可見 \_ 性 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="b1219-132">**static inline InitAsShaderResourceView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-133">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="b1219-133">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b1219-134">[**D3D12 \_ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="b1219-134">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="b1219-135">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="b1219-135">UINT shaderRegister</span></span>

<span data-ttu-id="b1219-136">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b1219-136">UINT registerSpace = 0</span></span>

<span data-ttu-id="b1219-137">[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="b1219-137">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b1219-138">[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="b1219-138">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b1219-139">**靜態內嵌 InitAsUnorderedAccessView (D3D12 \_ 根 \_ PARAMETER1 &ROOTPARAM，UINT SHADERREGISTER，UINT registerSpace = 0，D3D12 \_ 根目錄描述元旗標 \_ \_ 旗標 = D3D12 \_ 根目錄 \_ 描述項旗標 \_ \_ 無，D3D12 \_ 著色器可見 \_ 性 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="b1219-139">**static inline InitAsUnorderedAccessView(D3D12\_ROOT\_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-140">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="b1219-140">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b1219-141">[**D3D12 \_ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span><span class="sxs-lookup"><span data-stu-id="b1219-141">[**D3D12\_ROOT\_PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootParam</span></span>

<span data-ttu-id="b1219-142">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="b1219-142">UINT shaderRegister</span></span>

<span data-ttu-id="b1219-143">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b1219-143">UINT registerSpace = 0</span></span>

<span data-ttu-id="b1219-144">[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="b1219-144">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b1219-145">[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="b1219-145">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b1219-146">**內嵌 InitAsDescriptorTable (UINT numDescriptorRanges、const D3D12 \_ 描述項 \_ RANGE1 \* pDescriptorRanges、D3D12 \_ 著色器 \_ 可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="b1219-146">**inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12\_DESCRIPTOR\_RANGE1\* pDescriptorRanges, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-147">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="b1219-147">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b1219-148">UINT numDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="b1219-148">UINT numDescriptorRanges</span></span>

<span data-ttu-id="b1219-149">const [**D3D12 \_ 描述項 \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pDescriptorRanges</span><span class="sxs-lookup"><span data-stu-id="b1219-149">const [**D3D12\_DESCRIPTOR\_RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)\* pDescriptorRanges</span></span>

<span data-ttu-id="b1219-150">[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="b1219-150">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b1219-151">**內嵌 InitAsConstants (UINT num32BitValues、UINT shaderRegister、UINT registerSpace = 0、D3D12 \_ 著色器 \_ 可見度可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="b1219-151">**inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-152">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="b1219-152">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b1219-153">UINT num32BitValues</span><span class="sxs-lookup"><span data-stu-id="b1219-153">UINT num32BitValues</span></span>

<span data-ttu-id="b1219-154">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="b1219-154">UINT shaderRegister</span></span>

<span data-ttu-id="b1219-155">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b1219-155">UINT registerSpace = 0</span></span>

<span data-ttu-id="b1219-156">[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="b1219-156">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b1219-157">**inline InitAsConstantBufferView (UINT shaderRegister，UINT registerSpace = 0，D3D12 \_ 根 \_ 描述元 \_ 旗標旗標 = D3D12 \_ 根目錄描述項旗標 \_ \_ \_ 無，D3D12 \_ 著色器 \_ 可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="b1219-157">**inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-158">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="b1219-158">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b1219-159">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="b1219-159">UINT shaderRegister</span></span>

<span data-ttu-id="b1219-160">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b1219-160">UINT registerSpace = 0</span></span>

<span data-ttu-id="b1219-161">[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="b1219-161">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b1219-162">[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="b1219-162">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b1219-163">**inline InitAsShaderResourceView (UINT shaderRegister，UINT registerSpace = 0，D3D12 \_ 根 \_ 描述元 \_ 旗標旗標 = D3D12 \_ 根目錄描述項旗標 \_ \_ \_ 無，D3D12 \_ 著色器 \_ 可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="b1219-163">**inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-164">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="b1219-164">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b1219-165">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="b1219-165">UINT shaderRegister</span></span>

<span data-ttu-id="b1219-166">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b1219-166">UINT registerSpace = 0</span></span>

<span data-ttu-id="b1219-167">[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="b1219-167">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b1219-168">[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="b1219-168">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> <dt>

<span data-ttu-id="b1219-169">**inline InitAsUnorderedAccessView (UINT shaderRegister，UINT registerSpace = 0，D3D12 \_ 根 \_ 描述元 \_ 旗標旗標 = D3D12 \_ 根目錄描述項旗標 \_ \_ \_ 無，D3D12 \_ 著色器 \_ 可見度 = D3D12 \_ 著色器 \_ 可見度 \_ 所有)**</span><span class="sxs-lookup"><span data-stu-id="b1219-169">**inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12\_ROOT\_DESCRIPTOR\_FLAGS flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE, D3D12\_SHADER\_VISIBILITY visibility = D3D12\_SHADER\_VISIBILITY\_ALL)**</span></span>
</dt> <dd>

<span data-ttu-id="b1219-170">指定初始化下列參數的函式：</span><span class="sxs-lookup"><span data-stu-id="b1219-170">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="b1219-171">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="b1219-171">UINT shaderRegister</span></span>

<span data-ttu-id="b1219-172">UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="b1219-172">UINT registerSpace = 0</span></span>

<span data-ttu-id="b1219-173">[**D3D12 \_根 \_ 描述 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) 元旗標旗標 = D3D12 \_ 根目錄 \_ 描述元旗標 \_ \_ 無</span><span class="sxs-lookup"><span data-stu-id="b1219-173">[**D3D12\_ROOT\_DESCRIPTOR\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) flags = D3D12\_ROOT\_DESCRIPTOR\_FLAG\_NONE</span></span>

<span data-ttu-id="b1219-174">[**D3D12 \_著色器 \_ 可見度**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility)可見度 = D3D12 \_ 著色器 \_ 可見度 \_</span><span class="sxs-lookup"><span data-stu-id="b1219-174">[**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) visibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1219-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1219-175">Requirements</span></span>



| <span data-ttu-id="b1219-176">需求</span><span class="sxs-lookup"><span data-stu-id="b1219-176">Requirement</span></span> | <span data-ttu-id="b1219-177">值</span><span class="sxs-lookup"><span data-stu-id="b1219-177">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b1219-178">標頭</span><span class="sxs-lookup"><span data-stu-id="b1219-178">Header</span></span><br/> | <dl> <span data-ttu-id="b1219-179"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1219-179"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1219-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1219-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1219-181">**D3D12 \_ 根 \_ PARAMETER1**</span><span class="sxs-lookup"><span data-stu-id="b1219-181">**D3D12\_ROOT\_PARAMETER1**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[<span data-ttu-id="b1219-182">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="b1219-182">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





