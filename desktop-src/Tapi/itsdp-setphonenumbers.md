---
description: SetPhoneNumbers 方法會設定與會議 blob 相關聯的電話號碼陣列。
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'ITSdp：： SetPhoneNumbers 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec2820d8d033ac2eed9d9287c3ca52c9deb316
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979442"
---
# <a name="itsdpsetphonenumbers-method"></a><span data-ttu-id="cf976-103">ITSdp：： SetPhoneNumbers 方法</span><span class="sxs-lookup"><span data-stu-id="cf976-103">ITSdp::SetPhoneNumbers method</span></span>

<span data-ttu-id="cf976-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="cf976-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cf976-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="cf976-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cf976-106">**SetPhoneNumbers** 方法會設定與會議 blob 相關聯的電話號碼陣列。</span><span class="sxs-lookup"><span data-stu-id="cf976-106">The **SetPhoneNumbers** method sets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf976-107">語法</span><span class="sxs-lookup"><span data-stu-id="cf976-107">Syntax</span></span>


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="cf976-108">參數</span><span class="sxs-lookup"><span data-stu-id="cf976-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf976-109">*數位* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf976-109">*Numbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf976-110">列出電話號碼之 **BSTR** 的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="cf976-110">SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="cf976-111">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf976-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf976-112">**BSTR** 清單名稱的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="cf976-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf976-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf976-113">Return value</span></span>

<span data-ttu-id="cf976-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cf976-114">This method can return one of these values.</span></span>



| <span data-ttu-id="cf976-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cf976-115">Return code</span></span>                                                                                   | <span data-ttu-id="cf976-116">Description</span><span class="sxs-lookup"><span data-stu-id="cf976-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cf976-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cf976-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="cf976-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cf976-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cf976-120">*數位* 或 *名稱* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="cf976-120">The *Numbers* or *Names* parameter is not valid.</span></span><br/>     |
| <dl> <span data-ttu-id="cf976-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cf976-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="cf976-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="cf976-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="cf976-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cf976-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="cf976-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="cf976-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="cf976-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="cf976-127">備註</span><span class="sxs-lookup"><span data-stu-id="cf976-127">Remarks</span></span>

<span data-ttu-id="cf976-128">清單中的 *數位* 和 *名稱* 會指向相同的長度。</span><span class="sxs-lookup"><span data-stu-id="cf976-128">The lists that *Numbers* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf976-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf976-129">Requirements</span></span>



| <span data-ttu-id="cf976-130">需求</span><span class="sxs-lookup"><span data-stu-id="cf976-130">Requirement</span></span> | <span data-ttu-id="cf976-131">值</span><span class="sxs-lookup"><span data-stu-id="cf976-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf976-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="cf976-132">TAPI version</span></span><br/> | <span data-ttu-id="cf976-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="cf976-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cf976-134">標頭</span><span class="sxs-lookup"><span data-stu-id="cf976-134">Header</span></span><br/>       | <dl> <span data-ttu-id="cf976-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf976-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf976-136">Library</span></span><br/>      | <dl> <span data-ttu-id="cf976-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cf976-138">DLL</span><span class="sxs-lookup"><span data-stu-id="cf976-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="cf976-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf976-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf976-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf976-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="cf976-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




