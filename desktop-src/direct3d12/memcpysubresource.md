---
title: 'MemcpySubresource 函式 (D3dx12) '
description: 逐列複製 subresource 資料列。
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- MemcpySubresource 函式
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988202"
---
# <a name="memcpysubresource-function"></a><span data-ttu-id="5f967-104">MemcpySubresource 函式</span><span class="sxs-lookup"><span data-stu-id="5f967-104">MemcpySubresource function</span></span>

<span data-ttu-id="5f967-105">逐列複製 subresource 資料列。</span><span class="sxs-lookup"><span data-stu-id="5f967-105">Copies a subresource row by row.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f967-106">語法</span><span class="sxs-lookup"><span data-stu-id="5f967-106">Syntax</span></span>


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a><span data-ttu-id="5f967-107">參數</span><span class="sxs-lookup"><span data-stu-id="5f967-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f967-108">*pDest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f967-108">*pDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f967-109">Type： **Const [**D3D12 \_ MEMCPY \_ DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***</span><span class="sxs-lookup"><span data-stu-id="5f967-109">Type: **const [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest)\***</span></span>

<span data-ttu-id="5f967-110">[**D3D12 \_ MEMCPY \_ 目的地**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest)結構的指標，此結構描述記憶體複製作業的目的地。</span><span class="sxs-lookup"><span data-stu-id="5f967-110">A pointer to a [**D3D12\_MEMCPY\_DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) structure that describes the destination of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="5f967-111">*.psrc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5f967-111">*pSrc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f967-112">Type： **Const [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***</span><span class="sxs-lookup"><span data-stu-id="5f967-112">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="5f967-113">[**D3D12 \_ SUBRESOURCE \_ 資料**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)結構的指標，此結構描述記憶體複製作業的來源。</span><span class="sxs-lookup"><span data-stu-id="5f967-113">A pointer to a [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structure that describes the source of the memory copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="5f967-114">*RowSizeInBytes*</span><span class="sxs-lookup"><span data-stu-id="5f967-114">*RowSizeInBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="5f967-115">類型： **[**大小 \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5f967-115">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5f967-116">每個資料列的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5f967-116">The size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="5f967-117">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="5f967-117">*NumRows*</span></span> 
</dt> <dd>

<span data-ttu-id="5f967-118">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5f967-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5f967-119">列的數目。</span><span class="sxs-lookup"><span data-stu-id="5f967-119">The number of rows.</span></span>

</dd> <dt>

<span data-ttu-id="5f967-120">*NumSlices*</span><span class="sxs-lookup"><span data-stu-id="5f967-120">*NumSlices*</span></span> 
</dt> <dd>

<span data-ttu-id="5f967-121">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="5f967-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="5f967-122">配量的數目。</span><span class="sxs-lookup"><span data-stu-id="5f967-122">The number of slices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f967-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f967-123">Return value</span></span>

<span data-ttu-id="5f967-124">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5f967-124">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f967-125">備註</span><span class="sxs-lookup"><span data-stu-id="5f967-125">Remarks</span></span>

<span data-ttu-id="5f967-126">也請考慮下列方法：</span><span class="sxs-lookup"><span data-stu-id="5f967-126">Also consider the following methods:</span></span>

-   [<span data-ttu-id="5f967-127">**ID3D12Resource::WriteToSubresource**</span><span class="sxs-lookup"><span data-stu-id="5f967-127">**ID3D12Resource::WriteToSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [<span data-ttu-id="5f967-128">**ID3D12Resource::ReadFromSubresource**</span><span class="sxs-lookup"><span data-stu-id="5f967-128">**ID3D12Resource::ReadFromSubresource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [<span data-ttu-id="5f967-129">**ID3D12GraphicsCommandList::CopyResource**</span><span class="sxs-lookup"><span data-stu-id="5f967-129">**ID3D12GraphicsCommandList::CopyResource**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a><span data-ttu-id="5f967-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f967-130">Requirements</span></span>



| <span data-ttu-id="5f967-131">需求</span><span class="sxs-lookup"><span data-stu-id="5f967-131">Requirement</span></span> | <span data-ttu-id="5f967-132">值</span><span class="sxs-lookup"><span data-stu-id="5f967-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5f967-133">標頭</span><span class="sxs-lookup"><span data-stu-id="5f967-133">Header</span></span><br/>  | <dl> <span data-ttu-id="5f967-134"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f967-134"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="5f967-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="5f967-135">Library</span></span><br/> | <dl> <span data-ttu-id="5f967-136"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f967-136"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="5f967-137">DLL</span><span class="sxs-lookup"><span data-stu-id="5f967-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="5f967-138"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f967-138"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f967-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f967-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f967-140">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="5f967-140">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="5f967-141">子資源</span><span class="sxs-lookup"><span data-stu-id="5f967-141">Subresources</span></span>](subresources.md)
</dt> </dl>

 

