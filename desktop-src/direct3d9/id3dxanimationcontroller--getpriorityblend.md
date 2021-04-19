---
description: 取得動畫控制器所使用的目前優先權混合權數。
ms.assetid: ceaf611e-e85b-4958-b8ac-7e60b98b1aad
title: 'ID3DXAnimationController：： GetPriorityBlend 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c27e4c6d2cc706b30f2be99030e7bb4a5bccf209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982033"
---
# <a name="id3dxanimationcontrollergetpriorityblend-method"></a><span data-ttu-id="7eeee-103">ID3DXAnimationController：： GetPriorityBlend 方法</span><span class="sxs-lookup"><span data-stu-id="7eeee-103">ID3DXAnimationController::GetPriorityBlend method</span></span>

<span data-ttu-id="7eeee-104">取得動畫控制器所使用的目前優先權混合權數。</span><span class="sxs-lookup"><span data-stu-id="7eeee-104">Gets the current priority blending weight used by the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eeee-105">語法</span><span class="sxs-lookup"><span data-stu-id="7eeee-105">Syntax</span></span>


```C++
FLOAT GetPriorityBlend();
```



## <a name="parameters"></a><span data-ttu-id="7eeee-106">參數</span><span class="sxs-lookup"><span data-stu-id="7eeee-106">Parameters</span></span>

<span data-ttu-id="7eeee-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="7eeee-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7eeee-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7eeee-108">Return value</span></span>

<span data-ttu-id="7eeee-109">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7eeee-109">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7eeee-110">傳回目前的優先順序混合加權。</span><span class="sxs-lookup"><span data-stu-id="7eeee-110">Returns the current priority blending weight.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eeee-111">備註</span><span class="sxs-lookup"><span data-stu-id="7eeee-111">Remarks</span></span>

<span data-ttu-id="7eeee-112">優先權混合權數可用來將高優先順序和低優先順序的追蹤結合在一起。</span><span class="sxs-lookup"><span data-stu-id="7eeee-112">The priority blending weight is used to blend high and low priority tracks together.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eeee-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7eeee-113">Requirements</span></span>



| <span data-ttu-id="7eeee-114">需求</span><span class="sxs-lookup"><span data-stu-id="7eeee-114">Requirement</span></span> | <span data-ttu-id="7eeee-115">值</span><span class="sxs-lookup"><span data-stu-id="7eeee-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeee-116">標頭</span><span class="sxs-lookup"><span data-stu-id="7eeee-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7eeee-117"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="7eeee-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="7eeee-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="7eeee-118">Library</span></span><br/> | <dl> <span data-ttu-id="7eeee-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7eeee-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7eeee-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7eeee-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eeee-121">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="7eeee-121">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> <dt>

[<span data-ttu-id="7eeee-122">**SetPriorityBlend**</span><span class="sxs-lookup"><span data-stu-id="7eeee-122">**SetPriorityBlend**</span></span>](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
