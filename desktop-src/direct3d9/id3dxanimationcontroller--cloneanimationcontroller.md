---
description: 複製或複製動畫控制器。
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'ID3DXAnimationController：： CloneAnimationController 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323296"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a><span data-ttu-id="811a4-103">ID3DXAnimationController：： CloneAnimationController 方法</span><span class="sxs-lookup"><span data-stu-id="811a4-103">ID3DXAnimationController::CloneAnimationController method</span></span>

<span data-ttu-id="811a4-104">複製或複製動畫控制器。</span><span class="sxs-lookup"><span data-stu-id="811a4-104">Clones, or copies, an animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="811a4-105">語法</span><span class="sxs-lookup"><span data-stu-id="811a4-105">Syntax</span></span>


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="811a4-106">參數</span><span class="sxs-lookup"><span data-stu-id="811a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="811a4-107">*MaxNumAnimationOutputs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="811a4-107">*MaxNumAnimationOutputs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="811a4-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="811a4-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="811a4-109">控制器可支援的動畫輸出數目上限。</span><span class="sxs-lookup"><span data-stu-id="811a4-109">Maximum number of animation outputs the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="811a4-110">*MaxNumAnimationSets* \[在\]</span><span class="sxs-lookup"><span data-stu-id="811a4-110">*MaxNumAnimationSets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="811a4-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="811a4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="811a4-112">控制器可支援的動畫組數目上限。</span><span class="sxs-lookup"><span data-stu-id="811a4-112">Maximum number of animation sets the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="811a4-113">*MaxNumTracks* \[在\]</span><span class="sxs-lookup"><span data-stu-id="811a4-113">*MaxNumTracks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="811a4-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="811a4-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="811a4-115">控制器可支援的最大追蹤數目。</span><span class="sxs-lookup"><span data-stu-id="811a4-115">Maximum number of tracks the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="811a4-116">*MaxNumEvents* \[在\]</span><span class="sxs-lookup"><span data-stu-id="811a4-116">*MaxNumEvents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="811a4-117">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="811a4-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="811a4-118">控制器可支援的事件數目上限。</span><span class="sxs-lookup"><span data-stu-id="811a4-118">Maximum number of events the controller can support.</span></span>

</dd> <dt>

<span data-ttu-id="811a4-119">*ppAnimController* \[在\]</span><span class="sxs-lookup"><span data-stu-id="811a4-119">*ppAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="811a4-120">類型： **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="811a4-120">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="811a4-121">複製之 [**ID3DXAnimationController**](id3dxanimationcontroller.md) 動畫控制器指標的位址。</span><span class="sxs-lookup"><span data-stu-id="811a4-121">Address of a pointer to the cloned [**ID3DXAnimationController**](id3dxanimationcontroller.md) animation controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="811a4-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="811a4-122">Return value</span></span>

<span data-ttu-id="811a4-123">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="811a4-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="811a4-124">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="811a4-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="811a4-125">如果方法失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="811a4-125">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="811a4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="811a4-126">Requirements</span></span>



| <span data-ttu-id="811a4-127">需求</span><span class="sxs-lookup"><span data-stu-id="811a4-127">Requirement</span></span> | <span data-ttu-id="811a4-128">值</span><span class="sxs-lookup"><span data-stu-id="811a4-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="811a4-129">標頭</span><span class="sxs-lookup"><span data-stu-id="811a4-129">Header</span></span><br/>  | <dl> <span data-ttu-id="811a4-130"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="811a4-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="811a4-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="811a4-131">Library</span></span><br/> | <dl> <span data-ttu-id="811a4-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="811a4-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="811a4-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="811a4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="811a4-134">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="811a4-134">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
