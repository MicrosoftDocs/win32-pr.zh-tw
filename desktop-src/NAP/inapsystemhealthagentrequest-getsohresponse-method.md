---
title: 'INapSystemHealthAgentRequest GetSoHResponse 方法 (NapSystemHealthAgent .h) '
description: 當 NapAgent 呼叫 INapSystemHealthAgentCallback ProcessSoHResponse 時，health 代理程式會使用它來取得其 SoHResponse blob。
ms.assetid: 60319256-d5c2-46cc-a59b-f81732e21a7f
keywords:
- GetSoHResponse 方法 NAP
- GetSoHResponse 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，GetSoHResponse 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetSoHResponse
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d593ff897e69b86b554365561e43308adead5250
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094243"
---
# <a name="inapsystemhealthagentrequestgetsohresponse-method"></a><span data-ttu-id="0cdb3-106">INapSystemHealthAgentRequest：： GetSoHResponse 方法</span><span class="sxs-lookup"><span data-stu-id="0cdb3-106">INapSystemHealthAgentRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="0cdb3-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="0cdb3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0cdb3-108">**INapSystemHealthAgentRequest：： GetSoHResponse** 方法是由健康情況代理程式在 NapAgent 呼叫 [**INapSystemHealthAgentCallback：:P rocesssohresponse**](inapsystemhealthagentcallback-processsohresponse-method.md)時，用來取得其 SoHResponse blob。</span><span class="sxs-lookup"><span data-stu-id="0cdb3-108">The **INapSystemHealthAgentRequest::GetSoHResponse** method is used by the health agent to retrieve their SoHResponse blob when the NapAgent calls [**INapSystemHealthAgentCallback::ProcessSoHResponse**](inapsystemhealthagentcallback-processsohresponse-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0cdb3-109">語法</span><span class="sxs-lookup"><span data-stu-id="0cdb3-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse,
  [out] UINT8       *flags
);
```



## <a name="parameters"></a><span data-ttu-id="0cdb3-110">參數</span><span class="sxs-lookup"><span data-stu-id="0cdb3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cdb3-111">*sohResponse* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0cdb3-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cdb3-112">指向 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 封包指標的指標。</span><span class="sxs-lookup"><span data-stu-id="0cdb3-112">A pointer to a pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="0cdb3-113">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0cdb3-113">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cdb3-114">旗標的指標，如果設定 [**shaFixup**](nap-type-constants.md) 位，則會啟用 SHA 的修正，否則會停用修正。</span><span class="sxs-lookup"><span data-stu-id="0cdb3-114">A pointer to a flag that enables fix-up by the SHA if the [**shaFixup**](nap-type-constants.md) bit is set, otherwise fix-up is disabled.</span></span>



| <span data-ttu-id="0cdb3-115">可能的值</span><span class="sxs-lookup"><span data-stu-id="0cdb3-115">Possible Values</span></span>                                                                                                                                                          | <span data-ttu-id="0cdb3-116">意義</span><span class="sxs-lookup"><span data-stu-id="0cdb3-116">Meaning</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span><dl> <span data-ttu-id="0cdb3-117"><dt>**shaFixup**</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb3-117"><dt>**shaFixup**</dt></span></span> </dl> | <span data-ttu-id="0cdb3-118">SHA 預期會根據回應來執行修復。</span><span class="sxs-lookup"><span data-stu-id="0cdb3-118">The SHA is expected to perform the fixup based on the response.</span></span> <span data-ttu-id="0cdb3-119">如果未設定此旗標，則即使 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 指出其狀況不良，SHA 仍不應執行修正。</span><span class="sxs-lookup"><span data-stu-id="0cdb3-119">If this flag is not set, the SHA should not perform a fix-up even though the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) indicates that it is unhealthy.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cdb3-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="0cdb3-120">Return value</span></span>

<span data-ttu-id="0cdb3-121">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0cdb3-121">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0cdb3-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0cdb3-122">Return code</span></span>                                                                                     | <span data-ttu-id="0cdb3-123">Description</span><span class="sxs-lookup"><span data-stu-id="0cdb3-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0cdb3-124"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb3-124"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0cdb3-125">作業成功。</span><span class="sxs-lookup"><span data-stu-id="0cdb3-125">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0cdb3-126"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb3-126"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0cdb3-127">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="0cdb3-127">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0cdb3-128"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb3-128"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0cdb3-129">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="0cdb3-129">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0cdb3-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cdb3-130">Requirements</span></span>



| <span data-ttu-id="0cdb3-131">需求</span><span class="sxs-lookup"><span data-stu-id="0cdb3-131">Requirement</span></span> | <span data-ttu-id="0cdb3-132">值</span><span class="sxs-lookup"><span data-stu-id="0cdb3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cdb3-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0cdb3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0cdb3-134">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cdb3-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0cdb3-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0cdb3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0cdb3-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0cdb3-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0cdb3-137">標頭</span><span class="sxs-lookup"><span data-stu-id="0cdb3-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cdb3-138"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb3-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cdb3-139">Idl</span><span class="sxs-lookup"><span data-stu-id="0cdb3-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0cdb3-140"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb3-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="0cdb3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="0cdb3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cdb3-142"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cdb3-142"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="0cdb3-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cdb3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cdb3-144">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="0cdb3-144">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





