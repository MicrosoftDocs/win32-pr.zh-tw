---
description: 取得 \_ IsValid 方法會驗證會話描述項通訊協定 (SDP; 請參閱 RFC 2327) blob 中的結構和域值。
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: 'ITSdp：： get_IsValid 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ca3cfdc1061e0a2830010ec39b2e6667c9341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001018"
---
# <a name="itsdpget_isvalid-method"></a><span data-ttu-id="726ff-103">ITSdp：： get \_ IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="726ff-103">ITSdp::get\_IsValid method</span></span>

<span data-ttu-id="726ff-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="726ff-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="726ff-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="726ff-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="726ff-106">**取得 \_ IsValid** 方法會驗證會話描述項通訊協定 (SDP; 請參閱 RFC 2327) blob 中的結構和域值。</span><span class="sxs-lookup"><span data-stu-id="726ff-106">The **get\_IsValid** method validates the Session Descriptor Protocol (SDP; see RFC 2327) blob for structure and field values.</span></span>

## <a name="syntax"></a><span data-ttu-id="726ff-107">語法</span><span class="sxs-lookup"><span data-stu-id="726ff-107">Syntax</span></span>


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a><span data-ttu-id="726ff-108">參數</span><span class="sxs-lookup"><span data-stu-id="726ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="726ff-109">*pfIsValid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="726ff-109">*pfIsValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="726ff-110">指出 blob 結構是否有效。</span><span class="sxs-lookup"><span data-stu-id="726ff-110">Indicates whether the blob structure is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="726ff-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="726ff-111">Return value</span></span>

<span data-ttu-id="726ff-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="726ff-112">This method can return one of these values.</span></span>



| <span data-ttu-id="726ff-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="726ff-113">Return code</span></span>                                                                                   | <span data-ttu-id="726ff-114">Description</span><span class="sxs-lookup"><span data-stu-id="726ff-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="726ff-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="726ff-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="726ff-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="726ff-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="726ff-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="726ff-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="726ff-118">*PfIsValid* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="726ff-118">The *pfIsValid* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="726ff-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="726ff-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="726ff-120">*PfIsValid* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="726ff-120">The *pfIsValid* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="726ff-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="726ff-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="726ff-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="726ff-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="726ff-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="726ff-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="726ff-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="726ff-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="726ff-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="726ff-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="726ff-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="726ff-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="726ff-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="726ff-127">Requirements</span></span>



| <span data-ttu-id="726ff-128">需求</span><span class="sxs-lookup"><span data-stu-id="726ff-128">Requirement</span></span> | <span data-ttu-id="726ff-129">值</span><span class="sxs-lookup"><span data-stu-id="726ff-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="726ff-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="726ff-130">TAPI version</span></span><br/> | <span data-ttu-id="726ff-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="726ff-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="726ff-132">標頭</span><span class="sxs-lookup"><span data-stu-id="726ff-132">Header</span></span><br/>       | <dl> <span data-ttu-id="726ff-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="726ff-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="726ff-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="726ff-134">Library</span></span><br/>      | <dl> <span data-ttu-id="726ff-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="726ff-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="726ff-136">DLL</span><span class="sxs-lookup"><span data-stu-id="726ff-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="726ff-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="726ff-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="726ff-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="726ff-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726ff-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="726ff-139">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




