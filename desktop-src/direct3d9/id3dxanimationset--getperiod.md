---
description: 取得動畫集合的期間。
ms.assetid: 0bb19ec1-c918-44b6-83b0-4fdbb4e1a485
title: 'ID3DXAnimationSet：： GetPeriod 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetPeriod
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5f6eafbfe802afc8ff3084c49acf31addca66cef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976526"
---
# <a name="id3dxanimationsetgetperiod-method"></a><span data-ttu-id="4bb46-103">ID3DXAnimationSet：： GetPeriod 方法</span><span class="sxs-lookup"><span data-stu-id="4bb46-103">ID3DXAnimationSet::GetPeriod method</span></span>

<span data-ttu-id="4bb46-104">取得動畫集合的期間。</span><span class="sxs-lookup"><span data-stu-id="4bb46-104">Gets the period of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb46-105">語法</span><span class="sxs-lookup"><span data-stu-id="4bb46-105">Syntax</span></span>


```C++
DOUBLE GetPeriod();
```



## <a name="parameters"></a><span data-ttu-id="4bb46-106">參數</span><span class="sxs-lookup"><span data-stu-id="4bb46-106">Parameters</span></span>

<span data-ttu-id="4bb46-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4bb46-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4bb46-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bb46-108">Return value</span></span>

<span data-ttu-id="4bb46-109">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bb46-109">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bb46-110">動畫集合的期間。</span><span class="sxs-lookup"><span data-stu-id="4bb46-110">Period of the animation set.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bb46-111">備註</span><span class="sxs-lookup"><span data-stu-id="4bb46-111">Remarks</span></span>

<span data-ttu-id="4bb46-112">期間是動畫主要畫面格有效的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="4bb46-112">The period is the range of time that the animation key frames are valid.</span></span> <span data-ttu-id="4bb46-113">在迴圈的動畫中，這是迴圈的期間。</span><span class="sxs-lookup"><span data-stu-id="4bb46-113">For looping animations, this is the period of the loop.</span></span> <span data-ttu-id="4bb46-114">在 (中指定主要畫面格的時間單位（例如，秒) 是由應用程式所決定）。</span><span class="sxs-lookup"><span data-stu-id="4bb46-114">The time units that the key frames are specified in (for example, seconds) is determined by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bb46-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bb46-115">Requirements</span></span>



| <span data-ttu-id="4bb46-116">需求</span><span class="sxs-lookup"><span data-stu-id="4bb46-116">Requirement</span></span> | <span data-ttu-id="4bb46-117">值</span><span class="sxs-lookup"><span data-stu-id="4bb46-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb46-118">標頭</span><span class="sxs-lookup"><span data-stu-id="4bb46-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4bb46-119"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="4bb46-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4bb46-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="4bb46-120">Library</span></span><br/> | <dl> <span data-ttu-id="4bb46-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bb46-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4bb46-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bb46-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb46-123">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="4bb46-123">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
