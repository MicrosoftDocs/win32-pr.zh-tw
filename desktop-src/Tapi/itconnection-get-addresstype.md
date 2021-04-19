---
description: Get \_ AddressType 方法會取得網址類別型。
ms.assetid: b2ff6303-6beb-429c-ad1a-2f729749e5db
title: 'ITConnection：： get_AddressType 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d015b0b395f0219fa9a7af2ca7002f242cfaa1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981358"
---
# <a name="itconnectionget_addresstype-method"></a><span data-ttu-id="e9cef-103">ITConnection：： get \_ AddressType 方法</span><span class="sxs-lookup"><span data-stu-id="e9cef-103">ITConnection::get\_AddressType method</span></span>

<span data-ttu-id="e9cef-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="e9cef-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e9cef-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e9cef-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e9cef-106">**Get \_ AddressType** 方法會取得網址類別型。</span><span class="sxs-lookup"><span data-stu-id="e9cef-106">The **get\_AddressType** method gets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9cef-107">語法</span><span class="sxs-lookup"><span data-stu-id="e9cef-107">Syntax</span></span>


```C++
HRESULT get_AddressType(
  [out] BSTR *ppAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="e9cef-108">參數</span><span class="sxs-lookup"><span data-stu-id="e9cef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9cef-109">*ppAddressType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9cef-109">*ppAddressType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9cef-110">包含網址類別型之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="e9cef-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9cef-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9cef-111">Return value</span></span>

<span data-ttu-id="e9cef-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e9cef-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e9cef-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e9cef-113">Return code</span></span>                                                                                   | <span data-ttu-id="e9cef-114">Description</span><span class="sxs-lookup"><span data-stu-id="e9cef-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9cef-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e9cef-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e9cef-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="e9cef-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="e9cef-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="e9cef-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e9cef-118">*PpAddressType* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="e9cef-118">The *ppAddressType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="e9cef-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e9cef-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e9cef-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="e9cef-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="e9cef-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="e9cef-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e9cef-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e9cef-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e9cef-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e9cef-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e9cef-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="e9cef-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="e9cef-125">備註</span><span class="sxs-lookup"><span data-stu-id="e9cef-125">Remarks</span></span>

<span data-ttu-id="e9cef-126">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppAddressType* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e9cef-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppAddressType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9cef-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9cef-127">Requirements</span></span>



| <span data-ttu-id="e9cef-128">需求</span><span class="sxs-lookup"><span data-stu-id="e9cef-128">Requirement</span></span> | <span data-ttu-id="e9cef-129">值</span><span class="sxs-lookup"><span data-stu-id="e9cef-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e9cef-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e9cef-130">TAPI version</span></span><br/> | <span data-ttu-id="e9cef-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e9cef-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e9cef-132">標頭</span><span class="sxs-lookup"><span data-stu-id="e9cef-132">Header</span></span><br/>       | <dl> <span data-ttu-id="e9cef-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9cef-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e9cef-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9cef-134">Library</span></span><br/>      | <dl> <span data-ttu-id="e9cef-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="e9cef-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e9cef-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e9cef-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="e9cef-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9cef-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9cef-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9cef-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9cef-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="e9cef-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="e9cef-140">**ITConnection：:p 的 \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="e9cef-140">**ITConnection::put\_AddressType**</span></span>](itconnection-put-addresstype.md)
</dt> </dl>

 

