---
description: D3DXLoadMeshHierarchyFromXInMemory 函式-從. x 檔案載入第一個框架階層。
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: 'D3DXLoadMeshHierarchyFromXInMemory 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 551810c839e619985d9a380197553f5fe4fc9be8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098206"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a><span data-ttu-id="de09d-103">D3DXLoadMeshHierarchyFromXInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="de09d-103">D3DXLoadMeshHierarchyFromXInMemory function</span></span>

<span data-ttu-id="de09d-104">從. x 檔案載入第一個框架階層。</span><span class="sxs-lookup"><span data-stu-id="de09d-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="de09d-105">語法</span><span class="sxs-lookup"><span data-stu-id="de09d-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="de09d-106">參數</span><span class="sxs-lookup"><span data-stu-id="de09d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de09d-107">*pMemory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de09d-107">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de09d-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de09d-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de09d-109">包含網格階層之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="de09d-109">Pointer to a buffer that contains the mesh hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="de09d-110">*SizeOfMemory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de09d-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de09d-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de09d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de09d-112">PMemory 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="de09d-112">Size of the pMemory buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="de09d-113">*MeshOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de09d-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de09d-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="de09d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="de09d-115">[**D3DXMESH**](./d3dxmesh.md)列舉中的一或多個旗標組合，可指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="de09d-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="de09d-116">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de09d-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de09d-117">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="de09d-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="de09d-118">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="de09d-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="de09d-119">*pAlloc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de09d-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de09d-120">類型： **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="de09d-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="de09d-121">[**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="de09d-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="de09d-122">*pUserDataLoader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de09d-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de09d-123">類型： **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="de09d-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="de09d-124">應用程式提供的介面，可讓使用者資料載入。</span><span class="sxs-lookup"><span data-stu-id="de09d-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="de09d-125">請參閱 [**ID3DXLoadUserData**](id3dxloaduserdata.md)。</span><span class="sxs-lookup"><span data-stu-id="de09d-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="de09d-126">*ppFrameHeirarchy* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="de09d-126">*ppFrameHeirarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de09d-127">類型： **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="de09d-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="de09d-128">傳回已載入框架階層的指標。</span><span class="sxs-lookup"><span data-stu-id="de09d-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="de09d-129">請參閱 [**D3DXFRAME**](d3dxframe.md)。</span><span class="sxs-lookup"><span data-stu-id="de09d-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="de09d-130">*ppAnimController* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="de09d-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de09d-131">類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="de09d-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="de09d-132">傳回與. x 檔案中的動畫相對應的動畫控制器指標。</span><span class="sxs-lookup"><span data-stu-id="de09d-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="de09d-133">這會使用預設的追蹤和事件來建立。</span><span class="sxs-lookup"><span data-stu-id="de09d-133">This is created with default tracks and events.</span></span> <span data-ttu-id="de09d-134">請參閱 [**ID3DXAnimationController**](id3dxanimationcontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="de09d-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de09d-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="de09d-135">Return value</span></span>

<span data-ttu-id="de09d-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="de09d-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="de09d-137">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="de09d-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="de09d-138">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="de09d-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="de09d-139">備註</span><span class="sxs-lookup"><span data-stu-id="de09d-139">Remarks</span></span>

<span data-ttu-id="de09d-140">檔案中的所有網格都將折迭成一個輸出網格。</span><span class="sxs-lookup"><span data-stu-id="de09d-140">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="de09d-141">如果檔案包含框架階層，則所有轉換都會套用至網格。</span><span class="sxs-lookup"><span data-stu-id="de09d-141">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="de09d-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="de09d-142">Requirements</span></span>



| <span data-ttu-id="de09d-143">需求</span><span class="sxs-lookup"><span data-stu-id="de09d-143">Requirement</span></span> | <span data-ttu-id="de09d-144">值</span><span class="sxs-lookup"><span data-stu-id="de09d-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de09d-145">標頭</span><span class="sxs-lookup"><span data-stu-id="de09d-145">Header</span></span><br/>  | <dl> <span data-ttu-id="de09d-146"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="de09d-146"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="de09d-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="de09d-147">Library</span></span><br/> | <dl> <span data-ttu-id="de09d-148"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="de09d-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="de09d-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de09d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de09d-150">動畫函數</span><span class="sxs-lookup"><span data-stu-id="de09d-150">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
