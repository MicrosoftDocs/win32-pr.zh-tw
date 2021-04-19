---
description: 取得全域動畫時間。
ms.assetid: a46e2a57-a76a-4d79-a3b6-30b242321ed2
title: 'ID3DXAnimationController：： GetTime 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2bfc3c2c1d5bb0bbbb3c364b47f22f0790f8d102
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997407"
---
# <a name="id3dxanimationcontrollergettime-method"></a><span data-ttu-id="05d39-103">ID3DXAnimationController：： GetTime 方法</span><span class="sxs-lookup"><span data-stu-id="05d39-103">ID3DXAnimationController::GetTime method</span></span>

<span data-ttu-id="05d39-104">取得全域動畫時間。</span><span class="sxs-lookup"><span data-stu-id="05d39-104">Gets the global animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d39-105">語法</span><span class="sxs-lookup"><span data-stu-id="05d39-105">Syntax</span></span>


```C++
DOUBLE GetTime();
```



## <a name="parameters"></a><span data-ttu-id="05d39-106">參數</span><span class="sxs-lookup"><span data-stu-id="05d39-106">Parameters</span></span>

<span data-ttu-id="05d39-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="05d39-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05d39-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="05d39-108">Return value</span></span>

<span data-ttu-id="05d39-109">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="05d39-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="05d39-110">傳回全域動畫時間。</span><span class="sxs-lookup"><span data-stu-id="05d39-110">Returns the global animation time.</span></span>

## <a name="remarks"></a><span data-ttu-id="05d39-111">備註</span><span class="sxs-lookup"><span data-stu-id="05d39-111">Remarks</span></span>

<span data-ttu-id="05d39-112">動畫的設計是使用本機動畫時間，並使用 [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)混合到全球時間。</span><span class="sxs-lookup"><span data-stu-id="05d39-112">Animations are designed using a local animation time and mixed into global time with [**AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="05d39-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="05d39-113">Requirements</span></span>



| <span data-ttu-id="05d39-114">需求</span><span class="sxs-lookup"><span data-stu-id="05d39-114">Requirement</span></span> | <span data-ttu-id="05d39-115">值</span><span class="sxs-lookup"><span data-stu-id="05d39-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="05d39-116">標頭</span><span class="sxs-lookup"><span data-stu-id="05d39-116">Header</span></span><br/>  | <dl> <span data-ttu-id="05d39-117"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="05d39-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="05d39-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="05d39-118">Library</span></span><br/> | <dl> <span data-ttu-id="05d39-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="05d39-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="05d39-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05d39-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d39-121">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="05d39-121">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
