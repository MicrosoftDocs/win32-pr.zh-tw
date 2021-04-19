---
description: 檢查指定的事件控制碼是否有效，以及動畫事件是否尚未完成。
ms.assetid: 242ad1e2-4b04-4ce1-9cdf-f66da9f83f06
title: 'ID3DXAnimationController：： ValidateEvent 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ValidateEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e1a632fa867269f04e8f5f66e6bc352ef1701cd9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992354"
---
# <a name="id3dxanimationcontrollervalidateevent-method"></a><span data-ttu-id="8ed5f-103">ID3DXAnimationController：： ValidateEvent 方法</span><span class="sxs-lookup"><span data-stu-id="8ed5f-103">ID3DXAnimationController::ValidateEvent method</span></span>

<span data-ttu-id="8ed5f-104">檢查指定的事件控制碼是否有效，以及動畫事件是否尚未完成。</span><span class="sxs-lookup"><span data-stu-id="8ed5f-104">Checks whether a specified event handle is valid and the animation event has not yet completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed5f-105">語法</span><span class="sxs-lookup"><span data-stu-id="8ed5f-105">Syntax</span></span>


```C++
HRESULT ValidateEvent(
  [in] D3DXEVENTHANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="8ed5f-106">參數</span><span class="sxs-lookup"><span data-stu-id="8ed5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ed5f-107">*hEvent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ed5f-107">*hEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ed5f-108">類型： **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="8ed5f-108">Type: **[**D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="8ed5f-109">動畫事件的事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="8ed5f-109">Event handle to an animation event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ed5f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ed5f-110">Return value</span></span>

<span data-ttu-id="8ed5f-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ed5f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ed5f-112">\_如果事件控制碼有效且事件尚未完成，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="8ed5f-112">Returns S\_OK if the event handle is valid and the event has not yet completed.</span></span>

<span data-ttu-id="8ed5f-113">\_如果事件控制碼無效及/或事件已完成，則傳回 E 失敗。</span><span class="sxs-lookup"><span data-stu-id="8ed5f-113">Returns E\_FAIL if the event handle is invalid and/or the event has completed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed5f-114">備註</span><span class="sxs-lookup"><span data-stu-id="8ed5f-114">Remarks</span></span>

<span data-ttu-id="8ed5f-115">方法將表示事件控制碼有效，即使事件正在執行，但尚未完成。</span><span class="sxs-lookup"><span data-stu-id="8ed5f-115">The method will indicate that an event handle is valid even if the event is running but has not yet completed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ed5f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ed5f-116">Requirements</span></span>



| <span data-ttu-id="8ed5f-117">需求</span><span class="sxs-lookup"><span data-stu-id="8ed5f-117">Requirement</span></span> | <span data-ttu-id="8ed5f-118">值</span><span class="sxs-lookup"><span data-stu-id="8ed5f-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed5f-119">標頭</span><span class="sxs-lookup"><span data-stu-id="8ed5f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8ed5f-120"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ed5f-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8ed5f-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ed5f-121">Library</span></span><br/> | <dl> <span data-ttu-id="8ed5f-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ed5f-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8ed5f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ed5f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed5f-124">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="8ed5f-124">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 




