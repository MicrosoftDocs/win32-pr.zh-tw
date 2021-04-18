---
description: 要求會導致指定圖元、轉譯目標/UAV 和框架變更的事件清單。
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestIntersections\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryRequest2：： RequestIntersections 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8E47935-DFA1-4A76-9D0A-3DF5833A1249
api_name:
- IPixelHistoryRequest2.RequestIntersections
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 56f8da17ca492ca15ca51676ae4f1e1654c6f41f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510050"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestintersections-method"></a><span data-ttu-id="4fbd0-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2：： RequestIntersections 方法</span><span class="sxs-lookup"><span data-stu-id="4fbd0-103"><span id="vspixengine.ipixelhistoryrequest2_requestintersections_dword_point2d_dword_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestIntersections method</span></span>

<span data-ttu-id="4fbd0-104">要求會導致指定圖元、轉譯目標/UAV 和框架變更的事件清單。</span><span class="sxs-lookup"><span data-stu-id="4fbd0-104">Requests a list of events that cause a change in the specified pixel, render target / UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbd0-105">語法</span><span class="sxs-lookup"><span data-stu-id="4fbd0-105">Syntax</span></span>


```C++
HRESULT RequestIntersections(
   DWORD                    frameNumber,
   Point2D                  pixel,
   DWORD                    renderTargetPtr,
   IPixelHistoryCallback2 * requestCallback,
   DWORD                    requestCookie,
   DWORD                    progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="4fbd0-106">參數</span><span class="sxs-lookup"><span data-stu-id="4fbd0-106">Parameters</span></span>

<span data-ttu-id="4fbd0-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="4fbd0-107">*frameNumber* </span></span>  
<span data-ttu-id="4fbd0-108">指定的框架。</span><span class="sxs-lookup"><span data-stu-id="4fbd0-108">The specified frame.</span></span>

<span data-ttu-id="4fbd0-109">*圖元* </span><span class="sxs-lookup"><span data-stu-id="4fbd0-109">*pixel* </span></span>  
<span data-ttu-id="4fbd0-110">指定的圖元。</span><span class="sxs-lookup"><span data-stu-id="4fbd0-110">The specified pixel.</span></span>

<span data-ttu-id="4fbd0-111">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="4fbd0-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="4fbd0-112">指定之轉譯目標的位址</span><span class="sxs-lookup"><span data-stu-id="4fbd0-112">The address of the specified render target</span></span>

<span data-ttu-id="4fbd0-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="4fbd0-113">*requestCallback* </span></span>  
<span data-ttu-id="4fbd0-114">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="4fbd0-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="4fbd0-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="4fbd0-115">*requestCookie* </span></span>  
<span data-ttu-id="4fbd0-116">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="4fbd0-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="4fbd0-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="4fbd0-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="4fbd0-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="4fbd0-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="4fbd0-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="4fbd0-119">Return value</span></span>

<span data-ttu-id="4fbd0-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4fbd0-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4fbd0-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4fbd0-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fbd0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fbd0-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="4fbd0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="4fbd0-123">Header</span></span></p></td><td><span data-ttu-id="4fbd0-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="4fbd0-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="4fbd0-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="4fbd0-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="4fbd0-126">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="4fbd0-126">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
