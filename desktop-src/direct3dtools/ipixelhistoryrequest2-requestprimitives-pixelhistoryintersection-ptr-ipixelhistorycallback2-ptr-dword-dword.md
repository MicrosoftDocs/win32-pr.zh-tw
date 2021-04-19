---
description: 要求特定交集的基本欄表。 如需詳細資訊，請參閱 RequestIntersections 成員函式。
MS-HAID: vspixengine.IPixelHistoryRequest2\_RequestPrimitives\_PixelHistoryIntersection\_ptr\_IPixelHistoryCallback2\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryRequest2：： RequestPrimitives 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CFEB833C-1747-4153-A691-7529AA3F4095
api_name:
- IPixelHistoryRequest2.RequestPrimitives
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 71b248f86e20e560238a1c59b1a0199f285493a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106998425"
---
# <a name="span-idvspixengineipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dwordspanipixelhistoryrequest2requestprimitives-method"></a><span data-ttu-id="e56fe-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2：： RequestPrimitives 方法</span><span class="sxs-lookup"><span data-stu-id="e56fe-104"><span id="vspixengine.ipixelhistoryrequest2_requestprimitives_pixelhistoryintersection_ptr_ipixelhistorycallback2_ptr_dword_dword"></span>IPixelHistoryRequest2::RequestPrimitives method</span></span>

<span data-ttu-id="e56fe-105">要求特定交集的基本欄表。</span><span class="sxs-lookup"><span data-stu-id="e56fe-105">Requests a list of primitives from a particular intersection.</span></span> <span data-ttu-id="e56fe-106">如需詳細資訊，請參閱 RequestIntersections 成員函式。</span><span class="sxs-lookup"><span data-stu-id="e56fe-106">For more information, see the RequestIntersections member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e56fe-107">語法</span><span class="sxs-lookup"><span data-stu-id="e56fe-107">Syntax</span></span>


```C++
HRESULT RequestPrimitives(
   PixelHistoryIntersection * intersection,
   IPixelHistoryCallback2 *   requestCallback,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="e56fe-108">參數</span><span class="sxs-lookup"><span data-stu-id="e56fe-108">Parameters</span></span>

<span data-ttu-id="e56fe-109">*交叉 口* </span><span class="sxs-lookup"><span data-stu-id="e56fe-109">*intersection* </span></span>  
<span data-ttu-id="e56fe-110">指定之交集的位址。</span><span class="sxs-lookup"><span data-stu-id="e56fe-110">The address of the specified intersection.</span></span>

<span data-ttu-id="e56fe-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="e56fe-111">*requestCallback* </span></span>  
<span data-ttu-id="e56fe-112">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="e56fe-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="e56fe-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="e56fe-113">*requestCookie* </span></span>  
<span data-ttu-id="e56fe-114">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="e56fe-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="e56fe-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="e56fe-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="e56fe-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="e56fe-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="e56fe-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="e56fe-117">Return value</span></span>

<span data-ttu-id="e56fe-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e56fe-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e56fe-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e56fe-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e56fe-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e56fe-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e56fe-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e56fe-121">Header</span></span></p></td><td><span data-ttu-id="e56fe-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="e56fe-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="e56fe-123"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="e56fe-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="e56fe-124">**IPixelHistoryRequest2**</span><span class="sxs-lookup"><span data-stu-id="e56fe-124">**IPixelHistoryRequest2**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest2)

 

 
