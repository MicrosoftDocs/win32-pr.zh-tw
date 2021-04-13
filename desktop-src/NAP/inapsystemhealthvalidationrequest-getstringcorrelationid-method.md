---
title: 'INapSystemHealthValidationRequest GetStringCorrelationId 方法 (NapSystemHealthValidator .h) '
description: 系統健康狀態驗證會使用 (Shv) 必須記錄這項資訊。
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- GetStringCorrelationId 方法 NAP
- GetStringCorrelationId 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，GetStringCorrelationId 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 554a5a31f0aa46f6bcbd7a750662d47ab2c78040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509454"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a><span data-ttu-id="296f3-106">INapSystemHealthValidationRequest：： GetStringCorrelationId 方法</span><span class="sxs-lookup"><span data-stu-id="296f3-106">INapSystemHealthValidationRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="296f3-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="296f3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="296f3-108">**INapSystemHealthValidationRequest：： GetStringCorrelationId** 方法是由系統健康狀態驗證 (shv 所使用) 必須記錄這項資訊。</span><span class="sxs-lookup"><span data-stu-id="296f3-108">The **INapSystemHealthValidationRequest::GetStringCorrelationId** method is used by System Health Validators (SHVs) which must log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="296f3-109">語法</span><span class="sxs-lookup"><span data-stu-id="296f3-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="296f3-110">參數</span><span class="sxs-lookup"><span data-stu-id="296f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="296f3-111">*correlationId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="296f3-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="296f3-112">SoH 交換的唯一 [**StringCorrelationId**](nap-type-constants.md) 指標指標。</span><span class="sxs-lookup"><span data-stu-id="296f3-112">A pointer to a pointer to a unique [**StringCorrelationId**](nap-type-constants.md) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="296f3-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="296f3-113">Return value</span></span>

<span data-ttu-id="296f3-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="296f3-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="296f3-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="296f3-115">Return code</span></span>                                                                                     | <span data-ttu-id="296f3-116">Description</span><span class="sxs-lookup"><span data-stu-id="296f3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="296f3-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="296f3-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="296f3-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="296f3-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="296f3-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="296f3-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="296f3-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="296f3-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="296f3-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="296f3-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="296f3-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="296f3-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="296f3-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="296f3-123">Requirements</span></span>



| <span data-ttu-id="296f3-124">需求</span><span class="sxs-lookup"><span data-stu-id="296f3-124">Requirement</span></span> | <span data-ttu-id="296f3-125">值</span><span class="sxs-lookup"><span data-stu-id="296f3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="296f3-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="296f3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="296f3-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="296f3-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="296f3-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="296f3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="296f3-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="296f3-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="296f3-130">標頭</span><span class="sxs-lookup"><span data-stu-id="296f3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="296f3-131"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="296f3-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="296f3-132">Idl</span><span class="sxs-lookup"><span data-stu-id="296f3-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="296f3-133"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="296f3-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="296f3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="296f3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="296f3-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="296f3-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="296f3-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="296f3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="296f3-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="296f3-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





