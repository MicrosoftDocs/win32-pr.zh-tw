---
title: 'INapSystemHealthValidationRequest SetSoHResponse 方法 (NapSystemHealthValidator .h) '
description: 允許 (Shv) 的系統健康狀態驗證，將 SoHResponse 設定為要傳送到其系統健康情況代理程式 (用戶端上的 SHA) 對應。
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- SetSoHResponse 方法 NAP
- SetSoHResponse 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，SetSoHResponse 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385054"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a><span data-ttu-id="7f647-106">INapSystemHealthValidationRequest：： SetSoHResponse 方法</span><span class="sxs-lookup"><span data-stu-id="7f647-106">INapSystemHealthValidationRequest::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="7f647-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="7f647-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7f647-108">**INapSystemHealthValidationRequest：： SetSoHResponse** 方法可讓 (Shv 的系統健全狀況驗證程式) 將 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)設定為傳送至其系統健康情況代理程式 (用戶端上的 SHA) 對應。</span><span class="sxs-lookup"><span data-stu-id="7f647-108">The **INapSystemHealthValidationRequest::SetSoHResponse** method allows System Health Validators (SHVs) to set the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) to be sent to its System Health Agent (SHA) counterpart on the client-side.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f647-109">語法</span><span class="sxs-lookup"><span data-stu-id="7f647-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="7f647-110">參數</span><span class="sxs-lookup"><span data-stu-id="7f647-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f647-111">*sohResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7f647-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f647-112">[**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7f647-112">A pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f647-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7f647-113">Return value</span></span>

<span data-ttu-id="7f647-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7f647-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7f647-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7f647-115">Return code</span></span>                                                                                     | <span data-ttu-id="7f647-116">Description</span><span class="sxs-lookup"><span data-stu-id="7f647-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f647-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="7f647-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7f647-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="7f647-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7f647-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7f647-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7f647-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="7f647-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7f647-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7f647-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7f647-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="7f647-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7f647-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="7f647-123">Requirements</span></span>



| <span data-ttu-id="7f647-124">需求</span><span class="sxs-lookup"><span data-stu-id="7f647-124">Requirement</span></span> | <span data-ttu-id="7f647-125">值</span><span class="sxs-lookup"><span data-stu-id="7f647-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f647-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7f647-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7f647-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="7f647-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="7f647-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7f647-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7f647-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7f647-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f647-130">標頭</span><span class="sxs-lookup"><span data-stu-id="7f647-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f647-131"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="7f647-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f647-132">Idl</span><span class="sxs-lookup"><span data-stu-id="7f647-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f647-133"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f647-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="7f647-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7f647-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f647-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f647-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="7f647-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7f647-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f647-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="7f647-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





