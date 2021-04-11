---
title: 'INapEnforcementClientBinding 介面 (NapEnforcementClient .h) '
description: 強制用戶端用來與 NapAgent 通訊。
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- INapEnforcementClientBinding 介面 NAP
- INapEnforcementClientBinding 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844356"
---
# <a name="inapenforcementclientbinding-interface"></a><span data-ttu-id="8ca4d-105">INapEnforcementClientBinding 介面</span><span class="sxs-lookup"><span data-stu-id="8ca4d-105">INapEnforcementClientBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="8ca4d-106">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="8ca4d-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8ca4d-107">**INapEnforcementClientBinding** 會提供強制用戶端用來與 NapAgent 進行通訊的方法。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-107">The **INapEnforcementClientBinding** provides methods that enforcement clients use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="8ca4d-108">成員</span><span class="sxs-lookup"><span data-stu-id="8ca4d-108">Members</span></span>

<span data-ttu-id="8ca4d-109">**INapEnforcementClientBinding** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-109">The **INapEnforcementClientBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8ca4d-110">**INapEnforcementClientBinding** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8ca4d-110">**INapEnforcementClientBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="8ca4d-111">方法</span><span class="sxs-lookup"><span data-stu-id="8ca4d-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8ca4d-112">方法</span><span class="sxs-lookup"><span data-stu-id="8ca4d-112">Methods</span></span>

<span data-ttu-id="8ca4d-113">**INapEnforcementClientBinding** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-113">The **INapEnforcementClientBinding** interface has these methods.</span></span>



| <span data-ttu-id="8ca4d-114">方法</span><span class="sxs-lookup"><span data-stu-id="8ca4d-114">Method</span></span>                                                                                                                           | <span data-ttu-id="8ca4d-115">描述</span><span class="sxs-lookup"><span data-stu-id="8ca4d-115">Description</span></span>                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ca4d-116">**INapEnforcementClientBinding：： CreateConnection**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-116">**INapEnforcementClientBinding::CreateConnection**</span></span>](inapenforcementclientbinding-createconnection-method.md)                   | <span data-ttu-id="8ca4d-117">供 enforcers 用來建立連線物件。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-117">Used by enforcers to create connection objects.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="8ca4d-118">**INapEnforcementClientBinding::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-118">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)                         | <span data-ttu-id="8ca4d-119">在強制用戶端需要特定連接的 SoH 要求時使用。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-119">Used by the enforcement client when it needs an SoH-request for a particular connection.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="8ca4d-120">**INapEnforcementClientBinding：： Initialize**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-120">**INapEnforcementClientBinding::Initialize**</span></span>](inapenforcementclientbinding-initialize-method.md)                               | <span data-ttu-id="8ca4d-121">啟動 NapAgent 服務。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-121">Starts up the NapAgent service.</span></span> <span data-ttu-id="8ca4d-122">強制用戶端必須先呼叫這個方法，然後再呼叫這個介面的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-122">The enforcement client must call this method before calling any other method of this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="8ca4d-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | <span data-ttu-id="8ca4d-124">用來通知 NapAgent，與強制用戶端的連接已關閉。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-124">Used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="8ca4d-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span></span>](inapenforcementclientbinding-notifysohchangefailure-method.md)       | <span data-ttu-id="8ca4d-126">由強制用戶端用來通知 NapAgent，它無法處理先前的 [**INapEnforcementClientCallback：： NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-126">Used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span><br/> |
| [<span data-ttu-id="8ca4d-127">**INapEnforcementClientBinding：:P rocessSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-127">**INapEnforcementClientBinding::ProcessSoHResponse**</span></span>](inapenforcementclientbinding-processsohresponse-method.md)               | <span data-ttu-id="8ca4d-128">在強制用戶端從強制服務器取得 SoH-Response 資料 blob 時使用。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-128">Used by enforcement clients whenever they get an SoH-Response data blob from the enforcement server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="8ca4d-129">**INapEnforcementClientBinding：：解除初始化**</span><span class="sxs-lookup"><span data-stu-id="8ca4d-129">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)                           | <span data-ttu-id="8ca4d-130">結束此用戶端連接的 NapAgent 服務。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-130">Concludes the NapAgent service for this client connection.</span></span><br/>                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="8ca4d-131">備註</span><span class="sxs-lookup"><span data-stu-id="8ca4d-131">Remarks</span></span>

<span data-ttu-id="8ca4d-132">\_如果 NapAgent 已停止，此介面中的所有 api 都會傳回 RPC E \_ 中斷連線。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-132">All the APIs in this interface will return RPC\_E\_DISCONNECTED if the NapAgent is stopped.</span></span> <span data-ttu-id="8ca4d-133">這個物件會在重新開機後自動復原並重新系結至 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="8ca4d-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca4d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ca4d-134">Requirements</span></span>



| <span data-ttu-id="8ca4d-135">需求</span><span class="sxs-lookup"><span data-stu-id="8ca4d-135">Requirement</span></span> | <span data-ttu-id="8ca4d-136">值</span><span class="sxs-lookup"><span data-stu-id="8ca4d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca4d-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ca4d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca4d-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ca4d-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8ca4d-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ca4d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca4d-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ca4d-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8ca4d-141">標頭</span><span class="sxs-lookup"><span data-stu-id="8ca4d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ca4d-142"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca4d-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ca4d-143">Idl</span><span class="sxs-lookup"><span data-stu-id="8ca4d-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ca4d-144"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ca4d-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="8ca4d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8ca4d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ca4d-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ca4d-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="8ca4d-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ca4d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca4d-148">NAP 介面</span><span class="sxs-lookup"><span data-stu-id="8ca4d-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8ca4d-149">NAP 參考</span><span class="sxs-lookup"><span data-stu-id="8ca4d-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

