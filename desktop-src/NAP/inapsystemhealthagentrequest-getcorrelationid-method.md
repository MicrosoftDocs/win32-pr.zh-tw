---
title: 'INapSystemHealthAgentRequest GetCorrelationId 方法 (NapSystemHealthAgent .h) '
description: 系統健康狀態代理程式會使用它來相互關聯 SoH 的和 SoH 回應。
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- GetCorrelationId 方法 NAP
- GetCorrelationId 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，GetCorrelationId 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af5b182df738ec22c75f2afffd1adb3591007be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509480"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a><span data-ttu-id="cbe75-106">INapSystemHealthAgentRequest：： GetCorrelationId 方法</span><span class="sxs-lookup"><span data-stu-id="cbe75-106">INapSystemHealthAgentRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="cbe75-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="cbe75-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cbe75-108">系統健康狀態代理程式會使用 **INapSystemHealthAgentRequest：： GetCorrelationId** 方法，將 SoH 和 soh 回應相互關聯。</span><span class="sxs-lookup"><span data-stu-id="cbe75-108">The **INapSystemHealthAgentRequest::GetCorrelationId** method is used by system health agents to correlate SoH's and SoH-Responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe75-109">語法</span><span class="sxs-lookup"><span data-stu-id="cbe75-109">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="cbe75-110">參數</span><span class="sxs-lookup"><span data-stu-id="cbe75-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbe75-111">*correlationId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cbe75-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbe75-112">SoH 交換的唯一 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) 指標。</span><span class="sxs-lookup"><span data-stu-id="cbe75-112">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbe75-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="cbe75-113">Return value</span></span>

<span data-ttu-id="cbe75-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cbe75-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="cbe75-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cbe75-115">Return code</span></span>                                                                                     | <span data-ttu-id="cbe75-116">Description</span><span class="sxs-lookup"><span data-stu-id="cbe75-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="cbe75-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cbe75-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="cbe75-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="cbe75-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cbe75-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="cbe75-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="cbe75-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="cbe75-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="cbe75-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cbe75-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="cbe75-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="cbe75-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cbe75-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbe75-123">Requirements</span></span>



| <span data-ttu-id="cbe75-124">需求</span><span class="sxs-lookup"><span data-stu-id="cbe75-124">Requirement</span></span> | <span data-ttu-id="cbe75-125">值</span><span class="sxs-lookup"><span data-stu-id="cbe75-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe75-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cbe75-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cbe75-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbe75-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cbe75-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cbe75-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cbe75-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbe75-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cbe75-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cbe75-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbe75-131"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="cbe75-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="cbe75-132">Idl</span><span class="sxs-lookup"><span data-stu-id="cbe75-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cbe75-133"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="cbe75-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="cbe75-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cbe75-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbe75-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbe75-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="cbe75-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbe75-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe75-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="cbe75-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





