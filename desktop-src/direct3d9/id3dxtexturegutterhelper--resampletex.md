---
description: 將材質 Resamples 到這個 gutterhelper 的參數化。
ms.assetid: a5ace0e4-2e89-471b-bdfb-67d5e85c6f46
title: 'ID3DXTextureGutterHelper：： ResampleTex 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ResampleTex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0ad8b4cefe0b368cbf81de4ddc030f32cda8fb17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196376"
---
# <a name="id3dxtexturegutterhelperresampletex-method"></a><span data-ttu-id="81f22-103">ID3DXTextureGutterHelper：： ResampleTex 方法</span><span class="sxs-lookup"><span data-stu-id="81f22-103">ID3DXTextureGutterHelper::ResampleTex method</span></span>

<span data-ttu-id="81f22-104">將材質 Resamples 到這個 gutterhelper 的參數化。</span><span class="sxs-lookup"><span data-stu-id="81f22-104">Resamples a texture into this gutterhelper's parameterization.</span></span>

## <a name="syntax"></a><span data-ttu-id="81f22-105">語法</span><span class="sxs-lookup"><span data-stu-id="81f22-105">Syntax</span></span>


```C++
HRESULT ResampleTex(
  [in]  LPDIRECT3DTEXTURE9 pTextureIn,
  [in]  LPD3DXMESH         pMeshIn,
  [in]  D3DDECLUSAGE       Usage,
  [in]  UINT               UsageIndex,
  [out] LPDIRECT3DTEXTURE9 pTextureOut
);
```



## <a name="parameters"></a><span data-ttu-id="81f22-106">參數</span><span class="sxs-lookup"><span data-stu-id="81f22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81f22-107">*pTextureIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81f22-107">*pTextureIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f22-108">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="81f22-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="81f22-109">對應至 pMeshIn 中原始參數化的材質。</span><span class="sxs-lookup"><span data-stu-id="81f22-109">Texture that corresponds to the original parameterization in pMeshIn.</span></span> <span data-ttu-id="81f22-110">此材質將用來建立 pTextureOut。</span><span class="sxs-lookup"><span data-stu-id="81f22-110">This texture will be used to create pTextureOut.</span></span>

</dd> <dt>

<span data-ttu-id="81f22-111">*pMeshIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81f22-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f22-112">類型： **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="81f22-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="81f22-113">包含原始和新參數化的網格。</span><span class="sxs-lookup"><span data-stu-id="81f22-113">Mesh containing the original and new parameterizations.</span></span> <span data-ttu-id="81f22-114">您必須在 D3DDECLUSAGE TEXCOORD index 0 中儲存新的參數化 \_ 。</span><span class="sxs-lookup"><span data-stu-id="81f22-114">It is required to store the new parameterization in D3DDECLUSAGE\_TEXCOORD index 0.</span></span>

</dd> <dt>

<span data-ttu-id="81f22-115">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="81f22-115">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f22-116">類型： **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**</span><span class="sxs-lookup"><span data-stu-id="81f22-116">Type: **[**D3DDECLUSAGE**](./d3ddeclusage.md)**</span></span>

<span data-ttu-id="81f22-117">頂點資料使用量 (與 UsageIndex) 搭配使用，這會識別包含 pMeshIn 中原始參數化之頂點宣告的元件。</span><span class="sxs-lookup"><span data-stu-id="81f22-117">Vertex data usage (used in combination with UsageIndex) which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="81f22-118">請參閱 [**D3DDECLUSAGE**](./d3ddeclusage.md)。</span><span class="sxs-lookup"><span data-stu-id="81f22-118">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="81f22-119">*UsageIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="81f22-119">*UsageIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81f22-120">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="81f22-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="81f22-121">以零為基底的索引 (搭配使用) 使用，這會識別包含 pMeshIn 中原始參數化之頂點宣告的元件。</span><span class="sxs-lookup"><span data-stu-id="81f22-121">Zero-based index (used in combination with Usage), which identifies the component of the vertex declaration that contains the original parameterization in pMeshIn.</span></span> <span data-ttu-id="81f22-122">\_新參數化需要 D3DDECLUSAGE TEXCOORD 和 index 0 的組合; 您可以使用任何其他使用方式/索引組合。</span><span class="sxs-lookup"><span data-stu-id="81f22-122">The combination of D3DDECLUSAGE\_TEXCOORD and index 0 is required for the new parameterization; any other usage/index combination may be used.</span></span>

</dd> <dt>

<span data-ttu-id="81f22-123">*pTextureOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="81f22-123">*pTextureOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81f22-124">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="81f22-124">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="81f22-125">重新取樣的材質。</span><span class="sxs-lookup"><span data-stu-id="81f22-125">Resampled texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81f22-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="81f22-126">Return value</span></span>

<span data-ttu-id="81f22-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="81f22-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="81f22-128">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="81f22-128">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="81f22-129">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="81f22-129">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="81f22-130">備註</span><span class="sxs-lookup"><span data-stu-id="81f22-130">Remarks</span></span>

<span data-ttu-id="81f22-131">在此函式的情況下，參數化是一組材質座標，可將網格的三角形對應至材質上的三角形。</span><span class="sxs-lookup"><span data-stu-id="81f22-131">A parameterization in the case of this function is a set of texture coordinates that maps the triangles of a mesh to the triangles on a texture.</span></span> <span data-ttu-id="81f22-132">新的參數化是一組包含在裝訂邊協助程式介面中的材質座標，而原始參數化則是包含在輸入網格內的材質座標集合。</span><span class="sxs-lookup"><span data-stu-id="81f22-132">The new parameterization is the set of texture coordinates contained in the gutter helper interface, and the original parameterization is the set of texture coordinates contained within the input mesh.</span></span>

<span data-ttu-id="81f22-133">假設材質座標介於0和1（含）之間，而且新的參數化必須在頂點宣告中宣告為紋理座標索引0。</span><span class="sxs-lookup"><span data-stu-id="81f22-133">It is assumed that texture coordinates are between 0 and 1, inclusive, and the new parameterization must be declared in the vertex declaration as texture coordinate index 0.</span></span> <span data-ttu-id="81f22-134">原始材質和重新取樣的材質必須具有相同的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="81f22-134">The original texture and the resampled texture must have the same width and height.</span></span>

<span data-ttu-id="81f22-135">例如，為了準備將材質重新取樣：</span><span class="sxs-lookup"><span data-stu-id="81f22-135">For example, to prepare for resampling a texture:</span></span>

-   <span data-ttu-id="81f22-136">使用 [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)之類的函式，建立下面)  (pOriginalTex 的原始紋理介面。</span><span class="sxs-lookup"><span data-stu-id="81f22-136">Create the original texture interface (pOriginalTex below) using a function like [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>
-   <span data-ttu-id="81f22-137">為重新取樣的材質建立新的材質介面 (pResampledTex 以下) 。</span><span class="sxs-lookup"><span data-stu-id="81f22-137">Create the new texture interface for the resampled texture (pResampledTex below).</span></span> <span data-ttu-id="81f22-138">此材質的大小必須符合裝訂邊協助程式材質 (寬度和高度) 的大小。</span><span class="sxs-lookup"><span data-stu-id="81f22-138">The size of this texture must match the size (width and height) of the gutter helper texture.</span></span>
-   <span data-ttu-id="81f22-139">呼叫 [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) 以取得新的參數化，如下所示：</span><span class="sxs-lookup"><span data-stu-id="81f22-139">Call [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) to obtain the new parameterization as shown here:</span></span>


```
// Given:
// pMesh points to a mesh that contains the original and new texture coordinates
ID3DXTextureGutterHelper * pGutterHelper;
    
// Mesh vertex declaration
D3DVERTEXELEMENT9 decl[] = {
    {0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0},
    // contains new set of texcoords
    {0, 24, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0}, 
    // contains original set of texcoords
    {0, 32, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1}, 
    D3DDECL_END()
};
    
// Create a gutter helper with the new parameterization
hr = D3DXCreateTextureGutterHelper(width, height, pMesh, 1, &pGutterHelper);  
    
// Resample the texture
hr = pGutterHelper->ResampleTex(pOriginalTex, pMesh, D3DDECLUSAGE_TEXCOORD, 
           1, pResampledTex); 
    
// Release the gutter helper interface when done with it
```



<span data-ttu-id="81f22-140">其中一個常見的案例可能是使用 UVAtlas 來建立材質塔，然後使用 ResampleTex 將材質重新取樣至新的參數化。</span><span class="sxs-lookup"><span data-stu-id="81f22-140">One common scenario might be to use UVAtlas to create a texture atlas and then use ResampleTex to resample the texture into the new parameterization.</span></span> <span data-ttu-id="81f22-141">如需圖集的詳細資訊，請參閱 [使用 UVAtlas (Direct3D 9) ](using-uvatlas.md)。</span><span class="sxs-lookup"><span data-stu-id="81f22-141">For more information about atlases, see [Using UVAtlas (Direct3D 9)](using-uvatlas.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="81f22-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="81f22-142">Requirements</span></span>



| <span data-ttu-id="81f22-143">需求</span><span class="sxs-lookup"><span data-stu-id="81f22-143">Requirement</span></span> | <span data-ttu-id="81f22-144">值</span><span class="sxs-lookup"><span data-stu-id="81f22-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81f22-145">標頭</span><span class="sxs-lookup"><span data-stu-id="81f22-145">Header</span></span><br/>  | <dl> <span data-ttu-id="81f22-146"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="81f22-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="81f22-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="81f22-147">Library</span></span><br/> | <dl> <span data-ttu-id="81f22-148"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="81f22-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="81f22-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81f22-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81f22-150">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="81f22-150">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> <dt>

[<span data-ttu-id="81f22-151">**D3DXUVAtlasCreate**</span><span class="sxs-lookup"><span data-stu-id="81f22-151">**D3DXUVAtlasCreate**</span></span>](d3dxuvatlascreate.md)
</dt> </dl>

 

 
