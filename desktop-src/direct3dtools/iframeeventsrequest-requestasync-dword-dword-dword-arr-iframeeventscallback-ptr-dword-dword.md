---
description: 非同步要求，以取得單一指定框架的指定資訊。
MS-HAID: vspixengine.IFrameEventsRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameEventsRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 821E7674-A960-46F6-A7AF-386298902ED6
api_name:
- IFrameEventsRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a001f6a29d17806271ca4f5d29dc80d6e36251bf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108829"
---
# <a name="span-idvspixengineiframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspaniframeeventsrequestrequestasync-method"></a><span data-ttu-id="d9685-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="d9685-103"><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest::RequestAsync method</span></span>

<span data-ttu-id="d9685-104">非同步要求，以取得單一指定框架的指定資訊。</span><span class="sxs-lookup"><span data-stu-id="d9685-104">An asynchronous request to get specified information about a single specified frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9685-105">語法</span><span class="sxs-lookup"><span data-stu-id="d9685-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="d9685-106">參數</span><span class="sxs-lookup"><span data-stu-id="d9685-106">Parameters</span></span>

<span data-ttu-id="d9685-107">*frameNumber* </span><span class="sxs-lookup"><span data-stu-id="d9685-107">*frameNumber* </span></span>  
<span data-ttu-id="d9685-108">指定的框架。</span><span class="sxs-lookup"><span data-stu-id="d9685-108">The specified frame.</span></span>

<span data-ttu-id="d9685-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="d9685-109">*numColumns* </span></span>  
<span data-ttu-id="d9685-110">指定的資料行 (欄位) 。</span><span class="sxs-lookup"><span data-stu-id="d9685-110">The specified columns (fields).</span></span>

<span data-ttu-id="d9685-111">*count1 資料 \_ 行* </span><span class="sxs-lookup"><span data-stu-id="d9685-111">*count1\_columns* </span></span>  
<span data-ttu-id="d9685-112">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="d9685-112">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="d9685-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="d9685-113">*requestCallback* </span></span>  
<span data-ttu-id="d9685-114">用來通知主機結果的回呼位址。</span><span class="sxs-lookup"><span data-stu-id="d9685-114">The address of callback used to notify the host of results.</span></span>

<span data-ttu-id="d9685-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="d9685-115">*requestCookie* </span></span>  
<span data-ttu-id="d9685-116">可唯一識別要求的 cookie，而且可用來指示它被取消。</span><span class="sxs-lookup"><span data-stu-id="d9685-116">A cookie that uniquely identifies the request, and can be used to signal for it to be cancelled.</span></span>

<span data-ttu-id="d9685-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="d9685-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="d9685-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="d9685-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9685-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9685-119">Return value</span></span>

<span data-ttu-id="d9685-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d9685-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9685-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d9685-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9685-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9685-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="d9685-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d9685-123">Header</span></span></p></td><td><span data-ttu-id="d9685-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="d9685-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="d9685-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9685-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="d9685-126">**IFrameEventsRequest**</span><span class="sxs-lookup"><span data-stu-id="d9685-126">**IFrameEventsRequest**</span></span>](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
