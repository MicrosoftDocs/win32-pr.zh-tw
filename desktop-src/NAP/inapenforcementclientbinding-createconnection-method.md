---
title: 'INapEnforcementClientBinding CreateConnection 方法 (NapEnforcementClient .h) '
description: Enforcers 用來建立連線物件。
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- CreateConnection 方法 NAP
- CreateConnection 方法 NAP，INapEnforcementClientBinding 介面
- INapEnforcementClientBinding 介面 NAP，CreateConnection 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024892"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a><span data-ttu-id="13713-106">INapEnforcementClientBinding：： CreateConnection 方法</span><span class="sxs-lookup"><span data-stu-id="13713-106">INapEnforcementClientBinding::CreateConnection method</span></span>

> [!Note]  
> <span data-ttu-id="13713-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="13713-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="13713-108">Enforcers 會使用 **INapEnforcementClientBinding：： CreateConnection** factory 方法來建立連線物件。</span><span class="sxs-lookup"><span data-stu-id="13713-108">The **INapEnforcementClientBinding::CreateConnection** factory method is used by enforcers to create connection objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="13713-109">語法</span><span class="sxs-lookup"><span data-stu-id="13713-109">Syntax</span></span>


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a><span data-ttu-id="13713-110">參數</span><span class="sxs-lookup"><span data-stu-id="13713-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13713-111">*連接* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="13713-111">*connection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13713-112">NAP 系統傳回的新 [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) 介面的 COM 指標。</span><span class="sxs-lookup"><span data-stu-id="13713-112">A COM pointer to a new [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface returned by the NAP system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13713-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="13713-113">Return value</span></span>

<span data-ttu-id="13713-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="13713-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="13713-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="13713-115">Return code</span></span>                                                                                     | <span data-ttu-id="13713-116">Description</span><span class="sxs-lookup"><span data-stu-id="13713-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="13713-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="13713-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="13713-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="13713-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="13713-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="13713-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="13713-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="13713-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="13713-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="13713-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="13713-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="13713-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="13713-123">備註</span><span class="sxs-lookup"><span data-stu-id="13713-123">Remarks</span></span>

<span data-ttu-id="13713-124">強制用戶端必須先呼叫 [**INapEnforcementClientBinding：： Initialize**](inapenforcementclientbinding-initialize-method.md) 方法，才能呼叫這個或 [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) 介面的任何其他方法。</span><span class="sxs-lookup"><span data-stu-id="13713-124">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="13713-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="13713-125">Requirements</span></span>



| <span data-ttu-id="13713-126">需求</span><span class="sxs-lookup"><span data-stu-id="13713-126">Requirement</span></span> | <span data-ttu-id="13713-127">值</span><span class="sxs-lookup"><span data-stu-id="13713-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13713-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13713-128">Minimum supported client</span></span><br/> | <span data-ttu-id="13713-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13713-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="13713-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13713-130">Minimum supported server</span></span><br/> | <span data-ttu-id="13713-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13713-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="13713-132">標頭</span><span class="sxs-lookup"><span data-stu-id="13713-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="13713-133"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="13713-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="13713-134">Idl</span><span class="sxs-lookup"><span data-stu-id="13713-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13713-135"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="13713-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="13713-136">DLL</span><span class="sxs-lookup"><span data-stu-id="13713-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13713-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13713-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="13713-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13713-138">See also</span></span>

<dl> <span data-ttu-id="13713-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="13713-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="13713-140">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="13713-140">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="13713-141">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="13713-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





