---
description: 傳回動畫集合的當地時間範圍內的時間位置。
ms.assetid: d822e1d8-f371-43a1-bbcf-2223e28a200a
title: 'ID3DXAnimationSet：： GetPeriodicPosition 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriodicPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3c4f2e8e57efdfe0681b8ae691e0b5de42624e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323351"
---
# <a name="id3dxanimationsetgetperiodicposition-method"></a><span data-ttu-id="3aa00-103">ID3DXAnimationSet：： GetPeriodicPosition 方法</span><span class="sxs-lookup"><span data-stu-id="3aa00-103">ID3DXAnimationSet::GetPeriodicPosition method</span></span>

<span data-ttu-id="3aa00-104">傳回動畫集合的當地時間範圍內的時間位置。</span><span class="sxs-lookup"><span data-stu-id="3aa00-104">Returns time position in the local timeframe of an animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa00-105">語法</span><span class="sxs-lookup"><span data-stu-id="3aa00-105">Syntax</span></span>


```C++
DOUBLE GetPeriodicPosition(
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="3aa00-106">參數</span><span class="sxs-lookup"><span data-stu-id="3aa00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa00-107">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3aa00-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa00-108">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3aa00-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3aa00-109">動畫集合的本機時間。</span><span class="sxs-lookup"><span data-stu-id="3aa00-109">Local time of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa00-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3aa00-110">Return value</span></span>

<span data-ttu-id="3aa00-111">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3aa00-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3aa00-112">在動畫集的時間範圍內測量的時間位置。</span><span class="sxs-lookup"><span data-stu-id="3aa00-112">Time position as measured in the timeframe of the animation set.</span></span> <span data-ttu-id="3aa00-113">此值將會受動畫集合的期間所限制。</span><span class="sxs-lookup"><span data-stu-id="3aa00-113">This value will be bounded by the period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa00-114">備註</span><span class="sxs-lookup"><span data-stu-id="3aa00-114">Remarks</span></span>

<span data-ttu-id="3aa00-115">這個方法所傳回的時間位置可以用來做為 [**ID3DXAnimationSet：： GetSRT**](id3dxanimationset--getsrt.md)的 PeriodicPosition 參數。</span><span class="sxs-lookup"><span data-stu-id="3aa00-115">The time position returned by this method can be used as the PeriodicPosition parameter of [**ID3DXAnimationSet::GetSRT**](id3dxanimationset--getsrt.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa00-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3aa00-116">Requirements</span></span>



| <span data-ttu-id="3aa00-117">需求</span><span class="sxs-lookup"><span data-stu-id="3aa00-117">Requirement</span></span> | <span data-ttu-id="3aa00-118">值</span><span class="sxs-lookup"><span data-stu-id="3aa00-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa00-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3aa00-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3aa00-120"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="3aa00-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="3aa00-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="3aa00-121">Library</span></span><br/> | <dl> <span data-ttu-id="3aa00-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3aa00-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3aa00-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3aa00-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa00-124">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="3aa00-124">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
