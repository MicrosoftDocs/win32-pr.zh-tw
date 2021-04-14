---
title: 'INapSystemHealthAgentRequest GetCacheSoHFlag 方法 (NapSystemHealthAgent .h) '
description: 僅供 NapAgent 使用。
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- GetCacheSoHFlag 方法 NAP
- GetCacheSoHFlag 方法 NAP，INapSystemHealthAgentRequest 介面
- INapSystemHealthAgentRequest 介面 NAP，GetCacheSoHFlag 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d8b458e4a49b690fe1f0f53482a72dd253c7c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509003"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a><span data-ttu-id="f7b27-106">INapSystemHealthAgentRequest：： GetCacheSoHFlag 方法</span><span class="sxs-lookup"><span data-stu-id="f7b27-106">INapSystemHealthAgentRequest::GetCacheSoHFlag method</span></span>

> [!Note]  
> <span data-ttu-id="f7b27-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="f7b27-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f7b27-108">**INapSystemHealthAgentRequest：： GetCacheSoHFlag** 方法僅供 NapAgent 使用。</span><span class="sxs-lookup"><span data-stu-id="f7b27-108">The **INapSystemHealthAgentRequest::GetCacheSoHFlag** method is used only by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b27-109">語法</span><span class="sxs-lookup"><span data-stu-id="f7b27-109">Syntax</span></span>


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="f7b27-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7b27-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b27-111">*cacheSohForLaterUse*</span><span class="sxs-lookup"><span data-stu-id="f7b27-111">*cacheSohForLaterUse*</span></span> 
</dt> <dd>

<span data-ttu-id="f7b27-112">如果 NapAgent 應該快取 [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) ，則 **布林\*\*\*\*值為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f7b27-112">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b27-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7b27-113">Return value</span></span>

<span data-ttu-id="f7b27-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f7b27-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f7b27-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f7b27-115">Return code</span></span>                                                                                     | <span data-ttu-id="f7b27-116">Description</span><span class="sxs-lookup"><span data-stu-id="f7b27-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7b27-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b27-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f7b27-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="f7b27-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f7b27-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b27-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f7b27-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="f7b27-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f7b27-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b27-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f7b27-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="f7b27-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f7b27-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7b27-123">Requirements</span></span>



| <span data-ttu-id="f7b27-124">需求</span><span class="sxs-lookup"><span data-stu-id="f7b27-124">Requirement</span></span> | <span data-ttu-id="f7b27-125">值</span><span class="sxs-lookup"><span data-stu-id="f7b27-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b27-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7b27-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b27-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7b27-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f7b27-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7b27-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b27-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7b27-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f7b27-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f7b27-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b27-131"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b27-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7b27-132">Idl</span><span class="sxs-lookup"><span data-stu-id="f7b27-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7b27-133"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7b27-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="f7b27-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b27-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7b27-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b27-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="f7b27-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7b27-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b27-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="f7b27-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





