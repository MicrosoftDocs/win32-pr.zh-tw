---
description: SetAddressInfo 方法會設定位址資訊。
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'ITConnection：： SetAddressInfo 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae181911527c22639c8c2da3038c0377734fd1da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990160"
---
# <a name="itconnectionsetaddressinfo-method"></a><span data-ttu-id="4c003-103">ITConnection：： SetAddressInfo 方法</span><span class="sxs-lookup"><span data-stu-id="4c003-103">ITConnection::SetAddressInfo method</span></span>

<span data-ttu-id="4c003-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="4c003-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4c003-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="4c003-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4c003-106">**SetAddressInfo** 方法會設定位址資訊。</span><span class="sxs-lookup"><span data-stu-id="4c003-106">The **SetAddressInfo** method sets the address information.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c003-107">語法</span><span class="sxs-lookup"><span data-stu-id="4c003-107">Syntax</span></span>


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a><span data-ttu-id="4c003-108">參數</span><span class="sxs-lookup"><span data-stu-id="4c003-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c003-109">*pStartAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c003-109">*pStartAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c003-110">包含起始位址之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="4c003-110">Pointer to a **BSTR** containing the start address.</span></span>

</dd> <dt>

<span data-ttu-id="4c003-111">*NumAddresses* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c003-111">*NumAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c003-112">要用於會話的位址數目。</span><span class="sxs-lookup"><span data-stu-id="4c003-112">Number of addresses to be used for the session.</span></span>

</dd> <dt>

<span data-ttu-id="4c003-113">*Ttl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c003-113">*Ttl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c003-114"> (TTL) 位址上的傳輸範圍的生存 [*時間*](t-tapgloss.md)。</span><span class="sxs-lookup"><span data-stu-id="4c003-114">[*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c003-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c003-115">Return value</span></span>

<span data-ttu-id="4c003-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4c003-116">This method can return one of these values.</span></span>



| <span data-ttu-id="4c003-117">值</span><span class="sxs-lookup"><span data-stu-id="4c003-117">Value</span></span>                                                                                         | <span data-ttu-id="4c003-118">意義</span><span class="sxs-lookup"><span data-stu-id="4c003-118">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c003-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4c003-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4c003-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="4c003-120">Method succeeded.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="4c003-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4c003-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4c003-122">*PStartAddress*、 *NumAddresses* 或 *Ttl* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="4c003-122">The *pStartAddress*, *NumAddresses*, or *Ttl* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="4c003-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4c003-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4c003-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="4c003-124">Insufficient memory exists to perform the operation.</span></span><br/>                  |
| <dl> <span data-ttu-id="4c003-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="4c003-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="4c003-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c003-126">Unspecified error.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="4c003-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4c003-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="4c003-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="4c003-128">This method is not yet implemented.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="4c003-129">備註</span><span class="sxs-lookup"><span data-stu-id="4c003-129">Remarks</span></span>

<span data-ttu-id="4c003-130">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pStartAddress* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="4c003-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pStartAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c003-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c003-131">Requirements</span></span>



| <span data-ttu-id="4c003-132">需求</span><span class="sxs-lookup"><span data-stu-id="4c003-132">Requirement</span></span> | <span data-ttu-id="4c003-133">值</span><span class="sxs-lookup"><span data-stu-id="4c003-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c003-134">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="4c003-134">TAPI version</span></span><br/> | <span data-ttu-id="4c003-135">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4c003-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="4c003-136">標頭</span><span class="sxs-lookup"><span data-stu-id="4c003-136">Header</span></span><br/>       | <dl> <span data-ttu-id="4c003-137"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c003-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c003-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c003-138">Library</span></span><br/>      | <dl> <span data-ttu-id="4c003-139"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="4c003-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4c003-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4c003-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="4c003-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c003-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c003-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c003-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c003-143">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="4c003-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

