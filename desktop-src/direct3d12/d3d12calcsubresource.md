---
title: 'D3D12CalcSubresource 函式 (D3dx12) '
description: 計算材質的 subresource 索引。
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- D3D12CalcSubresource 函式
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986076"
---
# <a name="d3d12calcsubresource-function"></a><span data-ttu-id="f8dae-104">D3D12CalcSubresource 函式</span><span class="sxs-lookup"><span data-stu-id="f8dae-104">D3D12CalcSubresource function</span></span>

<span data-ttu-id="f8dae-105">計算材質的 subresource 索引。</span><span class="sxs-lookup"><span data-stu-id="f8dae-105">Calculates a subresource index for a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8dae-106">語法</span><span class="sxs-lookup"><span data-stu-id="f8dae-106">Syntax</span></span>


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="f8dae-107">參數</span><span class="sxs-lookup"><span data-stu-id="f8dae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8dae-108">*MipSlice*</span><span class="sxs-lookup"><span data-stu-id="f8dae-108">*MipSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="f8dae-109">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8dae-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8dae-110">要定址的 mipmap 層級之以零為基底的索引;0表示第一個最詳細的 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="f8dae-110">The zero-based index for the mipmap level to address; 0 indicates the first, most detailed mipmap level.</span></span>

</dd> <dt>

<span data-ttu-id="f8dae-111">*ArraySlice*</span><span class="sxs-lookup"><span data-stu-id="f8dae-111">*ArraySlice*</span></span> 
</dt> <dd>

<span data-ttu-id="f8dae-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8dae-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8dae-113">要定址的陣列層級之以零為基底的索引;針對 volume (3D) 材質，一律使用0。</span><span class="sxs-lookup"><span data-stu-id="f8dae-113">The zero-based index for the array level to address; always use 0 for volume (3D) textures.</span></span>

</dd> <dt>

<span data-ttu-id="f8dae-114">*PlaneSlice*</span><span class="sxs-lookup"><span data-stu-id="f8dae-114">*PlaneSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="f8dae-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8dae-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8dae-116">要定址之平面層級的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="f8dae-116">The zero-based index for the plane level to address.</span></span>

</dd> <dt>

<span data-ttu-id="f8dae-117">*MipLevels*</span><span class="sxs-lookup"><span data-stu-id="f8dae-117">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="f8dae-118">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8dae-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8dae-119">資源中的 mipmap 層級數目。</span><span class="sxs-lookup"><span data-stu-id="f8dae-119">The number of mipmap levels in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f8dae-120">[陣列大小]</span><span class="sxs-lookup"><span data-stu-id="f8dae-120">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="f8dae-121">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8dae-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8dae-122">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="f8dae-122">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8dae-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8dae-123">Return value</span></span>

<span data-ttu-id="f8dae-124">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f8dae-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f8dae-125">等於 MipSlice + (ArraySlice \* MipLevels) 的索引。</span><span class="sxs-lookup"><span data-stu-id="f8dae-125">The index which equals MipSlice + (ArraySlice \* MipLevels).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8dae-126">備註</span><span class="sxs-lookup"><span data-stu-id="f8dae-126">Remarks</span></span>

<span data-ttu-id="f8dae-127">緩衝區是非結構化的資源，因此定義為包含單一 subresource。</span><span class="sxs-lookup"><span data-stu-id="f8dae-127">A buffer is an unstructured resource and is therefore defined as containing a single subresource.</span></span> <span data-ttu-id="f8dae-128">採用緩衝區的 Api 不需要 subresource 索引。</span><span class="sxs-lookup"><span data-stu-id="f8dae-128">APIs that take buffers do not need a subresource index.</span></span> <span data-ttu-id="f8dae-129">另一方面，材質高度結構化。</span><span class="sxs-lookup"><span data-stu-id="f8dae-129">A texture on the other hand is highly structured.</span></span> <span data-ttu-id="f8dae-130">每個材質物件都可以包含一或多個子資源，視陣列大小和 mipmap 層級數目而定。</span><span class="sxs-lookup"><span data-stu-id="f8dae-130">Each texture object may contain one or more subresources depending on the size of the array and the number of mipmap levels.</span></span>

<span data-ttu-id="f8dae-131">針對 volume (3D) 材質，指定 mipmap 層級的所有配量都是單一 subresource 索引。</span><span class="sxs-lookup"><span data-stu-id="f8dae-131">For volume (3D) textures, all slices for a given mipmap level are a single subresource index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8dae-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8dae-132">Requirements</span></span>



| <span data-ttu-id="f8dae-133">需求</span><span class="sxs-lookup"><span data-stu-id="f8dae-133">Requirement</span></span> | <span data-ttu-id="f8dae-134">值</span><span class="sxs-lookup"><span data-stu-id="f8dae-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8dae-135">標頭</span><span class="sxs-lookup"><span data-stu-id="f8dae-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f8dae-136"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8dae-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="f8dae-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8dae-137">Library</span></span><br/> | <dl> <span data-ttu-id="f8dae-138"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8dae-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="f8dae-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f8dae-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="f8dae-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8dae-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8dae-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8dae-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8dae-142">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="f8dae-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f8dae-143">子資源</span><span class="sxs-lookup"><span data-stu-id="f8dae-143">Subresources</span></span>](subresources.md)
</dt> </dl>

 

