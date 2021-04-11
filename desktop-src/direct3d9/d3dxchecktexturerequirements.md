---
description: 檢查材質建立參數。
ms.assetid: f8e788f3-02a9-4ee7-b74d-9e781a2fb39f
title: 'D3DXCheckTextureRequirements 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d4fdc0998bfda2144e900c099919bc75c01e8ee3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196302"
---
# <a name="d3dxchecktexturerequirements-function"></a><span data-ttu-id="feb21-103">D3DXCheckTextureRequirements 函式</span><span class="sxs-lookup"><span data-stu-id="feb21-103">D3DXCheckTextureRequirements function</span></span>

<span data-ttu-id="feb21-104">檢查材質建立參數。</span><span class="sxs-lookup"><span data-stu-id="feb21-104">Checks texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb21-105">語法</span><span class="sxs-lookup"><span data-stu-id="feb21-105">Syntax</span></span>


```C++
HRESULT D3DXCheckTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="feb21-106">參數</span><span class="sxs-lookup"><span data-stu-id="feb21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feb21-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="feb21-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feb21-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="feb21-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="feb21-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表要與材質相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="feb21-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="feb21-110">*pWidth* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="feb21-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="feb21-111">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="feb21-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="feb21-112">要求的寬度（以圖元為單位）的指標，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="feb21-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="feb21-113">傳回已更正的大小。</span><span class="sxs-lookup"><span data-stu-id="feb21-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="feb21-114">*pHeight* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="feb21-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="feb21-115">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="feb21-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="feb21-116">要求高度（以圖元為單位）的指標，或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="feb21-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="feb21-117">傳回已更正的大小。</span><span class="sxs-lookup"><span data-stu-id="feb21-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="feb21-118">*pNumMipLevels* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="feb21-118">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="feb21-119">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="feb21-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="feb21-120">要求的 mipmap 層級數目的指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="feb21-120">Pointer to number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="feb21-121">傳回已更正的 mipmap 層級數目。</span><span class="sxs-lookup"><span data-stu-id="feb21-121">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="feb21-122">*使用* \[ 方式在\]</span><span class="sxs-lookup"><span data-stu-id="feb21-122">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feb21-123">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="feb21-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="feb21-124">0或 [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)。</span><span class="sxs-lookup"><span data-stu-id="feb21-124">0 or [**D3DUSAGE\_RENDERTARGET**](d3dusage.md).</span></span> <span data-ttu-id="feb21-125">將此旗標設定為 D3DUSAGE \_ RENDERTARGET 表示介面要當做轉譯目標使用。</span><span class="sxs-lookup"><span data-stu-id="feb21-125">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="feb21-126">然後，您可以將資源傳遞給 [**SetRenderTarget**](/windows/desktop/api) 方法的 pNewRenderTarget 參數。</span><span class="sxs-lookup"><span data-stu-id="feb21-126">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="feb21-127">如果指定了 **D3DUSAGE \_ RENDERTARGET** ，應用程式應該藉由呼叫 [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)來檢查裝置是否支援這項操作。</span><span class="sxs-lookup"><span data-stu-id="feb21-127">If **D3DUSAGE\_RENDERTARGET** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="feb21-128">*pformatetc 架構* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="feb21-128">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="feb21-129">類型： **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="feb21-129">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="feb21-130">[D3DFORMAT](d3dformat.md)列舉型別的成員指標。</span><span class="sxs-lookup"><span data-stu-id="feb21-130">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="feb21-131">指定所需的像素格式，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="feb21-131">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="feb21-132">傳回更正的格式。</span><span class="sxs-lookup"><span data-stu-id="feb21-132">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="feb21-133">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="feb21-133">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="feb21-134">類型： **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="feb21-134">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="feb21-135">[**D3DPOOL**](./d3dpool.md)列舉型別的成員，描述應放置紋理的記憶體類別。</span><span class="sxs-lookup"><span data-stu-id="feb21-135">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feb21-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="feb21-136">Return value</span></span>

<span data-ttu-id="feb21-137">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="feb21-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="feb21-138">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="feb21-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="feb21-139">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DERR \_ NOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="feb21-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE.</span></span>

## <a name="remarks"></a><span data-ttu-id="feb21-140">備註</span><span class="sxs-lookup"><span data-stu-id="feb21-140">Remarks</span></span>

<span data-ttu-id="feb21-141">如果此函式的參數無效，此函式會傳回已更正的參數。</span><span class="sxs-lookup"><span data-stu-id="feb21-141">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="feb21-142">在比較要求的要求與可用格式時，此函式會使用下列啟發學習法：</span><span class="sxs-lookup"><span data-stu-id="feb21-142">This function uses the following heuristics when comparing the requested requirements against available formats:</span></span>

-   <span data-ttu-id="feb21-143">請勿選擇頻道較少的格式。</span><span class="sxs-lookup"><span data-stu-id="feb21-143">Do not choose a format that has fewer channels.</span></span>
-   <span data-ttu-id="feb21-144">除非明確要求，否則請避免 [FOURCC](d3dformat.md) 和24位格式。</span><span class="sxs-lookup"><span data-stu-id="feb21-144">Avoid [FOURCC](d3dformat.md) And 24-bit formats unless explicitly requested.</span></span>
-   <span data-ttu-id="feb21-145">請不要新增通道。</span><span class="sxs-lookup"><span data-stu-id="feb21-145">Try not to add new channels.</span></span>
-   <span data-ttu-id="feb21-146">請不要變更每個通道的位數。</span><span class="sxs-lookup"><span data-stu-id="feb21-146">Try not to change the number of bits per channel.</span></span>
-   <span data-ttu-id="feb21-147">請嘗試避免在格式類型之間轉換。</span><span class="sxs-lookup"><span data-stu-id="feb21-147">Try to avoid converting between types of formats.</span></span> <span data-ttu-id="feb21-148">例如，請避免將 ARGB 格式轉換成深度格式。</span><span class="sxs-lookup"><span data-stu-id="feb21-148">For instance, avoid converting an ARGB format to a depth format.</span></span>

## <a name="requirements"></a><span data-ttu-id="feb21-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="feb21-149">Requirements</span></span>



| <span data-ttu-id="feb21-150">需求</span><span class="sxs-lookup"><span data-stu-id="feb21-150">Requirement</span></span> | <span data-ttu-id="feb21-151">值</span><span class="sxs-lookup"><span data-stu-id="feb21-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="feb21-152">標頭</span><span class="sxs-lookup"><span data-stu-id="feb21-152">Header</span></span><br/>  | <dl> <span data-ttu-id="feb21-153"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="feb21-153"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="feb21-154">程式庫</span><span class="sxs-lookup"><span data-stu-id="feb21-154">Library</span></span><br/> | <dl> <span data-ttu-id="feb21-155"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="feb21-155"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="feb21-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="feb21-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb21-157">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="feb21-157">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
