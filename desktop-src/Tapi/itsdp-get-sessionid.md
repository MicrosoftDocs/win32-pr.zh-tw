---
description: 取得 \_ SessionId 方法會取得32位 NTP (網路時間通訊協定) 值，作為會話識別碼。 這是在會話建立時自動產生的。
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'ITSdp：： get_SessionId 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad593b61f4c935a220e59383ae170569f04af54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995715"
---
# <a name="itsdpget_sessionid-method"></a><span data-ttu-id="e9757-104">ITSdp：： get \_ SessionId 方法</span><span class="sxs-lookup"><span data-stu-id="e9757-104">ITSdp::get\_SessionId method</span></span>

<span data-ttu-id="e9757-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="e9757-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e9757-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e9757-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e9757-107">**取得 \_ SessionId** 方法會取得32位 NTP (網路時間通訊協定) 值，作為會話識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9757-107">The **get\_SessionId** method gets the 32-bit NTP (Network Time Protocol) value that serves as the session identifier.</span></span> <span data-ttu-id="e9757-108">這是在會話建立時自動產生的。</span><span class="sxs-lookup"><span data-stu-id="e9757-108">This is generated automatically when the session is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9757-109">語法</span><span class="sxs-lookup"><span data-stu-id="e9757-109">Syntax</span></span>


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a><span data-ttu-id="e9757-110">參數</span><span class="sxs-lookup"><span data-stu-id="e9757-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9757-111">*pSessionId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9757-111">*pSessionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9757-112">會話識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="e9757-112">Pointer to the session identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9757-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9757-113">Return value</span></span>

<span data-ttu-id="e9757-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e9757-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e9757-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e9757-115">Return code</span></span>                                                                                   | <span data-ttu-id="e9757-116">Description</span><span class="sxs-lookup"><span data-stu-id="e9757-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e9757-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e9757-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e9757-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="e9757-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e9757-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e9757-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e9757-120">*PSessionId* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="e9757-120">The *pSessionId* parameter is not valid.</span></span><br/>             |
| <dl> <span data-ttu-id="e9757-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="e9757-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e9757-122">*PSessionId* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="e9757-122">The *pSessionId* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="e9757-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e9757-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e9757-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="e9757-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e9757-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="e9757-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e9757-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e9757-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e9757-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e9757-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e9757-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="e9757-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e9757-129">備註</span><span class="sxs-lookup"><span data-stu-id="e9757-129">Remarks</span></span>

<span data-ttu-id="e9757-130">這個方法的傳回值可以是 **ulong**，但是 Visual Basic 不支援 **ulong** 型別。</span><span class="sxs-lookup"><span data-stu-id="e9757-130">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="e9757-131">**DOUBLE** 是下一個最小的型別，其中包含所需的整個值範圍。</span><span class="sxs-lookup"><span data-stu-id="e9757-131">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9757-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9757-132">Requirements</span></span>



| <span data-ttu-id="e9757-133">需求</span><span class="sxs-lookup"><span data-stu-id="e9757-133">Requirement</span></span> | <span data-ttu-id="e9757-134">值</span><span class="sxs-lookup"><span data-stu-id="e9757-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9757-135">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e9757-135">TAPI version</span></span><br/> | <span data-ttu-id="e9757-136">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e9757-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e9757-137">標頭</span><span class="sxs-lookup"><span data-stu-id="e9757-137">Header</span></span><br/>       | <dl> <span data-ttu-id="e9757-138"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9757-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9757-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9757-139">Library</span></span><br/>      | <dl> <span data-ttu-id="e9757-140"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="e9757-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e9757-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e9757-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="e9757-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9757-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9757-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9757-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9757-144">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="e9757-144">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




