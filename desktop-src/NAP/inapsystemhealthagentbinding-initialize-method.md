---
title: 'INapSystemHealthAgentBinding Initialize 方法 (NapSystemHealthAgent .h) '
description: 將系統健全狀況代理程式初始化 (SHA) ，並將 SHA 系結至 NapAgent 服務。
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Initialize 方法 NAP
- Initialize 方法 NAP，INapSystemHealthAgentBinding 介面
- INapSystemHealthAgentBinding 介面 NAP，Initialize 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317132"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a><span data-ttu-id="db854-106">INapSystemHealthAgentBinding：： Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="db854-106">INapSystemHealthAgentBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="db854-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="db854-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="db854-108">**INapSystemHealthAgentBinding：： Initialize** 方法會將系統健全狀況代理程式初始化 (sha) ，並將 sha 系結至 NapAgent 服務。</span><span class="sxs-lookup"><span data-stu-id="db854-108">The **INapSystemHealthAgentBinding::Initialize** method initializes the system health agent (SHA) and binds the SHA to the NapAgent service.</span></span> <span data-ttu-id="db854-109">在呼叫 [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) 介面上的任何其他方法之前，必須先呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="db854-109">This method must be called before calling any other method on the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="db854-110">語法</span><span class="sxs-lookup"><span data-stu-id="db854-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="db854-111">參數</span><span class="sxs-lookup"><span data-stu-id="db854-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db854-112"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="db854-112">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db854-113">包含系結至 NapAgent 服務之 SHA 識別碼的唯一 [SystemHealthEntityId](nap-datatypes.md) 。</span><span class="sxs-lookup"><span data-stu-id="db854-113">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA being bound to the NapAgent service.</span></span>

</dd> <dt>

<span data-ttu-id="db854-114">*回呼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db854-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db854-115">[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)介面的 COM 指標，由 NapAgent 用來以通知/進程回呼健康情況代理程式。</span><span class="sxs-lookup"><span data-stu-id="db854-115">A COM pointer to an [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) interface used by the NapAgent to callback the health agent with a notify/process.</span></span> <span data-ttu-id="db854-116">NapAgent 會保存與這個介面相關聯之物件的參考，直到呼叫解除 [**初始化**](inapsystemhealthagentbinding-uninitialize-method.md) 為止。</span><span class="sxs-lookup"><span data-stu-id="db854-116">The NapAgent holds a reference to the object associated with this interface until [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db854-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="db854-117">Return value</span></span>

<span data-ttu-id="db854-118">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="db854-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="db854-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="db854-119">Return code</span></span>                                                                                                | <span data-ttu-id="db854-120">Description</span><span class="sxs-lookup"><span data-stu-id="db854-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db854-121"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="db854-121"><dt>**S\_OK** </dt></span></span> </dl>                      | <span data-ttu-id="db854-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="db854-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="db854-123"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="db854-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>            | <span data-ttu-id="db854-124">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="db854-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="db854-125"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="db854-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>             | <span data-ttu-id="db854-126">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="db854-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="db854-127"><dt>**錯誤 \_ 已 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="db854-127"><dt>**ERROR\_ALREADY\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="db854-128">如果 SHA 先前已初始化，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="db854-128">If the SHA has initialized previously, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="db854-129"><dt>**NAP \_ E \_ 未 \_ 註冊**</dt></span><span class="sxs-lookup"><span data-stu-id="db854-129"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>     | <span data-ttu-id="db854-130">如果 SHA 尚未註冊，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="db854-130">If the SHA has not registered earlier, this error is returned.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="db854-131"><dt>**RPC \_ E \_ 中斷連接**</dt></span><span class="sxs-lookup"><span data-stu-id="db854-131"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>        | <span data-ttu-id="db854-132">NapAgent 已停止。</span><span class="sxs-lookup"><span data-stu-id="db854-132">The NapAgent has been stopped.</span></span> <span data-ttu-id="db854-133">這個物件會在重新開機後自動復原並重新系結至 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="db854-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db854-134">備註</span><span class="sxs-lookup"><span data-stu-id="db854-134">Remarks</span></span>

<span data-ttu-id="db854-135">NapAgent 不會觸發 SoH 交換作為初始化的結果。</span><span class="sxs-lookup"><span data-stu-id="db854-135">The NapAgent does not trigger a SoH exchange as a result of initialization.</span></span> <span data-ttu-id="db854-136">系統健康狀態代理程式必須呼叫 [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) ，以要求在使用 NapAgent 初始化之後交換 SoH 封包。</span><span class="sxs-lookup"><span data-stu-id="db854-136">A system health agent must call [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) to request an exchange of SoH packets after initializing with the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="db854-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="db854-137">Requirements</span></span>



| <span data-ttu-id="db854-138">需求</span><span class="sxs-lookup"><span data-stu-id="db854-138">Requirement</span></span> | <span data-ttu-id="db854-139">值</span><span class="sxs-lookup"><span data-stu-id="db854-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db854-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db854-140">Minimum supported client</span></span><br/> | <span data-ttu-id="db854-141">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db854-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="db854-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db854-142">Minimum supported server</span></span><br/> | <span data-ttu-id="db854-143">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db854-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="db854-144">標頭</span><span class="sxs-lookup"><span data-stu-id="db854-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="db854-145"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="db854-145"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="db854-146">Idl</span><span class="sxs-lookup"><span data-stu-id="db854-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db854-147"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="db854-147"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="db854-148">DLL</span><span class="sxs-lookup"><span data-stu-id="db854-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db854-149"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db854-149"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="db854-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db854-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db854-151">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="db854-151">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





