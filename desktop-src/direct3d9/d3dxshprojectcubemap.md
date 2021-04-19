---
description: 將 cube 地圖上代表的函式投射到球面諧波 (SH) 。
ms.assetid: da5a3195-801e-4f1c-b52c-9eafc6e2e7b4
title: 'D3DXSHProjectCubeMap 函式 (D3dx9math) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHProjectCubeMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0e3e45b42907c47d8c7f1b9e5294738b8997cd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993901"
---
# <a name="d3dxshprojectcubemap-function"></a><span data-ttu-id="831bf-103">D3DXSHProjectCubeMap 函式</span><span class="sxs-lookup"><span data-stu-id="831bf-103">D3DXSHProjectCubeMap function</span></span>

<span data-ttu-id="831bf-104">將 cube 地圖上代表的函式投射到球面諧波 (SH) 。</span><span class="sxs-lookup"><span data-stu-id="831bf-104">Projects a function represented on a cube map into spherical harmonics (SH).</span></span>

## <a name="syntax"></a><span data-ttu-id="831bf-105">語法</span><span class="sxs-lookup"><span data-stu-id="831bf-105">Syntax</span></span>


```C++
HRESULT D3DXSHProjectCubeMap(
  _In_ UINT                   Order,
  _In_ LPDIRECT3DCUBETEXTURE9 pCubeMap,
  _In_ FLOAT                  *pROut,
  _In_ FLOAT                  *pGOut,
  _In_ FLOAT                  *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="831bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="831bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="831bf-107">*訂單* \[在\]</span><span class="sxs-lookup"><span data-stu-id="831bf-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831bf-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="831bf-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="831bf-109">球形調和 (SH) 評估的順序。</span><span class="sxs-lookup"><span data-stu-id="831bf-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="831bf-110">必須在 [D3DXSH \_ MINORDER](other-d3dx-constants.md) 到 D3DXSH \_ MAXORDER （含）的範圍內。</span><span class="sxs-lookup"><span data-stu-id="831bf-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="831bf-111">評估會產生順序²係數。</span><span class="sxs-lookup"><span data-stu-id="831bf-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="831bf-112">評估的程度是順序-1。</span><span class="sxs-lookup"><span data-stu-id="831bf-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="831bf-113">*pCubeMap* \[在\]</span><span class="sxs-lookup"><span data-stu-id="831bf-113">*pCubeMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831bf-114">類型： **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="831bf-114">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="831bf-115">來源 cube 材質的指標。</span><span class="sxs-lookup"><span data-stu-id="831bf-115">Pointer to a source cube texture.</span></span> <span data-ttu-id="831bf-116">請參閱 [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)。</span><span class="sxs-lookup"><span data-stu-id="831bf-116">See [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span></span>

</dd> <dt>

<span data-ttu-id="831bf-117">*pROut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="831bf-117">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831bf-118">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="831bf-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="831bf-119">紅色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="831bf-119">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="831bf-120">*pGOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="831bf-120">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831bf-121">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="831bf-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="831bf-122">綠色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="831bf-122">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="831bf-123">*pBOut* \[在\]</span><span class="sxs-lookup"><span data-stu-id="831bf-123">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="831bf-124">類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="831bf-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="831bf-125">藍色元件的輸出 SH 向量指標。</span><span class="sxs-lookup"><span data-stu-id="831bf-125">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="831bf-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="831bf-126">Return value</span></span>

<span data-ttu-id="831bf-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="831bf-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="831bf-128">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="831bf-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="831bf-129">如果函式失敗，則傳回值可以是： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="831bf-129">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="831bf-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="831bf-130">Requirements</span></span>



| <span data-ttu-id="831bf-131">需求</span><span class="sxs-lookup"><span data-stu-id="831bf-131">Requirement</span></span> | <span data-ttu-id="831bf-132">值</span><span class="sxs-lookup"><span data-stu-id="831bf-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="831bf-133">標頭</span><span class="sxs-lookup"><span data-stu-id="831bf-133">Header</span></span><br/>  | <dl> <span data-ttu-id="831bf-134"><dt>D3dx9math。h</dt></span><span class="sxs-lookup"><span data-stu-id="831bf-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="831bf-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="831bf-135">Library</span></span><br/> | <dl> <span data-ttu-id="831bf-136"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="831bf-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="831bf-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="831bf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="831bf-138">數學函數</span><span class="sxs-lookup"><span data-stu-id="831bf-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="831bf-139">預先計算 Radiance Transfer (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="831bf-139">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
