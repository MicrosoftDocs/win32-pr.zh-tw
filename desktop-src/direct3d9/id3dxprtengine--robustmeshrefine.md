---
description: 在網格上細分臉部，以提供不會消除網格上功能的保守調適型取樣。
ms.assetid: 0d74a01a-de67-4607-99eb-ed98e239f199
title: 'ID3DXPRTEngine：： RobustMeshRefine 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.RobustMeshRefine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65d49fcec3072956365ce1ed8dc5d7a11ce6c826
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991977"
---
# <a name="id3dxprtenginerobustmeshrefine-method"></a><span data-ttu-id="19cb3-103">ID3DXPRTEngine：： RobustMeshRefine 方法</span><span class="sxs-lookup"><span data-stu-id="19cb3-103">ID3DXPRTEngine::RobustMeshRefine method</span></span>

<span data-ttu-id="19cb3-104">在網格上細分臉部，以提供不會消除網格上功能的保守調適型取樣。</span><span class="sxs-lookup"><span data-stu-id="19cb3-104">Subdivides faces on a mesh, allowing for conservative adaptive sampling that will not eliminate features on the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="19cb3-105">語法</span><span class="sxs-lookup"><span data-stu-id="19cb3-105">Syntax</span></span>


```C++
HRESULT RobustMeshRefine(
  [in] FLOAT MinEdgeLength,
  [in] UINT  MaxSubdiv
);
```



## <a name="parameters"></a><span data-ttu-id="19cb3-106">參數</span><span class="sxs-lookup"><span data-stu-id="19cb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19cb3-107">*MinEdgeLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19cb3-107">*MinEdgeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cb3-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19cb3-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19cb3-109">自動調整取樣中將產生的最小臉部邊長度。</span><span class="sxs-lookup"><span data-stu-id="19cb3-109">Minimum face edge length that will be generated in adaptive sampling.</span></span> <span data-ttu-id="19cb3-110">如果為零，將會取代合理的預設值。</span><span class="sxs-lookup"><span data-stu-id="19cb3-110">If zero, a reasonable default value will be substituted.</span></span>

</dd> <dt>

<span data-ttu-id="19cb3-111">*MaxSubdiv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19cb3-111">*MaxSubdiv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cb3-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="19cb3-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="19cb3-113">臉部的最大細分層級，將用於適應性取樣中。</span><span class="sxs-lookup"><span data-stu-id="19cb3-113">Maximum level of subdivision of a face that will be used in adaptive sampling.</span></span> <span data-ttu-id="19cb3-114">如果為零，則會替代預設值5。</span><span class="sxs-lookup"><span data-stu-id="19cb3-114">If zero, a default value of 5 will be substituted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19cb3-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="19cb3-115">Return value</span></span>

<span data-ttu-id="19cb3-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="19cb3-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="19cb3-117">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="19cb3-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="19cb3-118">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="19cb3-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="19cb3-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="19cb3-119">Requirements</span></span>



| <span data-ttu-id="19cb3-120">需求</span><span class="sxs-lookup"><span data-stu-id="19cb3-120">Requirement</span></span> | <span data-ttu-id="19cb3-121">值</span><span class="sxs-lookup"><span data-stu-id="19cb3-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19cb3-122">標頭</span><span class="sxs-lookup"><span data-stu-id="19cb3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="19cb3-123"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="19cb3-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="19cb3-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="19cb3-124">Library</span></span><br/> | <dl> <span data-ttu-id="19cb3-125"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="19cb3-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="19cb3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19cb3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19cb3-127">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="19cb3-127">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="19cb3-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span><span class="sxs-lookup"><span data-stu-id="19cb3-128">**ID3DXPRTEngine::ComputeBounceAdaptive**</span></span>](id3dxprtengine--computebounceadaptive.md)
</dt> <dt>

[<span data-ttu-id="19cb3-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span><span class="sxs-lookup"><span data-stu-id="19cb3-129">**ID3DXPRTEngine::ComputeDirectLightingSHAdaptive**</span></span>](id3dxprtengine--computedirectlightingshadaptive.md)
</dt> </dl>

 

 
