---
description: 非同步要求，以取得指定事件) 的呼叫堆疊 Rva (相對虛擬位址。
MS-HAID: vspixengine.ICallStackRequest\_RequestAsync\_EventID\_ICallStackCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ICallStackRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1951716F-5382-41EE-90BB-A9053DB38A78
api_name:
- ICallStackRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cad4007a8bc3d0e7b7c9cf1efc7218ce09813a5a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187492"
---
# <a name="span-idvspixengineicallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dwordspanicallstackrequestrequestasync-method"></a><span data-ttu-id="fe2ed-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>ICallStackRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="fe2ed-103"><span id="vspixengine.icallstackrequest_requestasync_eventid_icallstackcallback_ptr_dword_dword"></span>ICallStackRequest::RequestAsync method</span></span>

<span data-ttu-id="fe2ed-104">非同步要求，以取得指定事件) 的呼叫堆疊 Rva (相對虛擬位址。</span><span class="sxs-lookup"><span data-stu-id="fe2ed-104">An asynchronous request to get the call stack RVAs (relative virtual addresses) of the specified event.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe2ed-105">語法</span><span class="sxs-lookup"><span data-stu-id="fe2ed-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID              eventID,
   ICallStackCallback * requestCallback,
   DWORD                requestCookie,
   DWORD                progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="fe2ed-106">參數</span><span class="sxs-lookup"><span data-stu-id="fe2ed-106">Parameters</span></span>

<span data-ttu-id="fe2ed-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="fe2ed-107">*eventID* </span></span>  
<span data-ttu-id="fe2ed-108">指定的事件。</span><span class="sxs-lookup"><span data-stu-id="fe2ed-108">The specified event.</span></span>

<span data-ttu-id="fe2ed-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="fe2ed-109">*requestCallback* </span></span>  
<span data-ttu-id="fe2ed-110">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="fe2ed-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="fe2ed-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="fe2ed-111">*requestCookie* </span></span>  
<span data-ttu-id="fe2ed-112">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="fe2ed-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="fe2ed-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="fe2ed-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="fe2ed-114">未使用。</span><span class="sxs-lookup"><span data-stu-id="fe2ed-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe2ed-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe2ed-115">Return value</span></span>

<span data-ttu-id="fe2ed-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fe2ed-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fe2ed-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fe2ed-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe2ed-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe2ed-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fe2ed-119">標頭</span><span class="sxs-lookup"><span data-stu-id="fe2ed-119">Header</span></span></p></td><td><span data-ttu-id="fe2ed-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="fe2ed-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="fe2ed-121"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe2ed-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="fe2ed-122">**ICallStackRequest**</span><span class="sxs-lookup"><span data-stu-id="fe2ed-122">**ICallStackRequest**</span></span>](/windows/desktop/direct3dtools/icallstackrequest)

 

 
