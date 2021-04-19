---
description: 要求指定之轉譯目標、事件和框架的畫面格緩衝區輸出。
MS-HAID: vspixengine.IFrameBufferRequest\_RequestAsync\_DWORD\_EventID\_DWORD\_IFrameBufferCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameBufferRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 93E9BDFE-3913-4242-A973-7C113B6663FB
api_name:
- IFrameBufferRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 35c50b78486f25051e14ce2811382875e1fab240
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971104"
---
# <a name="span-idvspixengineiframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dwordspaniframebufferrequestrequestasync-method"></a><span data-ttu-id="0b194-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>IFrameBufferRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="0b194-103"><span id="vspixengine.iframebufferrequest_requestasync_dword_eventid_dword_iframebuffercallback_ptr_dword_dword"></span>IFrameBufferRequest::RequestAsync method</span></span>

<span data-ttu-id="0b194-104">要求指定之轉譯目標、事件和框架的畫面格緩衝區輸出。</span><span class="sxs-lookup"><span data-stu-id="0b194-104">Requests framebuffer output of the specified render target, event, and frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b194-105">語法</span><span class="sxs-lookup"><span data-stu-id="0b194-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   EventID                eventID,
   DWORD                  renderTargetIndex,
   IFrameBufferCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="0b194-106">參數</span><span class="sxs-lookup"><span data-stu-id="0b194-106">Parameters</span></span>

<span data-ttu-id="0b194-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="0b194-107">*frameNumber* </span></span>  
<span data-ttu-id="0b194-108">指定的框架。</span><span class="sxs-lookup"><span data-stu-id="0b194-108">The specified frame.</span></span>

<span data-ttu-id="0b194-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="0b194-109">*eventID* </span></span>  
<span data-ttu-id="0b194-110">指定的事件。</span><span class="sxs-lookup"><span data-stu-id="0b194-110">The specified event.</span></span>

<span data-ttu-id="0b194-111">*renderTargetIndex* </span><span class="sxs-lookup"><span data-stu-id="0b194-111">*renderTargetIndex* </span></span>  
<span data-ttu-id="0b194-112">指定之呈現目標的索引。</span><span class="sxs-lookup"><span data-stu-id="0b194-112">The index of the specified render target.</span></span>

<span data-ttu-id="0b194-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="0b194-113">*requestCallback* </span></span>  
<span data-ttu-id="0b194-114">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="0b194-114">The address of a callback used to notify the host of results.</span></span>

<span data-ttu-id="0b194-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="0b194-115">*requestCookie* </span></span>  
<span data-ttu-id="0b194-116">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="0b194-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="0b194-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="0b194-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="0b194-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="0b194-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b194-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b194-119">Return value</span></span>

<span data-ttu-id="0b194-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0b194-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0b194-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0b194-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b194-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b194-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0b194-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0b194-123">Header</span></span></p></td><td><span data-ttu-id="0b194-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="0b194-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="0b194-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b194-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="0b194-126">**IFrameBufferRequest**</span><span class="sxs-lookup"><span data-stu-id="0b194-126">**IFrameBufferRequest**</span></span>](/windows/desktop/direct3dtools/iframebufferrequest)

 

 
