---
title: 'GetRequiredIntermediateSize 函式 (D3dx12) '
description: 傳回要用於資料上傳的緩衝區所需大小。
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- GetRequiredIntermediateSize 函式
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15293ce1588704d55f41c364c35db57cbf4c869d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976507"
---
# <a name="getrequiredintermediatesize-function"></a><span data-ttu-id="b79c3-104">GetRequiredIntermediateSize 函式</span><span class="sxs-lookup"><span data-stu-id="b79c3-104">GetRequiredIntermediateSize function</span></span>

<span data-ttu-id="b79c3-105">傳回要用於資料上傳的緩衝區所需大小。</span><span class="sxs-lookup"><span data-stu-id="b79c3-105">Returns the required size of a buffer to be used for data upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="b79c3-106">語法</span><span class="sxs-lookup"><span data-stu-id="b79c3-106">Syntax</span></span>


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a><span data-ttu-id="b79c3-107">參數</span><span class="sxs-lookup"><span data-stu-id="b79c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b79c3-108">*pDestinationResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b79c3-108">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b79c3-109">類型： **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="b79c3-109">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="b79c3-110">代表目的地資源之 [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b79c3-110">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="b79c3-111">*FirstSubresource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b79c3-111">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b79c3-112">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b79c3-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b79c3-113">資源中第一個 subresource 的索引。</span><span class="sxs-lookup"><span data-stu-id="b79c3-113">The index of the first subresource in the resource.</span></span> <span data-ttu-id="b79c3-114">有效值的範圍是0到 D3D12 的要求 \_ \_ 子資源。</span><span class="sxs-lookup"><span data-stu-id="b79c3-114">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="b79c3-115">*NumSubresources* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b79c3-115">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b79c3-116">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b79c3-116">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b79c3-117">資源中的子資源數目。</span><span class="sxs-lookup"><span data-stu-id="b79c3-117">The number of subresources in the resource.</span></span> <span data-ttu-id="b79c3-118">有效值的範圍是0到 (D3D12 \_ 需求 \_ 子資源- *FirstSubresource*) 。</span><span class="sxs-lookup"><span data-stu-id="b79c3-118">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b79c3-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b79c3-119">Return value</span></span>

<span data-ttu-id="b79c3-120">類型： **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b79c3-120">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b79c3-121">緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b79c3-121">The size of the buffer, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b79c3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b79c3-122">Requirements</span></span>



| <span data-ttu-id="b79c3-123">需求</span><span class="sxs-lookup"><span data-stu-id="b79c3-123">Requirement</span></span> | <span data-ttu-id="b79c3-124">值</span><span class="sxs-lookup"><span data-stu-id="b79c3-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b79c3-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b79c3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b79c3-126"><dt>D3dx12。h</dt></span><span class="sxs-lookup"><span data-stu-id="b79c3-126"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b79c3-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="b79c3-127">Library</span></span><br/> | <dl> <span data-ttu-id="b79c3-128"><dt>D3D12 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b79c3-128"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b79c3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b79c3-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="b79c3-130"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b79c3-130"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b79c3-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b79c3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b79c3-132">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="b79c3-132">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

