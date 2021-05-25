---
description: 定義材質階段的材質篩選模式。
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: 'D3DTEXTUREFILTERTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: bd6038e1b3d2b2f85e5766605583db9879427343
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343003"
---
# <a name="d3dtexturefiltertype-enumeration"></a><span data-ttu-id="33955-103">D3DTEXTUREFILTERTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="33955-103">D3DTEXTUREFILTERTYPE enumeration</span></span>

<span data-ttu-id="33955-104">定義材質階段的材質篩選模式。</span><span class="sxs-lookup"><span data-stu-id="33955-104">Defines texture filtering modes for a texture stage.</span></span>

## <a name="syntax"></a><span data-ttu-id="33955-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33955-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a><span data-ttu-id="33955-106">常數</span><span class="sxs-lookup"><span data-stu-id="33955-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="33955-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ 無**</span><span class="sxs-lookup"><span data-stu-id="33955-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="33955-108">搭配 [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md)使用時，會停用 mipmap。</span><span class="sxs-lookup"><span data-stu-id="33955-108">When used with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md), disables mipmapping.</span></span>

</dd> <dt>

<span data-ttu-id="33955-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF \_ 點**</span><span class="sxs-lookup"><span data-stu-id="33955-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="33955-110">搭配 [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) 或 [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)使用時，會指定點篩選要分別當做材質放大或縮制篩選使用。</span><span class="sxs-lookup"><span data-stu-id="33955-110">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that point filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="33955-111">搭配 **D3DSAMP \_ MIPFILTER** 使用時，會啟用 mipmap，並指定轉譯器會從最接近的 mip 層級材質中選擇色彩。</span><span class="sxs-lookup"><span data-stu-id="33955-111">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and specifies that the rasterizer chooses the color from the texel of the nearest mip level.</span></span>

</dd> <dt>

<span data-ttu-id="33955-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ 線性**</span><span class="sxs-lookup"><span data-stu-id="33955-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="33955-113">搭配 [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) 或 [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)使用時，會指定線性篩選要分別當做材質放大或縮制篩選使用。</span><span class="sxs-lookup"><span data-stu-id="33955-113">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that linear filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="33955-114">與 **D3DSAMP \_ MIPFILTER** 搭配使用時，會啟用 mipmap 和三線性篩選; 它會指定在兩個最接近的 mip 層級之間，進行轉譯器的插補。</span><span class="sxs-lookup"><span data-stu-id="33955-114">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and trilinear filtering; it specifies that the rasterizer interpolates between the two nearest mip levels.</span></span>

</dd> <dt>

<span data-ttu-id="33955-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ 各向異性**</span><span class="sxs-lookup"><span data-stu-id="33955-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF\_ANISOTROPIC**</span></span>
</dt> <dd>

<span data-ttu-id="33955-116">搭配 [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) 或 [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md)使用時，會指定用來分別作為紋理縮放比例或縮制篩選的非等向材質篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-116">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively.</span></span> <span data-ttu-id="33955-117">補償紋理多邊形和螢幕平面之間的角度差異所造成的扭曲。</span><span class="sxs-lookup"><span data-stu-id="33955-117">Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen.</span></span> <span data-ttu-id="33955-118">未定義搭配 **D3DSAMP \_ MIPFILTER** 使用。</span><span class="sxs-lookup"><span data-stu-id="33955-118">Use with **D3DSAMP\_MIPFILTER** is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="33955-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**</span><span class="sxs-lookup"><span data-stu-id="33955-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF\_PYRAMIDALQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="33955-120">用來作為材質放大或縮制濾波器的四個範例折做篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-120">A 4-sample tent filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="33955-121">未定義搭配 [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) 使用。</span><span class="sxs-lookup"><span data-stu-id="33955-121">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="33955-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**</span><span class="sxs-lookup"><span data-stu-id="33955-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF\_GAUSSIANQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="33955-123">用來作為材質放大或縮制濾波器的4個範例高斯篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-123">A 4-sample Gaussian filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="33955-124">未定義搭配 [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) 使用。</span><span class="sxs-lookup"><span data-stu-id="33955-124">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="33955-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**</span><span class="sxs-lookup"><span data-stu-id="33955-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF\_CONVOLUTIONMONO**</span></span>
</dt> <dd>

<span data-ttu-id="33955-126">單色紋理的卷積篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-126">Convolution filter for monochrome textures.</span></span> <span data-ttu-id="33955-127">請參閱 [D3DFMT \_ A1](d3dformat.md)。</span><span class="sxs-lookup"><span data-stu-id="33955-127">See [D3DFMT\_A1](d3dformat.md).</span></span>

<span data-ttu-id="33955-128">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="33955-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="33955-129">此旗標僅適用于 Direct3D 9Ex。</span><span class="sxs-lookup"><span data-stu-id="33955-129">This flag is available in Direct3D 9Ex only.</span></span>



 

<span data-ttu-id="33955-130">未定義搭配 [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) 使用。</span><span class="sxs-lookup"><span data-stu-id="33955-130">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="33955-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ 強制 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="33955-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="33955-132">強制此列舉的大小編譯為32位。</span><span class="sxs-lookup"><span data-stu-id="33955-132">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="33955-133">如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。</span><span class="sxs-lookup"><span data-stu-id="33955-133">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="33955-134">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="33955-134">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33955-135">備註</span><span class="sxs-lookup"><span data-stu-id="33955-135">Remarks</span></span>

<span data-ttu-id="33955-136">[**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)和 [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)會使用 D3DTEXTUREFILTERTYPE 來定義材質階段的材質篩選模式。</span><span class="sxs-lookup"><span data-stu-id="33955-136">D3DTEXTUREFILTERTYPE is used by [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) along with [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) to define texture filtering modes for a texture stage.</span></span>

<span data-ttu-id="33955-137">若要檢查格式是否支援 D3DTEXF 點以外的材質篩選類型 \_ ， (一律支援) ，請使用 D3DUSAGE 查詢篩選準則來呼叫 [**IDirect3D9：： CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="33955-137">To check if a format supports texture filter types other than D3DTEXF\_POINT (which is always supported), call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_FILTER.</span></span>

<span data-ttu-id="33955-138">藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 與 D3DSAMP \_ MAGFILTER 值做為第二個參數，並使用這個列舉的一個成員做為第三個參數，設定紋理階段的放大篩選篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-138">Set a texture stage's magnification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="33955-139">藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 與 D3DSAMP \_ MINFILTER 值做為第二個參數，並使用這個列舉的一個成員做為第三個參數，來設定紋理階段的縮制篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-139">Set a texture stage's minification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="33955-140">藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 與 D3DSAMP \_ MIPFILTER 值做為第二個參數，並將此列舉的一個成員作為第三個參數，將材質篩選設定為使用 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="33955-140">Set the texture filter to use between-mipmap levels by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="33955-141">並非所有適用于裝置的有效篩選模式都適用于磁片區對應。</span><span class="sxs-lookup"><span data-stu-id="33955-141">Not all valid filtering modes for a device will apply to volume maps.</span></span> <span data-ttu-id="33955-142">一般而言，磁片區 \_ 對應會支援 D3DTEXF POINT 和 D3DTEXF \_ 線性放大篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-142">In general, D3DTEXF\_POINT and D3DTEXF\_LINEAR magnification filters will be supported for volume maps.</span></span> <span data-ttu-id="33955-143">如果 \_ 設定了 D3DPTEXTURECAPS MIPVOLUMEMAP，則磁片區 \_ 對應將會支援 D3DTEXF 點 mipmap 濾波器和 D3DTEXF \_ 點以及 D3DTEXF \_ 線性縮制篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-143">If D3DPTEXTURECAPS\_MIPVOLUMEMAP is set, then the D3DTEXF\_POINT mipmap filter and D3DTEXF\_POINT and D3DTEXF\_LINEAR minification filters will be supported for volume maps.</span></span> <span data-ttu-id="33955-144">裝置不一定會支援磁片區對應的 D3DTEXF \_ 線性 mipmap 篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-144">The device may or may not support the D3DTEXF\_LINEAR mipmap filter for volume maps.</span></span> <span data-ttu-id="33955-145">支援2D 對應之非等向篩選的裝置不一定支援磁片區對應的非等向篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-145">Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps.</span></span> <span data-ttu-id="33955-146">不過，啟用非等向篩選的應用程式將會收到最佳的可用篩選 (可能的線性) 如果不支援非等向篩選。</span><span class="sxs-lookup"><span data-stu-id="33955-146">However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="33955-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="33955-147">Requirements</span></span>



| <span data-ttu-id="33955-148">需求</span><span class="sxs-lookup"><span data-stu-id="33955-148">Requirement</span></span> | <span data-ttu-id="33955-149">值</span><span class="sxs-lookup"><span data-stu-id="33955-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33955-150">標頭</span><span class="sxs-lookup"><span data-stu-id="33955-150">Header</span></span><br/> | <dl> <span data-ttu-id="33955-151"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="33955-151"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33955-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33955-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33955-153">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="33955-153">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="33955-154">**ID3DXPatchMesh::GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="33955-154">**ID3DXPatchMesh::GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="33955-155">**ID3DXPatchMesh::SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="33955-155">**ID3DXPatchMesh::SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="33955-156">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="33955-156">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> <dt>

[<span data-ttu-id="33955-157">**IDirect3DDevice9::SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="33955-157">**IDirect3DDevice9::SetSamplerState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
