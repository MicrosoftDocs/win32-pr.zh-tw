---
description: 建立動畫控制器物件。
ms.assetid: 771e5966-ac1a-43c2-8e81-b6d573343ff0
title: 'D3DXCreateAnimationController 函式 (D3dx9anim) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateAnimationController
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a61b2c42a1eafa2ed28ac98c753588181a0ccf7a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986509"
---
# <a name="d3dxcreateanimationcontroller-function"></a><span data-ttu-id="10c33-103">D3DXCreateAnimationController 函式</span><span class="sxs-lookup"><span data-stu-id="10c33-103">D3DXCreateAnimationController function</span></span>

<span data-ttu-id="10c33-104">建立動畫控制器物件。</span><span class="sxs-lookup"><span data-stu-id="10c33-104">Creates an animation controller object.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c33-105">語法</span><span class="sxs-lookup"><span data-stu-id="10c33-105">Syntax</span></span>


```C++
HRESULT D3DXCreateAnimationController(
  _In_  UINT                      MaxNumAnimationOutputs,
  _In_  UINT                      MaxNumAnimationSets,
  _In_  UINT                      MaxNumTracks,
  _In_  UINT                      MaxNumEvents,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="10c33-106">參數</span><span class="sxs-lookup"><span data-stu-id="10c33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10c33-107">*MaxNumAnimationOutputs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="10c33-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10c33-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10c33-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10c33-109">控制器可支援的動畫輸出數目上限。</span><span class="sxs-lookup"><span data-stu-id="10c33-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="10c33-110">*MaxNumAnimationSets* \[在\]</span><span class="sxs-lookup"><span data-stu-id="10c33-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10c33-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10c33-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10c33-112">可以混合的動畫集合數目上限。</span><span class="sxs-lookup"><span data-stu-id="10c33-112">Maximum number of animation sets that can be mixed.</span></span>

</dd> <dt>

<span data-ttu-id="10c33-113">*MaxNumTracks* \[在\]</span><span class="sxs-lookup"><span data-stu-id="10c33-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10c33-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10c33-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10c33-115">可以同時混合的動畫集合數目上限。</span><span class="sxs-lookup"><span data-stu-id="10c33-115">Maximum number of animation sets that can be mixed simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="10c33-116">*MaxNumEvents* \[在\]</span><span class="sxs-lookup"><span data-stu-id="10c33-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10c33-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="10c33-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="10c33-118">控制器將支援的未完成事件數目上限。</span><span class="sxs-lookup"><span data-stu-id="10c33-118">Maximum number of outstanding events that the controller will support.</span></span>

</dd> <dt>

<span data-ttu-id="10c33-119">*ppAnimController* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="10c33-119">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10c33-120">類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="10c33-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="10c33-121">建立的動畫控制器物件的指標。</span><span class="sxs-lookup"><span data-stu-id="10c33-121">Pointer to the animation controller object created.</span></span> <span data-ttu-id="10c33-122">請參閱 [**ID3DXAnimationController**](id3dxanimationcontroller.md)。</span><span class="sxs-lookup"><span data-stu-id="10c33-122">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10c33-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="10c33-123">Return value</span></span>

<span data-ttu-id="10c33-124">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="10c33-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="10c33-125">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="10c33-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="10c33-126">如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="10c33-126">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="10c33-127">備註</span><span class="sxs-lookup"><span data-stu-id="10c33-127">Remarks</span></span>

<span data-ttu-id="10c33-128">動畫控制器會控制動畫混音器。</span><span class="sxs-lookup"><span data-stu-id="10c33-128">An animation controller controls an animation mixer.</span></span> <span data-ttu-id="10c33-129">控制器會新增方法來修改一段時間的混合參數，以啟用平滑轉換。</span><span class="sxs-lookup"><span data-stu-id="10c33-129">The controller adds methods to modify blending parameters over time to enable smooth transitions.</span></span>

## <a name="requirements"></a><span data-ttu-id="10c33-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="10c33-130">Requirements</span></span>



| <span data-ttu-id="10c33-131">需求</span><span class="sxs-lookup"><span data-stu-id="10c33-131">Requirement</span></span> | <span data-ttu-id="10c33-132">值</span><span class="sxs-lookup"><span data-stu-id="10c33-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10c33-133">標頭</span><span class="sxs-lookup"><span data-stu-id="10c33-133">Header</span></span><br/>  | <dl> <span data-ttu-id="10c33-134"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="10c33-134"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="10c33-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="10c33-135">Library</span></span><br/> | <dl> <span data-ttu-id="10c33-136"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="10c33-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="10c33-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10c33-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c33-138">動畫函數</span><span class="sxs-lookup"><span data-stu-id="10c33-138">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
