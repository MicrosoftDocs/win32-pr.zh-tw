---
description: 取得動畫集。
ms.assetid: 61785f60-82c1-4ddc-b4cd-2e7f665cfe8c
title: 'ID3DXAnimationController：： GetAnimationSet 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c21f073b74d1ab7dac09ddd8bfb3d6be543e122a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116249"
---
# <a name="id3dxanimationcontrollergetanimationset-method"></a><span data-ttu-id="fe02a-103">ID3DXAnimationController：： GetAnimationSet 方法</span><span class="sxs-lookup"><span data-stu-id="fe02a-103">ID3DXAnimationController::GetAnimationSet method</span></span>

<span data-ttu-id="fe02a-104">取得動畫集。</span><span class="sxs-lookup"><span data-stu-id="fe02a-104">Gets an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe02a-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe02a-105">Syntax</span></span>


```C++
HRESULT GetAnimationSet(
  [in]  UINT               Index,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a><span data-ttu-id="fe02a-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe02a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe02a-107">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fe02a-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe02a-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fe02a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fe02a-109">動畫集合的索引。</span><span class="sxs-lookup"><span data-stu-id="fe02a-109">Index of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="fe02a-110">*ppAnimSet* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fe02a-110">*ppAnimSet* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe02a-111">類型： **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe02a-111">Type: **[**LPD3DXANIMATIONSET**](id3dxanimationset.md)\***</span></span>

<span data-ttu-id="fe02a-112">[**ID3DXAnimationSet**](id3dxanimationset.md)動畫集合的指標。</span><span class="sxs-lookup"><span data-stu-id="fe02a-112">Pointer to the [**ID3DXAnimationSet**](id3dxanimationset.md) animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe02a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe02a-113">Return value</span></span>

<span data-ttu-id="fe02a-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe02a-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe02a-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="fe02a-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fe02a-116">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="fe02a-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe02a-117">備註</span><span class="sxs-lookup"><span data-stu-id="fe02a-117">Remarks</span></span>

<span data-ttu-id="fe02a-118">動畫控制器包含動畫集合的陣列。</span><span class="sxs-lookup"><span data-stu-id="fe02a-118">The animation controller contains an array of animation sets.</span></span> <span data-ttu-id="fe02a-119">這個方法會在指定的索引處傳回其中一個。</span><span class="sxs-lookup"><span data-stu-id="fe02a-119">This method returns one of them at the given index.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe02a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe02a-120">Requirements</span></span>



| <span data-ttu-id="fe02a-121">需求</span><span class="sxs-lookup"><span data-stu-id="fe02a-121">Requirement</span></span> | <span data-ttu-id="fe02a-122">值</span><span class="sxs-lookup"><span data-stu-id="fe02a-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe02a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fe02a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fe02a-124"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe02a-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="fe02a-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="fe02a-125">Library</span></span><br/> | <dl> <span data-ttu-id="fe02a-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe02a-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe02a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe02a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe02a-128">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="fe02a-128">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
