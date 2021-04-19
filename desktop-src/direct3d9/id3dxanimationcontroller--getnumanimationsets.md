---
description: 傳回目前在動畫控制器中註冊的動畫集合數目。
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'ID3DXAnimationController：： GetNumAnimationSets 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975649"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a><span data-ttu-id="597fd-103">ID3DXAnimationController：： GetNumAnimationSets 方法</span><span class="sxs-lookup"><span data-stu-id="597fd-103">ID3DXAnimationController::GetNumAnimationSets method</span></span>

<span data-ttu-id="597fd-104">傳回目前在動畫控制器中註冊的動畫集合數目。</span><span class="sxs-lookup"><span data-stu-id="597fd-104">Returns the number of animation sets currently registered in the animation controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="597fd-105">語法</span><span class="sxs-lookup"><span data-stu-id="597fd-105">Syntax</span></span>


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a><span data-ttu-id="597fd-106">參數</span><span class="sxs-lookup"><span data-stu-id="597fd-106">Parameters</span></span>

<span data-ttu-id="597fd-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="597fd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="597fd-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="597fd-108">Return value</span></span>

<span data-ttu-id="597fd-109">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="597fd-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="597fd-110">動畫集合數目。</span><span class="sxs-lookup"><span data-stu-id="597fd-110">Number of animation sets.</span></span>

## <a name="remarks"></a><span data-ttu-id="597fd-111">備註</span><span class="sxs-lookup"><span data-stu-id="597fd-111">Remarks</span></span>

<span data-ttu-id="597fd-112">控制器包含任意數目的動畫集合和追蹤。</span><span class="sxs-lookup"><span data-stu-id="597fd-112">The controller contains any number of animations sets and tracks.</span></span> <span data-ttu-id="597fd-113">您可以使用 [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md)註冊動畫集合。</span><span class="sxs-lookup"><span data-stu-id="597fd-113">Animation sets can be registered with [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md).</span></span> <span data-ttu-id="597fd-114">呼叫 [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) 所建立的動畫控制器會自動註冊已載入的動畫集合。</span><span class="sxs-lookup"><span data-stu-id="597fd-114">An animation controller created by a call to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) will automatically register loaded animation sets.</span></span>

## <a name="requirements"></a><span data-ttu-id="597fd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="597fd-115">Requirements</span></span>



| <span data-ttu-id="597fd-116">需求</span><span class="sxs-lookup"><span data-stu-id="597fd-116">Requirement</span></span> | <span data-ttu-id="597fd-117">值</span><span class="sxs-lookup"><span data-stu-id="597fd-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="597fd-118">標頭</span><span class="sxs-lookup"><span data-stu-id="597fd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="597fd-119"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="597fd-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="597fd-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="597fd-120">Library</span></span><br/> | <dl> <span data-ttu-id="597fd-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="597fd-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="597fd-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="597fd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="597fd-123">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="597fd-123">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
