---
title: 'CB_REQUEST_STATUS 列舉 (Cbclient .h) '
description: 指定非同步要求的狀態。
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- CB_REQUEST_STATUS 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317191"
---
# <a name="cb_request_status-enumeration"></a><span data-ttu-id="5ff3c-104">CB \_ 要求 \_ 狀態列舉</span><span class="sxs-lookup"><span data-stu-id="5ff3c-104">CB\_REQUEST\_STATUS enumeration</span></span>

<span data-ttu-id="5ff3c-105">指定非同步要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-105">Specifies the status of an asynchronous request.</span></span> <span data-ttu-id="5ff3c-106">此列舉會搭配 [**IConnectionBrokerRequest：： CheckStatus**](iconnectionbrokerrequest-checkstatus.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-106">This enumeration is used with the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff3c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ff3c-107">Syntax</span></span>


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a><span data-ttu-id="5ff3c-108">常數</span><span class="sxs-lookup"><span data-stu-id="5ff3c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5ff3c-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB \_ 狀態 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="5ff3c-109"><span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**CB\_STATUS\_INVALID**</span></span>
</dt> <dd>

<span data-ttu-id="5ff3c-110">要求物件未初始化。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-110">The request object is not initialized.</span></span>

</dd> <dt>

<span data-ttu-id="5ff3c-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB \_ 狀態 \_ 起始 \_ 要求**</span><span class="sxs-lookup"><span data-stu-id="5ff3c-111"><span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**CB\_STATUS\_INITIATING\_REQUEST**</span></span>
</dt> <dd>

<span data-ttu-id="5ff3c-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5ff3c-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB \_ 狀態 \_ 要求 \_ 已完成**</span><span class="sxs-lookup"><span data-stu-id="5ff3c-113"><span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**CB\_STATUS\_REQUEST\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="5ff3c-114">要求已完成。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-114">The request is complete.</span></span>

</dd> <dt>

<span data-ttu-id="5ff3c-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**CB \_ 狀態 \_ 要求 \_ 失敗**</span><span class="sxs-lookup"><span data-stu-id="5ff3c-115"><span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**CB\_STATUS\_REQUEST\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="5ff3c-116">要求失敗。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-116">The request failed.</span></span>

</dd> <dt>

<span data-ttu-id="5ff3c-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB \_ 狀態 \_ 要求已 \_ 中止**</span><span class="sxs-lookup"><span data-stu-id="5ff3c-117"><span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**CB\_STATUS\_REQUEST\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="5ff3c-118">要求已中止。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-118">The request was aborted.</span></span>

</dd> <dt>

<span data-ttu-id="5ff3c-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB \_ 狀態 \_ 尋找 \_ 目的地**</span><span class="sxs-lookup"><span data-stu-id="5ff3c-119"><span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**CB\_STATUS\_FINDING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="5ff3c-120">未使用。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5ff3c-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB \_ 狀態 \_ 載入 \_ 目的地**</span><span class="sxs-lookup"><span data-stu-id="5ff3c-121"><span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**CB\_STATUS\_LOADING\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="5ff3c-122">未使用。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5ff3c-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB \_ 狀態 \_ 將 \_ 會話 \_ 上線**</span><span class="sxs-lookup"><span data-stu-id="5ff3c-123"><span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**CB\_STATUS\_BRINGING\_SESSION\_ONLINE**</span></span>
</dt> <dd>

<span data-ttu-id="5ff3c-124">未使用。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-124">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5ff3c-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB \_ 狀態重新導向 \_ \_ 至 \_ 目的地**</span><span class="sxs-lookup"><span data-stu-id="5ff3c-125"><span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**CB\_STATUS\_REDIRECTING\_TO\_DESTINATION**</span></span>
</dt> <dd>

<span data-ttu-id="5ff3c-126">未使用。</span><span class="sxs-lookup"><span data-stu-id="5ff3c-126">Not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ff3c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ff3c-127">Requirements</span></span>



| <span data-ttu-id="5ff3c-128">需求</span><span class="sxs-lookup"><span data-stu-id="5ff3c-128">Requirement</span></span> | <span data-ttu-id="5ff3c-129">值</span><span class="sxs-lookup"><span data-stu-id="5ff3c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff3c-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ff3c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5ff3c-131">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5ff3c-131">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="5ff3c-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ff3c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5ff3c-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ff3c-133">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="5ff3c-134">標頭</span><span class="sxs-lookup"><span data-stu-id="5ff3c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ff3c-135"><dt>Cbclient。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ff3c-135"><dt>Cbclient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ff3c-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ff3c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff3c-137">**IConnectionBrokerRequest：： CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="5ff3c-137">**IConnectionBrokerRequest::CheckStatus**</span></span>](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





