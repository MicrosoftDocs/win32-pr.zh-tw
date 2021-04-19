---
description: Put \_ NetworkType 方法會設定網路類型。
ms.assetid: 747e3133-d103-44dc-b119-5a4cb4ed7f18
title: 'ITConnection：:p ut_NetworkType 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0e08819bcc5cb00824c8c1510d85fdcb1de186b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997682"
---
# <a name="itconnectionput_networktype-method"></a><span data-ttu-id="3ef48-103">ITConnection：:p 的 \_ NetworkType 方法</span><span class="sxs-lookup"><span data-stu-id="3ef48-103">ITConnection::put\_NetworkType method</span></span>

<span data-ttu-id="3ef48-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="3ef48-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3ef48-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="3ef48-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3ef48-106">**Put \_ NetworkType** 方法會設定網路類型。</span><span class="sxs-lookup"><span data-stu-id="3ef48-106">The **put\_NetworkType** method sets the network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ef48-107">語法</span><span class="sxs-lookup"><span data-stu-id="3ef48-107">Syntax</span></span>


```C++
HRESULT put_NetworkType(
  [in] BSTR pNetworkType
);
```



## <a name="parameters"></a><span data-ttu-id="3ef48-108">參數</span><span class="sxs-lookup"><span data-stu-id="3ef48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ef48-109">*pNetworkType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ef48-109">*pNetworkType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ef48-110">包含網路類型之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="3ef48-110">Pointer to a **BSTR** containing the network type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ef48-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ef48-111">Return value</span></span>

<span data-ttu-id="3ef48-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3ef48-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3ef48-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3ef48-113">Return code</span></span>                                                                                   | <span data-ttu-id="3ef48-114">Description</span><span class="sxs-lookup"><span data-stu-id="3ef48-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3ef48-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3ef48-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3ef48-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="3ef48-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3ef48-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3ef48-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3ef48-118">*PNetworkType* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="3ef48-118">The *pNetworkType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="3ef48-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3ef48-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3ef48-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="3ef48-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3ef48-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="3ef48-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3ef48-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3ef48-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3ef48-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="3ef48-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3ef48-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="3ef48-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3ef48-125">備註</span><span class="sxs-lookup"><span data-stu-id="3ef48-125">Remarks</span></span>

<span data-ttu-id="3ef48-126">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pNetworkType* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="3ef48-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pNetworkType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ef48-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ef48-127">Requirements</span></span>



| <span data-ttu-id="3ef48-128">需求</span><span class="sxs-lookup"><span data-stu-id="3ef48-128">Requirement</span></span> | <span data-ttu-id="3ef48-129">值</span><span class="sxs-lookup"><span data-stu-id="3ef48-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef48-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="3ef48-130">TAPI version</span></span><br/> | <span data-ttu-id="3ef48-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3ef48-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3ef48-132">標頭</span><span class="sxs-lookup"><span data-stu-id="3ef48-132">Header</span></span><br/>       | <dl> <span data-ttu-id="3ef48-133"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ef48-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ef48-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="3ef48-134">Library</span></span><br/>      | <dl> <span data-ttu-id="3ef48-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="3ef48-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3ef48-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3ef48-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="3ef48-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ef48-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ef48-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ef48-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ef48-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="3ef48-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="3ef48-140">**ITConnection：： get \_ NetworkType**</span><span class="sxs-lookup"><span data-stu-id="3ef48-140">**ITConnection::get\_NetworkType**</span></span>](itconnection-get-networktype.md)
</dt> </dl>

 

