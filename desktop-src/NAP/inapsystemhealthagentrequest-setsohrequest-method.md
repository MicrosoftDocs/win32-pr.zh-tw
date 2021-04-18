---
title: 'INapSystemHealthAgentRequest SetSoHRequest 方法 (NapSystemHealthAgent .h) '
description: 健康情況代理程式會使用它來寫入自呼叫 INapSystemHealthAgentCallback GetSoHRequest 所產生的 SoH 要求。
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- SetSoHRequest 方法 NAP
- SetSoHRequest 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，SetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968954"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a><span data-ttu-id="83bcc-106">INapSystemHealthAgentRequest：： SetSoHRequest 方法</span><span class="sxs-lookup"><span data-stu-id="83bcc-106">INapSystemHealthAgentRequest::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="83bcc-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="83bcc-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="83bcc-108">健康情況代理程式會使用 **INapSystemHealthAgentRequest：： SetSoHRequest** 方法，來寫入由呼叫 [**INapSystemHealthAgentCallback：： GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md)所產生的 SoH 要求。</span><span class="sxs-lookup"><span data-stu-id="83bcc-108">The **INapSystemHealthAgentRequest::SetSoHRequest** method is used by health agents to write their SoH request resulting from the call to [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="83bcc-109">語法</span><span class="sxs-lookup"><span data-stu-id="83bcc-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="83bcc-110">參數</span><span class="sxs-lookup"><span data-stu-id="83bcc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83bcc-111">*sohRequest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83bcc-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bcc-112">[**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)封包的指標。</span><span class="sxs-lookup"><span data-stu-id="83bcc-112">A pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="83bcc-113">*cacheSohForLaterUse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="83bcc-113">*cacheSohForLaterUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83bcc-114">如果 NapAgent 應該快取 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則 **布林\*\*\*\*值為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="83bcc-114">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83bcc-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="83bcc-115">Return value</span></span>

<span data-ttu-id="83bcc-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="83bcc-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="83bcc-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="83bcc-117">Return code</span></span>                                                                                     | <span data-ttu-id="83bcc-118">Description</span><span class="sxs-lookup"><span data-stu-id="83bcc-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="83bcc-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="83bcc-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="83bcc-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="83bcc-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="83bcc-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="83bcc-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="83bcc-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="83bcc-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="83bcc-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="83bcc-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="83bcc-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="83bcc-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="83bcc-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="83bcc-125">Requirements</span></span>



| <span data-ttu-id="83bcc-126">需求</span><span class="sxs-lookup"><span data-stu-id="83bcc-126">Requirement</span></span> | <span data-ttu-id="83bcc-127">值</span><span class="sxs-lookup"><span data-stu-id="83bcc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83bcc-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83bcc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="83bcc-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83bcc-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="83bcc-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83bcc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="83bcc-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83bcc-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="83bcc-132">標頭</span><span class="sxs-lookup"><span data-stu-id="83bcc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="83bcc-133"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="83bcc-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="83bcc-134">Idl</span><span class="sxs-lookup"><span data-stu-id="83bcc-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83bcc-135"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="83bcc-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="83bcc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="83bcc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83bcc-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83bcc-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="83bcc-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83bcc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83bcc-139">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="83bcc-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





