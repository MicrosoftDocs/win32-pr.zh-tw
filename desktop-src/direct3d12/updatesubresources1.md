---
title: 'UpdateSubresources 函式 (D3dx12) '
description: 更新子資源，所有 subresource 陣列都應該填入，通常是藉由呼叫 ID3D12Device GetCopyableFootprints。
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
keywords:
- UpdateSubresources 函式
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988216"
---
# <a name="updatesubresources-function"></a><span data-ttu-id="da48b-104">UpdateSubresources 函式</span><span class="sxs-lookup"><span data-stu-id="da48b-104">UpdateSubresources function</span></span>

<span data-ttu-id="da48b-105">更新子資源，所有 subresource 陣列都應該填入，通常是藉由呼叫 [**ID3D12Device：： GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)。</span><span class="sxs-lookup"><span data-stu-id="da48b-105">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span>

## <a name="syntax"></a><span data-ttu-id="da48b-106">語法</span><span class="sxs-lookup"><span data-stu-id="da48b-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="da48b-107">參數</span><span class="sxs-lookup"><span data-stu-id="da48b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da48b-108">*pCmdList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da48b-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da48b-109">類型： **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="da48b-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="da48b-110">命令清單，做為 [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)的指標。</span><span class="sxs-lookup"><span data-stu-id="da48b-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="da48b-111">*pDestinationResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da48b-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da48b-112">類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="da48b-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="da48b-113">目的地資源，作為 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)的指標。</span><span class="sxs-lookup"><span data-stu-id="da48b-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="da48b-114">*pIntermediate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da48b-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da48b-115">類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="da48b-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="da48b-116">中繼資源，作為 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)的指標。</span><span class="sxs-lookup"><span data-stu-id="da48b-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="da48b-117">*FirstSubresource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da48b-117">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da48b-118">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="da48b-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="da48b-119">資源中第一個 subresource 的索引。</span><span class="sxs-lookup"><span data-stu-id="da48b-119">The index of the first subresource in the resource.</span></span> <span data-ttu-id="da48b-120">有效值的範圍是0到 D3D12 的要求 \_ \_ 子資源。</span><span class="sxs-lookup"><span data-stu-id="da48b-120">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="da48b-121">*NumSubresources* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da48b-121">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da48b-122">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="da48b-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="da48b-123">資源中的子資源數目。</span><span class="sxs-lookup"><span data-stu-id="da48b-123">The number of subresources in the resource.</span></span> <span data-ttu-id="da48b-124">有效值的範圍是0到 (D3D12 \_ 需求 \_ 子資源- *FirstSubresource*) 。</span><span class="sxs-lookup"><span data-stu-id="da48b-124">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="da48b-125">*RequiredSize*</span><span class="sxs-lookup"><span data-stu-id="da48b-125">*RequiredSize*</span></span> 
</dt> <dd>

<span data-ttu-id="da48b-126">類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="da48b-126">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="da48b-127">更新所需的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="da48b-127">The required size, in bytes, for the update.</span></span>

</dd> <dt>

<span data-ttu-id="da48b-128">*pLayouts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da48b-128">*pLayouts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da48b-129">型別： **Const [**D3D12 \_ 放置 SUBRESOURCE 的 \_ \_ 佔用量**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) \***</span><span class="sxs-lookup"><span data-stu-id="da48b-129">Type: **const [**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)\***</span></span>

<span data-ttu-id="da48b-130">陣列的指標， (長度 *NumSubresources*) 指標指向結構的指標，其中包含資源子資源的描述和位置。</span><span class="sxs-lookup"><span data-stu-id="da48b-130">Pointer to an array (of length *NumSubresources*) of pointers to the structures that contains the description and placement of the resource's subresources.</span></span>

</dd> <dt>

<span data-ttu-id="da48b-131">*pNumRows* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da48b-131">*pNumRows* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da48b-132">類型： **Const [**UINT**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="da48b-132">Type: **const [**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="da48b-133">陣列的指標 (長度為 *NumSubresources* 的 UINTS) ，其中包含每個 subresource 的資料列數目。</span><span class="sxs-lookup"><span data-stu-id="da48b-133">Pointer to an array (of length *NumSubresources*) of UINTS containing the number of rows for each subresource.</span></span>

</dd> <dt>

<span data-ttu-id="da48b-134">*pRowSizesInBytes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da48b-134">*pRowSizesInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da48b-135">類型： **Const [**UINT64**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="da48b-135">Type: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="da48b-136">陣列的指標 (長度為 *NumSubresources* 的 UINTS) ，其中包含每個資料列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="da48b-136">Pointer to an array (of length *NumSubresources*) of UINTS containing the size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="da48b-137">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da48b-137">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da48b-138">Type： **Const [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***</span><span class="sxs-lookup"><span data-stu-id="da48b-138">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="da48b-139">陣列的指標 (長度 *NumSubresources*) 指標指向 [**D3D12 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) 結構的指標，其中包含用於更新的 SUBRESOURCE 資料描述。</span><span class="sxs-lookup"><span data-stu-id="da48b-139">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da48b-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="da48b-140">Return value</span></span>

<span data-ttu-id="da48b-141">類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="da48b-141">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="da48b-142">緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="da48b-142">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="da48b-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="da48b-143">Requirements</span></span>



| <span data-ttu-id="da48b-144">需求</span><span class="sxs-lookup"><span data-stu-id="da48b-144">Requirement</span></span> | <span data-ttu-id="da48b-145">值</span><span class="sxs-lookup"><span data-stu-id="da48b-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="da48b-146">標頭</span><span class="sxs-lookup"><span data-stu-id="da48b-146">Header</span></span><br/>  | <dl> <span data-ttu-id="da48b-147"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="da48b-147"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="da48b-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="da48b-148">Library</span></span><br/> | <dl> <span data-ttu-id="da48b-149"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="da48b-149"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="da48b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="da48b-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="da48b-151"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da48b-151"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da48b-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da48b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da48b-153">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="da48b-153">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="da48b-154">子資源</span><span class="sxs-lookup"><span data-stu-id="da48b-154">Subresources</span></span>](subresources.md)
</dt> </dl>

 

