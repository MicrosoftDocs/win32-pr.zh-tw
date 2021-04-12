---
title: 'INapEnforcementClientBinding Initialize 方法 (NapEnforcementClient .h) '
description: 自動啟動 NapAgent 服務。
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Initialize 方法 NAP
- Initialize 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，Initialize 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464829"
---
# <a name="inapenforcementclientbindinginitialize-method"></a><span data-ttu-id="89c20-106">INapEnforcementClientBinding：： Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="89c20-106">INapEnforcementClientBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="89c20-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="89c20-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="89c20-108">**INapEnforcementClientBinding：： Initialize** 方法會自動啟動 NapAgent 服務。</span><span class="sxs-lookup"><span data-stu-id="89c20-108">The **INapEnforcementClientBinding::Initialize** method starts up the NapAgent service automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="89c20-109">語法</span><span class="sxs-lookup"><span data-stu-id="89c20-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="89c20-110">參數</span><span class="sxs-lookup"><span data-stu-id="89c20-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89c20-111"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="89c20-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c20-112">識別強制用戶端及其版本的 [**EnforcementEntityId**](nap-datatypes.md) 。</span><span class="sxs-lookup"><span data-stu-id="89c20-112">An [**EnforcementEntityId**](nap-datatypes.md) that identifies the enforcement client and its version.</span></span>

</dd> <dt>

<span data-ttu-id="89c20-113">*回呼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89c20-113">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c20-114">[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)介面的 COM 指標，由 NapAgent 用來以通知/進程回呼強制用戶端。</span><span class="sxs-lookup"><span data-stu-id="89c20-114">A COM pointer to an [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interface used by the NapAgent to callback the enforcement clients with notify/process.</span></span> <span data-ttu-id="89c20-115">NapAgent 會保存與這個介面相關聯之物件的參考，直到呼叫 [**INapEnforcementClientBinding：：解除初始化**](inapenforcementclientbinding-uninitialize-method.md) 為止。</span><span class="sxs-lookup"><span data-stu-id="89c20-115">The NapAgent holds a reference to the object associated with this interface until [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89c20-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="89c20-116">Return value</span></span>

<span data-ttu-id="89c20-117">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="89c20-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="89c20-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="89c20-118">Return code</span></span>                                                                                                         | <span data-ttu-id="89c20-119">Description</span><span class="sxs-lookup"><span data-stu-id="89c20-119">Description</span></span>                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89c20-120"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="89c20-120"><dt>**S\_OK** </dt></span></span> </dl>                               | <span data-ttu-id="89c20-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="89c20-121">The operation is successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="89c20-122"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="89c20-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>                     | <span data-ttu-id="89c20-123">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="89c20-123">Permissions error, access denied.</span></span><br/>                                             |
| <dl> <span data-ttu-id="89c20-124"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="89c20-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>                      | <span data-ttu-id="89c20-125">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="89c20-125">System resource limit, could not perform the operation.</span></span><br/>                       |
| <dl> <span data-ttu-id="89c20-126"><dt>**HRESULT (\_ 已初始化的錯誤 \_)**</dt></span><span class="sxs-lookup"><span data-stu-id="89c20-126"><dt>**HRESULT(ERROR\_ALREADY\_INITIALIZED)**</dt></span></span> </dl> | <span data-ttu-id="89c20-127">如果 enforcer 先前已初始化，則會傳回此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="89c20-127">If the enforcer has initialized previously, then this error code is returned.</span></span><br/> |
| <dl> <span data-ttu-id="89c20-128"><dt>**NAP \_ E \_ 未 \_ 註冊**</dt></span><span class="sxs-lookup"><span data-stu-id="89c20-128"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>              | <span data-ttu-id="89c20-129">如果 enforcer 之前未註冊，則會傳回此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="89c20-129">If the enforcer has not registered earlier, this error code is returned.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="89c20-130">備註</span><span class="sxs-lookup"><span data-stu-id="89c20-130">Remarks</span></span>

<span data-ttu-id="89c20-131">強制用戶端必須先呼叫 **INapEnforcementClientBinding：： Initialize** 方法，才能呼叫 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="89c20-131">The enforcement client must call the **INapEnforcementClientBinding::Initialize** method before calling any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c20-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="89c20-132">Requirements</span></span>



| <span data-ttu-id="89c20-133">需求</span><span class="sxs-lookup"><span data-stu-id="89c20-133">Requirement</span></span> | <span data-ttu-id="89c20-134">值</span><span class="sxs-lookup"><span data-stu-id="89c20-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c20-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89c20-135">Minimum supported client</span></span><br/> | <span data-ttu-id="89c20-136">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89c20-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="89c20-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89c20-137">Minimum supported server</span></span><br/> | <span data-ttu-id="89c20-138">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89c20-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="89c20-139">標頭</span><span class="sxs-lookup"><span data-stu-id="89c20-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="89c20-140"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="89c20-140"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="89c20-141">Idl</span><span class="sxs-lookup"><span data-stu-id="89c20-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="89c20-142"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="89c20-142"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="89c20-143">DLL</span><span class="sxs-lookup"><span data-stu-id="89c20-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89c20-144"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89c20-144"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="89c20-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89c20-145">See also</span></span>

<dl> <span data-ttu-id="89c20-146"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="89c20-146"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="89c20-147">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="89c20-147">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="89c20-148">**INapEnforcementClientBinding：：解除初始化**</span><span class="sxs-lookup"><span data-stu-id="89c20-148">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





