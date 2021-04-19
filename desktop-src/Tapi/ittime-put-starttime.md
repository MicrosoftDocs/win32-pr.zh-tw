---
description: Put \_ StartTime 方法會將32位 NTP (網路時間通訊協定設定) 開始時間值。 會話會在這段時間被視為有效。
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: 'ITTime：:p ut_StartTime 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b574f7c90d7cc2f92204e3a045b33e6fb8480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994649"
---
# <a name="ittimeput_starttime-method"></a><span data-ttu-id="5333a-104">ITTime：:p ui \_ StartTime 方法</span><span class="sxs-lookup"><span data-stu-id="5333a-104">ITTime::put\_StartTime method</span></span>

<span data-ttu-id="5333a-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="5333a-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5333a-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="5333a-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5333a-107">**Put \_ StartTime** 方法會將32位 NTP (網路時間通訊協定設定) 開始時間值。</span><span class="sxs-lookup"><span data-stu-id="5333a-107">The **put\_StartTime** method sets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="5333a-108">會話會在這段時間被視為有效。</span><span class="sxs-lookup"><span data-stu-id="5333a-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="5333a-109">語法</span><span class="sxs-lookup"><span data-stu-id="5333a-109">Syntax</span></span>


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a><span data-ttu-id="5333a-110">參數</span><span class="sxs-lookup"><span data-stu-id="5333a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5333a-111">*時間* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5333a-111">*Time* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5333a-112">會話的開始時間。</span><span class="sxs-lookup"><span data-stu-id="5333a-112">Start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5333a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5333a-113">Return value</span></span>

<span data-ttu-id="5333a-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5333a-114">This method can return one of these values.</span></span>



| <span data-ttu-id="5333a-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5333a-115">Return code</span></span>                                                                                   | <span data-ttu-id="5333a-116">Description</span><span class="sxs-lookup"><span data-stu-id="5333a-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5333a-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5333a-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5333a-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="5333a-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5333a-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5333a-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="5333a-120">*Tim* e 參數無效。</span><span class="sxs-lookup"><span data-stu-id="5333a-120">The *Tim* e parameter is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="5333a-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5333a-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5333a-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="5333a-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="5333a-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="5333a-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="5333a-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5333a-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5333a-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="5333a-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="5333a-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="5333a-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="5333a-127">備註</span><span class="sxs-lookup"><span data-stu-id="5333a-127">Remarks</span></span>

<span data-ttu-id="5333a-128">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="5333a-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="5333a-129">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="5333a-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5333a-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="5333a-130">Requirements</span></span>



| <span data-ttu-id="5333a-131">需求</span><span class="sxs-lookup"><span data-stu-id="5333a-131">Requirement</span></span> | <span data-ttu-id="5333a-132">值</span><span class="sxs-lookup"><span data-stu-id="5333a-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5333a-133">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="5333a-133">TAPI version</span></span><br/> | <span data-ttu-id="5333a-134">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5333a-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5333a-135">標頭</span><span class="sxs-lookup"><span data-stu-id="5333a-135">Header</span></span><br/>       | <dl> <span data-ttu-id="5333a-136"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="5333a-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5333a-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="5333a-137">Library</span></span><br/>      | <dl> <span data-ttu-id="5333a-138"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="5333a-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5333a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="5333a-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="5333a-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5333a-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5333a-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5333a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5333a-142">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="5333a-142">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="5333a-143">**ITTime：： get \_ StartTime**</span><span class="sxs-lookup"><span data-stu-id="5333a-143">**ITTime::get\_StartTime**</span></span>](ittime-get-starttime.md)
</dt> </dl>

 

 




