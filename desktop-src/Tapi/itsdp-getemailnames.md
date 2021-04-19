---
description: GetEmailNames 方法會取得與會議 blob 相關聯之電子郵件名稱的陣列。
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'ITSdp：： GetEmailNames 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f0200b5cc6ea0422f47a323cd1c57d7e0f9a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993468"
---
# <a name="itsdpgetemailnames-method"></a><span data-ttu-id="b1682-103">ITSdp：： GetEmailNames 方法</span><span class="sxs-lookup"><span data-stu-id="b1682-103">ITSdp::GetEmailNames method</span></span>

<span data-ttu-id="b1682-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="b1682-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b1682-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="b1682-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b1682-106">**GetEmailNames** 方法會取得與會議 blob 相關聯之電子郵件名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="b1682-106">The **GetEmailNames** method gets an array of e-mail names associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1682-107">語法</span><span class="sxs-lookup"><span data-stu-id="b1682-107">Syntax</span></span>


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="b1682-108">參數</span><span class="sxs-lookup"><span data-stu-id="b1682-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1682-109">*pAddresses* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b1682-109">*pAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1682-110">會列出電子郵件地址的 **BSTR** 之 SAFEARRAY 的 **VARIANT** 指標。</span><span class="sxs-lookup"><span data-stu-id="b1682-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="b1682-111">*pNames* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b1682-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1682-112">**BSTR** 清單名稱之 SAFEARRAY 的 **VARIANT** 指標。</span><span class="sxs-lookup"><span data-stu-id="b1682-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1682-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1682-113">Return value</span></span>

<span data-ttu-id="b1682-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b1682-114">This method can return one of these values.</span></span>



| <span data-ttu-id="b1682-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b1682-115">Return code</span></span>                                                                                   | <span data-ttu-id="b1682-116">Description</span><span class="sxs-lookup"><span data-stu-id="b1682-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1682-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b1682-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b1682-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="b1682-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="b1682-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="b1682-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b1682-120">*PAddresses* 或 *pNames* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="b1682-120">The *pAddresses* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="b1682-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b1682-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b1682-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="b1682-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="b1682-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="b1682-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="b1682-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b1682-124">Unspecified error.</span></span><br/>                                             |
| <dl> <span data-ttu-id="b1682-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="b1682-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="b1682-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="b1682-126">This method is not yet implemented.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="b1682-127">備註</span><span class="sxs-lookup"><span data-stu-id="b1682-127">Remarks</span></span>

<span data-ttu-id="b1682-128">*PAddresses* 和 *pNames* 所指向的清單長度相同。</span><span class="sxs-lookup"><span data-stu-id="b1682-128">The lists that *pAddresses* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1682-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1682-129">Requirements</span></span>



| <span data-ttu-id="b1682-130">需求</span><span class="sxs-lookup"><span data-stu-id="b1682-130">Requirement</span></span> | <span data-ttu-id="b1682-131">值</span><span class="sxs-lookup"><span data-stu-id="b1682-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1682-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="b1682-132">TAPI version</span></span><br/> | <span data-ttu-id="b1682-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b1682-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b1682-134">標頭</span><span class="sxs-lookup"><span data-stu-id="b1682-134">Header</span></span><br/>       | <dl> <span data-ttu-id="b1682-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1682-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1682-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1682-136">Library</span></span><br/>      | <dl> <span data-ttu-id="b1682-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="b1682-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b1682-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b1682-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="b1682-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1682-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1682-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1682-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1682-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="b1682-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




