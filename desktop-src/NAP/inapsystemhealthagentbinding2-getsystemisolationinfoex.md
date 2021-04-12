---
title: 'INapSystemHealthAgentBinding2 GetSystemIsolationInfoEx 方法 (NapSystemHealthAgent .h) '
description: 由 Sha 呼叫，以判斷系統隔離狀態和擴充的隔離狀態。
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- GetSystemIsolationInfoEx 方法 NAP
- GetSystemIsolationInfoEx 方法 NAP，INapSystemHealthAgentBinding2 介面
- INapSystemHealthAgentBinding2 介面 NAP，GetSystemIsolationInfoEx 方法
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508679"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a><span data-ttu-id="a3cce-106">INapSystemHealthAgentBinding2：： GetSystemIsolationInfoEx 方法</span><span class="sxs-lookup"><span data-stu-id="a3cce-106">INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="a3cce-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="a3cce-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a3cce-108">**INapSystemHealthAgentBinding2：： GetSystemIsolationInfoEx** 方法是由 sha 呼叫，以判斷系統隔離狀態和擴充的隔離狀態。</span><span class="sxs-lookup"><span data-stu-id="a3cce-108">The **INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx** method is called by SHAs to determine the system isolation state and extended isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="a3cce-109">使用 [**INapSystemHealthAgentBinding：： GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) ，以只判斷系統的隔離狀態。</span><span class="sxs-lookup"><span data-stu-id="a3cce-109">Use [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) in order to only determine the isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a3cce-110">語法</span><span class="sxs-lookup"><span data-stu-id="a3cce-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="a3cce-111">參數</span><span class="sxs-lookup"><span data-stu-id="a3cce-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3cce-112">*isolationInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3cce-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3cce-113">[**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex)結構指標的指標，其中包含已知連接之系統的擴充隔離狀態。</span><span class="sxs-lookup"><span data-stu-id="a3cce-113">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the extended isolation state of the system for known connections.</span></span> <span data-ttu-id="a3cce-114">*isolationInfo* 指出系統是否處於受限存取、試用或無限制存取的狀態，以及 [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) 資訊。</span><span class="sxs-lookup"><span data-stu-id="a3cce-114">*isolationInfo* indicates if the system is in a state of restricted access, probation, or unrestricted access, as well as [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) information.</span></span>

</dd> <dt>

<span data-ttu-id="a3cce-115">*unknownConnections* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a3cce-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3cce-116">**布林** 值的指標，如果有任何連接處於未知狀態，則為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a3cce-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3cce-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="a3cce-117">Return value</span></span>

<span data-ttu-id="a3cce-118">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a3cce-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a3cce-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a3cce-119">Return code</span></span>                                                                                             | <span data-ttu-id="a3cce-120">Description</span><span class="sxs-lookup"><span data-stu-id="a3cce-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3cce-121"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a3cce-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="a3cce-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="a3cce-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="a3cce-123"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a3cce-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="a3cce-124">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="a3cce-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="a3cce-125"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a3cce-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="a3cce-126">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="a3cce-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="a3cce-127"><dt>**NAP \_ E \_ 未 \_ 初始化**</dt></span><span class="sxs-lookup"><span data-stu-id="a3cce-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="a3cce-128">SHA 先前尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="a3cce-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="a3cce-129"><dt>**RPC \_ E \_ 中斷連接**</dt></span><span class="sxs-lookup"><span data-stu-id="a3cce-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="a3cce-130">NapAgent 已停止。</span><span class="sxs-lookup"><span data-stu-id="a3cce-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="a3cce-131">這個物件會在重新開機後自動復原並重新系結至 NapAgent。</span><span class="sxs-lookup"><span data-stu-id="a3cce-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a3cce-132">備註</span><span class="sxs-lookup"><span data-stu-id="a3cce-132">Remarks</span></span>

<span data-ttu-id="a3cce-133">SHA 必須藉由呼叫 [**FreeIsolationInfoEx**](freeisolationinfoex.md)來釋放 [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex)結構。</span><span class="sxs-lookup"><span data-stu-id="a3cce-133">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

<span data-ttu-id="a3cce-134">SHA 必須在呼叫這個方法或 [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)介面的任何其他方法之前呼叫 [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) 。</span><span class="sxs-lookup"><span data-stu-id="a3cce-134">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3cce-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3cce-135">Requirements</span></span>



| <span data-ttu-id="a3cce-136">需求</span><span class="sxs-lookup"><span data-stu-id="a3cce-136">Requirement</span></span> | <span data-ttu-id="a3cce-137">值</span><span class="sxs-lookup"><span data-stu-id="a3cce-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3cce-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3cce-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a3cce-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3cce-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a3cce-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3cce-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a3cce-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3cce-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a3cce-142">標頭</span><span class="sxs-lookup"><span data-stu-id="a3cce-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3cce-143"><dt>NapSystemHealthAgent。h</dt></span><span class="sxs-lookup"><span data-stu-id="a3cce-143"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="a3cce-144">Idl</span><span class="sxs-lookup"><span data-stu-id="a3cce-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a3cce-145"><dt>NapSystemHealthAgent .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a3cce-145"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="a3cce-146">DLL</span><span class="sxs-lookup"><span data-stu-id="a3cce-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3cce-147"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3cce-147"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a3cce-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3cce-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3cce-149">**INapSystemHealthAgentBinding2**</span><span class="sxs-lookup"><span data-stu-id="a3cce-149">**INapSystemHealthAgentBinding2**</span></span>](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





