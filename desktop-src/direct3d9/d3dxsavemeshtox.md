---
description: 將網格儲存至 x 檔案。
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: 'D3DXSaveMeshToX 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976703"
---
# <a name="d3dxsavemeshtox-function"></a><span data-ttu-id="f1aad-103">D3DXSaveMeshToX 函式</span><span class="sxs-lookup"><span data-stu-id="f1aad-103">D3DXSaveMeshToX function</span></span>

<span data-ttu-id="f1aad-104">將網格儲存至 x 檔案。</span><span class="sxs-lookup"><span data-stu-id="f1aad-104">Saves a mesh to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1aad-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1aad-105">Syntax</span></span>


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a><span data-ttu-id="f1aad-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1aad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1aad-107">*pFilename* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1aad-107">*pFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1aad-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1aad-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1aad-109">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="f1aad-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="f1aad-110">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="f1aad-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f1aad-111">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="f1aad-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="f1aad-112">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="f1aad-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f1aad-113">*pMesh* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1aad-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1aad-114">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f1aad-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="f1aad-115">[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表要儲存至 x.x 檔案的網格。</span><span class="sxs-lookup"><span data-stu-id="f1aad-115">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to save to a .x file.</span></span>

</dd> <dt>

<span data-ttu-id="f1aad-116">*pAdjacency* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1aad-116">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1aad-117">類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f1aad-117">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f1aad-118">指標，指向每個臉部的三個 Dword 陣列，為網格中的每個臉部指定三個相鄰專案。</span><span class="sxs-lookup"><span data-stu-id="f1aad-118">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="f1aad-119">這個參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f1aad-119">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f1aad-120">*pMaterials* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1aad-120">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1aad-121">Type： **Const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="f1aad-121">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="f1aad-122">[**D3DXMATERIAL**](d3dxmaterial.md)結構陣列的指標，其中包含要儲存在. x 檔案中的材質資訊。</span><span class="sxs-lookup"><span data-stu-id="f1aad-122">Pointer to an array of [**D3DXMATERIAL**](d3dxmaterial.md) structures, containing material information to be saved in the .x file.</span></span>

</dd> <dt>

<span data-ttu-id="f1aad-123">*pEffectInstances* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1aad-123">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1aad-124">Type： **Const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="f1aad-124">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="f1aad-125">效果實例陣列的指標，網格中的每個屬性群組都有一個。</span><span class="sxs-lookup"><span data-stu-id="f1aad-125">Pointer to an array of effect instances, one per attribute group in the mesh.</span></span> <span data-ttu-id="f1aad-126">這個參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f1aad-126">This parameter may be **NULL**.</span></span> <span data-ttu-id="f1aad-127">效果實例是用來初始化效果之狀態資訊的特定實例。</span><span class="sxs-lookup"><span data-stu-id="f1aad-127">An effect instance is a particular instance of state information used to initialize an effect.</span></span> <span data-ttu-id="f1aad-128">如需詳細資訊，請參閱 [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)。</span><span class="sxs-lookup"><span data-stu-id="f1aad-128">For more information, see [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1aad-129">*NumMaterials* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1aad-129">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1aad-130">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1aad-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1aad-131">*PMaterials* 陣列中的 [**D3DXMATERIAL**](d3dxmaterial.md)結構數目。</span><span class="sxs-lookup"><span data-stu-id="f1aad-131">Number of [**D3DXMATERIAL**](d3dxmaterial.md) structures in the *pMaterials* array.</span></span>

</dd> <dt>

<span data-ttu-id="f1aad-132">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1aad-132">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1aad-133">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1aad-133">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1aad-134">儲存. x 檔案時，檔案格式和儲存選項的組合。</span><span class="sxs-lookup"><span data-stu-id="f1aad-134">A combination of file format and save options when saving an .x file.</span></span> <span data-ttu-id="f1aad-135">請參閱 [D3DX X 檔案常數](dx9-graphics-reference-d3dx-x-file-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="f1aad-135">See [D3DX X File Constants](dx9-graphics-reference-d3dx-x-file-constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1aad-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1aad-136">Return value</span></span>

<span data-ttu-id="f1aad-137">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1aad-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1aad-138">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f1aad-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f1aad-139">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="f1aad-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1aad-140">備註</span><span class="sxs-lookup"><span data-stu-id="f1aad-140">Remarks</span></span>

<span data-ttu-id="f1aad-141">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="f1aad-141">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f1aad-142">如果已定義 Unicode，函式呼叫會解析為 D3DXSaveMeshToXW。</span><span class="sxs-lookup"><span data-stu-id="f1aad-142">If Unicode is defined, the function call resolves to D3DXSaveMeshToXW.</span></span> <span data-ttu-id="f1aad-143">否則，函式呼叫會解析為 D3DXSaveMeshToXA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="f1aad-143">Otherwise, the function call resolves to D3DXSaveMeshToXA because ANSI strings are being used.</span></span>

<span data-ttu-id="f1aad-144">預設檔案格式為 binary;但是，如果同時將檔案指定為二進位檔和文字檔，則會將它儲存為文字檔。</span><span class="sxs-lookup"><span data-stu-id="f1aad-144">The default file format is binary; however, if a file is specified as both a binary and a text file, it will be saved as a text file.</span></span> <span data-ttu-id="f1aad-145">無論檔案格式為何，您也可以使用壓縮格式來減少檔案大小。</span><span class="sxs-lookup"><span data-stu-id="f1aad-145">Regardless of the file format, you may also use the compressed format to reduce the file size.</span></span>

<span data-ttu-id="f1aad-146">以下是如何使用此函數的一般程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="f1aad-146">The following is a typical code example of how to use this function.</span></span>


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



## <a name="requirements"></a><span data-ttu-id="f1aad-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1aad-147">Requirements</span></span>



| <span data-ttu-id="f1aad-148">需求</span><span class="sxs-lookup"><span data-stu-id="f1aad-148">Requirement</span></span> | <span data-ttu-id="f1aad-149">值</span><span class="sxs-lookup"><span data-stu-id="f1aad-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1aad-150">標頭</span><span class="sxs-lookup"><span data-stu-id="f1aad-150">Header</span></span><br/>  | <dl> <span data-ttu-id="f1aad-151"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1aad-151"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f1aad-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="f1aad-152">Library</span></span><br/> | <dl> <span data-ttu-id="f1aad-153"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1aad-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f1aad-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1aad-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1aad-155">網格函數</span><span class="sxs-lookup"><span data-stu-id="f1aad-155">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="f1aad-156">**D3DXEFFECTDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f1aad-156">**D3DXEFFECTDEFAULT**</span></span>](d3dxeffectdefault.md)
</dt> <dt>

[<span data-ttu-id="f1aad-157">**D3DXEFFECTINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="f1aad-157">**D3DXEFFECTINSTANCE**</span></span>](d3dxeffectinstance.md)
</dt> </dl>

 

 
