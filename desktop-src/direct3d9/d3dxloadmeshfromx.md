---
description: 從 DirectX. x 檔案載入網格。
ms.assetid: cc43d2c4-3547-4431-b506-010cced26754
title: 'D3DXLoadMeshFromX 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35622bc62804f012b4ac858f56b336dc60fbbac5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322899"
---
# <a name="d3dxloadmeshfromx-function"></a><span data-ttu-id="9242a-103">D3DXLoadMeshFromX 函式</span><span class="sxs-lookup"><span data-stu-id="9242a-103">D3DXLoadMeshFromX function</span></span>

<span data-ttu-id="9242a-104">從 DirectX. x 檔案載入網格。</span><span class="sxs-lookup"><span data-stu-id="9242a-104">Loads a mesh from a DirectX .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9242a-105">語法</span><span class="sxs-lookup"><span data-stu-id="9242a-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshFromX(
  _In_  LPCTSTR           pFilename,
  _In_  DWORD             Options,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXBUFFER      *ppAdjacency,
  _Out_ LPD3DXBUFFER      *ppMaterials,
  _Out_ LPD3DXBUFFER      *ppEffectInstances,
  _Out_ DWORD             *pNumMaterials,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="9242a-106">參數</span><span class="sxs-lookup"><span data-stu-id="9242a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9242a-107">*pFilename* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9242a-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9242a-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9242a-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9242a-109">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="9242a-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="9242a-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="9242a-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="9242a-111">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="9242a-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="9242a-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="9242a-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9242a-113">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9242a-113">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9242a-114">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9242a-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9242a-115">[**D3DXMESH**](./d3dxmesh.md)列舉中的一或多個旗標組合，指定網格的建立選項。</span><span class="sxs-lookup"><span data-stu-id="9242a-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, which specifies creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9242a-116">*pD3DDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9242a-116">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9242a-117">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9242a-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9242a-118">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，與網格相關聯的裝置物件。</span><span class="sxs-lookup"><span data-stu-id="9242a-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9242a-119">*ppAdjacency* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9242a-119">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9242a-120">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9242a-120">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9242a-121">包含相鄰資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="9242a-121">Pointer to a buffer that contains adjacency data.</span></span> <span data-ttu-id="9242a-122">相鄰資料包含每個臉部的三個 Dword 陣列，可為網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="9242a-122">The adjacency data contains an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="9242a-123">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="9242a-123">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9242a-124">*ppMaterials* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9242a-124">*ppMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9242a-125">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9242a-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9242a-126">包含材質資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="9242a-126">Pointer to a buffer containing materials data.</span></span> <span data-ttu-id="9242a-127">緩衝區包含 [**D3DXMATERIAL**](d3dxmaterial.md) 結構的陣列，其中包含來自 DirectX 檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="9242a-127">The buffer contains an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing information from the DirectX file.</span></span> <span data-ttu-id="9242a-128">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="9242a-128">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9242a-129">*ppEffectInstances* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9242a-129">*ppEffectInstances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9242a-130">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9242a-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9242a-131">包含效果實例陣列的緩衝區指標，傳回網格中每個屬性群組一個。</span><span class="sxs-lookup"><span data-stu-id="9242a-131">Pointer to a buffer containing an array of effect instances, one per attribute group in the returned mesh.</span></span> <span data-ttu-id="9242a-132">效果實例是用來初始化效果之狀態資訊的特定實例。</span><span class="sxs-lookup"><span data-stu-id="9242a-132">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="9242a-133">請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。</span><span class="sxs-lookup"><span data-stu-id="9242a-133">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span> <span data-ttu-id="9242a-134">如需有關存取緩衝區的詳細資訊，請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="9242a-134">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="9242a-135">*pNumMaterials* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9242a-135">*pNumMaterials* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9242a-136">類型： **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9242a-136">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9242a-137">當方法傳回時，為 *ppMaterials* 陣列中 [**D3DXMATERIAL**](d3dxmaterial.md)結構數目的指標。</span><span class="sxs-lookup"><span data-stu-id="9242a-137">Pointer to the number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *ppMaterials* array, when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="9242a-138">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9242a-138">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9242a-139">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="9242a-139">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="9242a-140">[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示已載入的網格。</span><span class="sxs-lookup"><span data-stu-id="9242a-140">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the loaded mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9242a-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="9242a-141">Return value</span></span>

<span data-ttu-id="9242a-142">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9242a-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9242a-143">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="9242a-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9242a-144">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="9242a-144">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9242a-145">備註</span><span class="sxs-lookup"><span data-stu-id="9242a-145">Remarks</span></span>

<span data-ttu-id="9242a-146">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="9242a-146">The compiler setting also determines the function version.</span></span> <span data-ttu-id="9242a-147">如果已定義 Unicode，函式呼叫會解析為 D3DXLoadMeshFromXW。</span><span class="sxs-lookup"><span data-stu-id="9242a-147">If Unicode is defined, the function call resolves to D3DXLoadMeshFromXW.</span></span> <span data-ttu-id="9242a-148">否則，函式呼叫會解析為 D3DXLoadMeshFromXA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="9242a-148">Otherwise, the function call resolves to D3DXLoadMeshFromXA because ANSI strings are being used.</span></span>

<span data-ttu-id="9242a-149">檔案中的所有網格都將折迭成一個輸出網格。</span><span class="sxs-lookup"><span data-stu-id="9242a-149">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="9242a-150">如果檔案包含框架階層，則所有轉換都會套用至網格。</span><span class="sxs-lookup"><span data-stu-id="9242a-150">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

<span data-ttu-id="9242a-151">對於不包含效果實例資訊的網格檔，將會從. x 檔案中的材質資訊產生預設效果實例。</span><span class="sxs-lookup"><span data-stu-id="9242a-151">For mesh files that do not contain effect instance information, default effect instances will be generated from the material information in the .x file.</span></span> <span data-ttu-id="9242a-152">預設效果實例會有預設值，這些值會對應至 [**D3DMATERIAL9**](d3dmaterial9.md) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="9242a-152">A default effect instance will have default values that correspond to the members of the [**D3DMATERIAL9**](d3dmaterial9.md) structure.</span></span>

<span data-ttu-id="9242a-153">預設紋理名稱也會填入，但會以不同的方式處理。</span><span class="sxs-lookup"><span data-stu-id="9242a-153">The default texture name is also filled in, but is handled differently.</span></span> <span data-ttu-id="9242a-154">名稱會是 Texture0@Name ，它會以名稱為 "Texture0" 的 "" 名稱對應至效果變數，並具有稱為 "name" 的注釋。</span><span class="sxs-lookup"><span data-stu-id="9242a-154">The name will be Texture0@Name, which corresponds to an effect variable by the name of "Texture0" with an annotation called "Name."</span></span> <span data-ttu-id="9242a-155">這會包含材質的字串檔案名。</span><span class="sxs-lookup"><span data-stu-id="9242a-155">This will contain the string file name for the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="9242a-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="9242a-156">Requirements</span></span>



| <span data-ttu-id="9242a-157">需求</span><span class="sxs-lookup"><span data-stu-id="9242a-157">Requirement</span></span> | <span data-ttu-id="9242a-158">值</span><span class="sxs-lookup"><span data-stu-id="9242a-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9242a-159">標頭</span><span class="sxs-lookup"><span data-stu-id="9242a-159">Header</span></span><br/>  | <dl> <span data-ttu-id="9242a-160"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="9242a-160"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9242a-161">程式庫</span><span class="sxs-lookup"><span data-stu-id="9242a-161">Library</span></span><br/> | <dl> <span data-ttu-id="9242a-162"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9242a-162"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9242a-163">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9242a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9242a-164">網格函數</span><span class="sxs-lookup"><span data-stu-id="9242a-164">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="9242a-165">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9242a-165">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="9242a-166">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="9242a-166">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
