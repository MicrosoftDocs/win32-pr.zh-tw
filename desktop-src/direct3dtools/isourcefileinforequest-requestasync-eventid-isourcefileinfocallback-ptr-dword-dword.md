---
description: 非同步要求，以取得與事件呼叫堆疊相關聯的原始程式檔。
MS-HAID: vspixengine.ISourceFileInfoRequest\_RequestAsync\_EventID\_ISourceFileInfoCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISourceFileInfoRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 257361ED-7400-4320-8433-59A9A07E69E4
api_name:
- ISourceFileInfoRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba5fddf153b2a771ab54bf89036f8087ad0f7524
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973364"
---
# <a name="span-idvspixengineisourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dwordspanisourcefileinforequestrequestasync-method"></a><span data-ttu-id="f3d69-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>ISourceFileInfoRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="f3d69-103"><span id="vspixengine.isourcefileinforequest_requestasync_eventid_isourcefileinfocallback_ptr_dword_dword"></span>ISourceFileInfoRequest::RequestAsync method</span></span>

<span data-ttu-id="f3d69-104">非同步要求，以取得與事件呼叫堆疊相關聯的原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="f3d69-104">An asynchronous request to get the source files associated with the callstack of an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3d69-105">語法</span><span class="sxs-lookup"><span data-stu-id="f3d69-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   EventID                   eventID,
   ISourceFileInfoCallback * requestCallback,
   DWORD                     requestCookie,
   DWORD                     progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="f3d69-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3d69-106">Parameters</span></span>

<span data-ttu-id="f3d69-107">*eventID* </span><span class="sxs-lookup"><span data-stu-id="f3d69-107">*eventID* </span></span>  
<span data-ttu-id="f3d69-108">指定的事件。</span><span class="sxs-lookup"><span data-stu-id="f3d69-108">The specified event.</span></span>

<span data-ttu-id="f3d69-109">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="f3d69-109">*requestCallback* </span></span>  
<span data-ttu-id="f3d69-110">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="f3d69-110">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="f3d69-111">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="f3d69-111">*requestCookie* </span></span>  
<span data-ttu-id="f3d69-112">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="f3d69-112">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="f3d69-113">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="f3d69-113">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="f3d69-114">未使用。</span><span class="sxs-lookup"><span data-stu-id="f3d69-114">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3d69-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3d69-115">Return value</span></span>

<span data-ttu-id="f3d69-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f3d69-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f3d69-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f3d69-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3d69-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3d69-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f3d69-119">標頭</span><span class="sxs-lookup"><span data-stu-id="f3d69-119">Header</span></span></p></td><td><span data-ttu-id="f3d69-120">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="f3d69-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="f3d69-121"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3d69-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="f3d69-122">**ISourceFileInfoRequest**</span><span class="sxs-lookup"><span data-stu-id="f3d69-122">**ISourceFileInfoRequest**</span></span>](/windows/desktop/direct3dtools/isourcefileinforequest)

 

 
