---
description: 傳回包含自調適型空間取樣所產生之修改的網格。 傳回的網格僅包含位置、法線和材質座標 (如果定義) 。
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: 'ID3DXPRTEngine：： GetAdaptedMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3d012344a5dfbc1bc17780cb4ab9a53820fe34f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323255"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a><span data-ttu-id="bced8-104">ID3DXPRTEngine：： GetAdaptedMesh 方法</span><span class="sxs-lookup"><span data-stu-id="bced8-104">ID3DXPRTEngine::GetAdaptedMesh method</span></span>

<span data-ttu-id="bced8-105">傳回包含自調適型空間取樣所產生之修改的網格。</span><span class="sxs-lookup"><span data-stu-id="bced8-105">Returns a mesh with modifications resulting from adaptive spatial sampling.</span></span> <span data-ttu-id="bced8-106">傳回的網格僅包含位置、法線和材質座標 (如果定義) 。</span><span class="sxs-lookup"><span data-stu-id="bced8-106">The returned mesh contains only positions, normals, and texture coordinates (if defined).</span></span>

## <a name="syntax"></a><span data-ttu-id="bced8-107">語法</span><span class="sxs-lookup"><span data-stu-id="bced8-107">Syntax</span></span>


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="bced8-108">參數</span><span class="sxs-lookup"><span data-stu-id="bced8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bced8-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bced8-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bced8-110">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="bced8-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="bced8-111">用來建立輸出網格之 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 裝置的指標。</span><span class="sxs-lookup"><span data-stu-id="bced8-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="bced8-112">*pFaceRemap* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bced8-112">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bced8-113">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bced8-113">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bced8-114">已分割以產生目前臉部的原始網狀臉部指標。</span><span class="sxs-lookup"><span data-stu-id="bced8-114">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> <dt>

<span data-ttu-id="bced8-115">*pVertRemap* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bced8-115">*pVertRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bced8-116">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bced8-116">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bced8-117">目的地陣列的指標，其中包含做為目前頂點父系的三個原始網格頂點。</span><span class="sxs-lookup"><span data-stu-id="bced8-117">Pointer to a destination array containing the three original mesh vertices that are the parents of the current vertex.</span></span>

</dd> <dt>

<span data-ttu-id="bced8-118">*pfVertWeights* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="bced8-118">*pfVertWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bced8-119">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="bced8-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="bced8-120">目的地陣列的指標，其中包含 pVertRemap 頂點的混合因數。</span><span class="sxs-lookup"><span data-stu-id="bced8-120">Pointer to a destination array containing blending factors for the pVertRemap vertices.</span></span>

</dd> <dt>

<span data-ttu-id="bced8-121">*ppMesh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bced8-121">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bced8-122">類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="bced8-122">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="bced8-123">輸出 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標。</span><span class="sxs-lookup"><span data-stu-id="bced8-123">Pointer to the output [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bced8-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="bced8-124">Return value</span></span>

<span data-ttu-id="bced8-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bced8-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bced8-126">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="bced8-126">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="bced8-127">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="bced8-127">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="bced8-128">備註</span><span class="sxs-lookup"><span data-stu-id="bced8-128">Remarks</span></span>

<span data-ttu-id="bced8-129">pVertRemap 和 pfVertWeights 可以用來將任何每個頂點的值插到網格上。</span><span class="sxs-lookup"><span data-stu-id="bced8-129">pVertRemap and pfVertWeights can be used to interpolate any per-vertex value over the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="bced8-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="bced8-130">Requirements</span></span>



| <span data-ttu-id="bced8-131">需求</span><span class="sxs-lookup"><span data-stu-id="bced8-131">Requirement</span></span> | <span data-ttu-id="bced8-132">值</span><span class="sxs-lookup"><span data-stu-id="bced8-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bced8-133">標頭</span><span class="sxs-lookup"><span data-stu-id="bced8-133">Header</span></span><br/>  | <dl> <span data-ttu-id="bced8-134"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="bced8-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bced8-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="bced8-135">Library</span></span><br/> | <dl> <span data-ttu-id="bced8-136"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bced8-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bced8-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bced8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bced8-138">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="bced8-138">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
