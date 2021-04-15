---
description: 建立空白紋理，視需要調整呼叫參數。
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: 'D3DXCreateTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514604"
---
# <a name="d3dxcreatetexture-function"></a><span data-ttu-id="d5ac1-103">D3DXCreateTexture 函式</span><span class="sxs-lookup"><span data-stu-id="d5ac1-103">D3DXCreateTexture function</span></span>

<span data-ttu-id="d5ac1-104">建立空白紋理，視需要調整呼叫參數。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-104">Creates an empty texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ac1-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5ac1-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="d5ac1-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5ac1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ac1-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5ac1-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ac1-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d5ac1-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d5ac1-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="d5ac1-110">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5ac1-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ac1-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5ac1-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5ac1-112">寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-112">Width in pixels.</span></span> <span data-ttu-id="d5ac1-113">如果這個值為0，則會使用值1。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-113">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="d5ac1-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d5ac1-115">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5ac1-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ac1-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5ac1-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5ac1-117">高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-117">Height in pixels.</span></span> <span data-ttu-id="d5ac1-118">如果這個值為0，則會使用值1。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-118">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="d5ac1-119">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d5ac1-120">*MipLevels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5ac1-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ac1-121">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5ac1-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5ac1-122">要求的 mip 層級數目。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-122">Number of mip levels requested.</span></span> <span data-ttu-id="d5ac1-123">如果此值為零或 D3DX \_ 預設值，則會建立完整的 mipmap 鏈。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-123">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="d5ac1-124">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="d5ac1-124">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ac1-125">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5ac1-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5ac1-126">0、 [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)或 **D3DUSAGE \_ DYNAMIC**。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-126">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="d5ac1-127">將此旗標設定為 **D3DUSAGE \_ RENDERTARGET** ，表示介面會藉由呼叫 [**SetRenderTarget**](/windows/desktop/api) 方法當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-127">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target by calling the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="d5ac1-128">如果指定了 **D3DUSAGE \_ RENDERTARGET** 或 **D3DUSAGE \_ DYNAMIC** ，應用程式應該呼叫 [**CheckDeviceFormat**](/windows/desktop/api)來檢查裝置是否支援這項作業。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-128">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="d5ac1-129">如需使用動態紋理的詳細資訊，請參閱 [使用動態紋理](performance-optimizations.md)。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-129">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5ac1-130">*格式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5ac1-130">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ac1-131">類型： **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="d5ac1-131">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="d5ac1-132">[D3DFORMAT](d3dformat.md)列舉型別的成員，描述紋理所要求的像素格式。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-132">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="d5ac1-133">如果裝置不支援要求的格式，則傳回的材質可能會與指定的格式不同。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-133">The returned texture may be of a different format from that specified, if the device does not support the requested format.</span></span> <span data-ttu-id="d5ac1-134">應用程式應該檢查傳回材質的格式，以查看它是否符合要求的格式。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-134">Applications should check the format of the returned texture to see if it matches the format requested.</span></span>

</dd> <dt>

<span data-ttu-id="d5ac1-135">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="d5ac1-135">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ac1-136">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="d5ac1-136">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="d5ac1-137">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-137">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="d5ac1-138">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d5ac1-138">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ac1-139">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="d5ac1-139">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="d5ac1-140">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-140">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ac1-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5ac1-141">Return value</span></span>

<span data-ttu-id="d5ac1-142">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5ac1-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5ac1-143">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d5ac1-144">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ NOTAVAILABLE、D3DERR \_ OUTOFVIDEOMEMORY、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5ac1-145">備註</span><span class="sxs-lookup"><span data-stu-id="d5ac1-145">Remarks</span></span>

<span data-ttu-id="d5ac1-146">就內部而言，D3DXCreateTexture 會使用 [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) 來調整呼叫參數。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-146">Internally, D3DXCreateTexture uses [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="d5ac1-147">因此，呼叫 D3DXCreateTexture 通常會成功，因為對 [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) 的呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-147">Therefore, calls to D3DXCreateTexture will often succeed where calls to [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) would fail.</span></span>

<span data-ttu-id="d5ac1-148">如果高度和寬度都設定為 [D3DX \_ 預設](other-d3dx-constants.md)值，則兩個參數都使用256的值。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-148">If both Height and Width are set to [D3DX\_DEFAULT](other-d3dx-constants.md), a value of 256 is used for both parameters.</span></span> <span data-ttu-id="d5ac1-149">如果 [高度] 或 [寬度] 設定為 \_ [D3DX 預設值]，而另一個參數設定為數值，則紋理會是正方形，且高度和寬度都等於數位值。</span><span class="sxs-lookup"><span data-stu-id="d5ac1-149">If either Height or Width is set to D3DX\_DEFAULT And the other parameter is set to a numeric value, the texture will be square with both the height and width equal to the numeric value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ac1-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5ac1-150">Requirements</span></span>



| <span data-ttu-id="d5ac1-151">需求</span><span class="sxs-lookup"><span data-stu-id="d5ac1-151">Requirement</span></span> | <span data-ttu-id="d5ac1-152">值</span><span class="sxs-lookup"><span data-stu-id="d5ac1-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ac1-153">標頭</span><span class="sxs-lookup"><span data-stu-id="d5ac1-153">Header</span></span><br/>  | <dl> <span data-ttu-id="d5ac1-154"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ac1-154"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d5ac1-155">程式庫</span><span class="sxs-lookup"><span data-stu-id="d5ac1-155">Library</span></span><br/> | <dl> <span data-ttu-id="d5ac1-156"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5ac1-156"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d5ac1-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5ac1-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ac1-158">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="d5ac1-158">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
