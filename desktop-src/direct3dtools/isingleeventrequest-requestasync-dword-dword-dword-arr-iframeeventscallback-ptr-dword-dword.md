---
description: 未使用。
MS-HAID: vspixengine.ISingleEventRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ISingleEventRequest：： RequestAsync 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C85CAF18-6953-4C5D-9491-5F5A5F28C580
api_name:
- ISingleEventRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e6c78a7402082e4ca5222038bd3f5bd63c3cf7b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510041"
---
# <a name="span-idvspixengineisingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspanisingleeventrequestrequestasync-method"></a><span data-ttu-id="1c9c8-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>ISingleEventRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="1c9c8-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>ISingleEventRequest::RequestAsync method</span></span>

<span data-ttu-id="1c9c8-104">未使用。</span><span class="sxs-lookup"><span data-stu-id="1c9c8-104">Not used.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c9c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="1c9c8-105">Syntax</span></span>


```C++
HRESULT RequestAsync(
   DWORD                  eventId,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a><span data-ttu-id="1c9c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="1c9c8-106">Parameters</span></span>

<span data-ttu-id="1c9c8-107">*eventId* </span><span class="sxs-lookup"><span data-stu-id="1c9c8-107">*eventId* </span></span>  
<span data-ttu-id="1c9c8-108">未使用。</span><span class="sxs-lookup"><span data-stu-id="1c9c8-108">Not used.</span></span>

<span data-ttu-id="1c9c8-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="1c9c8-109">*numColumns* </span></span>  
<span data-ttu-id="1c9c8-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="1c9c8-110">Not used.</span></span>

<span data-ttu-id="1c9c8-111">*count1 資料 \_ 行* </span><span class="sxs-lookup"><span data-stu-id="1c9c8-111">*count1\_columns* </span></span>  
<span data-ttu-id="1c9c8-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="1c9c8-112">Not used.</span></span>

<span data-ttu-id="1c9c8-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="1c9c8-113">*requestCallback* </span></span>  
<span data-ttu-id="1c9c8-114">未使用。</span><span class="sxs-lookup"><span data-stu-id="1c9c8-114">Not used.</span></span>

<span data-ttu-id="1c9c8-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="1c9c8-115">*requestCookie* </span></span>  
<span data-ttu-id="1c9c8-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="1c9c8-116">Not used.</span></span>

<span data-ttu-id="1c9c8-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="1c9c8-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="1c9c8-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="1c9c8-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c9c8-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c9c8-119">Return value</span></span>

<span data-ttu-id="1c9c8-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1c9c8-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1c9c8-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1c9c8-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c9c8-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c9c8-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="1c9c8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="1c9c8-123">Header</span></span></p></td><td><span data-ttu-id="1c9c8-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="1c9c8-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="1c9c8-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c9c8-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="1c9c8-126">**ISingleEventRequest**</span><span class="sxs-lookup"><span data-stu-id="1c9c8-126">**ISingleEventRequest**</span></span>](/windows/desktop/direct3dtools/isingleeventrequest)

 

 
