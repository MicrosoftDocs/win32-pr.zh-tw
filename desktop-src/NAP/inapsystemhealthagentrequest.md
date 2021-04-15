---
title: 'INapSystemHealthAgentRequest 介面 (NapSystemHealthAgent .h) '
description: Sha 用來與 NAP 系統通訊和協調處理。
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- INapSystemHealthAgentRequest 介面 NAP
- INapSystemHealthAgentRequest 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508527"
---
# <a name="inapsystemhealthagentrequest-interface"></a><span data-ttu-id="65655-105">INapSystemHealthAgentRequest 介面</span><span class="sxs-lookup"><span data-stu-id="65655-105">INapSystemHealthAgentRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="65655-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="65655-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="65655-107">**INapSystemHealthAgentRequest** 介面提供 sha 用來與 NAP 系統進行通訊和協調處理的方法。</span><span class="sxs-lookup"><span data-stu-id="65655-107">The **INapSystemHealthAgentRequest** interface provides methods that SHAs use to communicate and coordinate processing with the NAP system.</span></span>

## <a name="members"></a><span data-ttu-id="65655-108">成員</span><span class="sxs-lookup"><span data-stu-id="65655-108">Members</span></span>

<span data-ttu-id="65655-109">**INapSystemHealthAgentRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="65655-109">The **INapSystemHealthAgentRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="65655-110">**INapSystemHealthAgentRequest** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="65655-110">**INapSystemHealthAgentRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="65655-111">方法</span><span class="sxs-lookup"><span data-stu-id="65655-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="65655-112">方法</span><span class="sxs-lookup"><span data-stu-id="65655-112">Methods</span></span>

<span data-ttu-id="65655-113">**INapSystemHealthAgentRequest** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="65655-113">The **INapSystemHealthAgentRequest** interface has these methods.</span></span>



| <span data-ttu-id="65655-114">方法</span><span class="sxs-lookup"><span data-stu-id="65655-114">Method</span></span>                                                                                                                     | <span data-ttu-id="65655-115">描述</span><span class="sxs-lookup"><span data-stu-id="65655-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65655-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span><span class="sxs-lookup"><span data-stu-id="65655-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span></span>](inapsystemhealthagentrequest-getcachesohflag-method.md)               | <span data-ttu-id="65655-117">僅供 NapAgent 使用。</span><span class="sxs-lookup"><span data-stu-id="65655-117">Used only by the NapAgent.</span></span><br/>                                                            |
| [<span data-ttu-id="65655-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="65655-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span></span>](inapsystemhealthagentrequest-getcorrelationid-method.md)             | <span data-ttu-id="65655-119">由系統健康情況代理程式用來讓 Soh 和 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)相互關聯。</span><span class="sxs-lookup"><span data-stu-id="65655-119">Used by system health agents to correlate SoHs and [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/> |
| [<span data-ttu-id="65655-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="65655-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span></span>](inapsystemhealthagentrequest-getsohrequest-method.md)                   | <span data-ttu-id="65655-121">由 Sha 用來取得 NapAgent 先前快取的 Soh。</span><span class="sxs-lookup"><span data-stu-id="65655-121">Used by SHAs to get SoHs previously cached by the NapAgent.</span></span><br/>                           |
| [<span data-ttu-id="65655-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="65655-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span></span>](inapsystemhealthagentrequest-getsohresponse-method.md)                 | <span data-ttu-id="65655-123">供 health 代理程式用來取出其 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)。</span><span class="sxs-lookup"><span data-stu-id="65655-123">Used by the health agent to retrieve their [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/>         |
| [<span data-ttu-id="65655-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="65655-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span></span>](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | <span data-ttu-id="65655-125">由系統健康情況代理程式用來記錄相互關聯識別碼。</span><span class="sxs-lookup"><span data-stu-id="65655-125">Used by system health agents to log the correlation ID.</span></span><br/>                               |
| [<span data-ttu-id="65655-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="65655-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span></span>](inapsystemhealthagentrequest-setsohrequest-method.md)                   | <span data-ttu-id="65655-127">供健康情況代理程式用來寫入其 SoH 要求。</span><span class="sxs-lookup"><span data-stu-id="65655-127">Used by health agents to write their SoH request.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="65655-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="65655-128">Requirements</span></span>



| <span data-ttu-id="65655-129">需求</span><span class="sxs-lookup"><span data-stu-id="65655-129">Requirement</span></span> | <span data-ttu-id="65655-130">值</span><span class="sxs-lookup"><span data-stu-id="65655-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65655-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65655-131">Minimum supported client</span></span><br/> | <span data-ttu-id="65655-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65655-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="65655-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65655-133">Minimum supported server</span></span><br/> | <span data-ttu-id="65655-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65655-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="65655-135">標頭</span><span class="sxs-lookup"><span data-stu-id="65655-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="65655-136"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="65655-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="65655-137">Idl</span><span class="sxs-lookup"><span data-stu-id="65655-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65655-138"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="65655-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="65655-139">DLL</span><span class="sxs-lookup"><span data-stu-id="65655-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65655-140"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65655-140"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="65655-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65655-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65655-142">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="65655-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="65655-143">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="65655-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

