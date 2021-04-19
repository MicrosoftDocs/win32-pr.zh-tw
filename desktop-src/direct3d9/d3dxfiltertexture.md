---
description: 篩選材質的 mipmap 層級。
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: 'D3DXFilterTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997394"
---
# <a name="d3dxfiltertexture-function"></a><span data-ttu-id="8f298-103">D3DXFilterTexture 函式</span><span class="sxs-lookup"><span data-stu-id="8f298-103">D3DXFilterTexture function</span></span>

<span data-ttu-id="8f298-104">篩選材質的 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="8f298-104">Filters mipmap levels of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f298-105">語法</span><span class="sxs-lookup"><span data-stu-id="8f298-105">Syntax</span></span>


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="8f298-106">參數</span><span class="sxs-lookup"><span data-stu-id="8f298-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f298-107">*pBaseTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f298-107">*pBaseTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f298-108">類型： **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="8f298-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="8f298-109">[**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)介面的指標，代表要篩選的材質物件。</span><span class="sxs-lookup"><span data-stu-id="8f298-109">Pointer to an [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface that represents the texture object to filter.</span></span>

</dd> <dt>

<span data-ttu-id="8f298-110">*pPalette* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f298-110">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f298-111">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="8f298-111">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="8f298-112">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)結構的指標，代表要填入的256色調色板，或 nonpalettized 格式的 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8f298-112">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure that represents a 256-color palette to fill in, or **NULL** for nonpalettized formats.</span></span> <span data-ttu-id="8f298-113">如果未指定調色板，則會提供預設的 Direct3D 調色板 (所有不透明的白色調色板) 。</span><span class="sxs-lookup"><span data-stu-id="8f298-113">If a palette is not specified, the default Direct3D palette (an all opaque white palette) is provided.</span></span> <span data-ttu-id="8f298-114">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="8f298-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8f298-115">*SrcLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f298-115">*SrcLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f298-116">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f298-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f298-117">映射用來產生後續層級的層級。</span><span class="sxs-lookup"><span data-stu-id="8f298-117">Level whose image is used to generate the subsequent levels.</span></span> <span data-ttu-id="8f298-118">指定 \_ 此參數的 D3DX 預設值，相當於指定0。</span><span class="sxs-lookup"><span data-stu-id="8f298-118">Specifying D3DX\_DEFAULT for this parameter is equivalent to specifying 0.</span></span>

</dd> <dt>

<span data-ttu-id="8f298-119">*MipFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f298-119">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f298-120">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f298-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f298-121">一或多個 [D3DX \_ 篩選準則](d3dx-filter.md) 的組合，可控制 mipmap 的篩選方式。</span><span class="sxs-lookup"><span data-stu-id="8f298-121">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the mipmap is filtered.</span></span> <span data-ttu-id="8f298-122">\_如果紋理大小是2的乘冪，則指定這個參數的 D3DX 預設值就相當於指定 D3DX \_ 篩選方塊 \_ ， \_ 否則 D3DX 篩選方塊 \_ \| D3DX \_ 篩選 \_ 遞色。</span><span class="sxs-lookup"><span data-stu-id="8f298-122">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f298-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f298-123">Return value</span></span>

<span data-ttu-id="8f298-124">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8f298-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8f298-125">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="8f298-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8f298-126">如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="8f298-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f298-127">備註</span><span class="sxs-lookup"><span data-stu-id="8f298-127">Remarks</span></span>

<span data-ttu-id="8f298-128">篩選會以遞迴方式套用到每個材質層級，以產生下一個材質層級。</span><span class="sxs-lookup"><span data-stu-id="8f298-128">A filter is recursively applied to each texture level to generate the next texture level.</span></span>

<span data-ttu-id="8f298-129">寫入至非層級零的材質介面，不會讓中途的矩形更新。</span><span class="sxs-lookup"><span data-stu-id="8f298-129">Writing to a non-level-zero surface of the texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="8f298-130">如果呼叫 **D3DXFilterTexture** ，但介面尚未變更 (這在正常使用方式下不太可能) ，應用程式必須在紋理上明確呼叫 [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) 。</span><span class="sxs-lookup"><span data-stu-id="8f298-130">If **D3DXFilterTexture** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the texture.</span></span>

<span data-ttu-id="8f298-131">在預設集區中建立的材質 (D3DPOOL \_ 預設) 不能搭配 **D3DXFilterTexture** (使用， \_) 除非物件需要鎖定作業。</span><span class="sxs-lookup"><span data-stu-id="8f298-131">Textures created in the default pool (D3DPOOL\_DEFAULT) cannot be used with **D3DXFilterTexture** (unless created with D3DUSAGE\_DYNAMIC) because a lock operation is needed on the object.</span></span> <span data-ttu-id="8f298-132">請注意，預設集區中的材質不允許鎖定 (除非它們是動態) 。</span><span class="sxs-lookup"><span data-stu-id="8f298-132">Note that locks are prohibited on textures in the default pool (unless they are dynamic).</span></span>

<span data-ttu-id="8f298-133">如需 [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)的詳細資訊，請參閱 Platform SDK。</span><span class="sxs-lookup"><span data-stu-id="8f298-133">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="8f298-134">請注意，從 DirectX 8.0 起， **PALETTEENTRY** 結構的 peFlags 成員無法如 Platform SDK 中所述運作。</span><span class="sxs-lookup"><span data-stu-id="8f298-134">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="8f298-135">PeFlags 成員現在是8位調色盤格式的 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="8f298-135">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="8f298-136">只有一個材質篩選函式，但是有兩個宏呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8f298-136">There is only one texture filtering function, but two macros that call this method.</span></span>


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a><span data-ttu-id="8f298-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f298-137">Requirements</span></span>



| <span data-ttu-id="8f298-138">需求</span><span class="sxs-lookup"><span data-stu-id="8f298-138">Requirement</span></span> | <span data-ttu-id="8f298-139">值</span><span class="sxs-lookup"><span data-stu-id="8f298-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f298-140">標頭</span><span class="sxs-lookup"><span data-stu-id="8f298-140">Header</span></span><br/>  | <dl> <span data-ttu-id="8f298-141"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f298-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8f298-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="8f298-142">Library</span></span><br/> | <dl> <span data-ttu-id="8f298-143"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f298-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8f298-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f298-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f298-145">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="8f298-145">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
