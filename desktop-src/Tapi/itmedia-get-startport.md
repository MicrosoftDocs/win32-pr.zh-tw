---
description: Get \_ StartPort 方法會取得第一個埠的16位埠值。
ms.assetid: 203b51ea-8e0c-47d2-b267-36a0bf3bff72
title: 'ITMedia：： get_StartPort 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c5cf50f4a8beb0a1694bd1ceaf000620c69b69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988664"
---
# <a name="itmediaget_startport-method"></a><span data-ttu-id="2cd2f-103">ITMedia：： get \_ StartPort 方法</span><span class="sxs-lookup"><span data-stu-id="2cd2f-103">ITMedia::get\_StartPort method</span></span>

<span data-ttu-id="2cd2f-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="2cd2f-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2cd2f-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="2cd2f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2cd2f-106">**Get \_ StartPort** 方法會取得第一個埠的16位埠值。</span><span class="sxs-lookup"><span data-stu-id="2cd2f-106">The **get\_StartPort** method gets the 16-bit port value for the first port.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd2f-107">語法</span><span class="sxs-lookup"><span data-stu-id="2cd2f-107">Syntax</span></span>


```C++
HRESULT get_StartPort(
  [out] LONG *pStartPort
);
```



## <a name="parameters"></a><span data-ttu-id="2cd2f-108">參數</span><span class="sxs-lookup"><span data-stu-id="2cd2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cd2f-109">*pStartPort* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2cd2f-109">*pStartPort* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd2f-110">第一個埠的值。</span><span class="sxs-lookup"><span data-stu-id="2cd2f-110">Value of the first port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cd2f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2cd2f-111">Return value</span></span>

<span data-ttu-id="2cd2f-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2cd2f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2cd2f-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2cd2f-113">Return code</span></span>                                                                                   | <span data-ttu-id="2cd2f-114">Description</span><span class="sxs-lookup"><span data-stu-id="2cd2f-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2cd2f-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2cd2f-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2cd2f-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="2cd2f-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2cd2f-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="2cd2f-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2cd2f-118">*PStartPort* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="2cd2f-118">The *pStartPort* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="2cd2f-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2cd2f-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2cd2f-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="2cd2f-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2cd2f-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="2cd2f-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2cd2f-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2cd2f-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2cd2f-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="2cd2f-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2cd2f-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="2cd2f-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="2cd2f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cd2f-125">Requirements</span></span>



| <span data-ttu-id="2cd2f-126">需求</span><span class="sxs-lookup"><span data-stu-id="2cd2f-126">Requirement</span></span> | <span data-ttu-id="2cd2f-127">值</span><span class="sxs-lookup"><span data-stu-id="2cd2f-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd2f-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="2cd2f-128">TAPI version</span></span><br/> | <span data-ttu-id="2cd2f-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2cd2f-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2cd2f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2cd2f-130">Header</span></span><br/>       | <dl> <span data-ttu-id="2cd2f-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2cd2f-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2cd2f-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="2cd2f-132">Library</span></span><br/>      | <dl> <span data-ttu-id="2cd2f-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="2cd2f-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2cd2f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2cd2f-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="2cd2f-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cd2f-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cd2f-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cd2f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd2f-137">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="2cd2f-137">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




