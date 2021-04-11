---
description: 從資源載入網格。
ms.assetid: 3cf253dc-4f3f-4949-ab24-8225667f95f2
title: 'D3DXLoadMeshFromXResource 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b3e1d9d14d86296df48e2d27f77e2f79f3ad73c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696631"
---
# <a name="d3dxloadmeshfromxresource-function"></a><span data-ttu-id="a3abb-103">D3DXLoadMeshFromXResource 函式</span><span class="sxs-lookup"><span data-stu-id="a3abb-103">D3DXLoadMeshFromXResource function</span></span>

<span data-ttu-id="a3abb-104">從資源載入網格。</span><span class="sxs-lookup"><span data-stu-id="a3abb-104">Loads a mesh from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3abb-105">語法</span><span class="sxs-lookup"><span data-stu-id="a3abb-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXResource(
  _In_  HMODULE           Module,
  _In_  LPCSTR            Name,
  _In_  LPCSTR            Type,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="a3abb-106">參數</span><span class="sxs-lookup"><span data-stu-id="a3abb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3abb-107">*課程模組* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3abb-107">*Module* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3abb-108">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3abb-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3abb-109">資源所在模組的控制碼，或與作業系統用來建立目前進程的映射相關聯的模組之 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a3abb-109">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span> <span data-ttu-id="a3abb-110">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a3abb-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a3abb-111">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3abb-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3abb-112">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3abb-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3abb-113">字串的指標，這個字串會指定要建立網格的來源資源。</span><span class="sxs-lookup"><span data-stu-id="a3abb-113">Pointer to a string that specifies the resource to create the mesh from.</span></span> <span data-ttu-id="a3abb-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a3abb-114">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a3abb-115">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3abb-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3abb-116">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3abb-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3abb-117">指定資源類型之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="a3abb-117">Pointer to a string that specifies the resource type.</span></span> <span data-ttu-id="a3abb-118">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="a3abb-118">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a3abb-119">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3abb-119">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3abb-120">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3abb-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3abb-121">[**D3DXMESH**](./d3dxmesh.md)列舉中的一或多個旗標組合，可指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="a3abb-121">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a3abb-122">*pD3DDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a3abb-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3abb-123">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a3abb-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a3abb-124">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="a3abb-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a3abb-125">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3abb-125">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3abb-126">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3abb-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a3abb-127">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="a3abb-127">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="a3abb-128">當方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="a3abb-128">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="a3abb-129">*ppMaterials* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3abb-129">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3abb-130">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3abb-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a3abb-131">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="a3abb-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="a3abb-132">當此方法傳回時，此參數會填入 [**D3DXMATERIAL**](d3dxmaterial.md) 結構的陣列，其中包含儲存在 DirectX 檔案中的資訊。</span><span class="sxs-lookup"><span data-stu-id="a3abb-132">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="a3abb-133">*ppEffectInstances* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3abb-133">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3abb-134">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3abb-134">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a3abb-135">包含效果實例陣列的緩衝區指標，傳回網格中每個屬性群組一個。</span><span class="sxs-lookup"><span data-stu-id="a3abb-135">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="a3abb-136">效果實例是用來初始化效果之狀態資訊的特定實例。</span><span class="sxs-lookup"><span data-stu-id="a3abb-136">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="a3abb-137">請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。</span><span class="sxs-lookup"><span data-stu-id="a3abb-137">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="a3abb-138">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="a3abb-138">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="a3abb-139">*pNumMaterials* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3abb-139">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3abb-140">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3abb-140">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a3abb-141">當方法傳回時，為 *ppMaterials* 陣列中 [**D3DXMATERIAL**](d3dxmaterial.md)結構數目的指標。</span><span class="sxs-lookup"><span data-stu-id="a3abb-141">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="a3abb-142">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3abb-142">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3abb-143">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3abb-143">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="a3abb-144">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示已載入的網格。</span><span class="sxs-lookup"><span data-stu-id="a3abb-144">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3abb-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3abb-145">Return value</span></span>

<span data-ttu-id="a3abb-146">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3abb-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3abb-147">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a3abb-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3abb-148">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="a3abb-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3abb-149">備註</span><span class="sxs-lookup"><span data-stu-id="a3abb-149">Remarks</span></span>

<span data-ttu-id="a3abb-150">若要深入瞭解模組、名稱和類型參數，請參閱 [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) 。</span><span class="sxs-lookup"><span data-stu-id="a3abb-150">See [**FindResource**](/windows/win32/api/winbase/nf-winbase-findresourcea) to find out more about the Module, Name and Type parameters.</span></span>

<span data-ttu-id="a3abb-151">檔案中的所有網格都將折迭成一個輸出網格。</span><span class="sxs-lookup"><span data-stu-id="a3abb-151">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="a3abb-152">如果檔案包含框架階層，則所有轉換都會套用至網格。</span><span class="sxs-lookup"><span data-stu-id="a3abb-152">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="a3abb-153">對於不包含效果實例資訊的網格檔，將會從. x 檔案中的材質資訊產生預設效果實例。</span><span class="sxs-lookup"><span data-stu-id="a3abb-153">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="a3abb-154">預設效果實例會有預設值，這些值會對應至 [**D3DMATERIAL9**](d3dmaterial9.md) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="a3abb-154">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="a3abb-155">預設紋理名稱也會填入，但會以不同的方式處理。</span><span class="sxs-lookup"><span data-stu-id="a3abb-155">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="a3abb-156">名稱會是 Texture0@Name ，它會以名稱為 "Texture0" 的 "" 名稱對應至效果變數，並具有稱為 "name" 的注釋。</span><span class="sxs-lookup"><span data-stu-id="a3abb-156">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="a3abb-157">這會包含材質的字串檔案名。</span><span class="sxs-lookup"><span data-stu-id="a3abb-157">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3abb-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3abb-158">Requirements</span></span>



| <span data-ttu-id="a3abb-159">需求</span><span class="sxs-lookup"><span data-stu-id="a3abb-159">Requirement</span></span> | <span data-ttu-id="a3abb-160">值</span><span class="sxs-lookup"><span data-stu-id="a3abb-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3abb-161">標頭</span><span class="sxs-lookup"><span data-stu-id="a3abb-161">Header</span></span><br/>  | <dl> <span data-ttu-id="a3abb-162"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="a3abb-162"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a3abb-163">程式庫</span><span class="sxs-lookup"><span data-stu-id="a3abb-163">Library</span></span><br/> | <dl> <span data-ttu-id="a3abb-164"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3abb-164"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3abb-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3abb-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3abb-166">網格函數</span><span class="sxs-lookup"><span data-stu-id="a3abb-166">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="a3abb-167">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a3abb-167">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="a3abb-168">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="a3abb-168">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
