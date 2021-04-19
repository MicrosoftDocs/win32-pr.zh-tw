---
title: 'INapSystemHealthAgentCallback 介面 (NapSystemHealthAgent .h) '
description: 由系統宣告並由 SHA 寫入器所執行，讓 NapAgent 可以與 SHA 進行通訊。
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- INapSystemHealthAgentCallback 介面 NAP
- INapSystemHealthAgentCallback 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969196"
---
# <a name="inapsystemhealthagentcallback-interface"></a><span data-ttu-id="414e5-105">INapSystemHealthAgentCallback 介面</span><span class="sxs-lookup"><span data-stu-id="414e5-105">INapSystemHealthAgentCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="414e5-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="414e5-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="414e5-107">**INapSystemHealthAgentCallback** 介面會提供由系統宣告並由 sha 寫入器所執行的回呼方法，讓 NapAgent 可以與 sha 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="414e5-107">The **INapSystemHealthAgentCallback** interface provides callback methods that are declared by the system and implemented by the SHA writer so the NapAgent can communicate with the SHA.</span></span>

## <a name="members"></a><span data-ttu-id="414e5-108">成員</span><span class="sxs-lookup"><span data-stu-id="414e5-108">Members</span></span>

<span data-ttu-id="414e5-109">**INapSystemHealthAgentCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="414e5-109">The **INapSystemHealthAgentCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="414e5-110">**INapSystemHealthAgentCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="414e5-110">**INapSystemHealthAgentCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="414e5-111">方法</span><span class="sxs-lookup"><span data-stu-id="414e5-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="414e5-112">方法</span><span class="sxs-lookup"><span data-stu-id="414e5-112">Methods</span></span>

<span data-ttu-id="414e5-113">**INapSystemHealthAgentCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="414e5-113">The **INapSystemHealthAgentCallback** interface has these methods.</span></span>



| <span data-ttu-id="414e5-114">方法</span><span class="sxs-lookup"><span data-stu-id="414e5-114">Method</span></span>                                                                                                                                           | <span data-ttu-id="414e5-115">描述</span><span class="sxs-lookup"><span data-stu-id="414e5-115">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="414e5-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span><span class="sxs-lookup"><span data-stu-id="414e5-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span></span>](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | <span data-ttu-id="414e5-117">由 SHA 用來比較 Soh。</span><span class="sxs-lookup"><span data-stu-id="414e5-117">Used by the SHA to compare the SoHs.</span></span><br/>                                                                      |
| [<span data-ttu-id="414e5-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="414e5-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span></span>](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | <span data-ttu-id="414e5-119">由 NapAgent 呼叫以判斷 SHA 的狀態。</span><span class="sxs-lookup"><span data-stu-id="414e5-119">Called by the NapAgent to determine the state of the SHA.</span></span><br/>                                                 |
| [<span data-ttu-id="414e5-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="414e5-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span></span>](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | <span data-ttu-id="414e5-121">由 NapAgent 呼叫以查詢 SHA 的 SoH 要求。</span><span class="sxs-lookup"><span data-stu-id="414e5-121">Called by the NapAgent to query the SHA's SoH request.</span></span><br/>                                                    |
| [<span data-ttu-id="414e5-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="414e5-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span></span>](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | <span data-ttu-id="414e5-123">如果從 SHA 查詢 SoH 要求，但回應從未回傳，則呼叫。</span><span class="sxs-lookup"><span data-stu-id="414e5-123">Called if an SoH request was queried from the SHA, but the response never came back.</span></span><br/>                      |
| [<span data-ttu-id="414e5-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span><span class="sxs-lookup"><span data-stu-id="414e5-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span></span>](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | <span data-ttu-id="414e5-125">由 NapAgent 呼叫，表示系統隔離狀態或試用結束時間已變更。</span><span class="sxs-lookup"><span data-stu-id="414e5-125">Called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span><br/> |
| [<span data-ttu-id="414e5-126">**INapSystemHealthAgentCallback：:P rocessSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="414e5-126">**INapSystemHealthAgentCallback::ProcessSoHResponse**</span></span>](inapsystemhealthagentcallback-processsohresponse-method.md)                             | <span data-ttu-id="414e5-127">當 NapAgent 收到目的地為此健康情況代理程式的 SoH 回應時呼叫。</span><span class="sxs-lookup"><span data-stu-id="414e5-127">Called when the NapAgent receives an SoH response destined for this health agent.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="414e5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="414e5-128">Requirements</span></span>



| <span data-ttu-id="414e5-129">需求</span><span class="sxs-lookup"><span data-stu-id="414e5-129">Requirement</span></span> | <span data-ttu-id="414e5-130">值</span><span class="sxs-lookup"><span data-stu-id="414e5-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="414e5-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="414e5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="414e5-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="414e5-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="414e5-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="414e5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="414e5-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="414e5-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="414e5-135">標頭</span><span class="sxs-lookup"><span data-stu-id="414e5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="414e5-136"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="414e5-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="414e5-137">Idl</span><span class="sxs-lookup"><span data-stu-id="414e5-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="414e5-138"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="414e5-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="414e5-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="414e5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414e5-140">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="414e5-140">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="414e5-141">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="414e5-141">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

