---
description: Put \_ StopTime 方法會將 NTP (網路時間通訊協定) 結束時間值。 如果結束時間為零，則不會限制會話。
ms.assetid: 6f07054c-5fb2-4ee4-9025-3acf9b51ddbd
title: 'ITTime：:p ut_StopTime 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53446ea1d7ee93589987c42b005d7a84e7e728ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978660"
---
# <a name="ittimeput_stoptime-method"></a><span data-ttu-id="d0352-104">ITTime：:p 的 \_ StopTime 方法</span><span class="sxs-lookup"><span data-stu-id="d0352-104">ITTime::put\_StopTime method</span></span>

<span data-ttu-id="d0352-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="d0352-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d0352-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="d0352-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d0352-107">**Put \_ StopTime** 方法會將 NTP (網路時間通訊協定) 結束時間值。</span><span class="sxs-lookup"><span data-stu-id="d0352-107">The **put\_StopTime** method sets the NTP (Network Time Protocol) ending time value.</span></span> <span data-ttu-id="d0352-108">如果結束時間為零，則不會限制會話。</span><span class="sxs-lookup"><span data-stu-id="d0352-108">If the end time is zero, the session is not bounded.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0352-109">語法</span><span class="sxs-lookup"><span data-stu-id="d0352-109">Syntax</span></span>


```C++
HRESULT put_StopTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="d0352-110">參數</span><span class="sxs-lookup"><span data-stu-id="d0352-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0352-111">*時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0352-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0352-112">會話的停止時間。</span><span class="sxs-lookup"><span data-stu-id="d0352-112">Stop time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0352-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0352-113">Return value</span></span>

<span data-ttu-id="d0352-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d0352-114">This method can return one of these values.</span></span>



| <span data-ttu-id="d0352-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d0352-115">Return code</span></span>                                                                                   | <span data-ttu-id="d0352-116">Description</span><span class="sxs-lookup"><span data-stu-id="d0352-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d0352-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d0352-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d0352-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="d0352-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d0352-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d0352-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d0352-120">*Time* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="d0352-120">The *Time* parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="d0352-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d0352-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d0352-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="d0352-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="d0352-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="d0352-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d0352-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d0352-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="d0352-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d0352-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d0352-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="d0352-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="d0352-127">備註</span><span class="sxs-lookup"><span data-stu-id="d0352-127">Remarks</span></span>

<span data-ttu-id="d0352-128">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="d0352-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="d0352-129">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="d0352-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0352-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0352-130">Requirements</span></span>



| <span data-ttu-id="d0352-131">需求</span><span class="sxs-lookup"><span data-stu-id="d0352-131">Requirement</span></span> | <span data-ttu-id="d0352-132">值</span><span class="sxs-lookup"><span data-stu-id="d0352-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0352-133">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d0352-133">TAPI version</span></span><br/> | <span data-ttu-id="d0352-134">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d0352-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d0352-135">標頭</span><span class="sxs-lookup"><span data-stu-id="d0352-135">Header</span></span><br/>       | <dl> <span data-ttu-id="d0352-136"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0352-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0352-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="d0352-137">Library</span></span><br/>      | <dl> <span data-ttu-id="d0352-138"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="d0352-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d0352-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d0352-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="d0352-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0352-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0352-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0352-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0352-142">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="d0352-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="d0352-143">**ITTime：： get \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="d0352-143">**ITTime::get\_StopTime**</span></span>](ittime-get-stoptime.md)
</dt> </dl>

 

 




