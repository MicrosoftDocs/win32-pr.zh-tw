---
description: Get \_ Description 方法會取得 (BSTR) 的會話描述。
ms.assetid: 09a372fe-0dcd-4daf-8f13-c4c89b1ecd16
title: 'ITSdp：： get_Description 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5f60f7aefcfac852a1665f54a59ff0541b1d82a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001224"
---
# <a name="itsdpget_description-method"></a><span data-ttu-id="4f015-103">ITSdp：： get \_ Description 方法</span><span class="sxs-lookup"><span data-stu-id="4f015-103">ITSdp::get\_Description method</span></span>

<span data-ttu-id="4f015-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="4f015-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4f015-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="4f015-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4f015-106">**Get \_ Description** 方法會取得 (**BSTR**) 的會話描述。</span><span class="sxs-lookup"><span data-stu-id="4f015-106">The **get\_Description** method gets the session description (**BSTR**).</span></span> <span data-ttu-id="4f015-107">如果字元集是 ASCII，則必須是 ASCII 可轉換字串。</span><span class="sxs-lookup"><span data-stu-id="4f015-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="4f015-108"> (否則，它可以是任何 **BSTR** 字串。 ) </span><span class="sxs-lookup"><span data-stu-id="4f015-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="4f015-109">語法</span><span class="sxs-lookup"><span data-stu-id="4f015-109">Syntax</span></span>


```C++
HRESULT get_Description(
  [out] BSTR *ppDescription
);
```



## <a name="parameters"></a><span data-ttu-id="4f015-110">參數</span><span class="sxs-lookup"><span data-stu-id="4f015-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f015-111">*ppDescription* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4f015-111">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f015-112">包含會話描述之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="4f015-112">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f015-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f015-113">Return value</span></span>

<span data-ttu-id="4f015-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4f015-114">This method can return one of these values.</span></span>



| <span data-ttu-id="4f015-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4f015-115">Return code</span></span>                                                                                   | <span data-ttu-id="4f015-116">Description</span><span class="sxs-lookup"><span data-stu-id="4f015-116">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f015-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4f015-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4f015-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="4f015-118">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4f015-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="4f015-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4f015-120">*PpDescription* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="4f015-120">The *ppDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="4f015-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4f015-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4f015-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="4f015-122">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="4f015-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="4f015-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4f015-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4f015-124">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4f015-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4f015-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4f015-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="4f015-126">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="4f015-127">備註</span><span class="sxs-lookup"><span data-stu-id="4f015-127">Remarks</span></span>

<span data-ttu-id="4f015-128">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放 *ppDescription* 參數。</span><span class="sxs-lookup"><span data-stu-id="4f015-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the *ppDescription* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f015-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f015-129">Requirements</span></span>



| <span data-ttu-id="4f015-130">需求</span><span class="sxs-lookup"><span data-stu-id="4f015-130">Requirement</span></span> | <span data-ttu-id="4f015-131">值</span><span class="sxs-lookup"><span data-stu-id="4f015-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f015-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="4f015-132">TAPI version</span></span><br/> | <span data-ttu-id="4f015-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4f015-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4f015-134">標頭</span><span class="sxs-lookup"><span data-stu-id="4f015-134">Header</span></span><br/>       | <dl> <span data-ttu-id="4f015-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f015-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4f015-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="4f015-136">Library</span></span><br/>      | <dl> <span data-ttu-id="4f015-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="4f015-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4f015-138">DLL</span><span class="sxs-lookup"><span data-stu-id="4f015-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="4f015-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f015-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f015-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f015-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f015-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="4f015-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="4f015-142">**ITSdp：:p 的 ui \_ 描述**</span><span class="sxs-lookup"><span data-stu-id="4f015-142">**ITSdp::put\_Description**</span></span>](itsdp-put-description.md)
</dt> </dl>

 

