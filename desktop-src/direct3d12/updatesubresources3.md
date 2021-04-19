---
title: 'UpdateSubresources (堆疊-配置) 函數 (D3dx12 .h) '
description: 使用堆疊配置執行更新子資源。
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997616"
---
# <a name="updatesubresources-stack-allocating-function"></a><span data-ttu-id="fb0f8-104">UpdateSubresources (堆疊配置) 函數</span><span class="sxs-lookup"><span data-stu-id="fb0f8-104">UpdateSubresources (stack-allocating) function</span></span>

<span data-ttu-id="fb0f8-105">使用堆疊配置執行更新子資源。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-105">Updates subresources with a stack-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb0f8-106">語法</span><span class="sxs-lookup"><span data-stu-id="fb0f8-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fb0f8-107">參數</span><span class="sxs-lookup"><span data-stu-id="fb0f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb0f8-108">*pCmdList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb0f8-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0f8-109">類型： **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="fb0f8-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="fb0f8-110">命令清單，做為 [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)的指標。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="fb0f8-111">*pDestinationResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb0f8-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0f8-112">類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="fb0f8-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="fb0f8-113">目的地資源，作為 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)的指標。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="fb0f8-114">*pIntermediate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb0f8-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0f8-115">類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="fb0f8-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="fb0f8-116">中繼資源，作為 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)的指標。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="fb0f8-117">*IntermediateOffset*</span><span class="sxs-lookup"><span data-stu-id="fb0f8-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="fb0f8-118">類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb0f8-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb0f8-119">中繼資源的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="fb0f8-120">*FirstSubresource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb0f8-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0f8-121">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb0f8-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb0f8-122">資源中第一個 subresource 的索引。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="fb0f8-123">有效的值範圍從0到 *MaxSubresources*。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-123">Valid values range from 0 to *MaxSubresources*.</span></span>

</dd> <dt>

<span data-ttu-id="fb0f8-124">*NumSubresources* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb0f8-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0f8-125">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb0f8-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb0f8-126">資源中的子資源數目。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-126">The number of subresources in the resource.</span></span> <span data-ttu-id="fb0f8-127">有效的值範圍從1到 (*MaxSubresources*  -  *FirstSubresource*) 。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-127">Valid values range from 1 to (*MaxSubresources* - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="fb0f8-128">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fb0f8-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0f8-129">類型： **[ **D3D12 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="fb0f8-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="fb0f8-130">陣列的指標 (長度 *NumSubresources*) 指標指向 [**D3D12 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) 結構的指標，其中包含用於更新的 SUBRESOURCE 資料描述。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb0f8-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb0f8-131">Return value</span></span>

<span data-ttu-id="fb0f8-132">類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fb0f8-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fb0f8-133">緩衝區的大小 (以位元組為單位)。</span><span class="sxs-lookup"><span data-stu-id="fb0f8-133">The size, in bytes, of the buffer.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb0f8-134">備註</span><span class="sxs-lookup"><span data-stu-id="fb0f8-134">Remarks</span></span>

<span data-ttu-id="fb0f8-135">此函式的宣告開頭為： `template <UINT MaxSubresources>`</span><span class="sxs-lookup"><span data-stu-id="fb0f8-135">The declaration of this function begins with: `template <UINT MaxSubresources>`</span></span>

## <a name="requirements"></a><span data-ttu-id="fb0f8-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb0f8-136">Requirements</span></span>



| <span data-ttu-id="fb0f8-137">需求</span><span class="sxs-lookup"><span data-stu-id="fb0f8-137">Requirement</span></span> | <span data-ttu-id="fb0f8-138">值</span><span class="sxs-lookup"><span data-stu-id="fb0f8-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fb0f8-139">標頭</span><span class="sxs-lookup"><span data-stu-id="fb0f8-139">Header</span></span><br/>  | <dl> <span data-ttu-id="fb0f8-140"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb0f8-140"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="fb0f8-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="fb0f8-141">Library</span></span><br/> | <dl> <span data-ttu-id="fb0f8-142"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb0f8-142"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="fb0f8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="fb0f8-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb0f8-144"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb0f8-144"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb0f8-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb0f8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb0f8-146">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="fb0f8-146">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="fb0f8-147">子資源</span><span class="sxs-lookup"><span data-stu-id="fb0f8-147">Subresources</span></span>](subresources.md)
</dt> </dl>

 

