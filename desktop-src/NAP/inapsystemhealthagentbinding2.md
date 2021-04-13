---
title: 'INapSystemHealthAgentBinding2 介面 (NapSystemHealthAgent .h) '
description: 'Sha 用來與 NapAgent 通訊。 |INapSystemHealthAgentBinding2 介面 (NapSystemHealthAgent .h) '
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- INapSystemHealthAgentBinding2 介面 NAP
- INapSystemHealthAgentBinding2 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322095"
---
# <a name="inapsystemhealthagentbinding2-interface"></a><span data-ttu-id="7ced6-106">INapSystemHealthAgentBinding2 介面</span><span class="sxs-lookup"><span data-stu-id="7ced6-106">INapSystemHealthAgentBinding2 interface</span></span>

> [!Note]  
> <span data-ttu-id="7ced6-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="7ced6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7ced6-108">**INapSystemHealthAgentBinding2** 會提供 sha 用來與 NapAgent 進行通訊的方法。</span><span class="sxs-lookup"><span data-stu-id="7ced6-108">The **INapSystemHealthAgentBinding2** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="7ced6-109">此介面會繼承 [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) 的所有方法，因此應該改用。</span><span class="sxs-lookup"><span data-stu-id="7ced6-109">This interface inherits all the methods of [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="7ced6-110">成員</span><span class="sxs-lookup"><span data-stu-id="7ced6-110">Members</span></span>

<span data-ttu-id="7ced6-111">**INapSystemHealthAgentBinding2** 介面繼承自 [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)。</span><span class="sxs-lookup"><span data-stu-id="7ced6-111">The **INapSystemHealthAgentBinding2** interface inherits from [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span></span> <span data-ttu-id="7ced6-112">**INapSystemHealthAgentBinding2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="7ced6-112">**INapSystemHealthAgentBinding2** also has these types of members:</span></span>

-   [<span data-ttu-id="7ced6-113">方法</span><span class="sxs-lookup"><span data-stu-id="7ced6-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7ced6-114">方法</span><span class="sxs-lookup"><span data-stu-id="7ced6-114">Methods</span></span>

<span data-ttu-id="7ced6-115">**INapSystemHealthAgentBinding2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="7ced6-115">The **INapSystemHealthAgentBinding2** interface has these methods.</span></span>



| <span data-ttu-id="7ced6-116">方法</span><span class="sxs-lookup"><span data-stu-id="7ced6-116">Method</span></span>                                                                                                                    | <span data-ttu-id="7ced6-117">描述</span><span class="sxs-lookup"><span data-stu-id="7ced6-117">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7ced6-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="7ced6-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span></span>](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | <span data-ttu-id="7ced6-119">由 Sha 呼叫以判斷系統隔離狀態和擴充的隔離狀態。</span><span class="sxs-lookup"><span data-stu-id="7ced6-119">Called by SHAs to determine the system isolation state and extended isolation state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ced6-120">備註</span><span class="sxs-lookup"><span data-stu-id="7ced6-120">Remarks</span></span>

<span data-ttu-id="7ced6-121">如果 NapAgent 已停止，此介面中的所有 Api 都會傳回 **RPC \_ E \_ 中斷** 連線。</span><span class="sxs-lookup"><span data-stu-id="7ced6-121">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="7ced6-122">這個物件會在重新開機後自動復原並重新系結至 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="7ced6-122">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ced6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="7ced6-123">Requirements</span></span>



| <span data-ttu-id="7ced6-124">需求</span><span class="sxs-lookup"><span data-stu-id="7ced6-124">Requirement</span></span> | <span data-ttu-id="7ced6-125">值</span><span class="sxs-lookup"><span data-stu-id="7ced6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ced6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7ced6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7ced6-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ced6-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7ced6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7ced6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7ced6-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7ced6-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7ced6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="7ced6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ced6-131"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="7ced6-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ced6-132">Idl</span><span class="sxs-lookup"><span data-stu-id="7ced6-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ced6-133"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ced6-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="7ced6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7ced6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ced6-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ced6-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7ced6-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7ced6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ced6-137">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="7ced6-137">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> <dt>

[<span data-ttu-id="7ced6-138">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="7ced6-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="7ced6-139">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="7ced6-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





