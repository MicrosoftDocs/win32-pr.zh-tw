---
description: <span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>ISingleEventRequest：： RequestAsync 方法-未使用。
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
ms.openlocfilehash: 6365614d8a787ea4b252e04ae4e03c4e69ac2283
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107036"
---
# <a name="span-idvspixengineisingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspanisingleeventrequestrequestasync-method"></a><span data-ttu-id="28ec0-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>ISingleEventRequest：： RequestAsync 方法</span><span class="sxs-lookup"><span data-stu-id="28ec0-103"><span id="vspixengine.isingleeventrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>ISingleEventRequest::RequestAsync method</span></span>

<span data-ttu-id="28ec0-104">未使用。</span><span class="sxs-lookup"><span data-stu-id="28ec0-104">Not used.</span></span>

## <a name="syntax"></a><span data-ttu-id="28ec0-105">語法</span><span class="sxs-lookup"><span data-stu-id="28ec0-105">Syntax</span></span>


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

## <a name="parameters"></a><span data-ttu-id="28ec0-106">參數</span><span class="sxs-lookup"><span data-stu-id="28ec0-106">Parameters</span></span>

<span data-ttu-id="28ec0-107">*eventId* </span><span class="sxs-lookup"><span data-stu-id="28ec0-107">*eventId* </span></span>  
<span data-ttu-id="28ec0-108">未使用。</span><span class="sxs-lookup"><span data-stu-id="28ec0-108">Not used.</span></span>

<span data-ttu-id="28ec0-109">*numColumns* </span><span class="sxs-lookup"><span data-stu-id="28ec0-109">*numColumns* </span></span>  
<span data-ttu-id="28ec0-110">未使用。</span><span class="sxs-lookup"><span data-stu-id="28ec0-110">Not used.</span></span>

<span data-ttu-id="28ec0-111">*count1 資料 \_ 行* </span><span class="sxs-lookup"><span data-stu-id="28ec0-111">*count1\_columns* </span></span>  
<span data-ttu-id="28ec0-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="28ec0-112">Not used.</span></span>

<span data-ttu-id="28ec0-113">*requestCallback* </span><span class="sxs-lookup"><span data-stu-id="28ec0-113">*requestCallback* </span></span>  
<span data-ttu-id="28ec0-114">未使用。</span><span class="sxs-lookup"><span data-stu-id="28ec0-114">Not used.</span></span>

<span data-ttu-id="28ec0-115">*requestCookie* </span><span class="sxs-lookup"><span data-stu-id="28ec0-115">*requestCookie* </span></span>  
<span data-ttu-id="28ec0-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="28ec0-116">Not used.</span></span>

<span data-ttu-id="28ec0-117">*progressIntervalMsecs* </span><span class="sxs-lookup"><span data-stu-id="28ec0-117">*progressIntervalMsecs* </span></span>  
<span data-ttu-id="28ec0-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="28ec0-118">Not used.</span></span>

## <a name="return-value"></a><span data-ttu-id="28ec0-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="28ec0-119">Return value</span></span>

<span data-ttu-id="28ec0-120">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="28ec0-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28ec0-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="28ec0-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="28ec0-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="28ec0-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="28ec0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="28ec0-123">Header</span></span></p></td><td><span data-ttu-id="28ec0-124">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="28ec0-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="28ec0-125"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="28ec0-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="28ec0-126">**ISingleEventRequest**</span><span class="sxs-lookup"><span data-stu-id="28ec0-126">**ISingleEventRequest**</span></span>](/windows/desktop/direct3dtools/isingleeventrequest)

 

 
