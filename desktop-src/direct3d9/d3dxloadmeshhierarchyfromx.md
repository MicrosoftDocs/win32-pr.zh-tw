---
description: 從. x 檔案載入第一個框架階層。
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: 'D3DXLoadMeshHierarchyFromX 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 308ebf127708849bec8ee8a4f2601f029562634a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946049"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a><span data-ttu-id="15c37-103">D3DXLoadMeshHierarchyFromX 函式</span><span class="sxs-lookup"><span data-stu-id="15c37-103">D3DXLoadMeshHierarchyFromX function</span></span>

<span data-ttu-id="15c37-104">從. x 檔案載入第一個框架階層。</span><span class="sxs-lookup"><span data-stu-id="15c37-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c37-105">語法</span><span class="sxs-lookup"><span data-stu-id="15c37-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="15c37-106">參數</span><span class="sxs-lookup"><span data-stu-id="15c37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c37-107">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="15c37-107">*Filename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c37-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15c37-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15c37-109">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="15c37-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="15c37-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="15c37-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="15c37-111">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="15c37-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="15c37-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="15c37-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="15c37-113">*MeshOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="15c37-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c37-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15c37-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15c37-115">[**D3DXMESH**](./d3dxmesh.md)列舉中的一或多個旗標組合，可指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="15c37-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="15c37-116">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="15c37-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c37-117">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="15c37-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="15c37-118">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="15c37-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="15c37-119">*pAlloc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="15c37-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c37-120">類型： **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="15c37-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="15c37-121">[**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="15c37-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="15c37-122">*pUserDataLoader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="15c37-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c37-123">類型： **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="15c37-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="15c37-124">應用程式提供的介面，可讓使用者資料載入。</span><span class="sxs-lookup"><span data-stu-id="15c37-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="15c37-125">請參閱 [**ID3DXLoadUserData**](id3dxloaduserdata.md)。</span><span class="sxs-lookup"><span data-stu-id="15c37-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="15c37-126">*ppFrameHierarchy* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="15c37-126">*ppFrameHierarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15c37-127">類型： **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="15c37-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="15c37-128">傳回已載入框架階層的指標。</span><span class="sxs-lookup"><span data-stu-id="15c37-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="15c37-129">請參閱 [**D3DXFRAME**](d3dxframe.md)。</span><span class="sxs-lookup"><span data-stu-id="15c37-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="15c37-130">*ppAnimController* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="15c37-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15c37-131">類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="15c37-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="15c37-132">傳回與. x 檔案中的動畫相對應的動畫控制器指標。</span><span class="sxs-lookup"><span data-stu-id="15c37-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="15c37-133">這會使用預設的追蹤和事件來建立。</span><span class="sxs-lookup"><span data-stu-id="15c37-133">This is created with default tracks and events.</span></span> <span data-ttu-id="15c37-134">請參閱 [**ID3DXAnimationController**](id3dxanimationcontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="15c37-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15c37-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="15c37-135">Return value</span></span>

<span data-ttu-id="15c37-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15c37-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15c37-137">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="15c37-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="15c37-138">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="15c37-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="15c37-139">備註</span><span class="sxs-lookup"><span data-stu-id="15c37-139">Remarks</span></span>

<span data-ttu-id="15c37-140">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="15c37-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="15c37-141">如果已定義 Unicode，函式呼叫會解析為 D3DXLoadMeshHierarchyFromXW。</span><span class="sxs-lookup"><span data-stu-id="15c37-141">If Unicode is defined, the function call resolves to D3DXLoadMeshHierarchyFromXW.</span></span> <span data-ttu-id="15c37-142">否則，函式呼叫會解析為 D3DXLoadMeshHierarchyFromXA。</span><span class="sxs-lookup"><span data-stu-id="15c37-142">Otherwise, the function call resolves to D3DXLoadMeshHierarchyFromXA.</span></span>

<span data-ttu-id="15c37-143">檔案中的所有網格都將折迭成一個輸出網格。</span><span class="sxs-lookup"><span data-stu-id="15c37-143">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="15c37-144">如果檔案包含框架階層，則所有轉換都會套用至網格。</span><span class="sxs-lookup"><span data-stu-id="15c37-144">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="15c37-145">**D3DXLoadMeshHierarchyFromX** 會從. x 檔案載入動畫資料和框架階層。</span><span class="sxs-lookup"><span data-stu-id="15c37-145">**D3DXLoadMeshHierarchyFromX** loads the animation data and frame hierarchy from a .x file.</span></span> <span data-ttu-id="15c37-146">它會掃描. x 檔案，並根據透過 pAlloc 傳遞給它的 [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)衍生物件，建立框架階層和動畫控制器。</span><span class="sxs-lookup"><span data-stu-id="15c37-146">It scans the .x file and builds a frame hierarchy and animation controller according to the [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)-derived object passed to it through pAlloc.</span></span> <span data-ttu-id="15c37-147">載入資料需要幾個步驟，如下所示：</span><span class="sxs-lookup"><span data-stu-id="15c37-147">Loading the data requires several steps as follows:</span></span>

1.  <span data-ttu-id="15c37-148">衍生 [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)，以執行每個方法。</span><span class="sxs-lookup"><span data-stu-id="15c37-148">Derive [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), implementing each method.</span></span> <span data-ttu-id="15c37-149">這會控制如何配置和釋放畫面格和網格。</span><span class="sxs-lookup"><span data-stu-id="15c37-149">This controls how frames and meshes are allocated and freed.</span></span>
2.  <span data-ttu-id="15c37-150">衍生 [**ID3DXLoadUserData**](id3dxloaduserdata.md)，以執行每個方法。</span><span class="sxs-lookup"><span data-stu-id="15c37-150">Derive [**ID3DXLoadUserData**](id3dxloaduserdata.md), implementing each method.</span></span> <span data-ttu-id="15c37-151">如果您的. x 檔案沒有內嵌使用者定義的資料，或者您不需要它，您可以略過這個部分。</span><span class="sxs-lookup"><span data-stu-id="15c37-151">If your .x file has no embedded user-defined data, or if you do not need it, you can skip this part.</span></span>
3.  <span data-ttu-id="15c37-152">建立 [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) 類別的物件，並選擇性地建立您的 LoadUserData 類別。</span><span class="sxs-lookup"><span data-stu-id="15c37-152">Create an object of your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class, and optionally of your LoadUserData class.</span></span> <span data-ttu-id="15c37-153">您不需要自行呼叫這些物件的任何方法。</span><span class="sxs-lookup"><span data-stu-id="15c37-153">You do not need to call any methods of these objects yourself.</span></span>
4.  <span data-ttu-id="15c37-154">呼叫 **D3DXLoadMeshHierarchyFromX**，傳入您的 [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) 物件和 [**ID3DXLoadUserData**](id3dxloaduserdata.md) 物件 (或 **Null**) ，以建立框架階層和動畫控制器。</span><span class="sxs-lookup"><span data-stu-id="15c37-154">Call **D3DXLoadMeshHierarchyFromX**, passing in your [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) object and your [**ID3DXLoadUserData**](id3dxloaduserdata.md) object (or **NULL**) to create the frame hierarchy and animation controller.</span></span> <span data-ttu-id="15c37-155">所有的動畫集合和框架都會自動註冊至動畫控制器。</span><span class="sxs-lookup"><span data-stu-id="15c37-155">All the animation sets and frames are automatically registered to the animation controller.</span></span>

<span data-ttu-id="15c37-156">在載入期間，會在每個畫面上呼叫 [**CreateFrame**](id3dxallocatehierarchy--createframe.md) 和 [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) ，以控制框架的載入和配置。</span><span class="sxs-lookup"><span data-stu-id="15c37-156">During the load, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) and [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) are called back on each frame to control loading and allocation of the frame.</span></span> <span data-ttu-id="15c37-157">應用程式會定義這些方法來控制框架的儲存方式。</span><span class="sxs-lookup"><span data-stu-id="15c37-157">The application defines these methods to control how frames are stored.</span></span> <span data-ttu-id="15c37-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) 和 [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) 會在每個網格物件上被回呼，以控制網格物件的載入和配置。</span><span class="sxs-lookup"><span data-stu-id="15c37-158">[**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) and [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) are called back on each mesh object to control loading and allocation of mesh objects.</span></span> <span data-ttu-id="15c37-159">針對不是由其他方法載入的每個最上層物件，會呼叫 [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) 。</span><span class="sxs-lookup"><span data-stu-id="15c37-159">[**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) is called back for each top level object that doesn't get loaded by the other methods.</span></span>

<span data-ttu-id="15c37-160">若要釋放這項資料，請呼叫 ID3DXAnimationController：： Release 來釋出動畫集，並在框架階層的根節點和衍生 [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)類別的物件中傳遞 [**D3DXFRAMEDestroy**](d3dxframedestroy.md)。</span><span class="sxs-lookup"><span data-stu-id="15c37-160">To free this data, call ID3DXAnimationController::Release to free the animation sets, and [**D3DXFRAMEDestroy**](d3dxframedestroy.md), passing in the root node of the frame hierarchy and an object of your derived [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) class.</span></span> <span data-ttu-id="15c37-161">系統會針對框架階層中的每個畫面格和網格物件呼叫 [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md)和 [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) 。</span><span class="sxs-lookup"><span data-stu-id="15c37-161">[**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) and [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) will each be called for every frame and mesh object in the frame hierarchy.</span></span> <span data-ttu-id="15c37-162">**DestroyFrame** 的執行應該釋出 [**CreateFrame**](id3dxallocatehierarchy--createframe.md)所配置的所有專案，同樣是針對網格容器方法。</span><span class="sxs-lookup"><span data-stu-id="15c37-162">Your implementation of **DestroyFrame** should release everything allocated by [**CreateFrame**](id3dxallocatehierarchy--createframe.md), and likewise for the mesh container methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c37-163">規格需求</span><span class="sxs-lookup"><span data-stu-id="15c37-163">Requirements</span></span>



| <span data-ttu-id="15c37-164">需求</span><span class="sxs-lookup"><span data-stu-id="15c37-164">Requirement</span></span> | <span data-ttu-id="15c37-165">值</span><span class="sxs-lookup"><span data-stu-id="15c37-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15c37-166">標頭</span><span class="sxs-lookup"><span data-stu-id="15c37-166">Header</span></span><br/>  | <dl> <span data-ttu-id="15c37-167"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="15c37-167"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="15c37-168">程式庫</span><span class="sxs-lookup"><span data-stu-id="15c37-168">Library</span></span><br/> | <dl> <span data-ttu-id="15c37-169"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="15c37-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15c37-170">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15c37-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c37-171">動畫函數</span><span class="sxs-lookup"><span data-stu-id="15c37-171">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
