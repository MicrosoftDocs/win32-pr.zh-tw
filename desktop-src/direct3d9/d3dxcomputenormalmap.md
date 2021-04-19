---
description: 將高度地圖轉換成一般地圖。 每個標準的 (x、y、z) 元件都會對應到輸出材質 (r、g、b) 通道。
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: 'D3DXComputeNormalMap 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e22418f5a023dbe70fee8ea0fba8a449abbcc8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982895"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="c2605-104">D3DXComputeNormalMap 函式</span><span class="sxs-lookup"><span data-stu-id="c2605-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="c2605-105">將高度地圖轉換成一般地圖。</span><span class="sxs-lookup"><span data-stu-id="c2605-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="c2605-106">每個標準的 (x、y、z) 元件都會對應到輸出材質 (r、g、b) 通道。</span><span class="sxs-lookup"><span data-stu-id="c2605-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2605-107">語法</span><span class="sxs-lookup"><span data-stu-id="c2605-107">Syntax</span></span>


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a><span data-ttu-id="c2605-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2605-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2605-109">*pTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c2605-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2605-110">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c2605-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c2605-111">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面的指標，表示目的地材質。</span><span class="sxs-lookup"><span data-stu-id="c2605-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="c2605-112">*pSrcTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2605-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2605-113">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c2605-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c2605-114">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面的指標，代表來源的高度地圖材質。</span><span class="sxs-lookup"><span data-stu-id="c2605-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="c2605-115">*pSrcPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2605-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2605-116">Type： **Const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="c2605-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="c2605-117">[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)類型的指標，其中包含256色彩的來源調色板或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c2605-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c2605-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c2605-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2605-119">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2605-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2605-120">控制正常對應產生的一或多個 [D3DX \_ NORMALMAP](d3dx-normalmap.md) 旗標。</span><span class="sxs-lookup"><span data-stu-id="c2605-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="c2605-121">*頻道* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2605-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2605-122">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2605-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2605-123">一個 [D3DX \_ 通道](d3dx-channel.md) 旗標，指定高度資訊的來源。</span><span class="sxs-lookup"><span data-stu-id="c2605-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="c2605-124">*振幅* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2605-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2605-125">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c2605-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c2605-126">常數值乘數，可增加 (或減少標準對應中的值) 。</span><span class="sxs-lookup"><span data-stu-id="c2605-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="c2605-127">較高的值通常會使凹凸變得更明顯，較低的值通常會讓顯示的偏低。</span><span class="sxs-lookup"><span data-stu-id="c2605-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2605-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2605-128">Return value</span></span>

<span data-ttu-id="c2605-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c2605-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c2605-130">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c2605-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c2605-131">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="c2605-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2605-132">備註</span><span class="sxs-lookup"><span data-stu-id="c2605-132">Remarks</span></span>

<span data-ttu-id="c2605-133">這個方法會使用核心大小為3x3 的中央差異來計算正常。</span><span class="sxs-lookup"><span data-stu-id="c2605-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="c2605-134">使用的中央差異分母為2.0。</span><span class="sxs-lookup"><span data-stu-id="c2605-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="c2605-135">目的地中的 RGB 通道包含一般 (x、y、z) 元件的偏誤。</span><span class="sxs-lookup"><span data-stu-id="c2605-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2605-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2605-136">Requirements</span></span>



| <span data-ttu-id="c2605-137">需求</span><span class="sxs-lookup"><span data-stu-id="c2605-137">Requirement</span></span> | <span data-ttu-id="c2605-138">值</span><span class="sxs-lookup"><span data-stu-id="c2605-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2605-139">標頭</span><span class="sxs-lookup"><span data-stu-id="c2605-139">Header</span></span><br/>  | <dl> <span data-ttu-id="c2605-140"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2605-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c2605-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="c2605-141">Library</span></span><br/> | <dl> <span data-ttu-id="c2605-142"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2605-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c2605-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2605-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2605-144">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="c2605-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
