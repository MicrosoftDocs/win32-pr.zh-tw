---
description: 傳回已排定在指定事件之後發生之下一個優先權 blend 事件的事件控制碼。
ms.assetid: 64fa6fca-dc4a-4534-ab8e-b11b3c7ed23c
title: 'ID3DXAnimationController：： GetUpcomingPriorityBlend 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetUpcomingPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 72f9b8854041094d43d9e8250ab61b5f59a67848
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386422"
---
# <a name="id3dxanimationcontrollergetupcomingpriorityblend-method"></a><span data-ttu-id="90bf5-103">ID3DXAnimationController：： GetUpcomingPriorityBlend 方法</span><span class="sxs-lookup"><span data-stu-id="90bf5-103">ID3DXAnimationController::GetUpcomingPriorityBlend method</span></span>

<span data-ttu-id="90bf5-104">傳回已排定在指定事件之後發生之下一個優先權 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="90bf5-104">Returns an event handle to the next priority blend event scheduled to occur after a specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="90bf5-105">語法</span><span class="sxs-lookup"><span data-stu-id="90bf5-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetUpcomingPriorityBlend(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="90bf5-106">參數</span><span class="sxs-lookup"><span data-stu-id="90bf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90bf5-107">*hEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90bf5-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90bf5-108">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="90bf5-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="90bf5-109">指定事件的事件控制碼，之後會在此搜尋下列優先權 blend 事件。</span><span class="sxs-lookup"><span data-stu-id="90bf5-109">Event handle to a specified event after which to search for a following priority blend event.</span></span> <span data-ttu-id="90bf5-110">如果設定為 **Null**，則方法會傳回下一個排程的 priority blend 事件。</span><span class="sxs-lookup"><span data-stu-id="90bf5-110">If set to **NULL**, then the method will return the next scheduled priority blend event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90bf5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="90bf5-111">Return value</span></span>

<span data-ttu-id="90bf5-112">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="90bf5-112">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="90bf5-113">下一個排程優先權 blend 事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="90bf5-113">Event handle to the next scheduled priority blend event.</span></span> <span data-ttu-id="90bf5-114">如果未排定新的優先權 blend 事件，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="90bf5-114">**NULL** is returned if no new priority blend event is scheduled.</span></span>

## <a name="remarks"></a><span data-ttu-id="90bf5-115">備註</span><span class="sxs-lookup"><span data-stu-id="90bf5-115">Remarks</span></span>

<span data-ttu-id="90bf5-116">您可以重複傳遞 **Null** 來 hEvent，以反復使用這個方法來尋找所需的優先順序 blend 事件。</span><span class="sxs-lookup"><span data-stu-id="90bf5-116">This method can be used iteratively to locate a desired priority blend event by repeatedly passing in **NULL** for hEvent.</span></span>

> [!Note]  
> <span data-ttu-id="90bf5-117">當方法傳回 **Null** 之後，請勿再逐一查看。</span><span class="sxs-lookup"><span data-stu-id="90bf5-117">Do not iterate further after the method has returned **NULL**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="90bf5-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="90bf5-118">Requirements</span></span>



| <span data-ttu-id="90bf5-119">需求</span><span class="sxs-lookup"><span data-stu-id="90bf5-119">Requirement</span></span> | <span data-ttu-id="90bf5-120">值</span><span class="sxs-lookup"><span data-stu-id="90bf5-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90bf5-121">標頭</span><span class="sxs-lookup"><span data-stu-id="90bf5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="90bf5-122"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="90bf5-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="90bf5-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="90bf5-123">Library</span></span><br/> | <dl> <span data-ttu-id="90bf5-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="90bf5-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="90bf5-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90bf5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90bf5-126">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="90bf5-126">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




