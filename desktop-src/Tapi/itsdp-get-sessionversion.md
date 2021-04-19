---
description: Get \_ SessionVersion 方法會取得32位 (理想的網路時間通訊協定，或作為會話版本的 NTP) 值。
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'ITSdp：： get_SessionVersion 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994917"
---
# <a name="itsdpget_sessionversion-method"></a><span data-ttu-id="cf336-103">ITSdp：： get \_ SessionVersion 方法</span><span class="sxs-lookup"><span data-stu-id="cf336-103">ITSdp::get\_SessionVersion method</span></span>

<span data-ttu-id="cf336-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="cf336-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cf336-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="cf336-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cf336-106">**Get \_ SessionVersion** 方法會取得32位 (理想的網路時間通訊協定，或作為會話版本的 NTP) 值。</span><span class="sxs-lookup"><span data-stu-id="cf336-106">The **get\_SessionVersion** method gets the 32-bit (ideally Network Time Protocol, or NTP) value that serves as the session version.</span></span> <span data-ttu-id="cf336-107">雖然這是在會話建立時自動產生的，但在更改 SDP 時，使用者必須負責變更。</span><span class="sxs-lookup"><span data-stu-id="cf336-107">Although this is generated automatically when the session is created, the user is responsible for changing it when the SDP is modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf336-108">語法</span><span class="sxs-lookup"><span data-stu-id="cf336-108">Syntax</span></span>


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="cf336-109">參數</span><span class="sxs-lookup"><span data-stu-id="cf336-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf336-110">*pSessionVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf336-110">*pSessionVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf336-111">會話版本識別碼的指標。</span><span class="sxs-lookup"><span data-stu-id="cf336-111">Pointer to the session version identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf336-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf336-112">Return value</span></span>

<span data-ttu-id="cf336-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cf336-113">This method can return one of these values.</span></span>



| <span data-ttu-id="cf336-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cf336-114">Return code</span></span>                                                                                   | <span data-ttu-id="cf336-115">Description</span><span class="sxs-lookup"><span data-stu-id="cf336-115">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf336-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cf336-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cf336-117">方法成功。</span><span class="sxs-lookup"><span data-stu-id="cf336-117">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="cf336-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cf336-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cf336-119">*PSessionVersion* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="cf336-119">The *pSessionVersion* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="cf336-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="cf336-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cf336-121">*PSessionVersion* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="cf336-121">The *pSessionVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="cf336-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cf336-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cf336-123">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="cf336-123">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="cf336-124"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="cf336-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cf336-125">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cf336-125">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="cf336-126"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="cf336-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cf336-127">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="cf336-127">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="cf336-128">備註</span><span class="sxs-lookup"><span data-stu-id="cf336-128">Remarks</span></span>

<span data-ttu-id="cf336-129">這個方法的傳回值可以是 **ulong**，但是 Visual Basic 不支援 **ulong** 型別。</span><span class="sxs-lookup"><span data-stu-id="cf336-129">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="cf336-130">**DOUBLE** 是下一個最小的型別，其中包含所需的整個值範圍。</span><span class="sxs-lookup"><span data-stu-id="cf336-130">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf336-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf336-131">Requirements</span></span>



| <span data-ttu-id="cf336-132">需求</span><span class="sxs-lookup"><span data-stu-id="cf336-132">Requirement</span></span> | <span data-ttu-id="cf336-133">值</span><span class="sxs-lookup"><span data-stu-id="cf336-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf336-134">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="cf336-134">TAPI version</span></span><br/> | <span data-ttu-id="cf336-135">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="cf336-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cf336-136">標頭</span><span class="sxs-lookup"><span data-stu-id="cf336-136">Header</span></span><br/>       | <dl> <span data-ttu-id="cf336-137"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf336-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf336-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf336-138">Library</span></span><br/>      | <dl> <span data-ttu-id="cf336-139"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="cf336-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cf336-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cf336-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="cf336-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf336-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf336-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf336-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf336-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="cf336-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="cf336-144">**ITSdp：:p 的 \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="cf336-144">**ITSdp::put\_SessionVersion**</span></span>](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




