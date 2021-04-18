---
title: 'INapEnforcementClientBinding 解除初始化方法 (NapEnforcementClient .h) '
description: 結束 NapAgent 服務。
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- 解除初始化方法 NAP
- 解除初始化方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，解除初始化方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965535"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a><span data-ttu-id="57bb4-106">INapEnforcementClientBinding：：解除初始化方法</span><span class="sxs-lookup"><span data-stu-id="57bb4-106">INapEnforcementClientBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="57bb4-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="57bb4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="57bb4-108">**INapEnforcementClientBinding：：解除初始化** 方法會結束 NapAgent 服務。</span><span class="sxs-lookup"><span data-stu-id="57bb4-108">The **INapEnforcementClientBinding::Uninitialize** method concludes the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="57bb4-109">語法</span><span class="sxs-lookup"><span data-stu-id="57bb4-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="57bb4-110">參數</span><span class="sxs-lookup"><span data-stu-id="57bb4-110">Parameters</span></span>

<span data-ttu-id="57bb4-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="57bb4-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="57bb4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="57bb4-112">Return value</span></span>

<span data-ttu-id="57bb4-113">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57bb4-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="57bb4-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="57bb4-114">Return code</span></span>                                                                                     | <span data-ttu-id="57bb4-115">Description</span><span class="sxs-lookup"><span data-stu-id="57bb4-115">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="57bb4-116"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="57bb4-116"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="57bb4-117">作業成功。</span><span class="sxs-lookup"><span data-stu-id="57bb4-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="57bb4-118"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="57bb4-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="57bb4-119">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="57bb4-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="57bb4-120"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="57bb4-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="57bb4-121">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="57bb4-121">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="57bb4-122">備註</span><span class="sxs-lookup"><span data-stu-id="57bb4-122">Remarks</span></span>

<span data-ttu-id="57bb4-123">NapAgent 會封鎖進一步處理，直到 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 和 [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) 介面上的所有現有呼叫都完成為止。</span><span class="sxs-lookup"><span data-stu-id="57bb4-123">The NapAgent blocks further processing until all existing calls on the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) and [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interfaces complete.</span></span> <span data-ttu-id="57bb4-124">在此通話結束時，NapAgent 會釋放其在強制用戶端 COM 指標上的所有參考。</span><span class="sxs-lookup"><span data-stu-id="57bb4-124">At the end of this call, the NapAgent releases all its references on enforcement client COM pointers.</span></span>

<span data-ttu-id="57bb4-125">在呼叫此函式之前，enforcer 必須在其所有使用中的連接上呼叫 [**INapEnforcementClientBinding：： NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) ，如此一來，如果任何 SoH-Requests 為孤立的，sha 就可以收到通知。</span><span class="sxs-lookup"><span data-stu-id="57bb4-125">Before this function is called, the enforcer must call [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) on all its active connections, so the SHAs can be notified if any of their SoH-Requests were orphaned.</span></span>

<span data-ttu-id="57bb4-126">強制用戶端必須先呼叫 [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md) 方法，才能呼叫這個或 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="57bb4-126">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="57bb4-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="57bb4-127">Requirements</span></span>



| <span data-ttu-id="57bb4-128">需求</span><span class="sxs-lookup"><span data-stu-id="57bb4-128">Requirement</span></span> | <span data-ttu-id="57bb4-129">值</span><span class="sxs-lookup"><span data-stu-id="57bb4-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57bb4-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57bb4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="57bb4-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57bb4-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="57bb4-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57bb4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="57bb4-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57bb4-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="57bb4-134">標頭</span><span class="sxs-lookup"><span data-stu-id="57bb4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="57bb4-135"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="57bb4-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="57bb4-136">Idl</span><span class="sxs-lookup"><span data-stu-id="57bb4-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57bb4-137"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="57bb4-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="57bb4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="57bb4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57bb4-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57bb4-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="57bb4-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57bb4-140">See also</span></span>

<dl> <span data-ttu-id="57bb4-141"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="57bb4-141"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="57bb4-142">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="57bb4-142">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="57bb4-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span><span class="sxs-lookup"><span data-stu-id="57bb4-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[<span data-ttu-id="57bb4-144">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="57bb4-144">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





