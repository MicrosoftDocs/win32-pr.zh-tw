---
description: 傳回目前在指定動畫播放軌上執行的事件的事件控制碼。
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'ID3DXAnimationController：： GetCurrentTrackEvent 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986532"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a><span data-ttu-id="2494d-103">ID3DXAnimationController：： GetCurrentTrackEvent 方法</span><span class="sxs-lookup"><span data-stu-id="2494d-103">ID3DXAnimationController::GetCurrentTrackEvent method</span></span>

<span data-ttu-id="2494d-104">傳回目前在指定動畫播放軌上執行的事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="2494d-104">Returns an event handle to the event currently running on the specified animation track.</span></span>

## <a name="syntax"></a><span data-ttu-id="2494d-105">語法</span><span class="sxs-lookup"><span data-stu-id="2494d-105">Syntax</span></span>


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a><span data-ttu-id="2494d-106">參數</span><span class="sxs-lookup"><span data-stu-id="2494d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2494d-107">*追蹤* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2494d-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2494d-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2494d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2494d-109">追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="2494d-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2494d-110">*事件* \[ 的在\]</span><span class="sxs-lookup"><span data-stu-id="2494d-110">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2494d-111">類型： **[ **D3DXEVENT \_ 類型**](./d3dxevent-type.md)**</span><span class="sxs-lookup"><span data-stu-id="2494d-111">Type: **[**D3DXEVENT\_TYPE**](./d3dxevent-type.md)**</span></span>

<span data-ttu-id="2494d-112">要查詢的事件種類。</span><span class="sxs-lookup"><span data-stu-id="2494d-112">Type of event to query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2494d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2494d-113">Return value</span></span>

<span data-ttu-id="2494d-114">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="2494d-114">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="2494d-115">目前在指定的追蹤上執行的事件的事件控制碼。如果未在指定的追蹤上執行任何事件，就會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2494d-115">Event handle to the event currently running on the specified track. **NULL** is returned if no event is running on the specified track.</span></span>

## <a name="requirements"></a><span data-ttu-id="2494d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2494d-116">Requirements</span></span>



| <span data-ttu-id="2494d-117">需求</span><span class="sxs-lookup"><span data-stu-id="2494d-117">Requirement</span></span> | <span data-ttu-id="2494d-118">值</span><span class="sxs-lookup"><span data-stu-id="2494d-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2494d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="2494d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2494d-120"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="2494d-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2494d-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="2494d-121">Library</span></span><br/> | <dl> <span data-ttu-id="2494d-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2494d-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2494d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2494d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2494d-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="2494d-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
