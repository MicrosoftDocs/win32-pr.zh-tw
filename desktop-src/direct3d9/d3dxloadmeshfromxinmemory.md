---
description: 從記憶體載入網格。
ms.assetid: bbaecc00-97ab-433c-b0c7-ac7837bfc3be
title: 'D3DXLoadMeshFromXInMemory 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 66b07a88a938b09217a2fee2b9eed272233edc75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982207"
---
# <a name="d3dxloadmeshfromxinmemory-function"></a><span data-ttu-id="347c9-103">D3DXLoadMeshFromXInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="347c9-103">D3DXLoadMeshFromXInMemory function</span></span>

<span data-ttu-id="347c9-104">從記憶體載入網格。</span><span class="sxs-lookup"><span data-stu-id="347c9-104">Loads a mesh from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="347c9-105">語法</span><span class="sxs-lookup"><span data-stu-id="347c9-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXInMemory(
  _In_  LPCVOID           Memory,
  _In_  DWORD             SizeOfMemory,
  _Out_ DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="347c9-106">參數</span><span class="sxs-lookup"><span data-stu-id="347c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="347c9-107">*記憶體* \[在\]</span><span class="sxs-lookup"><span data-stu-id="347c9-107">*Memory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="347c9-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="347c9-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="347c9-109">包含網格資料之記憶體緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="347c9-109">Pointer to the memory buffer which contains the mesh data.</span></span>

</dd> <dt>

<span data-ttu-id="347c9-110">*SizeOfMemory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="347c9-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="347c9-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="347c9-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="347c9-112">檔案在記憶體中的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="347c9-112">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="347c9-113">*選項* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="347c9-113">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="347c9-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="347c9-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="347c9-115">結合 [**D3DXMESH**](./d3dxmesh.md) 列舉中的一或多個旗標，指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="347c9-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="347c9-116">*pD3DDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="347c9-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="347c9-117">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="347c9-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="347c9-118">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="347c9-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="347c9-119">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="347c9-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="347c9-120">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="347c9-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="347c9-121">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="347c9-121">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="347c9-122">當方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="347c9-122">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="347c9-123">*ppMaterials* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="347c9-123">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="347c9-124">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="347c9-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="347c9-125">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="347c9-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="347c9-126">當此方法傳回時，此參數會填入 [**D3DXMATERIAL**](d3dxmaterial.md) 結構的陣列，其中包含儲存在 DirectX 檔案中的資訊。</span><span class="sxs-lookup"><span data-stu-id="347c9-126">When this method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information saved in the DirectX file.</span></span>

</dd> <dt>

<span data-ttu-id="347c9-127">*ppEffectInstances* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="347c9-127">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="347c9-128">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="347c9-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="347c9-129">包含效果實例陣列的緩衝區指標，傳回網格中每個屬性群組一個。</span><span class="sxs-lookup"><span data-stu-id="347c9-129">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="347c9-130">效果實例是用來初始化效果之狀態資訊的特定實例。</span><span class="sxs-lookup"><span data-stu-id="347c9-130">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="347c9-131">請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。</span><span class="sxs-lookup"><span data-stu-id="347c9-131">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="347c9-132">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="347c9-132">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="347c9-133">*pNumMaterials* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="347c9-133">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="347c9-134">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="347c9-134">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="347c9-135">當方法傳回時，為 *ppMaterials* 陣列中 [**D3DXMATERIAL**](d3dxmaterial.md)結構數目的指標。</span><span class="sxs-lookup"><span data-stu-id="347c9-135">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="347c9-136">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="347c9-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="347c9-137">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="347c9-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="347c9-138">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示已載入的網格。</span><span class="sxs-lookup"><span data-stu-id="347c9-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="347c9-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="347c9-139">Return value</span></span>

<span data-ttu-id="347c9-140">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="347c9-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="347c9-141">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="347c9-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="347c9-142">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="347c9-142">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="347c9-143">備註</span><span class="sxs-lookup"><span data-stu-id="347c9-143">Remarks</span></span>

<span data-ttu-id="347c9-144">檔案中的所有網格都將折迭成一個輸出網格。</span><span class="sxs-lookup"><span data-stu-id="347c9-144">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="347c9-145">如果檔案包含框架階層，則所有轉換都會套用至網格。</span><span class="sxs-lookup"><span data-stu-id="347c9-145">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="347c9-146">對於不包含效果實例資訊的網格檔，將會從. x 檔案中的材質資訊產生預設效果實例。</span><span class="sxs-lookup"><span data-stu-id="347c9-146">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="347c9-147">預設效果實例會有預設值，這些值會對應至 [**D3DMATERIAL9**](d3dmaterial9.md) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="347c9-147">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="347c9-148">預設紋理名稱也會填入，但會以不同的方式處理。</span><span class="sxs-lookup"><span data-stu-id="347c9-148">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="347c9-149">名稱會是 Texture0@Name ，它會以名稱為 "Texture0" 的 "" 名稱對應至效果變數，並具有稱為 "name" 的注釋。</span><span class="sxs-lookup"><span data-stu-id="347c9-149">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="347c9-150">這會包含材質的字串檔案名。</span><span class="sxs-lookup"><span data-stu-id="347c9-150">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="347c9-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="347c9-151">Requirements</span></span>



| <span data-ttu-id="347c9-152">需求</span><span class="sxs-lookup"><span data-stu-id="347c9-152">Requirement</span></span> | <span data-ttu-id="347c9-153">值</span><span class="sxs-lookup"><span data-stu-id="347c9-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="347c9-154">標頭</span><span class="sxs-lookup"><span data-stu-id="347c9-154">Header</span></span><br/>  | <dl> <span data-ttu-id="347c9-155"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="347c9-155"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="347c9-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="347c9-156">Library</span></span><br/> | <dl> <span data-ttu-id="347c9-157"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="347c9-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="347c9-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="347c9-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="347c9-159">網格函數</span><span class="sxs-lookup"><span data-stu-id="347c9-159">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="347c9-160">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="347c9-160">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="347c9-161">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="347c9-161">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
