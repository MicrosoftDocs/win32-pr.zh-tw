---
description: 傳回目前正在執行之優先順序 blend 事件的事件控制碼。
ms.assetid: a7184459-7644-4e65-a8ea-13019889e02b
title: 'ID3DXAnimationController：： GetCurrentPriorityBlend 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df8b52a5bd5267cf88eaf101a0589000099dd600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323295"
---
# <a name="id3dxanimationcontrollergetcurrentpriorityblend-method"></a><span data-ttu-id="e9c07-103">ID3DXAnimationController：： GetCurrentPriorityBlend 方法</span><span class="sxs-lookup"><span data-stu-id="e9c07-103">ID3DXAnimationController::GetCurrentPriorityBlend method</span></span>

<span data-ttu-id="e9c07-104">傳回目前正在執行之優先順序 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="e9c07-104">Returns an event handle to a priority blend event that is currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c07-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9c07-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentPriorityBlend();
```



## <a name="parameters"></a><span data-ttu-id="e9c07-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9c07-106">Parameters</span></span>

<span data-ttu-id="e9c07-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e9c07-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e9c07-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9c07-108">Return value</span></span>

<span data-ttu-id="e9c07-109">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="e9c07-109">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="e9c07-110">目前正在執行之優先權 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="e9c07-110">Event handle to the currently running priority blend event.</span></span> <span data-ttu-id="e9c07-111">如果目前沒有任何優先權 blend 事件正在執行，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="e9c07-111">**NULL** is returned if no priority blend event is currently running.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c07-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9c07-112">Requirements</span></span>



| <span data-ttu-id="e9c07-113">需求</span><span class="sxs-lookup"><span data-stu-id="e9c07-113">Requirement</span></span> | <span data-ttu-id="e9c07-114">值</span><span class="sxs-lookup"><span data-stu-id="e9c07-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c07-115">標頭</span><span class="sxs-lookup"><span data-stu-id="e9c07-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e9c07-116"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9c07-116"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="e9c07-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9c07-117">Library</span></span><br/> | <dl> <span data-ttu-id="e9c07-118"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9c07-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e9c07-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9c07-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9c07-120">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="e9c07-120">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




