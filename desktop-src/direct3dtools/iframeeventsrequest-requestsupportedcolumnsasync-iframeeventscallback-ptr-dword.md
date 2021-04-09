---
description: 非同步要求，以取得) 此框架事件要求類型所支援之資料行 (欄位的相關資訊。
MS-HAID: vspixengine.IFrameEventsRequest\_RequestSupportedColumnsAsync\_IFrameEventsCallback\_ptr\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameEventsRequest：： RequestSupportedColumnsAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8F8ED8F7-F764-4CC8-891B-F0582F6B1337
api_name:
- IFrameEventsRequest.RequestSupportedColumnsAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 13d4c797e338f6b0901781760a39511a1f136174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688043"
---
# <a name="span-idvspixengineiframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dwordspaniframeeventsrequestrequestsupportedcolumnsasync-method"></a><span data-ttu-id="b63e6-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>IFrameEventsRequest：： RequestSupportedColumnsAsync 方法</span><span class="sxs-lookup"><span data-stu-id="b63e6-103"><span id="vspixengine.iframeeventsrequest_requestsupportedcolumnsasync_iframeeventscallback_ptr_dword"></span>IFrameEventsRequest::RequestSupportedColumnsAsync method</span></span>

<span data-ttu-id="b63e6-104">非同步要求，以取得) 此框架事件要求類型所支援之資料行 (欄位的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b63e6-104">An asynchronous request to get information about what columns (fields) this frame events request type supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="b63e6-105">語法</span><span class="sxs-lookup"><span data-stu-id="b63e6-105">Syntax</span></span>


```C++
HRESULT RequestSupportedColumnsAsync(
   IFrameEventsCallback * requestCallback,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="b63e6-106">參數</span><span class="sxs-lookup"><span data-stu-id="b63e6-106">Parameters</span></span>

<span data-ttu-id="b63e6-107">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="b63e6-107">*requestCallback* </span></span>  
<span data-ttu-id="b63e6-108">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="b63e6-108">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="b63e6-109">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="b63e6-109">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="b63e6-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="b63e6-110">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="b63e6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b63e6-111">Return value</span></span>

<span data-ttu-id="b63e6-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b63e6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b63e6-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b63e6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b63e6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b63e6-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b63e6-115">標頭</span><span class="sxs-lookup"><span data-stu-id="b63e6-115">Header</span></span></p></td><td><span data-ttu-id="b63e6-116">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="b63e6-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="b63e6-117"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="b63e6-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="b63e6-118">**IFrameEventsRequest**</span><span class="sxs-lookup"><span data-stu-id="b63e6-118">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
