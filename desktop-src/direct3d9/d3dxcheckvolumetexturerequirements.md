---
description: 檢查磁片區材質建立參數。
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: 'D3DXCheckVolumeTextureRequirements 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4940cab936ed14c847e7224c9f619244c6e422a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386471"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a><span data-ttu-id="38e36-103">D3DXCheckVolumeTextureRequirements 函式</span><span class="sxs-lookup"><span data-stu-id="38e36-103">D3DXCheckVolumeTextureRequirements function</span></span>

<span data-ttu-id="38e36-104">檢查磁片區材質建立參數。</span><span class="sxs-lookup"><span data-stu-id="38e36-104">Checks volume-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e36-105">語法</span><span class="sxs-lookup"><span data-stu-id="38e36-105">Syntax</span></span>


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="38e36-106">參數</span><span class="sxs-lookup"><span data-stu-id="38e36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38e36-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38e36-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e36-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="38e36-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="38e36-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與磁片區材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="38e36-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="38e36-110">*pWidth* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="38e36-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38e36-111">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38e36-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38e36-112">要求的寬度（以圖元為單位）的指標，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="38e36-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="38e36-113">傳回已更正的大小。</span><span class="sxs-lookup"><span data-stu-id="38e36-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="38e36-114">*pHeight* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="38e36-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38e36-115">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38e36-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38e36-116">要求高度（以圖元為單位）的指標，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="38e36-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="38e36-117">傳回已更正的大小。</span><span class="sxs-lookup"><span data-stu-id="38e36-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="38e36-118">*pDepth* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="38e36-118">*pDepth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38e36-119">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38e36-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38e36-120">要求的深度（以圖元為單位）的指標，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="38e36-120">Pointer to the requested depth in pixels, or **NULL**.</span></span> <span data-ttu-id="38e36-121">傳回已更正的大小。</span><span class="sxs-lookup"><span data-stu-id="38e36-121">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="38e36-122">*pNumMipLevels* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="38e36-122">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38e36-123">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="38e36-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="38e36-124">要求的 mipmap 層級數目的指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="38e36-124">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="38e36-125">傳回已更正的 mipmap 層級數目。</span><span class="sxs-lookup"><span data-stu-id="38e36-125">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="38e36-126">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="38e36-126">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e36-127">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38e36-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38e36-128">目前未使用，設定為0。</span><span class="sxs-lookup"><span data-stu-id="38e36-128">Currently not used, set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="38e36-129">*pformatetc 架構* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="38e36-129">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="38e36-130">類型： **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="38e36-130">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="38e36-131">[D3DFORMAT](d3dformat.md)列舉型別的成員指標。</span><span class="sxs-lookup"><span data-stu-id="38e36-131">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="38e36-132">指定所需的像素格式，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="38e36-132">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="38e36-133">傳回更正的格式。</span><span class="sxs-lookup"><span data-stu-id="38e36-133">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="38e36-134">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="38e36-134">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38e36-135">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="38e36-135">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="38e36-136">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置磁片區材質的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="38e36-136">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38e36-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="38e36-137">Return value</span></span>

<span data-ttu-id="38e36-138">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38e36-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38e36-139">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="38e36-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38e36-140">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE，D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="38e36-140">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="38e36-141">備註</span><span class="sxs-lookup"><span data-stu-id="38e36-141">Remarks</span></span>

<span data-ttu-id="38e36-142">如果此函式的參數無效，此函式會傳回已更正的參數。</span><span class="sxs-lookup"><span data-stu-id="38e36-142">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="38e36-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="38e36-143">Requirements</span></span>



| <span data-ttu-id="38e36-144">需求</span><span class="sxs-lookup"><span data-stu-id="38e36-144">Requirement</span></span> | <span data-ttu-id="38e36-145">值</span><span class="sxs-lookup"><span data-stu-id="38e36-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38e36-146">標頭</span><span class="sxs-lookup"><span data-stu-id="38e36-146">Header</span></span><br/>  | <dl> <span data-ttu-id="38e36-147"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="38e36-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="38e36-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="38e36-148">Library</span></span><br/> | <dl> <span data-ttu-id="38e36-149"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="38e36-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="38e36-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38e36-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38e36-151">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="38e36-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
