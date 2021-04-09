---
title: 'INapSystemHealthAgentRequest GetStringCorrelationId 方法 (NapSystemHealthAgent .h) '
description: 系統健康狀態代理程式會使用來記錄相互關聯識別碼。
ms.assetid: 5d6f2392-2ada-474a-b150-31e0583c2ea7
keywords:
- GetStringCorrelationId 方法 NAP
- GetStringCorrelationId 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，GetStringCorrelationId 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetStringCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f33e98ae4b0fd76d97e85fb3588bcd1f2d33fd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685759"
---
# <a name="inapsystemhealthagentrequestgetstringcorrelationid-method"></a><span data-ttu-id="adbbd-106">INapSystemHealthAgentRequest：： GetStringCorrelationId 方法</span><span class="sxs-lookup"><span data-stu-id="adbbd-106">INapSystemHealthAgentRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="adbbd-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="adbbd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="adbbd-108">**INapSystemHealthAgentRequest：： GetStringCorrelationId** 方法是由系統健康情況代理程式用來記錄相互關聯識別碼。</span><span class="sxs-lookup"><span data-stu-id="adbbd-108">The **INapSystemHealthAgentRequest::GetStringCorrelationId** method is used by system health agents to log the correlation ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="adbbd-109">語法</span><span class="sxs-lookup"><span data-stu-id="adbbd-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="adbbd-110">參數</span><span class="sxs-lookup"><span data-stu-id="adbbd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adbbd-111">*correlationId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="adbbd-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="adbbd-112">此 SoH 交換的唯一 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) 指標指標。</span><span class="sxs-lookup"><span data-stu-id="adbbd-112">A pointer to a pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for this SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="adbbd-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="adbbd-113">Return value</span></span>

<span data-ttu-id="adbbd-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="adbbd-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="adbbd-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="adbbd-115">Return code</span></span>                                                                                     | <span data-ttu-id="adbbd-116">Description</span><span class="sxs-lookup"><span data-stu-id="adbbd-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="adbbd-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="adbbd-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="adbbd-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="adbbd-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="adbbd-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="adbbd-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="adbbd-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="adbbd-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="adbbd-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="adbbd-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="adbbd-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="adbbd-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="adbbd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="adbbd-123">Requirements</span></span>



| <span data-ttu-id="adbbd-124">需求</span><span class="sxs-lookup"><span data-stu-id="adbbd-124">Requirement</span></span> | <span data-ttu-id="adbbd-125">值</span><span class="sxs-lookup"><span data-stu-id="adbbd-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adbbd-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="adbbd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="adbbd-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adbbd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="adbbd-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="adbbd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="adbbd-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="adbbd-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="adbbd-130">標頭</span><span class="sxs-lookup"><span data-stu-id="adbbd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="adbbd-131"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="adbbd-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="adbbd-132">Idl</span><span class="sxs-lookup"><span data-stu-id="adbbd-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="adbbd-133"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="adbbd-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="adbbd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="adbbd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="adbbd-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adbbd-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="adbbd-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adbbd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adbbd-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="adbbd-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





