---
title: 'INapSystemHealthValidationRequest GetCorrelationId 方法 (NapSystemHealthValidator .h) '
description: 系統健康狀態驗證 (Shv) 用來取出相互關聯識別碼。 然後，SHV 必須記錄此資訊。
ms.assetid: 72603d24-219e-4bb0-9b2b-b58d42939da8
keywords:
- GetCorrelationId 方法 NAP
- GetCorrelationId 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，GetCorrelationId 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1095a2c3eec90ff33613b6d37b43f31fdabd107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465141"
---
# <a name="inapsystemhealthvalidationrequestgetcorrelationid-method"></a><span data-ttu-id="8bdee-107">INapSystemHealthValidationRequest：： GetCorrelationId 方法</span><span class="sxs-lookup"><span data-stu-id="8bdee-107">INapSystemHealthValidationRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="8bdee-108">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="8bdee-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8bdee-109">**INapSystemHealthValidationRequest：： GetCorrelationId** 方法是由系統健康狀態驗證 (shv) 用來取出相互關聯識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bdee-109">The **INapSystemHealthValidationRequest::GetCorrelationId** method is used by System Health Validators (SHVs) to retrieve the correlation ID.</span></span> <span data-ttu-id="8bdee-110">然後，SHV 必須記錄此資訊。</span><span class="sxs-lookup"><span data-stu-id="8bdee-110">The SHV must then log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bdee-111">語法</span><span class="sxs-lookup"><span data-stu-id="8bdee-111">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="8bdee-112">參數</span><span class="sxs-lookup"><span data-stu-id="8bdee-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bdee-113">*correlationId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8bdee-113">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bdee-114">SoH 交換的唯一 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) 指標。</span><span class="sxs-lookup"><span data-stu-id="8bdee-114">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bdee-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8bdee-115">Return value</span></span>

<span data-ttu-id="8bdee-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8bdee-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8bdee-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8bdee-117">Return code</span></span>                                                                                     | <span data-ttu-id="8bdee-118">Description</span><span class="sxs-lookup"><span data-stu-id="8bdee-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8bdee-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8bdee-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="8bdee-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="8bdee-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8bdee-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8bdee-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="8bdee-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="8bdee-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8bdee-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8bdee-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="8bdee-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="8bdee-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8bdee-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="8bdee-125">Requirements</span></span>



| <span data-ttu-id="8bdee-126">需求</span><span class="sxs-lookup"><span data-stu-id="8bdee-126">Requirement</span></span> | <span data-ttu-id="8bdee-127">值</span><span class="sxs-lookup"><span data-stu-id="8bdee-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bdee-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8bdee-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8bdee-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="8bdee-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="8bdee-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8bdee-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8bdee-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8bdee-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bdee-132">標頭</span><span class="sxs-lookup"><span data-stu-id="8bdee-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bdee-133"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="8bdee-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bdee-134">Idl</span><span class="sxs-lookup"><span data-stu-id="8bdee-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bdee-135"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8bdee-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="8bdee-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8bdee-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bdee-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bdee-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="8bdee-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8bdee-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bdee-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="8bdee-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





