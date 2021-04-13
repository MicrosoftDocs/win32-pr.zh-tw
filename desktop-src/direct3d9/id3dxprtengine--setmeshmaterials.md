---
description: 設定3D 場景中的網格材質屬性。 使用這個方法來指定地下散佈參數。
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'ID3DXPRTEngine：： SetMeshMaterials 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323251"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a><span data-ttu-id="b7318-104">ID3DXPRTEngine：： SetMeshMaterials 方法</span><span class="sxs-lookup"><span data-stu-id="b7318-104">ID3DXPRTEngine::SetMeshMaterials method</span></span>

<span data-ttu-id="b7318-105">設定3D 場景中的網格材質屬性。</span><span class="sxs-lookup"><span data-stu-id="b7318-105">Sets mesh material properties in the 3D scene.</span></span> <span data-ttu-id="b7318-106">使用這個方法來指定地下散佈參數。</span><span class="sxs-lookup"><span data-stu-id="b7318-106">Use this method to specify subsurface scattering parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7318-107">語法</span><span class="sxs-lookup"><span data-stu-id="b7318-107">Syntax</span></span>


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a><span data-ttu-id="b7318-108">參數</span><span class="sxs-lookup"><span data-stu-id="b7318-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7318-109">*ppMaterials* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7318-109">*ppMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7318-110">Type： **Const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***</span><span class="sxs-lookup"><span data-stu-id="b7318-110">Type: **const [**D3DXSHMATERIAL**](d3dxshmaterial.md)\*\***</span></span>

<span data-ttu-id="b7318-111">所需之網格材質屬性指標的位址。</span><span class="sxs-lookup"><span data-stu-id="b7318-111">Address of a pointer to desired mesh material properties.</span></span> <span data-ttu-id="b7318-112">請參閱 [**D3DXSHMATERIAL**](d3dxshmaterial.md)。</span><span class="sxs-lookup"><span data-stu-id="b7318-112">See [**D3DXSHMATERIAL**](d3dxshmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7318-113">*NumMeshes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7318-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7318-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7318-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7318-115">要在其上設定材質屬性之網格的索引。</span><span class="sxs-lookup"><span data-stu-id="b7318-115">Index of the mesh on which to set material properties.</span></span>

</dd> <dt>

<span data-ttu-id="b7318-116">*NumChannels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7318-116">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7318-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7318-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7318-118">要在網格中設定的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="b7318-118">Number of color channels to set in the mesh.</span></span> <span data-ttu-id="b7318-119">設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。</span><span class="sxs-lookup"><span data-stu-id="b7318-119">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span> <span data-ttu-id="b7318-120">如果您想要變更此參數，請先使用另一種方法來設定 >albedo，例如 [**ID3DXPRTEngine：： SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) 或 [**ID3DXPRTEngine：： SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md)。</span><span class="sxs-lookup"><span data-stu-id="b7318-120">If you intend to change this parameter, first set the albedo using another method such as [**ID3DXPRTEngine::SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) or [**ID3DXPRTEngine::SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7318-121">*bSetAlbedo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7318-121">*bSetAlbedo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7318-122">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7318-122">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7318-123">若 **為 TRUE**，則會將網格的 >albedo 設定為 ppMaterials，並覆寫所有現有的材質和頂點 >albedo 值。</span><span class="sxs-lookup"><span data-stu-id="b7318-123">If **TRUE**, sets the albedo of the mesh to ppMaterials, overwriting all existing texel and vertex albedo values.</span></span> <span data-ttu-id="b7318-124">如果 **為 FALSE**，則會保留其他方法所設定的所有現有材質和頂點 >albedo 值;NumChannels 必須符合用來在 [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) 或 [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)中建立緩衝區的 NumChannels 參數。</span><span class="sxs-lookup"><span data-stu-id="b7318-124">If **FALSE**, preserves all existing texel and vertex albedo values set by other methods; NumChannels must match the NumChannels parameter used to create the buffer in [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) or [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7318-125">*fLengthScale* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7318-125">*fLengthScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7318-126">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7318-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7318-127">相對於 1 mm cube 的3D 場景規模。</span><span class="sxs-lookup"><span data-stu-id="b7318-127">Scale of the 3D scene relative to a 1-mm cube.</span></span> <span data-ttu-id="b7318-128">用於地下散佈計算。</span><span class="sxs-lookup"><span data-stu-id="b7318-128">Used for subsurface scattering computations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7318-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7318-129">Return value</span></span>

<span data-ttu-id="b7318-130">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7318-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7318-131">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b7318-131">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b7318-132">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="b7318-132">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7318-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7318-133">Requirements</span></span>



| <span data-ttu-id="b7318-134">需求</span><span class="sxs-lookup"><span data-stu-id="b7318-134">Requirement</span></span> | <span data-ttu-id="b7318-135">值</span><span class="sxs-lookup"><span data-stu-id="b7318-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7318-136">標頭</span><span class="sxs-lookup"><span data-stu-id="b7318-136">Header</span></span><br/>  | <dl> <span data-ttu-id="b7318-137"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7318-137"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b7318-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="b7318-138">Library</span></span><br/> | <dl> <span data-ttu-id="b7318-139"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7318-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b7318-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7318-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7318-141">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="b7318-141">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
