---
description: 針對框架階層，在動畫混音器中註冊所有命名的矩陣。
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: 'D3DXFrameRegisterNamedMatrices 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8496f467e668939c5d5aa0e90266ab012d436038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997393"
---
# <a name="d3dxframeregisternamedmatrices-function"></a><span data-ttu-id="b2812-103">D3DXFrameRegisterNamedMatrices 函式</span><span class="sxs-lookup"><span data-stu-id="b2812-103">D3DXFrameRegisterNamedMatrices function</span></span>

<span data-ttu-id="b2812-104">針對框架階層，在動畫混音器中註冊所有命名的矩陣。</span><span class="sxs-lookup"><span data-stu-id="b2812-104">Given a frame hierarchy, registers all the named matrices in the animation mixer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2812-105">語法</span><span class="sxs-lookup"><span data-stu-id="b2812-105">Syntax</span></span>


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="b2812-106">參數</span><span class="sxs-lookup"><span data-stu-id="b2812-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2812-107">*pFrameRoot* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2812-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2812-108">類型： **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="b2812-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="b2812-109">框架階層中的最上層節點。</span><span class="sxs-lookup"><span data-stu-id="b2812-109">The top level node in the frame hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="b2812-110">*pAnimController* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2812-110">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2812-111">類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="b2812-111">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="b2812-112">動畫控制器物件的指標。</span><span class="sxs-lookup"><span data-stu-id="b2812-112">Pointer to the animation controller object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2812-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2812-113">Return value</span></span>

<span data-ttu-id="b2812-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b2812-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b2812-115">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b2812-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b2812-116">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="b2812-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2812-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2812-117">Requirements</span></span>



| <span data-ttu-id="b2812-118">需求</span><span class="sxs-lookup"><span data-stu-id="b2812-118">Requirement</span></span> | <span data-ttu-id="b2812-119">值</span><span class="sxs-lookup"><span data-stu-id="b2812-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2812-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b2812-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b2812-121"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2812-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b2812-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="b2812-122">Library</span></span><br/> | <dl> <span data-ttu-id="b2812-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2812-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b2812-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2812-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2812-125">動畫函數</span><span class="sxs-lookup"><span data-stu-id="b2812-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




