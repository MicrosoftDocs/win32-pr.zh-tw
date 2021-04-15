---
description: 非同步要求，以取得是否針對指定的框架和事件使用計算著色器階段。
MS-HAID: vspixengine.IPipeLineStagesRequest2\_RequestComputeShaderStageAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesRequest2：： RequestComputeShaderStageAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EC5695A6-70B5-4F7D-A235-974A0A59A44F
api_name:
- IPipeLineStagesRequest2.RequestComputeShaderStageAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ec7fe36a35e73ae2d047be11a2d5cf72f65825f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467767"
---
# <a name="span-idvspixengineipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequest2requestcomputeshaderstageasync-method"></a><span data-ttu-id="b536c-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest2：： RequestComputeShaderStageAsync 方法</span><span class="sxs-lookup"><span data-stu-id="b536c-103"><span id="vspixengine.ipipelinestagesrequest2_requestcomputeshaderstageasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest2::RequestComputeShaderStageAsync method</span></span>

<span data-ttu-id="b536c-104">非同步要求，以取得是否針對指定的框架和事件使用計算著色器階段。</span><span class="sxs-lookup"><span data-stu-id="b536c-104">An asynchronous request to get whether the compute shader stage was used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="b536c-105">語法</span><span class="sxs-lookup"><span data-stu-id="b536c-105">Syntax</span></span>


```C++
HRESULT RequestComputeShaderStageAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b536c-106">參數</span><span class="sxs-lookup"><span data-stu-id="b536c-106">Parameters</span></span>

<span data-ttu-id="b536c-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="b536c-107">*frameNumber* </span></span>  
<span data-ttu-id="b536c-108">指定的框架。</span><span class="sxs-lookup"><span data-stu-id="b536c-108">The specified frame.</span></span>

<span data-ttu-id="b536c-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="b536c-109">*eventID* </span></span>  
<span data-ttu-id="b536c-110">指定的事件。</span><span class="sxs-lookup"><span data-stu-id="b536c-110">The specified event.</span></span>

<span data-ttu-id="b536c-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="b536c-111">*requestCallback* </span></span>  
<span data-ttu-id="b536c-112">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="b536c-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="b536c-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="b536c-113">*requestCookie* </span></span>  
<span data-ttu-id="b536c-114">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="b536c-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="b536c-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b536c-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b536c-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="b536c-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b536c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="b536c-117">Return value</span></span>

<span data-ttu-id="b536c-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b536c-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b536c-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b536c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b536c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b536c-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b536c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b536c-121">Header</span></span></p></td><td><span data-ttu-id="b536c-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="b536c-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b536c-123"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="b536c-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b536c-124">**IPipeLineStagesRequest2**</span><span class="sxs-lookup"><span data-stu-id="b536c-124">**IPipeLineStagesRequest2**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest2)

 

 
