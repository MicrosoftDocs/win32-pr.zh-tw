---
description: 使用使用者提供的函式來填滿給定磁片區材質之每個 mip 層級的每個材質。
ms.assetid: cc9eb051-8a62-4e35-87df-c255f10e94d8
title: 'D3DXFillVolumeTexture 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFillVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d817470f0f0617001fd83054e24e8881ac9a3a1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322920"
---
# <a name="d3dxfillvolumetexture-function"></a><span data-ttu-id="978d6-103">D3DXFillVolumeTexture 函式</span><span class="sxs-lookup"><span data-stu-id="978d6-103">D3DXFillVolumeTexture function</span></span>

<span data-ttu-id="978d6-104">使用使用者提供的函式來填滿給定磁片區材質之每個 mip 層級的每個材質。</span><span class="sxs-lookup"><span data-stu-id="978d6-104">Uses a user-provided function to fill each texel of each mip level of a given volume texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="978d6-105">語法</span><span class="sxs-lookup"><span data-stu-id="978d6-105">Syntax</span></span>


```C++
HRESULT D3DXFillVolumeTexture(
  _Out_ LPDIRECT3DVOLUMETEXTURE9 pTexture,
  _In_  LPD3DXFILL3D             pFunction,
  _In_  LPVOID                   pData
);
```



## <a name="parameters"></a><span data-ttu-id="978d6-106">參數</span><span class="sxs-lookup"><span data-stu-id="978d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="978d6-107">*pTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="978d6-107">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="978d6-108">類型： **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="978d6-108">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="978d6-109">[**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)介面的指標，代表填滿的材質。</span><span class="sxs-lookup"><span data-stu-id="978d6-109">Pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the filled texture.</span></span>

</dd> <dt>

<span data-ttu-id="978d6-110">*pFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="978d6-110">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="978d6-111">類型： **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span><span class="sxs-lookup"><span data-stu-id="978d6-111">Type: **[LPD3DXFILL3D](lpd3dxfill3d.md)**</span></span>

<span data-ttu-id="978d6-112">使用者提供的評估工具函式的指標，該函式將用來計算每個材質的值。</span><span class="sxs-lookup"><span data-stu-id="978d6-112">Pointer to a user-provided evaluator function, which will be used to compute the value of each texel.</span></span> <span data-ttu-id="978d6-113">函數會遵循 [LPD3DXFILL3D](lpd3dxfill3d.md)的原型。</span><span class="sxs-lookup"><span data-stu-id="978d6-113">The function follows the prototype of [LPD3DXFILL3D](lpd3dxfill3d.md).</span></span>

</dd> <dt>

<span data-ttu-id="978d6-114">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="978d6-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="978d6-115">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="978d6-115">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="978d6-116">使用者定義資料之任意區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="978d6-116">Pointer to an arbitrary block of user-defined data.</span></span> <span data-ttu-id="978d6-117">此指標會傳遞至 *pFunction* 中提供的函式。</span><span class="sxs-lookup"><span data-stu-id="978d6-117">This pointer will be passed to the function provided in *pFunction*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="978d6-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="978d6-118">Return value</span></span>

<span data-ttu-id="978d6-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="978d6-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="978d6-120">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="978d6-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="978d6-121">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="978d6-121">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="978d6-122">備註</span><span class="sxs-lookup"><span data-stu-id="978d6-122">Remarks</span></span>

<span data-ttu-id="978d6-123">如果磁片區為非動態 (，因為使用方式在建立時設為 0) ，而且位於視訊記憶體 (記憶體集區設定為 D3DPOOL \_ 預設) 時， **D3DXFillVolumeTexture** 將會失敗，因為無法鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="978d6-123">If the volume is non-dynamic (because usage is set to 0 when it is created), and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXFillVolumeTexture** will fail because the volume cannot be locked.</span></span>

<span data-ttu-id="978d6-124">這個範例會建立一個名為 ColorVolumeFill 的函式，此函式依賴 D3DXFillVolumeTexture。</span><span class="sxs-lookup"><span data-stu-id="978d6-124">This example creates a function called ColorVolumeFill, which relies on D3DXFillVolumeTexture.</span></span>


```
// Define a function that matches the prototype of LPD3DXFILL3D
VOID WINAPI ColorVolumeFill (D3DXVECTOR4* pOut, const D3DXVECTOR3* pTexCoord, 
const D3DXVECTOR3* pTexelSize, LPVOID pData)
{
   *pOut = D3DXVECTOR4(pTexCoord->x, pTexCoord->y, pTexCoord->z, 0.0f);
}
    
    
// Fill volume texture
if (FAILED (hr = D3DXFillVolumeTexture (m_pTexture, ColorVolumeFill, NULL)))
{
       return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="978d6-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="978d6-125">Requirements</span></span>



| <span data-ttu-id="978d6-126">需求</span><span class="sxs-lookup"><span data-stu-id="978d6-126">Requirement</span></span> | <span data-ttu-id="978d6-127">值</span><span class="sxs-lookup"><span data-stu-id="978d6-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="978d6-128">標頭</span><span class="sxs-lookup"><span data-stu-id="978d6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="978d6-129"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="978d6-129"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="978d6-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="978d6-130">Library</span></span><br/> | <dl> <span data-ttu-id="978d6-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="978d6-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="978d6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="978d6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="978d6-133">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="978d6-133">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
