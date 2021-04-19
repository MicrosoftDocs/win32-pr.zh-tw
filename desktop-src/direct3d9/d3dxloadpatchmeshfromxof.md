---
description: 從 ID3DXFileData 物件載入 patch 網狀。
ms.assetid: 8054e33e-6bf8-4a56-9f66-30600732c84f
title: 'D3DXLoadPatchMeshFromXof 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPatchMeshFromXof
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aa2e75e34927d0bb3c68445b994ee0911adb08f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981249"
---
# <a name="d3dxloadpatchmeshfromxof-function"></a><span data-ttu-id="c38ab-103">D3DXLoadPatchMeshFromXof 函式</span><span class="sxs-lookup"><span data-stu-id="c38ab-103">D3DXLoadPatchMeshFromXof function</span></span>

<span data-ttu-id="c38ab-104">從 [**ID3DXFileData**](id3dxfiledata.md) 物件載入 patch 網狀。</span><span class="sxs-lookup"><span data-stu-id="c38ab-104">Loads a patch mesh from an [**ID3DXFileData**](id3dxfiledata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c38ab-105">語法</span><span class="sxs-lookup"><span data-stu-id="c38ab-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPatchMeshFromXof(
  _In_  LPD3DXFILEDATA    pxofMesh,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ PDWORD            pNumMaterials,
  _Out_ LPD3DXPATCHMESH   *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="c38ab-106">參數</span><span class="sxs-lookup"><span data-stu-id="c38ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c38ab-107">*pxofMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c38ab-107">*pxofMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c38ab-108">類型： **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="c38ab-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="c38ab-109">[**ID3DXFileData**](id3dxfiledata.md)介面的指標，代表要載入的檔案資料物件。</span><span class="sxs-lookup"><span data-stu-id="c38ab-109">Pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the file data object to load.</span></span>

</dd> <dt>

<span data-ttu-id="c38ab-110">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c38ab-110">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c38ab-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c38ab-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c38ab-112">一或多個 [**D3DXMESH**](./d3dxmesh.md) 旗標的組合，指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="c38ab-112">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c38ab-113">*pD3DDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c38ab-113">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c38ab-114">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c38ab-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c38ab-115">用來建立網格之裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="c38ab-115">Pointer to the device that the mesh is created from.</span></span>

</dd> <dt>

<span data-ttu-id="c38ab-116">*ppMaterials* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c38ab-116">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c38ab-117">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c38ab-117">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c38ab-118">網格中包含的材質陣列。</span><span class="sxs-lookup"><span data-stu-id="c38ab-118">Array of materials contained in the mesh.</span></span> <span data-ttu-id="c38ab-119">每個材質都會以 [**ID3DXBuffer**](id3dxbuffer.md) 介面編制索引。</span><span class="sxs-lookup"><span data-stu-id="c38ab-119">Each material is indexed by an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c38ab-120">*ppEffectInstances* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c38ab-120">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c38ab-121">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c38ab-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c38ab-122">包含效果實例陣列的緩衝區指標，傳回網格中每個屬性群組一個。</span><span class="sxs-lookup"><span data-stu-id="c38ab-122">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="c38ab-123">效果實例是用來初始化效果之狀態資訊的特定實例。</span><span class="sxs-lookup"><span data-stu-id="c38ab-123">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="c38ab-124">請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。</span><span class="sxs-lookup"><span data-stu-id="c38ab-124">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="c38ab-125">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="c38ab-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c38ab-126">*pNumMaterials* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c38ab-126">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c38ab-127">類型： **PDWORD**</span><span class="sxs-lookup"><span data-stu-id="c38ab-127">Type: **PDWORD**</span></span>

<span data-ttu-id="c38ab-128">包含網格中材質數目的指標。</span><span class="sxs-lookup"><span data-stu-id="c38ab-128">Pointer that contains the number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c38ab-129">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c38ab-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c38ab-130">類型： **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="c38ab-130">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="c38ab-131">[**ID3DXPatchMesh**](id3dxpatchmesh.md)介面指標的位址，表示已載入的網格。</span><span class="sxs-lookup"><span data-stu-id="c38ab-131">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c38ab-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="c38ab-132">Return value</span></span>

<span data-ttu-id="c38ab-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c38ab-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c38ab-134">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c38ab-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c38ab-135">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="c38ab-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c38ab-136">備註</span><span class="sxs-lookup"><span data-stu-id="c38ab-136">Remarks</span></span>

<span data-ttu-id="c38ab-137">對於不包含效果實例資訊的網格檔，將會從. x 檔案中的材質資訊產生預設效果實例。</span><span class="sxs-lookup"><span data-stu-id="c38ab-137">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="c38ab-138">預設效果實例會有預設值，這些值會對應至 [**D3DMATERIAL9**](d3dmaterial9.md) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="c38ab-138">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="c38ab-139">預設紋理名稱也會填入，但會以不同的方式處理。</span><span class="sxs-lookup"><span data-stu-id="c38ab-139">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="c38ab-140">名稱會是 Texture0@Name ，它會以名稱為 "Texture0" 的 "" 名稱對應至效果變數，並具有稱為 "name" 的注釋。</span><span class="sxs-lookup"><span data-stu-id="c38ab-140">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="c38ab-141">這會包含材質的字串檔案名。</span><span class="sxs-lookup"><span data-stu-id="c38ab-141">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="c38ab-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="c38ab-142">Requirements</span></span>



| <span data-ttu-id="c38ab-143">需求</span><span class="sxs-lookup"><span data-stu-id="c38ab-143">Requirement</span></span> | <span data-ttu-id="c38ab-144">值</span><span class="sxs-lookup"><span data-stu-id="c38ab-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c38ab-145">標頭</span><span class="sxs-lookup"><span data-stu-id="c38ab-145">Header</span></span><br/>  | <dl> <span data-ttu-id="c38ab-146"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="c38ab-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c38ab-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="c38ab-147">Library</span></span><br/> | <dl> <span data-ttu-id="c38ab-148"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c38ab-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c38ab-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c38ab-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c38ab-150">網格函數</span><span class="sxs-lookup"><span data-stu-id="c38ab-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="c38ab-151">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c38ab-151">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="c38ab-152">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="c38ab-152">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
