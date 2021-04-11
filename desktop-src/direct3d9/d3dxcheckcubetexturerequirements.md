---
description: 檢查 cube 材質建立參數。
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: 'D3DXCheckCubeTextureRequirements 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696844"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a><span data-ttu-id="dad89-103">D3DXCheckCubeTextureRequirements 函式</span><span class="sxs-lookup"><span data-stu-id="dad89-103">D3DXCheckCubeTextureRequirements function</span></span>

<span data-ttu-id="dad89-104">檢查 cube 材質建立參數。</span><span class="sxs-lookup"><span data-stu-id="dad89-104">Checks cube-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="dad89-105">語法</span><span class="sxs-lookup"><span data-stu-id="dad89-105">Syntax</span></span>


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="dad89-106">參數</span><span class="sxs-lookup"><span data-stu-id="dad89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dad89-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dad89-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad89-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="dad89-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="dad89-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與 cube 材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="dad89-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="dad89-110">*pSize* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="dad89-110">*pSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dad89-111">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dad89-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dad89-112">要求的寬度和高度（以圖元為單位）的指標，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="dad89-112">Pointer to the requested width and height in pixels, or **NULL**.</span></span> <span data-ttu-id="dad89-113">傳回已更正的大小。</span><span class="sxs-lookup"><span data-stu-id="dad89-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="dad89-114">*pNumMipLevels* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="dad89-114">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dad89-115">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="dad89-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dad89-116">要求的 mipmap 層級數目的指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="dad89-116">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="dad89-117">傳回已更正的 mipmap 層級數目。</span><span class="sxs-lookup"><span data-stu-id="dad89-117">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="dad89-118">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="dad89-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad89-119">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dad89-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dad89-120">0或 D3DUSAGE \_ RENDERTARGET。</span><span class="sxs-lookup"><span data-stu-id="dad89-120">0 or D3DUSAGE\_RENDERTARGET.</span></span> <span data-ttu-id="dad89-121">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="dad89-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="dad89-122">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api) 方法的 pNewRenderTarget 參數。</span><span class="sxs-lookup"><span data-stu-id="dad89-122">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="dad89-123">如果指定了 D3DUSAGE \_ RENDERTARGET，應用程式應該藉由呼叫 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="dad89-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="dad89-124">*pformatetc 架構* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="dad89-124">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dad89-125">類型： **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="dad89-125">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="dad89-126">[D3DFORMAT](d3dformat.md)列舉型別的成員指標。</span><span class="sxs-lookup"><span data-stu-id="dad89-126">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="dad89-127">指定所需的像素格式，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="dad89-127">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="dad89-128">傳回更正的格式。</span><span class="sxs-lookup"><span data-stu-id="dad89-128">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="dad89-129">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="dad89-129">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad89-130">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="dad89-130">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="dad89-131">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="dad89-131">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dad89-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="dad89-132">Return value</span></span>

<span data-ttu-id="dad89-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dad89-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dad89-134">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="dad89-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dad89-135">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ NOTAVAILABLE，D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="dad89-135">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="dad89-136">備註</span><span class="sxs-lookup"><span data-stu-id="dad89-136">Remarks</span></span>

<span data-ttu-id="dad89-137">如果此函式的參數無效，此函式會傳回已更正的參數。</span><span class="sxs-lookup"><span data-stu-id="dad89-137">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="dad89-138">Cube 紋理不同于其他表面，因為它們是表面的集合。</span><span class="sxs-lookup"><span data-stu-id="dad89-138">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="dad89-139">若要使用 cube 材質來呼叫 [**SetRenderTarget**](/windows/desktop/api) ，您必須使用 [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) 選取個別臉部，並將產生的介面傳遞至 **SetRenderTarget**。</span><span class="sxs-lookup"><span data-stu-id="dad89-139">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad89-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="dad89-140">Requirements</span></span>



| <span data-ttu-id="dad89-141">需求</span><span class="sxs-lookup"><span data-stu-id="dad89-141">Requirement</span></span> | <span data-ttu-id="dad89-142">值</span><span class="sxs-lookup"><span data-stu-id="dad89-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dad89-143">標頭</span><span class="sxs-lookup"><span data-stu-id="dad89-143">Header</span></span><br/>  | <dl> <span data-ttu-id="dad89-144"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="dad89-144"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="dad89-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="dad89-145">Library</span></span><br/> | <dl> <span data-ttu-id="dad89-146"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dad89-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dad89-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dad89-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad89-148">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="dad89-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
