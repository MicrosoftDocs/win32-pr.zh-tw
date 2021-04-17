---
title: 'INapEnforcementClientBinding NotifySoHChangeFailure 方法 (NapEnforcementClient .h) '
description: 由強制用戶端用來通知 NapAgent，它無法處理先前的 INapEnforcementClientCallback NotifySoHChange。
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- NotifySoHChangeFailure 方法 NAP
- NotifySoHChangeFailure 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，NotifySoHChangeFailure 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af23fd41e5a8b97064c089062eae13e93cf9ff0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467005"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a><span data-ttu-id="affa5-106">INapEnforcementClientBinding：： NotifySoHChangeFailure 方法</span><span class="sxs-lookup"><span data-stu-id="affa5-106">INapEnforcementClientBinding::NotifySoHChangeFailure method</span></span>

> [!Note]  
> <span data-ttu-id="affa5-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="affa5-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="affa5-108">**INapEnforcementClientBinding：： NotifySoHChangeFailure** 方法是由強制用戶端用來通知 NapAgent 它無法處理先前的 [**INapEnforcementClientCallback：： NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)。</span><span class="sxs-lookup"><span data-stu-id="affa5-108">The **INapEnforcementClientBinding::NotifySoHChangeFailure** method is used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="affa5-109">語法</span><span class="sxs-lookup"><span data-stu-id="affa5-109">Syntax</span></span>


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a><span data-ttu-id="affa5-110">參數</span><span class="sxs-lookup"><span data-stu-id="affa5-110">Parameters</span></span>

<span data-ttu-id="affa5-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="affa5-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="affa5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="affa5-112">Return value</span></span>

<span data-ttu-id="affa5-113">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="affa5-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="affa5-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="affa5-114">Return code</span></span>                                                                                             | <span data-ttu-id="affa5-115">Description</span><span class="sxs-lookup"><span data-stu-id="affa5-115">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="affa5-116"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="affa5-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="affa5-117">作業成功。</span><span class="sxs-lookup"><span data-stu-id="affa5-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="affa5-118"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="affa5-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="affa5-119">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="affa5-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="affa5-120"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="affa5-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="affa5-121">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="affa5-121">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="affa5-122"><dt>**NAP \_ E \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="affa5-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="affa5-123">Enforcer 先前尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="affa5-123">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="affa5-124">備註</span><span class="sxs-lookup"><span data-stu-id="affa5-124">Remarks</span></span>

<span data-ttu-id="affa5-125">由於這個方法會呼叫 [**INapEnforcementClientCallback：： NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) ，因此在稍後呼叫 NapAgent 時，會重新嘗試套用 SoH 變更。</span><span class="sxs-lookup"><span data-stu-id="affa5-125">As a result of this method call the NapAgent retries applying the SoH change at a later time by calling [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md) again.</span></span> <span data-ttu-id="affa5-126">一旦強制用戶端呼叫 [**INapEnforcementClientBinding：： GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)之後，就必須套用變更，也就是在這個時間點之後，NapAgent 不會處理任何失敗。</span><span class="sxs-lookup"><span data-stu-id="affa5-126">Once the enforcement client has called [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md), it then must apply the change, i.e. no failures are handled by the NapAgent after this point.</span></span>

<span data-ttu-id="affa5-127">強制用戶端必須先呼叫 [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md) 方法，才能呼叫這個或 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="affa5-127">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="affa5-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="affa5-128">Requirements</span></span>



| <span data-ttu-id="affa5-129">需求</span><span class="sxs-lookup"><span data-stu-id="affa5-129">Requirement</span></span> | <span data-ttu-id="affa5-130">值</span><span class="sxs-lookup"><span data-stu-id="affa5-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="affa5-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="affa5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="affa5-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="affa5-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="affa5-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="affa5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="affa5-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="affa5-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="affa5-135">標頭</span><span class="sxs-lookup"><span data-stu-id="affa5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="affa5-136"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="affa5-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="affa5-137">Idl</span><span class="sxs-lookup"><span data-stu-id="affa5-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="affa5-138"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="affa5-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="affa5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="affa5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="affa5-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="affa5-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="affa5-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="affa5-141">See also</span></span>

<dl> <span data-ttu-id="affa5-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="affa5-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="affa5-143">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="affa5-143">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="affa5-144">**INapEnforcementClientBinding::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="affa5-144">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[<span data-ttu-id="affa5-145">**INapEnforcementClientCallback::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="affa5-145">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





