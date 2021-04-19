---
title: 'INapSystemHealthAgentBinding 介面 (NapSystemHealthAgent .h) '
description: 'Sha 用來與 NapAgent 通訊。 |INapSystemHealthAgentBinding 介面 (NapSystemHealthAgent .h) '
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- INapSystemHealthAgentBinding 介面 NAP
- INapSystemHealthAgentBinding 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106974822"
---
# <a name="inapsystemhealthagentbinding-interface"></a><span data-ttu-id="bb6dc-106">INapSystemHealthAgentBinding 介面</span><span class="sxs-lookup"><span data-stu-id="bb6dc-106">INapSystemHealthAgentBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="bb6dc-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="bb6dc-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bb6dc-108">**INapSystemHealthAgentBinding** 會提供 sha 用來與 NapAgent 進行通訊的方法。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-108">The **INapSystemHealthAgentBinding** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="bb6dc-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) 會繼承此介面的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="bb6dc-110">成員</span><span class="sxs-lookup"><span data-stu-id="bb6dc-110">Members</span></span>

<span data-ttu-id="bb6dc-111">**INapSystemHealthAgentBinding** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-111">The **INapSystemHealthAgentBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bb6dc-112">**INapSystemHealthAgentBinding** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bb6dc-112">**INapSystemHealthAgentBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="bb6dc-113">方法</span><span class="sxs-lookup"><span data-stu-id="bb6dc-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bb6dc-114">方法</span><span class="sxs-lookup"><span data-stu-id="bb6dc-114">Methods</span></span>

<span data-ttu-id="bb6dc-115">**INapSystemHealthAgentBinding** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-115">The **INapSystemHealthAgentBinding** interface has these methods.</span></span>



| <span data-ttu-id="bb6dc-116">方法</span><span class="sxs-lookup"><span data-stu-id="bb6dc-116">Method</span></span>                                                                                                                     | <span data-ttu-id="bb6dc-117">描述</span><span class="sxs-lookup"><span data-stu-id="bb6dc-117">Description</span></span>                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb6dc-118">**INapSystemHealthAgentBinding::FlushCache**</span><span class="sxs-lookup"><span data-stu-id="bb6dc-118">**INapSystemHealthAgentBinding::FlushCache**</span></span>](inapsystemhealthagentbinding-flushcache-method.md)                         | <span data-ttu-id="bb6dc-119">由 SHA 呼叫以排清其 SoH 快取。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-119">Called by an SHA to flush its SoH cache.</span></span><br/>                                                |
| [<span data-ttu-id="bb6dc-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="bb6dc-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span></span>](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | <span data-ttu-id="bb6dc-121">由 Sha 呼叫以判斷系統隔離狀態。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-121">Called by SHAs to determine the system isolation state.</span></span><br/>                                 |
| [<span data-ttu-id="bb6dc-122">**INapSystemHealthAgentBinding：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="bb6dc-122">**INapSystemHealthAgentBinding::Initialize**</span></span>](inapsystemhealthagentbinding-initialize-method.md)                         | <span data-ttu-id="bb6dc-123">初始化 SHA，並將 SHA 系結至 NapAgent 服務。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-123">Initializes the SHA and binds the SHA to the NapAgent service.</span></span> <br/>                         |
| [<span data-ttu-id="bb6dc-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="bb6dc-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span></span>](inapsystemhealthagentbinding-notifysohchange-method.md)               | <span data-ttu-id="bb6dc-125">當其 SoH 變更時由 Sha 呼叫。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-125">Called by SHAs when their SoH changes.</span></span><br/>                                                  |
| [<span data-ttu-id="bb6dc-126">**INapSystemHealthAgentBinding：：解除初始化**</span><span class="sxs-lookup"><span data-stu-id="bb6dc-126">**INapSystemHealthAgentBinding::Uninitialize**</span></span>](inapsystemhealthagentbinding-uninitialize-method.md)                     | <span data-ttu-id="bb6dc-127">由 Sha 呼叫，使 NapAgent 釋放所有對 SHA COM 指標的參考。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-127">Called by SHAs to cause the NapAgent to release all its references to SHA COM pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb6dc-128">備註</span><span class="sxs-lookup"><span data-stu-id="bb6dc-128">Remarks</span></span>

<span data-ttu-id="bb6dc-129">如果 NapAgent 已停止，此介面中的所有 Api 都會傳回 **RPC \_ E \_ 中斷** 連線。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-129">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="bb6dc-130">這個物件會在重新開機後自動復原並重新系結至 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="bb6dc-130">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6dc-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb6dc-131">Requirements</span></span>



| <span data-ttu-id="bb6dc-132">需求</span><span class="sxs-lookup"><span data-stu-id="bb6dc-132">Requirement</span></span> | <span data-ttu-id="bb6dc-133">值</span><span class="sxs-lookup"><span data-stu-id="bb6dc-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6dc-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb6dc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bb6dc-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb6dc-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bb6dc-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb6dc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bb6dc-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb6dc-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bb6dc-138">標頭</span><span class="sxs-lookup"><span data-stu-id="bb6dc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb6dc-139"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb6dc-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb6dc-140">Idl</span><span class="sxs-lookup"><span data-stu-id="bb6dc-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb6dc-141"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb6dc-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="bb6dc-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bb6dc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb6dc-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb6dc-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="bb6dc-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb6dc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6dc-145">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="bb6dc-145">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="bb6dc-146">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="bb6dc-146">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

