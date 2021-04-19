---
description: 取得 \_ StartTime 方法會取得32位 NTP (網路時間通訊協定) 開始時間值。 會話會在這段時間被視為有效。
ms.assetid: 511e4486-4c73-4610-8e64-9c70acc98eab
title: 'ITTime：： get_StartTime 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051096c6cbdab1960c67ddb2cbcaf57eccab9556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997684"
---
# <a name="ittimeget_starttime-method"></a><span data-ttu-id="32b84-104">ITTime：： get \_ StartTime 方法</span><span class="sxs-lookup"><span data-stu-id="32b84-104">ITTime::get\_StartTime method</span></span>

<span data-ttu-id="32b84-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="32b84-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="32b84-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="32b84-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="32b84-107">**取得 \_ StartTime** 方法會取得32位 NTP (網路時間通訊協定) 開始時間值。</span><span class="sxs-lookup"><span data-stu-id="32b84-107">The **get\_StartTime** method gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span> <span data-ttu-id="32b84-108">會話會在這段時間被視為有效。</span><span class="sxs-lookup"><span data-stu-id="32b84-108">The session is considered active from this time.</span></span>

## <a name="syntax"></a><span data-ttu-id="32b84-109">語法</span><span class="sxs-lookup"><span data-stu-id="32b84-109">Syntax</span></span>


```C++
HRESULT get_StartTime(
  [out] DOUBLE *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="32b84-110">參數</span><span class="sxs-lookup"><span data-stu-id="32b84-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b84-111">*pTime* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="32b84-111">*pTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32b84-112">會話開始時間的指標。</span><span class="sxs-lookup"><span data-stu-id="32b84-112">Pointer to the start time for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32b84-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="32b84-113">Return value</span></span>

<span data-ttu-id="32b84-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="32b84-114">This method can return one of these values.</span></span>



| <span data-ttu-id="32b84-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="32b84-115">Return code</span></span>                                                                                   | <span data-ttu-id="32b84-116">Description</span><span class="sxs-lookup"><span data-stu-id="32b84-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="32b84-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="32b84-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="32b84-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="32b84-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="32b84-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="32b84-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="32b84-120">*PTime* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="32b84-120">The *pTime* parameter is not a valid pointer.</span></span><br/>        |
| <dl> <span data-ttu-id="32b84-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="32b84-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="32b84-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="32b84-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="32b84-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="32b84-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="32b84-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="32b84-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="32b84-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="32b84-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="32b84-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="32b84-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="32b84-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="32b84-127">Requirements</span></span>



| <span data-ttu-id="32b84-128">需求</span><span class="sxs-lookup"><span data-stu-id="32b84-128">Requirement</span></span> | <span data-ttu-id="32b84-129">值</span><span class="sxs-lookup"><span data-stu-id="32b84-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32b84-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="32b84-130">TAPI version</span></span><br/> | <span data-ttu-id="32b84-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="32b84-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="32b84-132">標頭</span><span class="sxs-lookup"><span data-stu-id="32b84-132">Header</span></span><br/>       | <dl> <span data-ttu-id="32b84-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="32b84-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="32b84-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="32b84-134">Library</span></span><br/>      | <dl> <span data-ttu-id="32b84-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="32b84-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="32b84-136">DLL</span><span class="sxs-lookup"><span data-stu-id="32b84-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="32b84-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32b84-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32b84-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32b84-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32b84-139">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="32b84-139">**ITTime**</span></span>](ittime.md)
</dt> <dt>

[<span data-ttu-id="32b84-140">**ITTime：:p 的時間 \_ StartTime StartTime**</span><span class="sxs-lookup"><span data-stu-id="32b84-140">**ITTime::put\_StartTime**</span></span>](ittime-put-starttime.md)
</dt> </dl>

 

 




