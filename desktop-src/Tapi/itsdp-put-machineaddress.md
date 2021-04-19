---
description: Put \_ MachineAddress 方法會設定來源主機的電腦位址。
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: 'ITSdp：:p ut_MachineAddress 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec09d41cb7735383f08ce8c8983331165c54fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000480"
---
# <a name="itsdpput_machineaddress-method"></a><span data-ttu-id="94204-103">ITSdp：:p 的 \_ MachineAddress 方法</span><span class="sxs-lookup"><span data-stu-id="94204-103">ITSdp::put\_MachineAddress method</span></span>

<span data-ttu-id="94204-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="94204-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="94204-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="94204-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="94204-106">**Put \_ MachineAddress** 方法會設定來源主機的電腦位址。</span><span class="sxs-lookup"><span data-stu-id="94204-106">The **put\_MachineAddress** method sets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="94204-107">語法</span><span class="sxs-lookup"><span data-stu-id="94204-107">Syntax</span></span>


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="94204-108">參數</span><span class="sxs-lookup"><span data-stu-id="94204-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94204-109">*pMachineAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="94204-109">*pMachineAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94204-110">包含會議主機之電腦位址之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="94204-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94204-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="94204-111">Return value</span></span>

<span data-ttu-id="94204-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="94204-112">This method can return one of these values.</span></span>



| <span data-ttu-id="94204-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="94204-113">Return code</span></span>                                                                                   | <span data-ttu-id="94204-114">Description</span><span class="sxs-lookup"><span data-stu-id="94204-114">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="94204-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="94204-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="94204-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="94204-116">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="94204-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="94204-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="94204-118">*PMachineAddress* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="94204-118">The *pMachineAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="94204-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="94204-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="94204-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="94204-120">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="94204-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="94204-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="94204-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="94204-122">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="94204-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="94204-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="94204-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="94204-124">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="94204-125">備註</span><span class="sxs-lookup"><span data-stu-id="94204-125">Remarks</span></span>

<span data-ttu-id="94204-126">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 為 *pMachineAddress* 參數配置記憶體，並在不再需要該變數時，使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="94204-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMachineAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="94204-127">*PMachineAddress* 參數可以是 DNS 名稱 ( "JohnSmith.workinghard.microsoft.com" ) 或 ( "10.111.222.111" ) 的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="94204-127">The *pMachineAddress* parameter can be either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

<span data-ttu-id="94204-128">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="94204-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="94204-129">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="94204-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="94204-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="94204-130">Requirements</span></span>



| <span data-ttu-id="94204-131">需求</span><span class="sxs-lookup"><span data-stu-id="94204-131">Requirement</span></span> | <span data-ttu-id="94204-132">值</span><span class="sxs-lookup"><span data-stu-id="94204-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94204-133">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="94204-133">TAPI version</span></span><br/> | <span data-ttu-id="94204-134">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="94204-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="94204-135">標頭</span><span class="sxs-lookup"><span data-stu-id="94204-135">Header</span></span><br/>       | <dl> <span data-ttu-id="94204-136"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="94204-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="94204-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="94204-137">Library</span></span><br/>      | <dl> <span data-ttu-id="94204-138"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="94204-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="94204-139">DLL</span><span class="sxs-lookup"><span data-stu-id="94204-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="94204-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94204-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94204-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94204-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94204-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="94204-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="94204-143">**ITSdp：： get \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="94204-143">**ITSdp::get\_MachineAddress**</span></span>](itsdp-get-machineaddress.md)
</dt> </dl>

 

