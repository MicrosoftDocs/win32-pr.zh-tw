---
title: 'INapSystemHealthAgentCallback NotifyOrphanedSoHRequest 方法 (NapSystemHealthAgent .h) '
description: 如果從 SHA 查詢了 SoHRequest，則會呼叫，但是回應絕不會傳回。
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- NotifyOrphanedSoHRequest 方法 NAP
- NotifyOrphanedSoHRequest 方法 NAP，INapSystemHealthAgentCallback 介面
- INapSystemHealthAgentCallback 介面 NAP，NotifyOrphanedSoHRequest 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385190"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a><span data-ttu-id="f73db-106">INapSystemHealthAgentCallback：： NotifyOrphanedSoHRequest 方法</span><span class="sxs-lookup"><span data-stu-id="f73db-106">INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="f73db-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="f73db-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f73db-108">如果從 SHA 查詢 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則會呼叫 **INapSystemHealthAgentCallback：： NotifyOrphanedSoHRequest** 方法，但回應絕不會傳回。</span><span class="sxs-lookup"><span data-stu-id="f73db-108">The **INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest** method is called if an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was queried from the SHA, but the response never came back.</span></span>

## <a name="syntax"></a><span data-ttu-id="f73db-109">語法</span><span class="sxs-lookup"><span data-stu-id="f73db-109">Syntax</span></span>


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="f73db-110">參數</span><span class="sxs-lookup"><span data-stu-id="f73db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f73db-111">*correlationId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f73db-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f73db-112">識別孤立 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)的唯一 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)結構指標。</span><span class="sxs-lookup"><span data-stu-id="f73db-112">A pointer to the unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies the orphaned [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f73db-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f73db-113">Return value</span></span>

<span data-ttu-id="f73db-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f73db-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f73db-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f73db-115">Return code</span></span>                                                                          | <span data-ttu-id="f73db-116">Description</span><span class="sxs-lookup"><span data-stu-id="f73db-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="f73db-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f73db-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f73db-118">表示成功。</span><span class="sxs-lookup"><span data-stu-id="f73db-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f73db-119">備註</span><span class="sxs-lookup"><span data-stu-id="f73db-119">Remarks</span></span>

<span data-ttu-id="f73db-120">此回呼方法是由 NAP 系統所宣告，而且是由 SHA 寫入器所執行。</span><span class="sxs-lookup"><span data-stu-id="f73db-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="f73db-121">在下列情況下，系統可以呼叫這個方法：</span><span class="sxs-lookup"><span data-stu-id="f73db-121">This method can be called by the system in the following cases:</span></span>

-   <span data-ttu-id="f73db-122">無法在網路上傳送 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 。</span><span class="sxs-lookup"><span data-stu-id="f73db-122">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) could not be sent on the wire.</span></span>
-   <span data-ttu-id="f73db-123">[**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)是在網路上傳送，但未傳回 **SoHResponse** ，也就是 enforcer 超時，或伺服器端沒有對應的 SHV。</span><span class="sxs-lookup"><span data-stu-id="f73db-123">A [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was sent on the wire, but no **SoHResponse** came back, i.e. the enforcer timed out or there was no corresponding SHV on the server-side.</span></span>
-   <span data-ttu-id="f73db-124">連接中斷或 enforcer 離線。</span><span class="sxs-lookup"><span data-stu-id="f73db-124">The connection went down or an enforcer went offline.</span></span>

<span data-ttu-id="f73db-125">這只是最棒的通知，因此 Sha 不能依賴這項資訊來清除狀態。</span><span class="sxs-lookup"><span data-stu-id="f73db-125">This is only a best effort notification, so SHAs must not rely on this information to clean up state.</span></span> <span data-ttu-id="f73db-126">在許多情況下，將不會收到 SHA 的通知：</span><span class="sxs-lookup"><span data-stu-id="f73db-126">There are several situations in which an SHA will not be notified:</span></span>

-   <span data-ttu-id="f73db-127">如果是 enforcer misbehaves，也就是它不會在連接狀態為關閉時通知 SHA。</span><span class="sxs-lookup"><span data-stu-id="f73db-127">If an enforcer misbehaves, i.e. it does not notify the SHA when the connection state is down.</span></span>
-   <span data-ttu-id="f73db-128">如果 enforcer 損毀。</span><span class="sxs-lookup"><span data-stu-id="f73db-128">If an enforcer crashes.</span></span>
-   <span data-ttu-id="f73db-129">在錯誤狀況中，也就是 NapAgent 記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="f73db-129">In error conditions, i.e. the NapAgent is out of memory.</span></span>

<span data-ttu-id="f73db-130">Sha 可能會在第一次系結至 NapAgent 時收到一些偽造的通知，例如，當 SHA 系結時，如果 SoH 交換正在進行中，則會發生一些假的通知。</span><span class="sxs-lookup"><span data-stu-id="f73db-130">SHAs may get some spurious notifications when they first bind to the NapAgent, for instance, if an SoH exchange is in progress when the SHA bound, and then it times out.</span></span>

## <a name="requirements"></a><span data-ttu-id="f73db-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f73db-131">Requirements</span></span>



| <span data-ttu-id="f73db-132">需求</span><span class="sxs-lookup"><span data-stu-id="f73db-132">Requirement</span></span> | <span data-ttu-id="f73db-133">值</span><span class="sxs-lookup"><span data-stu-id="f73db-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f73db-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f73db-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f73db-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f73db-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f73db-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f73db-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f73db-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f73db-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f73db-138">標頭</span><span class="sxs-lookup"><span data-stu-id="f73db-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f73db-139"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="f73db-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="f73db-140">Idl</span><span class="sxs-lookup"><span data-stu-id="f73db-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f73db-141"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f73db-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f73db-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f73db-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f73db-143">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="f73db-143">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





