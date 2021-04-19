---
description: Get \_ StopTime 方法會取得 NTP (網路時間通訊協定) 結束時間值。 如果結束時間為零，則不會限制會話。
ms.assetid: f18042c0-e41d-43b3-a75d-6ab161afde6e
title: 'ITTime：： get_StopTime 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b55ac03c4701884b5a4b7716cb2758887b6160bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977170"
---
# <a name="ittimeget_stoptime-method"></a><span data-ttu-id="89921-104">ITTime：： get \_ StopTime 方法</span><span class="sxs-lookup"><span data-stu-id="89921-104">ITTime::get\_StopTime method</span></span>

<span data-ttu-id="89921-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="89921-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="89921-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="89921-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="89921-107">**Get \_ StopTime** 方法會取得 NTP (網路時間通訊協定) 結束時間值。</span><span class="sxs-lookup"><span data-stu-id="89921-107">The **get\_StopTime** method gets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="89921-108">如果結束時間為零，則不會限制會話。</span><span class="sxs-lookup"><span data-stu-id="89921-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="89921-109">語法</span><span class="sxs-lookup"><span data-stu-id="89921-109">Syntax</span></span>


```C++
HRESULT get_StopTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="89921-110">參數</span><span class="sxs-lookup"><span data-stu-id="89921-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89921-111">*pTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="89921-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89921-112">會話停止時間的指標。</span><span class="sxs-lookup"><span data-stu-id="89921-112">Pointer to the stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89921-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="89921-113">Return value</span></span>

<span data-ttu-id="89921-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="89921-114">This method can return one of these values.</span></span>



| <span data-ttu-id="89921-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="89921-115">Return code</span></span>                                                                                   | <span data-ttu-id="89921-116">Description</span><span class="sxs-lookup"><span data-stu-id="89921-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="89921-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="89921-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="89921-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="89921-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="89921-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="89921-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="89921-120">*PTime* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="89921-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="89921-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="89921-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="89921-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="89921-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="89921-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="89921-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="89921-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="89921-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="89921-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="89921-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="89921-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="89921-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="89921-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="89921-127">Requirements</span></span>



| <span data-ttu-id="89921-128">需求</span><span class="sxs-lookup"><span data-stu-id="89921-128">Requirement</span></span> | <span data-ttu-id="89921-129">值</span><span class="sxs-lookup"><span data-stu-id="89921-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89921-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="89921-130">TAPI version</span></span><br/> | <span data-ttu-id="89921-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="89921-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="89921-132">標頭</span><span class="sxs-lookup"><span data-stu-id="89921-132">Header</span></span><br/>       | <dl> <span data-ttu-id="89921-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="89921-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="89921-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="89921-134">Library</span></span><br/>      | <dl> <span data-ttu-id="89921-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="89921-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="89921-136">DLL</span><span class="sxs-lookup"><span data-stu-id="89921-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="89921-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89921-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89921-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89921-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89921-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="89921-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="89921-140">**ITTime：:p 的 \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="89921-140">**ITTime::put\_StopTime**</span></span>](ittime-put-stoptime.md)
</dt> </dl>

 

 




