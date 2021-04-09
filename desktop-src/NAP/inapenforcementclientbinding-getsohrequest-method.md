---
title: 'INapEnforcementClientBinding GetSoHRequest 方法 (NapEnforcementClient .h) '
description: 由強制用戶端用來取得特定連接的 SoH 要求。
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- GetSoHRequest 方法 NAP
- GetSoHRequest 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，GetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9fed4872df7ab328ab241b070a9eeb07907de85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934167"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a><span data-ttu-id="c9cf3-106">INapEnforcementClientBinding：： GetSoHRequest 方法</span><span class="sxs-lookup"><span data-stu-id="c9cf3-106">INapEnforcementClientBinding::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="c9cf3-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="c9cf3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c9cf3-108">**INapEnforcementClientBinding：： GetSoHRequest** 方法是由強制用戶端用來取得特定連接的 SoH 要求。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-108">The **INapEnforcementClientBinding::GetSoHRequest** method is used by the enforcement client to retrieve an SoH-request for a particular connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9cf3-109">語法</span><span class="sxs-lookup"><span data-stu-id="c9cf3-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a><span data-ttu-id="c9cf3-110">參數</span><span class="sxs-lookup"><span data-stu-id="c9cf3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9cf3-111">*連接* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9cf3-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9cf3-112">[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)介面的 COM 指標。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-112">A COM pointer to an [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface.</span></span> <span data-ttu-id="c9cf3-113">在方法完成之後，NapAgent 不會保留與這個介面相關聯之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-113">The NapAgent does not hold references to the object associated with this interface after the method completes.</span></span>

</dd> <dt>

<span data-ttu-id="c9cf3-114">*retriggerHint* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c9cf3-114">*retriggerHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9cf3-115">**布林** 值的指標，指出是否應該重新觸發連接。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-115">A pointer to a **BOOL** that indicates if the connection should be re-triggered.</span></span> <span data-ttu-id="c9cf3-116">如果自上次呼叫此函式之後，或 [**ProbationTime**](nap-datatypes.md)已過期， [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)已變更，則為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-116">It is **TRUE** if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) has changed since this function was last called or if [**ProbationTime**](nap-datatypes.md) has expired.</span></span> <span data-ttu-id="c9cf3-117">否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-117">Otherwise, **FALSE** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9cf3-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9cf3-118">Return value</span></span>

<span data-ttu-id="c9cf3-119">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c9cf3-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c9cf3-120">Return code</span></span>                                                                                             | <span data-ttu-id="c9cf3-121">Description</span><span class="sxs-lookup"><span data-stu-id="c9cf3-121">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9cf3-122"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c9cf3-122"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="c9cf3-123">作業成功。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-123">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="c9cf3-124"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c9cf3-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="c9cf3-125">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c9cf3-126"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c9cf3-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="c9cf3-127">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-127">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c9cf3-128"><dt>**NAP \_ E \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="c9cf3-128"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="c9cf3-129">Enforcer 先前尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-129">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="c9cf3-130">備註</span><span class="sxs-lookup"><span data-stu-id="c9cf3-130">Remarks</span></span>

<span data-ttu-id="c9cf3-131">NapAgent 會在連線物件上設定 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-131">The NapAgent sets the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the connection object.</span></span>

<span data-ttu-id="c9cf3-132">如果這個連線上的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 未完成，則會捨棄它，而 sha 會收到孤立 **SoHRequests** 的通知。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-132">If an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) was outstanding on this connection, then it is discarded, and the SHAs are notified of orphaned **SoHRequests**.</span></span>

<span data-ttu-id="c9cf3-133">強制用戶端必須先呼叫 [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md) 方法，才能呼叫這個或 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="c9cf3-133">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9cf3-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9cf3-134">Requirements</span></span>



| <span data-ttu-id="c9cf3-135">需求</span><span class="sxs-lookup"><span data-stu-id="c9cf3-135">Requirement</span></span> | <span data-ttu-id="c9cf3-136">值</span><span class="sxs-lookup"><span data-stu-id="c9cf3-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9cf3-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9cf3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c9cf3-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9cf3-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c9cf3-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9cf3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c9cf3-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9cf3-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c9cf3-141">標頭</span><span class="sxs-lookup"><span data-stu-id="c9cf3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9cf3-142"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9cf3-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9cf3-143">Idl</span><span class="sxs-lookup"><span data-stu-id="c9cf3-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9cf3-144"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9cf3-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="c9cf3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c9cf3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9cf3-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9cf3-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c9cf3-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9cf3-147">See also</span></span>

<dl> <span data-ttu-id="c9cf3-148"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c9cf3-148"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="c9cf3-149">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="c9cf3-149">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





