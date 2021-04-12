---
title: 'INapEnforcementClientBinding NotifyConnectionStateDown 方法 (NapEnforcementClient .h) '
description: 用來通知 NapAgent，與強制用戶端的連接已關閉。
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- NotifyConnectionStateDown 方法 NAP
- NotifyConnectionStateDown 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，NotifyConnectionStateDown 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509482"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a><span data-ttu-id="ba24c-106">INapEnforcementClientBinding：： NotifyConnectionStateDown 方法</span><span class="sxs-lookup"><span data-stu-id="ba24c-106">INapEnforcementClientBinding::NotifyConnectionStateDown method</span></span>

> [!Note]  
> <span data-ttu-id="ba24c-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="ba24c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ba24c-108">**INapEnforcementClientBinding：： NotifyConnectionStateDown** 方法是用來通知 NapAgent 與強制用戶端的連接已關閉。</span><span class="sxs-lookup"><span data-stu-id="ba24c-108">The **INapEnforcementClientBinding::NotifyConnectionStateDown** method is used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba24c-109">語法</span><span class="sxs-lookup"><span data-stu-id="ba24c-109">Syntax</span></span>


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a><span data-ttu-id="ba24c-110">參數</span><span class="sxs-lookup"><span data-stu-id="ba24c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba24c-111">*downCxn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ba24c-111">*downCxn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba24c-112">向下連接之 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 介面的 COM 指標。</span><span class="sxs-lookup"><span data-stu-id="ba24c-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the down connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba24c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba24c-113">Return value</span></span>

<span data-ttu-id="ba24c-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ba24c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ba24c-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ba24c-115">Return code</span></span>                                                                                             | <span data-ttu-id="ba24c-116">Description</span><span class="sxs-lookup"><span data-stu-id="ba24c-116">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba24c-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ba24c-117"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="ba24c-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ba24c-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="ba24c-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ba24c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="ba24c-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="ba24c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ba24c-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ba24c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="ba24c-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="ba24c-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ba24c-123"><dt>**NAP \_ E \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="ba24c-123"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="ba24c-124">Enforcer 先前尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="ba24c-124">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="ba24c-125">備註</span><span class="sxs-lookup"><span data-stu-id="ba24c-125">Remarks</span></span>

<span data-ttu-id="ba24c-126">當強制用戶端所建立的任何連線中斷時，強制用戶端應該從其使用中清單移除連線，並使用這個方法通知 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="ba24c-126">When any of the connections established by an enforcement client go down, the enforcement client should remove the connection from its active list and inform the NapAgent using this method.</span></span> <span data-ttu-id="ba24c-127">當這個呼叫傳回時，就可以釋出和釋放連線物件。</span><span class="sxs-lookup"><span data-stu-id="ba24c-127">As soon as this call returns, the connection object can be released and freed.</span></span> <span data-ttu-id="ba24c-128">NapAgent 不會保留連線物件的參考。</span><span class="sxs-lookup"><span data-stu-id="ba24c-128">The NapAgent will not hold references to the connection object.</span></span>

<span data-ttu-id="ba24c-129">由於此通知，NapAgent 會適當地更新其系統 NAP 狀態。</span><span class="sxs-lookup"><span data-stu-id="ba24c-129">As a result of this notification, the NapAgent updates its system NAP state as appropriate.</span></span>

<span data-ttu-id="ba24c-130">強制用戶端必須先呼叫 [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md) 方法，才能呼叫這個或 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="ba24c-130">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba24c-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba24c-131">Requirements</span></span>



| <span data-ttu-id="ba24c-132">需求</span><span class="sxs-lookup"><span data-stu-id="ba24c-132">Requirement</span></span> | <span data-ttu-id="ba24c-133">值</span><span class="sxs-lookup"><span data-stu-id="ba24c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba24c-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba24c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ba24c-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba24c-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ba24c-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ba24c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ba24c-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ba24c-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ba24c-138">標頭</span><span class="sxs-lookup"><span data-stu-id="ba24c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba24c-139"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="ba24c-139"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba24c-140">Idl</span><span class="sxs-lookup"><span data-stu-id="ba24c-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ba24c-141"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ba24c-141"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="ba24c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ba24c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba24c-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba24c-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ba24c-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba24c-144">See also</span></span>

<dl> <span data-ttu-id="ba24c-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ba24c-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="ba24c-146">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="ba24c-146">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





