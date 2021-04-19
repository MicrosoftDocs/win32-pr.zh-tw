---
description: Put \_ AddressType 方法會設定網址類別型。
ms.assetid: 73c64904-925c-4a35-a8f9-88b196b59b1e
title: 'ITConnection：:p ut_AddressType 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb9bc9b83a71f78a68b6efc2fa73c259c4afe9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994234"
---
# <a name="itconnectionput_addresstype-method"></a><span data-ttu-id="6761c-103">ITConnection：:p 的 \_ AddressType 方法</span><span class="sxs-lookup"><span data-stu-id="6761c-103">ITConnection::put\_AddressType method</span></span>

<span data-ttu-id="6761c-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="6761c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6761c-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6761c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6761c-106">**Put \_ AddressType** 方法會設定網址類別型。</span><span class="sxs-lookup"><span data-stu-id="6761c-106">The **put\_AddressType** method sets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6761c-107">語法</span><span class="sxs-lookup"><span data-stu-id="6761c-107">Syntax</span></span>


```C++
HRESULT put_AddressType(
  [in] BSTR pAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="6761c-108">參數</span><span class="sxs-lookup"><span data-stu-id="6761c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6761c-109">*pAddressType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6761c-109">*pAddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6761c-110">包含網址類別型之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="6761c-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6761c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6761c-111">Return value</span></span>

<span data-ttu-id="6761c-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6761c-112">This method can return one of these values.</span></span>



| <span data-ttu-id="6761c-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6761c-113">Return code</span></span>                                                                                   | <span data-ttu-id="6761c-114">Description</span><span class="sxs-lookup"><span data-stu-id="6761c-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6761c-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6761c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6761c-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="6761c-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6761c-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6761c-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6761c-118">*PAddressType* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="6761c-118">The *pAddressType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="6761c-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6761c-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6761c-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="6761c-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="6761c-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="6761c-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="6761c-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6761c-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6761c-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6761c-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="6761c-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="6761c-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="6761c-125">備註</span><span class="sxs-lookup"><span data-stu-id="6761c-125">Remarks</span></span>

<span data-ttu-id="6761c-126">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pAddressType* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="6761c-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAddressType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6761c-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="6761c-127">Requirements</span></span>



| <span data-ttu-id="6761c-128">需求</span><span class="sxs-lookup"><span data-stu-id="6761c-128">Requirement</span></span> | <span data-ttu-id="6761c-129">值</span><span class="sxs-lookup"><span data-stu-id="6761c-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6761c-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="6761c-130">TAPI version</span></span><br/> | <span data-ttu-id="6761c-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6761c-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6761c-132">標頭</span><span class="sxs-lookup"><span data-stu-id="6761c-132">Header</span></span><br/>       | <dl> <span data-ttu-id="6761c-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="6761c-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6761c-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="6761c-134">Library</span></span><br/>      | <dl> <span data-ttu-id="6761c-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="6761c-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6761c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="6761c-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="6761c-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6761c-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6761c-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6761c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6761c-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="6761c-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="6761c-140">**ITConnection：： get \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="6761c-140">**ITConnection::get\_AddressType**</span></span>](itconnection-get-addresstype.md)
</dt> </dl>

 

