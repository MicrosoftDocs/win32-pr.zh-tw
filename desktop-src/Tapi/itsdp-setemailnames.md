---
description: SetEmailNames 方法會設定與會議 blob 相關聯的電子郵件地址陣列。
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: 'ITSdp：： SetEmailNames 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ff31e66f5f69fe7fad43da5ec436c3f567cd49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983078"
---
# <a name="itsdpsetemailnames-method"></a><span data-ttu-id="ea37b-103">ITSdp：： SetEmailNames 方法</span><span class="sxs-lookup"><span data-stu-id="ea37b-103">ITSdp::SetEmailNames method</span></span>

<span data-ttu-id="ea37b-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="ea37b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ea37b-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ea37b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ea37b-106">**SetEmailNames** 方法會設定與會議 blob 相關聯的電子郵件地址陣列。</span><span class="sxs-lookup"><span data-stu-id="ea37b-106">The **SetEmailNames** method sets an array of e-mail addresses associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea37b-107">語法</span><span class="sxs-lookup"><span data-stu-id="ea37b-107">Syntax</span></span>


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="ea37b-108">參數</span><span class="sxs-lookup"><span data-stu-id="ea37b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea37b-109">*位址* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ea37b-109">*Addresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea37b-110">列出電子郵件地址之 **BSTR** 的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="ea37b-110">SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="ea37b-111">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ea37b-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea37b-112">**BSTR** 清單名稱的 SAFEARRAY。</span><span class="sxs-lookup"><span data-stu-id="ea37b-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea37b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ea37b-113">Return value</span></span>

<span data-ttu-id="ea37b-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ea37b-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ea37b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ea37b-115">Return code</span></span>                                                                                   | <span data-ttu-id="ea37b-116">Description</span><span class="sxs-lookup"><span data-stu-id="ea37b-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ea37b-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ea37b-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ea37b-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="ea37b-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ea37b-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ea37b-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ea37b-120">*位址* 或 *名稱* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="ea37b-120">The *Addresses* or *Names* parameter is not valid.</span></span><br/>   |
| <dl> <span data-ttu-id="ea37b-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ea37b-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ea37b-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="ea37b-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ea37b-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="ea37b-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ea37b-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ea37b-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ea37b-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ea37b-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ea37b-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="ea37b-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="ea37b-127">備註</span><span class="sxs-lookup"><span data-stu-id="ea37b-127">Remarks</span></span>

<span data-ttu-id="ea37b-128">*位址* 和 *名稱* 的清單會指向相同的長度。</span><span class="sxs-lookup"><span data-stu-id="ea37b-128">The lists that *Addresses* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea37b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea37b-129">Requirements</span></span>



| <span data-ttu-id="ea37b-130">需求</span><span class="sxs-lookup"><span data-stu-id="ea37b-130">Requirement</span></span> | <span data-ttu-id="ea37b-131">值</span><span class="sxs-lookup"><span data-stu-id="ea37b-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea37b-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ea37b-132">TAPI version</span></span><br/> | <span data-ttu-id="ea37b-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ea37b-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ea37b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="ea37b-134">Header</span></span><br/>       | <dl> <span data-ttu-id="ea37b-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea37b-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea37b-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="ea37b-136">Library</span></span><br/>      | <dl> <span data-ttu-id="ea37b-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="ea37b-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ea37b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ea37b-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="ea37b-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea37b-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea37b-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea37b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea37b-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="ea37b-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




