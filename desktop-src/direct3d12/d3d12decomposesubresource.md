---
title: 'D3D12DecomposeSubresource 函式 (D3dx12) '
description: 輸出對應至指定之 subresource 索引的 mip 配量、陣列配量和平面配量。
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- D3D12DecomposeSubresource 函式
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986495"
---
# <a name="d3d12decomposesubresource-function"></a><span data-ttu-id="f11f0-104">D3D12DecomposeSubresource 函式</span><span class="sxs-lookup"><span data-stu-id="f11f0-104">D3D12DecomposeSubresource function</span></span>

<span data-ttu-id="f11f0-105">輸出對應至指定之 subresource 索引的 mip 配量、陣列配量和平面配量。</span><span class="sxs-lookup"><span data-stu-id="f11f0-105">Outputs the mip slice, array slice, and plane slice that correspond to the specified subresource index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11f0-106">語法</span><span class="sxs-lookup"><span data-stu-id="f11f0-106">Syntax</span></span>


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a><span data-ttu-id="f11f0-107">參數</span><span class="sxs-lookup"><span data-stu-id="f11f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f11f0-108">*子資源*</span><span class="sxs-lookup"><span data-stu-id="f11f0-108">*Subresource*</span></span> 
</dt> <dd>

<span data-ttu-id="f11f0-109">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f11f0-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f11f0-110">Subresource 的索引。</span><span class="sxs-lookup"><span data-stu-id="f11f0-110">The index of the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="f11f0-111">*MipLevels*</span><span class="sxs-lookup"><span data-stu-id="f11f0-111">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="f11f0-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f11f0-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f11f0-113">Subresource 中 mipmap 層級的最大數目。</span><span class="sxs-lookup"><span data-stu-id="f11f0-113">The maximum number of mipmap levels in the subresource.</span></span>

</dd> <dt>

<span data-ttu-id="f11f0-114">[陣列大小]</span><span class="sxs-lookup"><span data-stu-id="f11f0-114">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="f11f0-115">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f11f0-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f11f0-116">陣列中的項目數。</span><span class="sxs-lookup"><span data-stu-id="f11f0-116">The number of elements in the array.</span></span>

</dd> <dt>

<span data-ttu-id="f11f0-117">*MipSlice* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="f11f0-117">*MipSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f11f0-118">類型： **T**</span><span class="sxs-lookup"><span data-stu-id="f11f0-118">Type: **T**</span></span>

<span data-ttu-id="f11f0-119">輸出對應至指定之 subresource 索引的 mip 配量。</span><span class="sxs-lookup"><span data-stu-id="f11f0-119">Outputs the mip slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="f11f0-120">*ArraySlice* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="f11f0-120">*ArraySlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f11f0-121">類型： **U**</span><span class="sxs-lookup"><span data-stu-id="f11f0-121">Type: **U**</span></span>

<span data-ttu-id="f11f0-122">輸出對應至指定之 subresource 索引的陣列配量。</span><span class="sxs-lookup"><span data-stu-id="f11f0-122">Outputs the array slice that corresponds to the given subresource index.</span></span>

</dd> <dt>

<span data-ttu-id="f11f0-123">*PlaneSlice* \[out、ref\]</span><span class="sxs-lookup"><span data-stu-id="f11f0-123">*PlaneSlice* \[out, ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f11f0-124">類型： **V**</span><span class="sxs-lookup"><span data-stu-id="f11f0-124">Type: **V**</span></span>

<span data-ttu-id="f11f0-125">輸出對應至指定之 subresource 索引的平面配量。</span><span class="sxs-lookup"><span data-stu-id="f11f0-125">Outputs the plane slice that corresponds to the given subresource index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f11f0-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="f11f0-126">Return value</span></span>

<span data-ttu-id="f11f0-127">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f11f0-127">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f11f0-128">備註</span><span class="sxs-lookup"><span data-stu-id="f11f0-128">Remarks</span></span>

<span data-ttu-id="f11f0-129">此函數會決定哪一個 mip 配量、陣列配量和平面配量對應到指定的 subresource 索引。</span><span class="sxs-lookup"><span data-stu-id="f11f0-129">This function determines which mip slice, array slice, and plane slice correspond to a given subresource index.</span></span> <span data-ttu-id="f11f0-130">這是很實用的公用程式，但它是 c + + 特有的。</span><span class="sxs-lookup"><span data-stu-id="f11f0-130">This is a useful utility, though it is C++ specific.</span></span>

<span data-ttu-id="f11f0-131">此函式的宣告方式如下： **T**、 **U** 和 **V** 類型的 c + + 範本化參數：</span><span class="sxs-lookup"><span data-stu-id="f11f0-131">This function is declared as follows, with C++ templatized parameters for types **T**, **U**, and **V**:</span></span>


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a><span data-ttu-id="f11f0-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="f11f0-132">Requirements</span></span>



| <span data-ttu-id="f11f0-133">需求</span><span class="sxs-lookup"><span data-stu-id="f11f0-133">Requirement</span></span> | <span data-ttu-id="f11f0-134">值</span><span class="sxs-lookup"><span data-stu-id="f11f0-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f11f0-135">標頭</span><span class="sxs-lookup"><span data-stu-id="f11f0-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f11f0-136"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="f11f0-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="f11f0-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="f11f0-137">Library</span></span><br/> | <dl> <span data-ttu-id="f11f0-138"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f11f0-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="f11f0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f11f0-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="f11f0-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f11f0-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f11f0-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f11f0-141">See also</span></span>

[<span data-ttu-id="f11f0-142">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="f11f0-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)

[<span data-ttu-id="f11f0-143">子資源</span><span class="sxs-lookup"><span data-stu-id="f11f0-143">Subresources</span></span>](subresources.md)
