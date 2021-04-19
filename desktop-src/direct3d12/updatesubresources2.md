---
title: 'UpdateSubresources (堆積-配置) 函數 (D3dx12 .h) '
description: 以堆積配置的執行更新子資源。
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
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
ms.openlocfilehash: c97abe59bdd0334fe4b7badf03e44ddc03b85495
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992724"
---
# <a name="updatesubresources-heap-allocating-function"></a><span data-ttu-id="44250-104">UpdateSubresources (堆積配置) 函數</span><span class="sxs-lookup"><span data-stu-id="44250-104">UpdateSubresources (heap-allocating) function</span></span>

<span data-ttu-id="44250-105">以堆積配置的執行更新子資源。</span><span class="sxs-lookup"><span data-stu-id="44250-105">Updates subresources with a heap-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="44250-106">語法</span><span class="sxs-lookup"><span data-stu-id="44250-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="44250-107">參數</span><span class="sxs-lookup"><span data-stu-id="44250-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44250-108">*pCmdList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44250-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44250-109">類型： **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="44250-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="44250-110">命令清單的 [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="44250-110">A pointer to the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface for the command list.</span></span>

</dd> <dt>

<span data-ttu-id="44250-111">*pDestinationResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44250-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44250-112">類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="44250-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="44250-113">代表目的地資源之 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="44250-113">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="44250-114">*pIntermediate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44250-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44250-115">類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="44250-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="44250-116">代表中繼資源之 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="44250-116">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="44250-117">*IntermediateOffset*</span><span class="sxs-lookup"><span data-stu-id="44250-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="44250-118">類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="44250-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="44250-119">中繼資源的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="44250-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="44250-120">*FirstSubresource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44250-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44250-121">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="44250-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="44250-122">資源中第一個 subresource 的索引。</span><span class="sxs-lookup"><span data-stu-id="44250-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="44250-123">有效值的範圍是0到 D3D12 的要求 \_ \_ 子資源。</span><span class="sxs-lookup"><span data-stu-id="44250-123">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="44250-124">*NumSubresources* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44250-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44250-125">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="44250-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="44250-126">資源中的子資源數目。</span><span class="sxs-lookup"><span data-stu-id="44250-126">The number of subresources in the resource.</span></span> <span data-ttu-id="44250-127">有效值的範圍是0到 (D3D12 \_ 需求 \_ 子資源- *FirstSubresource*) 。</span><span class="sxs-lookup"><span data-stu-id="44250-127">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="44250-128">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44250-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44250-129">類型： **[ **D3D12 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="44250-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="44250-130">陣列的指標 (長度 *NumSubresources*) 指標指向 [**D3D12 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) 結構的指標，其中包含用於更新的 SUBRESOURCE 資料描述。</span><span class="sxs-lookup"><span data-stu-id="44250-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44250-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="44250-131">Return value</span></span>

<span data-ttu-id="44250-132">類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="44250-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="44250-133">緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="44250-133">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="44250-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="44250-134">Requirements</span></span>



| <span data-ttu-id="44250-135">需求</span><span class="sxs-lookup"><span data-stu-id="44250-135">Requirement</span></span> | <span data-ttu-id="44250-136">值</span><span class="sxs-lookup"><span data-stu-id="44250-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44250-137">標頭</span><span class="sxs-lookup"><span data-stu-id="44250-137">Header</span></span><br/>  | <dl> <span data-ttu-id="44250-138"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="44250-138"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="44250-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="44250-139">Library</span></span><br/> | <dl> <span data-ttu-id="44250-140"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="44250-140"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="44250-141">DLL</span><span class="sxs-lookup"><span data-stu-id="44250-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="44250-142"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44250-142"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44250-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44250-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44250-144">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="44250-144">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="44250-145">子資源</span><span class="sxs-lookup"><span data-stu-id="44250-145">Subresources</span></span>](subresources.md)
</dt> </dl>

 

