---
title: 'INapSystemHealthAgentBinding 解除初始化方法 (NapSystemHealthAgent .h) '
description: 導致 NapAgent 釋出其所有對系統健康情況代理程式 COM 指標的參考。
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- 解除初始化方法 NAP
- 解除初始化方法 NAP，INapSystemHealthAgentBinding 介面
- INapSystemHealthAgentBinding 介面 NAP，解除初始化方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991776"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a><span data-ttu-id="d4ebf-106">INapSystemHealthAgentBinding：：解除初始化方法</span><span class="sxs-lookup"><span data-stu-id="d4ebf-106">INapSystemHealthAgentBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="d4ebf-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="d4ebf-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d4ebf-108">**INapSystemHealthAgentBinding：：解除初始化** 方法會使 NapAgent 釋放對系統健康情況代理程式 COM 指標的所有參考。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-108">The **INapSystemHealthAgentBinding::Uninitialize** method causes the NapAgent to release all its references to system health agent COM pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ebf-109">語法</span><span class="sxs-lookup"><span data-stu-id="d4ebf-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="d4ebf-110">參數</span><span class="sxs-lookup"><span data-stu-id="d4ebf-110">Parameters</span></span>

<span data-ttu-id="d4ebf-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d4ebf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4ebf-112">Return value</span></span>

<span data-ttu-id="d4ebf-113">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d4ebf-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d4ebf-114">Return code</span></span>                                                                                             | <span data-ttu-id="d4ebf-115">Description</span><span class="sxs-lookup"><span data-stu-id="d4ebf-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4ebf-116"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebf-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="d4ebf-117">作業成功。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="d4ebf-118"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebf-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="d4ebf-119">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="d4ebf-120"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebf-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="d4ebf-121">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="d4ebf-122"><dt>**NAP \_ E \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebf-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="d4ebf-123">SHA 先前尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="d4ebf-124"><dt>**RPC \_ E \_ 中斷連接**</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebf-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="d4ebf-125">NapAgent 已停止。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="d4ebf-126">這個物件會在重新開機後自動復原並重新系結至 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d4ebf-127">備註</span><span class="sxs-lookup"><span data-stu-id="d4ebf-127">Remarks</span></span>

<span data-ttu-id="d4ebf-128">NapAgent 會封鎖此方法呼叫的執行，直到系結和回呼介面上所有現有的呼叫都完成為止。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-128">The NapAgent blocks execution of this method call until all existing calls on the Binding and Callback interfaces complete.</span></span>

<span data-ttu-id="d4ebf-129">SHA 必須在呼叫這個方法或 [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)介面的任何其他方法之前呼叫 [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="d4ebf-129">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4ebf-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4ebf-130">Requirements</span></span>



| <span data-ttu-id="d4ebf-131">需求</span><span class="sxs-lookup"><span data-stu-id="d4ebf-131">Requirement</span></span> | <span data-ttu-id="d4ebf-132">值</span><span class="sxs-lookup"><span data-stu-id="d4ebf-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ebf-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4ebf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d4ebf-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4ebf-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d4ebf-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4ebf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d4ebf-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4ebf-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d4ebf-137">標頭</span><span class="sxs-lookup"><span data-stu-id="d4ebf-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4ebf-138"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebf-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4ebf-139">Idl</span><span class="sxs-lookup"><span data-stu-id="d4ebf-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4ebf-140"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebf-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="d4ebf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d4ebf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4ebf-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4ebf-142"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="d4ebf-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4ebf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ebf-144">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="d4ebf-144">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





