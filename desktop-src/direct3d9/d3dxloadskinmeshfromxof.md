---
description: 從 DirectX. x 檔案資料物件載入外觀網格。
ms.assetid: db284061-2996-4a5f-972d-24577dd1a6d7
title: 'D3DXLoadSkinMeshFromXof 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSkinMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b87e97e0bde7be37497f68c276a09163ea68ee71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696576"
---
# <a name="d3dxloadskinmeshfromxof-function"></a><span data-ttu-id="c5d90-103">D3DXLoadSkinMeshFromXof 函式</span><span class="sxs-lookup"><span data-stu-id="c5d90-103">D3DXLoadSkinMeshFromXof function</span></span>

<span data-ttu-id="c5d90-104">從 DirectX. x 檔案資料物件載入外觀網格。</span><span class="sxs-lookup"><span data-stu-id="c5d90-104">Loads a skin mesh from a DirectX .x file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d90-105">語法</span><span class="sxs-lookup"><span data-stu-id="c5d90-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSkinMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pMatOut,
  _Out_ LPD3DXSKININFO    *ppSkinInfo,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="c5d90-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5d90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5d90-107">*pxofMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5d90-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d90-108">類型： **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="c5d90-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="c5d90-109">[**ID3DXFileData**](id3dxfiledata.md)介面的指標，代表要載入的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="c5d90-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="c5d90-110">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5d90-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d90-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5d90-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5d90-112">一或多個旗標的組合，從 [**D3DXMESH**](./d3dxmesh.md) 列舉中指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="c5d90-112">Combination of one or more flags, from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c5d90-113">*pD3DDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5d90-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d90-114">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c5d90-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c5d90-115">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="c5d90-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c5d90-116">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5d90-116">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d90-117">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5d90-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c5d90-118">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c5d90-118">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="c5d90-119">當此方法傳回時，此參數會填入三個 Dword 的陣列，每個臉部會針對網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="c5d90-119">When this method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c5d90-120">*ppMaterials* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5d90-120">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d90-121">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5d90-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c5d90-122">[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c5d90-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="c5d90-123">當方法傳回時，這個參數會填入 [**D3DXMATERIAL**](d3dxmaterial.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="c5d90-123">When the method returns, this parameter is filled with an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="c5d90-124">*ppEffectInstances* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5d90-124">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d90-125">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5d90-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c5d90-126">包含效果實例陣列的緩衝區指標，傳回網格中每個屬性群組一個。</span><span class="sxs-lookup"><span data-stu-id="c5d90-126">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="c5d90-127">效果實例是用來初始化效果之狀態資訊的特定實例。</span><span class="sxs-lookup"><span data-stu-id="c5d90-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="c5d90-128">請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。</span><span class="sxs-lookup"><span data-stu-id="c5d90-128">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="c5d90-129">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="c5d90-129">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c5d90-130">*pMatOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5d90-130">*pMatOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d90-131">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5d90-131">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c5d90-132">當方法傳回時，為 *ppMaterials* 陣列中 [**D3DXMATERIAL**](d3dxmaterial.md)結構數目的指標。</span><span class="sxs-lookup"><span data-stu-id="c5d90-132">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="c5d90-133">*ppSkinInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5d90-133">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d90-134">類型： **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5d90-134">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***</span></span>

<span data-ttu-id="c5d90-135">[**ID3DXSkinInfo**](id3dxskininfo.md)介面指標的位址，代表外觀資訊。</span><span class="sxs-lookup"><span data-stu-id="c5d90-135">Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, which represents the skinning information.</span></span>

</dd> <dt>

<span data-ttu-id="c5d90-136">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5d90-136">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5d90-137">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5d90-137">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="c5d90-138">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示已載入的網格。</span><span class="sxs-lookup"><span data-stu-id="c5d90-138">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, which represents the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5d90-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5d90-139">Return value</span></span>

<span data-ttu-id="c5d90-140">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5d90-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5d90-141">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c5d90-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c5d90-142">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="c5d90-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY</span></span>

## <a name="remarks"></a><span data-ttu-id="c5d90-143">備註</span><span class="sxs-lookup"><span data-stu-id="c5d90-143">Remarks</span></span>

<span data-ttu-id="c5d90-144">這個方法會取得. x 檔案中內建物件的指標，讓您可以載入框架階層。</span><span class="sxs-lookup"><span data-stu-id="c5d90-144">This method takes a pointer to an internal object in the .x file, enabling you to load the frame hierarchy.</span></span>

<span data-ttu-id="c5d90-145">對於不包含效果實例資訊的網格檔，將會從. x 檔案中的材質資訊產生預設效果實例。</span><span class="sxs-lookup"><span data-stu-id="c5d90-145">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="c5d90-146">預設效果實例會有預設值，這些值會對應至 [**D3DMATERIAL9**](d3dmaterial9.md) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="c5d90-146">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="c5d90-147">預設紋理名稱也會填入，但會以不同的方式處理。</span><span class="sxs-lookup"><span data-stu-id="c5d90-147">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="c5d90-148">名稱會是 Texture0@Name ，它會以名稱為 "Texture0" 的 "" 名稱對應至效果變數，並具有稱為 "name" 的注釋。</span><span class="sxs-lookup"><span data-stu-id="c5d90-148">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="c5d90-149">這會包含材質的字串檔案名。</span><span class="sxs-lookup"><span data-stu-id="c5d90-149">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d90-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5d90-150">Requirements</span></span>



| <span data-ttu-id="c5d90-151">需求</span><span class="sxs-lookup"><span data-stu-id="c5d90-151">Requirement</span></span> | <span data-ttu-id="c5d90-152">值</span><span class="sxs-lookup"><span data-stu-id="c5d90-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d90-153">標頭</span><span class="sxs-lookup"><span data-stu-id="c5d90-153">Header</span></span><br/>  | <dl> <span data-ttu-id="c5d90-154"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5d90-154"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c5d90-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="c5d90-155">Library</span></span><br/> | <dl> <span data-ttu-id="c5d90-156"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5d90-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c5d90-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5d90-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d90-158">網格函數</span><span class="sxs-lookup"><span data-stu-id="c5d90-158">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="c5d90-159">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c5d90-159">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="c5d90-160">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="c5d90-160">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
