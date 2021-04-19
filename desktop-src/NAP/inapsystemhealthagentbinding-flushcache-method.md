---
title: 'INapSystemHealthAgentBinding FlushCache 方法 (NapSystemHealthAgent .h) '
description: 由 SHA 呼叫以排清其 SoH 快取。
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- FlushCache 方法 NAP
- FlushCache 方法 NAP，INapSystemHealthAgentBinding 介面
- INapSystemHealthAgentBinding 介面 NAP，FlushCache 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.FlushCache
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ead6e496d220619439b80fdc5c7601675fdb7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967946"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a><span data-ttu-id="8071c-106">INapSystemHealthAgentBinding：： FlushCache 方法</span><span class="sxs-lookup"><span data-stu-id="8071c-106">INapSystemHealthAgentBinding::FlushCache method</span></span>

> [!Note]  
> <span data-ttu-id="8071c-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="8071c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8071c-108">SHA 會呼叫 **INapSystemHealthAgentBinding：： FlushCache** 方法，以排清其 SoH 快取。</span><span class="sxs-lookup"><span data-stu-id="8071c-108">The **INapSystemHealthAgentBinding::FlushCache** method is called by an SHA to flush its SoH cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="8071c-109">語法</span><span class="sxs-lookup"><span data-stu-id="8071c-109">Syntax</span></span>


```C++
HRESULT FlushCache();
```



## <a name="parameters"></a><span data-ttu-id="8071c-110">參數</span><span class="sxs-lookup"><span data-stu-id="8071c-110">Parameters</span></span>

<span data-ttu-id="8071c-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8071c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8071c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8071c-112">Return value</span></span>

<span data-ttu-id="8071c-113">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8071c-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8071c-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8071c-114">Return code</span></span>                                                                                         | <span data-ttu-id="8071c-115">Description</span><span class="sxs-lookup"><span data-stu-id="8071c-115">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8071c-116"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8071c-116"><dt>**S\_OK** </dt></span></span> </dl>               | <span data-ttu-id="8071c-117">作業成功。</span><span class="sxs-lookup"><span data-stu-id="8071c-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="8071c-118"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8071c-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>     | <span data-ttu-id="8071c-119">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="8071c-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="8071c-120"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8071c-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>      | <span data-ttu-id="8071c-121">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="8071c-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="8071c-122"><dt>**RPC \_ E \_ 中斷連接**</dt></span><span class="sxs-lookup"><span data-stu-id="8071c-122"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8071c-123">NapAgent 已停止。</span><span class="sxs-lookup"><span data-stu-id="8071c-123">The NapAgent has been stopped.</span></span> <span data-ttu-id="8071c-124">這個物件會在重新開機後自動復原並重新系結至 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="8071c-124">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8071c-125">備註</span><span class="sxs-lookup"><span data-stu-id="8071c-125">Remarks</span></span>

<span data-ttu-id="8071c-126">NapAgent 會維護不同 Sha 所提供的最新 Soh 快取。</span><span class="sxs-lookup"><span data-stu-id="8071c-126">The NapAgent maintains a cache of recent SoHs provided by different SHAs.</span></span> <span data-ttu-id="8071c-127">當 Sha 可能或可能不會系結至系統時，此快取非常適合用來將開機時間效能優化。</span><span class="sxs-lookup"><span data-stu-id="8071c-127">This cache is useful to optimize boot-time performance, when SHAs may or may not be bound to the system.</span></span>

<span data-ttu-id="8071c-128">SHA 必須在呼叫這個方法或 [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)介面的任何其他方法之前呼叫 [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="8071c-128">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="8071c-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="8071c-129">Requirements</span></span>



| <span data-ttu-id="8071c-130">需求</span><span class="sxs-lookup"><span data-stu-id="8071c-130">Requirement</span></span> | <span data-ttu-id="8071c-131">值</span><span class="sxs-lookup"><span data-stu-id="8071c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8071c-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8071c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8071c-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8071c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8071c-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8071c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8071c-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8071c-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8071c-136">標頭</span><span class="sxs-lookup"><span data-stu-id="8071c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8071c-137"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="8071c-137"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="8071c-138">Idl</span><span class="sxs-lookup"><span data-stu-id="8071c-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8071c-139"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8071c-139"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="8071c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8071c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8071c-141"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8071c-141"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="8071c-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8071c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8071c-143">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="8071c-143">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





