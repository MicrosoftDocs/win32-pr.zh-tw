---
description: 使用使用者提供的函式來填滿給定材質之每個 mip 層級的每個材質。
ms.assetid: 9c822472-2bbf-4629-bdb3-6491573e8de2
title: 'D3DXFillTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 20790a9e4c1a9ce242a5e067dd617c7871a70b7c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322923"
---
# <a name="d3dxfilltexture-function"></a><span data-ttu-id="bb21f-103">D3DXFillTexture 函式</span><span class="sxs-lookup"><span data-stu-id="bb21f-103">D3DXFillTexture function</span></span>

<span data-ttu-id="bb21f-104">使用使用者提供的函式來填滿給定材質之每個 mip 層級的每個材質。</span><span class="sxs-lookup"><span data-stu-id="bb21f-104">Uses a user-provided function to fill each texel of each mip level of a given texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb21f-105">語法</span><span class="sxs-lookup"><span data-stu-id="bb21f-105">Syntax</span></span>


```C++
HRESULT D3DXFillTexture(
  _Out_ LPDIRECT3DTEXTURE9 pTexture,
  _In_  LPD3DXFILL2D       pFunction,
  _In_  LPVOID             pData
);
```



## <a name="parameters"></a><span data-ttu-id="bb21f-106">參數</span><span class="sxs-lookup"><span data-stu-id="bb21f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb21f-107">*pTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bb21f-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb21f-108">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="bb21f-108">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="bb21f-109">[**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)介面的指標，代表填滿的材質。</span><span class="sxs-lookup"><span data-stu-id="bb21f-109">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="bb21f-110">*pFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb21f-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb21f-111">類型： **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span><span class="sxs-lookup"><span data-stu-id="bb21f-111">Type: **[LPD3DXFILL2D](lpd3dxfill2d.md)**</span></span>

<span data-ttu-id="bb21f-112">使用者提供的評估工具函式的指標，該函式將用來計算每個材質的值。</span><span class="sxs-lookup"><span data-stu-id="bb21f-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="bb21f-113">函數會遵循 [LPD3DXFILL2D](lpd3dxfill2d.md)的原型。</span><span class="sxs-lookup"><span data-stu-id="bb21f-113">The function follows the prototype of [LPD3DXFILL2D](lpd3dxfill2d.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb21f-114">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb21f-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb21f-115">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb21f-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb21f-116">使用者定義資料之任意區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="bb21f-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="bb21f-117">此指標會傳遞至 *pFunction* 中提供的函式。</span><span class="sxs-lookup"><span data-stu-id="bb21f-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb21f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb21f-118">Return value</span></span>

<span data-ttu-id="bb21f-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb21f-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb21f-120">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="bb21f-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bb21f-121">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="bb21f-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb21f-122">備註</span><span class="sxs-lookup"><span data-stu-id="bb21f-122">Remarks</span></span>

<span data-ttu-id="bb21f-123">以下範例會建立一個名為 ColorFill 的函式，該函式依賴 D3DXFillTexture。</span><span class="sxs-lookup"><span data-stu-id="bb21f-123">Here is an example that creates a function called ColorFill, which relies on D3DXFillTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorFill (D3DXVECTOR4* pOut, const D3DXVECTOR2* pTexCoord, 
const D3DXVECTOR2* pTexelSize, LPVOID pData)
{
    *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, 0.0f, 0.0f);
}
    
    
// Fill the texture using D3DXFillTexture
if (FAILED (hr = D3DXFillTexture (m_pTexture, ColorFill, NULL)))
{
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="bb21f-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb21f-124">Requirements</span></span>



| <span data-ttu-id="bb21f-125">需求</span><span class="sxs-lookup"><span data-stu-id="bb21f-125">Requirement</span></span> | <span data-ttu-id="bb21f-126">值</span><span class="sxs-lookup"><span data-stu-id="bb21f-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb21f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="bb21f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bb21f-128"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb21f-128"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="bb21f-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="bb21f-129">Library</span></span><br/> | <dl> <span data-ttu-id="bb21f-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb21f-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="bb21f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb21f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb21f-132">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="bb21f-132">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
