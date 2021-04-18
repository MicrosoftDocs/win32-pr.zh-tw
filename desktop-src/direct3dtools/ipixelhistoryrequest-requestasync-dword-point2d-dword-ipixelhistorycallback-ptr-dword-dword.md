---
description: 要求圖元歷程記錄的清單會產生指定的圖元、轉譯目標/UAV 和框架。
MS-HAID: vspixengine.IPixelHistoryRequest\_RequestAsync\_DWORD\_Point2D\_DWORD\_IPixelHistoryCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixelHistoryRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 00A90033-FC57-4BEE-B950-82E678437F2A
api_name:
- IPixelHistoryRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f0209730e0e388b67281451a0337928257c1bae7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510343"
---
# <a name="span-idvspixengineipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dwordspanipixelhistoryrequestrequestasync-method"></a><span data-ttu-id="b4de6-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="b4de6-103"><span id="vspixengine.ipixelhistoryrequest_requestasync_dword_point2d_dword_ipixelhistorycallback_ptr_dword_dword"></span>IPixelHistoryRequest::RequestAsync method</span></span>

<span data-ttu-id="b4de6-104">要求圖元歷程記錄的清單會產生指定的圖元、轉譯目標/UAV 和框架。</span><span class="sxs-lookup"><span data-stu-id="b4de6-104">Requests a list of pixel history results in the specified pixel, render tartget /UAV, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4de6-105">語法</span><span class="sxs-lookup"><span data-stu-id="b4de6-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                   frameNumber,
   Point2D                 pixel,
   DWORD                   renderTargetPtr,
   IPixelHistoryCallback * requestCallback,
   DWORD                   requestCookie,
   DWORD                   progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b4de6-106">參數</span><span class="sxs-lookup"><span data-stu-id="b4de6-106">Parameters</span></span>

<span data-ttu-id="b4de6-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="b4de6-107">*frameNumber* </span></span>  
<span data-ttu-id="b4de6-108">指定的框架。</span><span class="sxs-lookup"><span data-stu-id="b4de6-108">The specified frame.</span></span>

<span data-ttu-id="b4de6-109">*圖元* </span><span class="sxs-lookup"><span data-stu-id="b4de6-109">*pixel* </span></span>  
<span data-ttu-id="b4de6-110">指定的圖元。</span><span class="sxs-lookup"><span data-stu-id="b4de6-110">The specified pixel.</span></span>

<span data-ttu-id="b4de6-111">*renderTargetPtr* </span><span class="sxs-lookup"><span data-stu-id="b4de6-111">*renderTargetPtr* </span></span>  
<span data-ttu-id="b4de6-112">指定的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="b4de6-112">The specified render target.</span></span>

<span data-ttu-id="b4de6-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="b4de6-113">*requestCallback* </span></span>  
<span data-ttu-id="b4de6-114">用來 notifify 結果主機的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="b4de6-114">The address of a callback used to notifify the host of results.</span></span>

<span data-ttu-id="b4de6-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b4de6-115">*requestCookie* </span></span>  
<span data-ttu-id="b4de6-116">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="b4de6-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b4de6-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b4de6-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b4de6-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="b4de6-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4de6-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4de6-119">Return value</span></span>

<span data-ttu-id="b4de6-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b4de6-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b4de6-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b4de6-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4de6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4de6-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b4de6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b4de6-123">Header</span></span></p></td><td><span data-ttu-id="b4de6-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="b4de6-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b4de6-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4de6-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b4de6-126">**IPixelHistoryRequest**</span><span class="sxs-lookup"><span data-stu-id="b4de6-126">**IPixelHistoryRequest**</span></span>](/windows/desktop/direct3dtools/ipixelhistoryrequest)

 

 
