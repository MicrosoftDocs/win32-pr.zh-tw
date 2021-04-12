---
title: 'INapSystemHealthAgentRequest GetSoHRequest 方法 (NapSystemHealthAgent .h) '
description: 可由 NapAgent 先前快取的 Sha get Soh 使用。
ms.assetid: 187a4513-79db-45cb-8d64-6a92a2d3b004
keywords:
- GetSoHRequest 方法 NAP
- GetSoHRequest 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，GetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab52e52c952c2dc1f891098e10c3ecb688052295
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025422"
---
# <a name="inapsystemhealthagentrequestgetsohrequest-method"></a><span data-ttu-id="ff6c1-106">INapSystemHealthAgentRequest：： GetSoHRequest 方法</span><span class="sxs-lookup"><span data-stu-id="ff6c1-106">INapSystemHealthAgentRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="ff6c1-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="ff6c1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ff6c1-108">**INapSystemHealthAgentRequest：： GetSoHRequest** 方法可以由 NapAgent 先前快取的 Sha get soh 使用。</span><span class="sxs-lookup"><span data-stu-id="ff6c1-108">The **INapSystemHealthAgentRequest::GetSoHRequest** method can be used by SHAs get SoHs previously cached by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff6c1-109">語法</span><span class="sxs-lookup"><span data-stu-id="ff6c1-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="ff6c1-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff6c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff6c1-111">*sohRequest* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ff6c1-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff6c1-112">指向 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="ff6c1-112">A pointer to a pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff6c1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff6c1-113">Return value</span></span>

<span data-ttu-id="ff6c1-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ff6c1-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ff6c1-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ff6c1-115">Return code</span></span>                                                                                            | <span data-ttu-id="ff6c1-116">Description</span><span class="sxs-lookup"><span data-stu-id="ff6c1-116">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff6c1-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ff6c1-117"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="ff6c1-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ff6c1-118">Operation succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="ff6c1-119"><dt>**NAP \_ E 沒有快取的 \_ \_ \_ SOH**</dt></span><span class="sxs-lookup"><span data-stu-id="ff6c1-119"><dt>**NAP\_E\_NO\_CACHED\_SOH**</dt></span></span> </dl> | <span data-ttu-id="ff6c1-120">找不到 SoH;NapAgent 沒有快取的複本。</span><span class="sxs-lookup"><span data-stu-id="ff6c1-120">The SoH is not found; NapAgent does not have a cached copy.</span></span><br/> |
| <dl> <span data-ttu-id="ff6c1-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ff6c1-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="ff6c1-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="ff6c1-122">Permissions error, access denied.</span></span><br/>                           |
| <dl> <span data-ttu-id="ff6c1-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ff6c1-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="ff6c1-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="ff6c1-124">System resource limit, could not perform the operation.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="ff6c1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff6c1-125">Requirements</span></span>



| <span data-ttu-id="ff6c1-126">需求</span><span class="sxs-lookup"><span data-stu-id="ff6c1-126">Requirement</span></span> | <span data-ttu-id="ff6c1-127">值</span><span class="sxs-lookup"><span data-stu-id="ff6c1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6c1-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff6c1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ff6c1-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff6c1-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ff6c1-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff6c1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ff6c1-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff6c1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ff6c1-132">標頭</span><span class="sxs-lookup"><span data-stu-id="ff6c1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff6c1-133"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="ff6c1-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff6c1-134">Idl</span><span class="sxs-lookup"><span data-stu-id="ff6c1-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff6c1-135"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff6c1-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="ff6c1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ff6c1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff6c1-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff6c1-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="ff6c1-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff6c1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff6c1-139">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="ff6c1-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





