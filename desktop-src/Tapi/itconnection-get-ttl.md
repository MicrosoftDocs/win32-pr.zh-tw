---
description: 取得 \_ ttl 方法會取得位址上的傳輸 (Ttl) 範圍的存留時間。
ms.assetid: ea3c22d8-476e-4b4b-98c6-f1075e704f3d
title: 'ITConnection：： get_Ttl 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88f4810eeefc19647e6ed5601b3a6b88870f1e9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984300"
---
# <a name="itconnectionget_ttl-method"></a><span data-ttu-id="792a8-103">ITConnection：： get \_ Ttl 方法</span><span class="sxs-lookup"><span data-stu-id="792a8-103">ITConnection::get\_Ttl method</span></span>

<span data-ttu-id="792a8-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="792a8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="792a8-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="792a8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="792a8-106">**取得 \_ ttl** 方法會取得位址上的傳輸 (Ttl) 範圍的 [*存留時間*](t-tapgloss.md)。</span><span class="sxs-lookup"><span data-stu-id="792a8-106">The **get\_Ttl** method gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="792a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="792a8-107">Syntax</span></span>


```C++
HRESULT get_Ttl(
  [out] unsigned char *pTtl
);
```



## <a name="parameters"></a><span data-ttu-id="792a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="792a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="792a8-109">*pTtl* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="792a8-109">*pTtl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="792a8-110">TTL 範圍。</span><span class="sxs-lookup"><span data-stu-id="792a8-110">TTL scope.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="792a8-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="792a8-111">Return value</span></span>

<span data-ttu-id="792a8-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="792a8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="792a8-113">值</span><span class="sxs-lookup"><span data-stu-id="792a8-113">Value</span></span>                                                                                         | <span data-ttu-id="792a8-114">意義</span><span class="sxs-lookup"><span data-stu-id="792a8-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="792a8-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="792a8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="792a8-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="792a8-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="792a8-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="792a8-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="792a8-118">*PTtl* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="792a8-118">The *pTtl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="792a8-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="792a8-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="792a8-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="792a8-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="792a8-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="792a8-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="792a8-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="792a8-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="792a8-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="792a8-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="792a8-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="792a8-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="792a8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="792a8-125">Requirements</span></span>



| <span data-ttu-id="792a8-126">需求</span><span class="sxs-lookup"><span data-stu-id="792a8-126">Requirement</span></span> | <span data-ttu-id="792a8-127">值</span><span class="sxs-lookup"><span data-stu-id="792a8-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="792a8-128">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="792a8-128">TAPI version</span></span><br/> | <span data-ttu-id="792a8-129">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="792a8-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="792a8-130">標頭</span><span class="sxs-lookup"><span data-stu-id="792a8-130">Header</span></span><br/>       | <dl> <span data-ttu-id="792a8-131"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="792a8-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="792a8-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="792a8-132">Library</span></span><br/>      | <dl> <span data-ttu-id="792a8-133"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="792a8-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="792a8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="792a8-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="792a8-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="792a8-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="792a8-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="792a8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792a8-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="792a8-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




