---
description: 從 ID3DXFileData 物件載入網格。
ms.assetid: 3fcf6a91-fcd4-46da-8278-13bda8af8274
title: 'D3DXLoadMeshFromXof 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ac58e5e0c27fb3daaa4795f3d4c4a8488e6c3571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322896"
---
# <a name="d3dxloadmeshfromxof-function"></a><span data-ttu-id="c3494-103">D3DXLoadMeshFromXof 函式</span><span class="sxs-lookup"><span data-stu-id="c3494-103">D3DXLoadMeshFromXof function</span></span>

<span data-ttu-id="c3494-104">從 [**ID3DXFileData**](id3dxfiledata.md) 物件載入網格。</span><span class="sxs-lookup"><span data-stu-id="c3494-104">Loads a mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3494-105">語法</span><span class="sxs-lookup"><span data-stu-id="c3494-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromXof(
  _In_    LPD3DXFILEDATA    pxofMesh,
  _Out_   DWORD             Options,
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Out_   LPD3DXBUFFER      *ppAdjacency,
  _Inout_ LPD3DXBUFFER      *ppMaterials,
  _Out_   LPD3DXBUFFER      *ppEffectInstances,
  _Inout_ DWORD             *pNumMaterials,
  _Out_   LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="c3494-106">參數</span><span class="sxs-lookup"><span data-stu-id="c3494-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3494-107">*pxofMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3494-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3494-108">類型： **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="c3494-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="c3494-109">[**ID3DXFileData**](id3dxfiledata.md)介面的指標，代表要載入的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="c3494-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="c3494-110">*選項* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c3494-110">*Options* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3494-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c3494-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c3494-112">結合 [**D3DXMESH**](./d3dxmesh.md) 列舉中的一或多個旗標，指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="c3494-112">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c3494-113">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3494-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3494-114">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c3494-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c3494-115">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="c3494-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c3494-116">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c3494-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3494-117">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3494-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c3494-118">包含相鄰資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="c3494-118">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="c3494-119">相鄰資料包含每個臉部的三個 Dword 陣列，可為網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="c3494-119">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="c3494-120">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="c3494-120">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3494-121">*ppMaterials* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c3494-121">*ppMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3494-122">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3494-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c3494-123">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c3494-123">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="c3494-124">當方法傳回時，這個參數會填入 [**D3DXMATERIAL**](d3dxmaterial.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="c3494-124">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="c3494-125">*ppEffectInstances* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c3494-125">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3494-126">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3494-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c3494-127">包含效果實例陣列的緩衝區指標，傳回網格中每個屬性群組一個。</span><span class="sxs-lookup"><span data-stu-id="c3494-127">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="c3494-128">效果實例是用來初始化效果之狀態資訊的特定實例。</span><span class="sxs-lookup"><span data-stu-id="c3494-128">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="c3494-129">請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。</span><span class="sxs-lookup"><span data-stu-id="c3494-129">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="c3494-130">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="c3494-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3494-131">*pNumMaterials* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c3494-131">*pNumMaterials* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3494-132">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3494-132">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c3494-133">當方法傳回時，為 *ppMaterials* 陣列中 [**D3DXMATERIAL**](d3dxmaterial.md)結構數目的指標。</span><span class="sxs-lookup"><span data-stu-id="c3494-133">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="c3494-134">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c3494-134">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3494-135">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="c3494-135">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="c3494-136">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示已載入的網格。</span><span class="sxs-lookup"><span data-stu-id="c3494-136">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3494-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3494-137">Return value</span></span>

<span data-ttu-id="c3494-138">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3494-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3494-139">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c3494-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c3494-140">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="c3494-140">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3494-141">備註</span><span class="sxs-lookup"><span data-stu-id="c3494-141">Remarks</span></span>

<span data-ttu-id="c3494-142">對於不包含效果實例資訊的網格檔，將會從. x 檔案中的材質資訊產生預設效果實例。</span><span class="sxs-lookup"><span data-stu-id="c3494-142">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="c3494-143">預設效果實例會有預設值，這些值會對應至 [**D3DMATERIAL9**](d3dmaterial9.md) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="c3494-143">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="c3494-144">預設紋理名稱也會填入，但會以不同的方式處理。</span><span class="sxs-lookup"><span data-stu-id="c3494-144">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="c3494-145">名稱會是 Texture0@Name ，它會以名稱為 "Texture0" 的 "" 名稱對應至效果變數，並具有稱為 "name" 的注釋。</span><span class="sxs-lookup"><span data-stu-id="c3494-145">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="c3494-146">這會包含材質的字串檔案名。</span><span class="sxs-lookup"><span data-stu-id="c3494-146">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3494-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3494-147">Requirements</span></span>



| <span data-ttu-id="c3494-148">需求</span><span class="sxs-lookup"><span data-stu-id="c3494-148">Requirement</span></span> | <span data-ttu-id="c3494-149">值</span><span class="sxs-lookup"><span data-stu-id="c3494-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3494-150">標頭</span><span class="sxs-lookup"><span data-stu-id="c3494-150">Header</span></span><br/>  | <dl> <span data-ttu-id="c3494-151"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3494-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c3494-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="c3494-152">Library</span></span><br/> | <dl> <span data-ttu-id="c3494-153"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3494-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3494-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3494-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3494-155">網格函數</span><span class="sxs-lookup"><span data-stu-id="c3494-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="c3494-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c3494-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="c3494-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="c3494-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
