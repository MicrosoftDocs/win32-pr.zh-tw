---
title: 'INapSystemHealthAgentBinding NotifySoHChange 方法 (NapSystemHealthAgent .h) '
description: Sha 會在其 SoH 變更時使用。
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- NotifySoHChange 方法 NAP
- NotifySoHChange 方法 NAP，INapSystemHealthAgentBinding 介面
- INapSystemHealthAgentBinding 介面 NAP，NotifySoHChange 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509355"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a><span data-ttu-id="c7553-106">INapSystemHealthAgentBinding：： NotifySoHChange 方法</span><span class="sxs-lookup"><span data-stu-id="c7553-106">INapSystemHealthAgentBinding::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="c7553-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="c7553-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c7553-108">**INapSystemHealthAgentBinding：： NotifySoHChange** 方法是在其 SoH 變更時由 sha 使用。</span><span class="sxs-lookup"><span data-stu-id="c7553-108">The **INapSystemHealthAgentBinding::NotifySoHChange** method is used by SHAs when their SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7553-109">語法</span><span class="sxs-lookup"><span data-stu-id="c7553-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="c7553-110">參數</span><span class="sxs-lookup"><span data-stu-id="c7553-110">Parameters</span></span>

<span data-ttu-id="c7553-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c7553-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c7553-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7553-112">Return value</span></span>

<span data-ttu-id="c7553-113">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c7553-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c7553-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c7553-114">Return code</span></span>                                                                                             | <span data-ttu-id="c7553-115">Description</span><span class="sxs-lookup"><span data-stu-id="c7553-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7553-116"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c7553-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="c7553-117">作業成功。</span><span class="sxs-lookup"><span data-stu-id="c7553-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="c7553-118"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c7553-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="c7553-119">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="c7553-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="c7553-120"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c7553-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="c7553-121">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="c7553-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="c7553-122"><dt>**NAP \_ E \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="c7553-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="c7553-123">SHA 先前尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="c7553-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="c7553-124"><dt>**RPC \_ E \_ 中斷連接**</dt></span><span class="sxs-lookup"><span data-stu-id="c7553-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="c7553-125">NapAgent 已停止。</span><span class="sxs-lookup"><span data-stu-id="c7553-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="c7553-126">這個物件會在重新開機後自動復原並重新系結至 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="c7553-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7553-127">備註</span><span class="sxs-lookup"><span data-stu-id="c7553-127">Remarks</span></span>

<span data-ttu-id="c7553-128">Sha 不能呼叫此 API 推測式運算，因為它會在網路上產生 SoH 交換。</span><span class="sxs-lookup"><span data-stu-id="c7553-128">SHAs must not call this API speculatively since it results in an SoH exchange on the wire.</span></span> <span data-ttu-id="c7553-129">只有在必要時，才應該進行此 API 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c7553-129">Calls to this API should only be made when necessary.</span></span>

<span data-ttu-id="c7553-130">NapAgent 不會保留這個執行緒來處理 SoH 變更。</span><span class="sxs-lookup"><span data-stu-id="c7553-130">The NapAgent does not hold this thread to process the SoH change.</span></span> <span data-ttu-id="c7553-131">相反地，它會立即返回，並以非同步方式處理變更。</span><span class="sxs-lookup"><span data-stu-id="c7553-131">Instead, it returns immediately and processes the change asynchronously.</span></span>

<span data-ttu-id="c7553-132">SHA 必須在呼叫這個方法或 [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)介面的任何其他方法之前呼叫 [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="c7553-132">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7553-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7553-133">Requirements</span></span>



| <span data-ttu-id="c7553-134">需求</span><span class="sxs-lookup"><span data-stu-id="c7553-134">Requirement</span></span> | <span data-ttu-id="c7553-135">值</span><span class="sxs-lookup"><span data-stu-id="c7553-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7553-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7553-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c7553-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7553-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c7553-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7553-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c7553-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7553-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c7553-140">標頭</span><span class="sxs-lookup"><span data-stu-id="c7553-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7553-141"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="c7553-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7553-142">Idl</span><span class="sxs-lookup"><span data-stu-id="c7553-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7553-143"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7553-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="c7553-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c7553-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7553-145"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7553-145"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c7553-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7553-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7553-147">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="c7553-147">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





