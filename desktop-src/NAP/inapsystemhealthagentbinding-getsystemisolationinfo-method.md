---
title: 'INapSystemHealthAgentBinding GetSystemIsolationInfo 方法 (NapSystemHealthAgent .h) '
description: 由 Sha 呼叫以判斷系統隔離狀態。
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- GetSystemIsolationInfo 方法 NAP
- GetSystemIsolationInfo 方法 NAP，INapSystemHealthAgentBinding 介面
- INapSystemHealthAgentBinding 介面 NAP，GetSystemIsolationInfo 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0323149be50cd8896a191ca57584cea0c015487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466861"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a><span data-ttu-id="def1f-106">INapSystemHealthAgentBinding：： GetSystemIsolationInfo 方法</span><span class="sxs-lookup"><span data-stu-id="def1f-106">INapSystemHealthAgentBinding::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="def1f-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="def1f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="def1f-108">**INapSystemHealthAgentBinding：： GetSystemIsolationInfo** 方法是由 sha 呼叫，以判斷系統隔離狀態。</span><span class="sxs-lookup"><span data-stu-id="def1f-108">The **INapSystemHealthAgentBinding::GetSystemIsolationInfo** method is called by SHAs to determine the system isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="def1f-109">使用 [**INapSystemHealthAgentBinding2：： GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) 來判斷系統的擴充隔離狀態。</span><span class="sxs-lookup"><span data-stu-id="def1f-109">Use [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) in order to determine the extended isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="def1f-110">語法</span><span class="sxs-lookup"><span data-stu-id="def1f-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a><span data-ttu-id="def1f-111">參數</span><span class="sxs-lookup"><span data-stu-id="def1f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def1f-112">*isolationInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="def1f-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="def1f-113">[**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo)結構指標的指標，其中包含已知連接之系統的隔離狀態。</span><span class="sxs-lookup"><span data-stu-id="def1f-113">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the isolation state of the system for known connections.</span></span> <span data-ttu-id="def1f-114">如果系統處於限制存取、試用或無限制存取的狀態，則為 *isolationInfoindicates* 。</span><span class="sxs-lookup"><span data-stu-id="def1f-114">*isolationInfoindicates* if the system is in a state of restricted access, probation, or unrestricted access.</span></span>

</dd> <dt>

<span data-ttu-id="def1f-115">*unknownConnections* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="def1f-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="def1f-116">**布林** 值的指標，如果有任何連接處於未知狀態，則為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="def1f-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def1f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="def1f-117">Return value</span></span>

<span data-ttu-id="def1f-118">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="def1f-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="def1f-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="def1f-119">Return code</span></span>                                                                                             | <span data-ttu-id="def1f-120">Description</span><span class="sxs-lookup"><span data-stu-id="def1f-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="def1f-121"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="def1f-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="def1f-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="def1f-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="def1f-123"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="def1f-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="def1f-124">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="def1f-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="def1f-125"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="def1f-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="def1f-126">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="def1f-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="def1f-127"><dt>**NAP \_ E \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="def1f-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="def1f-128">SHA 先前尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="def1f-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="def1f-129"><dt>**RPC \_ E \_ 中斷連接**</dt></span><span class="sxs-lookup"><span data-stu-id="def1f-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="def1f-130">NapAgent 已停止。</span><span class="sxs-lookup"><span data-stu-id="def1f-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="def1f-131">這個物件會在重新開機後自動復原並重新系結至 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="def1f-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="def1f-132">備註</span><span class="sxs-lookup"><span data-stu-id="def1f-132">Remarks</span></span>

<span data-ttu-id="def1f-133">SHA 必須在呼叫這個方法或 [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)介面的任何其他方法之前呼叫 [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="def1f-133">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="def1f-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="def1f-134">Requirements</span></span>



| <span data-ttu-id="def1f-135">需求</span><span class="sxs-lookup"><span data-stu-id="def1f-135">Requirement</span></span> | <span data-ttu-id="def1f-136">值</span><span class="sxs-lookup"><span data-stu-id="def1f-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def1f-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="def1f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="def1f-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="def1f-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="def1f-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="def1f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="def1f-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="def1f-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="def1f-141">標頭</span><span class="sxs-lookup"><span data-stu-id="def1f-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="def1f-142"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="def1f-142"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="def1f-143">Idl</span><span class="sxs-lookup"><span data-stu-id="def1f-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="def1f-144"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="def1f-144"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="def1f-145">DLL</span><span class="sxs-lookup"><span data-stu-id="def1f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="def1f-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="def1f-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="def1f-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="def1f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def1f-148">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="def1f-148">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





