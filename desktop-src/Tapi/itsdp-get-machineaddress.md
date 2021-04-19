---
description: Get \_ MachineAddress 方法會取得來源主機的電腦位址。
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'ITSdp：： get_MachineAddress 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34968efa16f04cba8f99dbc0dc42b0cf4995a43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984004"
---
# <a name="itsdpget_machineaddress-method"></a><span data-ttu-id="e4188-103">ITSdp：： get \_ MachineAddress 方法</span><span class="sxs-lookup"><span data-stu-id="e4188-103">ITSdp::get\_MachineAddress method</span></span>

<span data-ttu-id="e4188-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="e4188-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e4188-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e4188-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e4188-106">**Get \_ MachineAddress** 方法會取得來源主機的電腦位址。</span><span class="sxs-lookup"><span data-stu-id="e4188-106">The **get\_MachineAddress** method gets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4188-107">語法</span><span class="sxs-lookup"><span data-stu-id="e4188-107">Syntax</span></span>


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="e4188-108">參數</span><span class="sxs-lookup"><span data-stu-id="e4188-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4188-109">*ppMachineAddress* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e4188-109">*ppMachineAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4188-110">包含會議主機之電腦位址之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="e4188-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4188-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e4188-111">Return value</span></span>

<span data-ttu-id="e4188-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e4188-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e4188-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e4188-113">Return code</span></span>                                                                                   | <span data-ttu-id="e4188-114">Description</span><span class="sxs-lookup"><span data-stu-id="e4188-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="e4188-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e4188-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e4188-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="e4188-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="e4188-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="e4188-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e4188-118">*PpMachineAddres* s 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="e4188-118">The *ppMachineAddres* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="e4188-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e4188-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e4188-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="e4188-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="e4188-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="e4188-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e4188-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e4188-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="e4188-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e4188-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e4188-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="e4188-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="e4188-125">備註</span><span class="sxs-lookup"><span data-stu-id="e4188-125">Remarks</span></span>

<span data-ttu-id="e4188-126">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppMachineAddress* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e4188-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMachineAddress* parameter.</span></span>

<span data-ttu-id="e4188-127">*PpMachineAddress* 參數可以做為 DNS 名稱 ( "JohnSmith.workinghard.microsoft.com" ) 或 ( "10.111.222.111" ) 的 IP 位址傳回。</span><span class="sxs-lookup"><span data-stu-id="e4188-127">The *ppMachineAddress* parameter can be returned as either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

## <a name="requirements"></a><span data-ttu-id="e4188-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4188-128">Requirements</span></span>



| <span data-ttu-id="e4188-129">需求</span><span class="sxs-lookup"><span data-stu-id="e4188-129">Requirement</span></span> | <span data-ttu-id="e4188-130">值</span><span class="sxs-lookup"><span data-stu-id="e4188-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4188-131">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e4188-131">TAPI version</span></span><br/> | <span data-ttu-id="e4188-132">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e4188-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e4188-133">標頭</span><span class="sxs-lookup"><span data-stu-id="e4188-133">Header</span></span><br/>       | <dl> <span data-ttu-id="e4188-134"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="e4188-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4188-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="e4188-135">Library</span></span><br/>      | <dl> <span data-ttu-id="e4188-136"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="e4188-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e4188-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e4188-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="e4188-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4188-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4188-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4188-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4188-140">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="e4188-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="e4188-141">**ITSdp：:p 的 \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="e4188-141">**ITSdp::put\_MachineAddress**</span></span>](itsdp-put-machineaddress.md)
</dt> </dl>

 

