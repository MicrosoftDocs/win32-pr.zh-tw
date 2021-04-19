---
description: Get \_ ProtocolVersion 方法會取得會話描述元 (SDP 的通訊協定，請參閱 RFC 2327) 通訊協定版本。
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: 'ITSdp：： get_ProtocolVersion 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652c6c3d6723a10cfe474376cf8b9f1342321db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994266"
---
# <a name="itsdpget_protocolversion-method"></a><span data-ttu-id="adc43-103">ITSdp：： get \_ ProtocolVersion 方法</span><span class="sxs-lookup"><span data-stu-id="adc43-103">ITSdp::get\_ProtocolVersion method</span></span>

<span data-ttu-id="adc43-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="adc43-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="adc43-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="adc43-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="adc43-106">**Get \_ ProtocolVersion** 方法會取得會話描述元 (SDP 的通訊協定，請參閱 RFC 2327) 通訊協定版本。</span><span class="sxs-lookup"><span data-stu-id="adc43-106">The **get\_ProtocolVersion** method gets the Session Descriptor Protocol (SDP; see RFC 2327) protocol version.</span></span>

## <a name="syntax"></a><span data-ttu-id="adc43-107">語法</span><span class="sxs-lookup"><span data-stu-id="adc43-107">Syntax</span></span>


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="adc43-108">參數</span><span class="sxs-lookup"><span data-stu-id="adc43-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adc43-109">*pProtocolVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="adc43-109">*pProtocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adc43-110">通訊協定版本的指標。</span><span class="sxs-lookup"><span data-stu-id="adc43-110">Pointer to the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adc43-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="adc43-111">Return value</span></span>

<span data-ttu-id="adc43-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="adc43-112">This method can return one of these values.</span></span>



| <span data-ttu-id="adc43-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="adc43-113">Return code</span></span>                                                                                   | <span data-ttu-id="adc43-114">Description</span><span class="sxs-lookup"><span data-stu-id="adc43-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="adc43-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="adc43-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="adc43-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="adc43-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="adc43-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="adc43-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="adc43-118">*PProtocolVersion* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="adc43-118">The *pProtocolVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="adc43-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="adc43-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="adc43-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="adc43-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="adc43-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="adc43-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="adc43-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="adc43-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="adc43-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="adc43-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="adc43-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="adc43-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="adc43-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="adc43-125">Requirements</span></span>



| <span data-ttu-id="adc43-126">需求</span><span class="sxs-lookup"><span data-stu-id="adc43-126">Requirement</span></span> | <span data-ttu-id="adc43-127">值</span><span class="sxs-lookup"><span data-stu-id="adc43-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adc43-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="adc43-128">TAPI version</span></span><br/> | <span data-ttu-id="adc43-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="adc43-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="adc43-130">標頭</span><span class="sxs-lookup"><span data-stu-id="adc43-130">Header</span></span><br/>       | <dl> <span data-ttu-id="adc43-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="adc43-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="adc43-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="adc43-132">Library</span></span><br/>      | <dl> <span data-ttu-id="adc43-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="adc43-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="adc43-134">DLL</span><span class="sxs-lookup"><span data-stu-id="adc43-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="adc43-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adc43-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adc43-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adc43-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc43-137">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="adc43-137">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




