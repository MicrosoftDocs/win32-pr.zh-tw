---
description: 非同步要求，以取得用於指定之框架和事件的階段清單。
MS-HAID: vspixengine.IPipeLineStagesRequest\_RequestSupportedStagesAsync\_DWORD\_EventID\_IPipeLineStagesCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesRequest：： RequestSupportedStagesAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C636FC40-0505-486B-B25D-9B424F5A584D
api_name:
- IPipeLineStagesRequest.RequestSupportedStagesAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0c3ebedee8dba4d7630d1bdff60bdaf479ea3561
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972322"
---
# <a name="span-idvspixengineipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dwordspanipipelinestagesrequestrequestsupportedstagesasync-method"></a><span data-ttu-id="53d7d-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest：： RequestSupportedStagesAsync 方法</span><span class="sxs-lookup"><span data-stu-id="53d7d-103"><span id="vspixengine.ipipelinestagesrequest_requestsupportedstagesasync_dword_eventid_ipipelinestagescallback_ptr_dword_dword"></span>IPipeLineStagesRequest::RequestSupportedStagesAsync method</span></span>

<span data-ttu-id="53d7d-104">非同步要求，以取得用於指定之框架和事件的階段清單。</span><span class="sxs-lookup"><span data-stu-id="53d7d-104">An asynchronous request to get a list of stages used for the specified frame and event.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d7d-105">語法</span><span class="sxs-lookup"><span data-stu-id="53d7d-105">Syntax</span></span>


```C++
HRESULT RequestSupportedStagesAsync(
   DWORD                     frameNumber,
   EventID                   eventID,
   IPipeLineStagesCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="53d7d-106">參數</span><span class="sxs-lookup"><span data-stu-id="53d7d-106">Parameters</span></span>

<span data-ttu-id="53d7d-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="53d7d-107">*frameNumber* </span></span>  
<span data-ttu-id="53d7d-108">指定的框架。</span><span class="sxs-lookup"><span data-stu-id="53d7d-108">The specified frame.</span></span>

<span data-ttu-id="53d7d-109">*eventID* </span><span class="sxs-lookup"><span data-stu-id="53d7d-109">*eventID* </span></span>  
<span data-ttu-id="53d7d-110">指定的事件。</span><span class="sxs-lookup"><span data-stu-id="53d7d-110">The specified event.</span></span>

<span data-ttu-id="53d7d-111">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="53d7d-111">*requestCallback* </span></span>  
<span data-ttu-id="53d7d-112">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="53d7d-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="53d7d-113">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="53d7d-113">*requestCookie* </span></span>  
<span data-ttu-id="53d7d-114">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="53d7d-114">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="53d7d-115">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="53d7d-115">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="53d7d-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="53d7d-116">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="53d7d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="53d7d-117">Return value</span></span>

<span data-ttu-id="53d7d-118">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="53d7d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="53d7d-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="53d7d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d7d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="53d7d-120">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="53d7d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="53d7d-121">Header</span></span></p></td><td><span data-ttu-id="53d7d-122">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="53d7d-122">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="53d7d-123"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="53d7d-123"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="53d7d-124">**IPipeLineStagesRequest**</span><span class="sxs-lookup"><span data-stu-id="53d7d-124">**IPipeLineStagesRequest**</span></span>](/windows/desktop/direct3dtools/ipipelinestagesrequest)

 

 
