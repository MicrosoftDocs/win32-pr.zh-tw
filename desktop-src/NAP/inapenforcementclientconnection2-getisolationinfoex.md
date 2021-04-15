---
title: 'INapEnforcementClientConnection2 GetIsolationInfoEx 方法 (NapEnforcementClient .h) '
description: 用來取得用戶端的隔離資訊。
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- GetIsolationInfoEx 方法 NAP
- GetIsolationInfoEx 方法 NAP，INapEnforcementClientConnection2 介面
- INapEnforcementClientConnection2 介面 NAP，GetIsolationInfoEx 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467061"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a><span data-ttu-id="f407a-106">INapEnforcementClientConnection2：： GetIsolationInfoEx 方法</span><span class="sxs-lookup"><span data-stu-id="f407a-106">INapEnforcementClientConnection2::GetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="f407a-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="f407a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f407a-108">**INapEnforcementClientConnection2：： GetIsolationInfoEx** 方法是用來取得用戶端的隔離資訊。</span><span class="sxs-lookup"><span data-stu-id="f407a-108">The **INapEnforcementClientConnection2::GetIsolationInfoEx** method is used to get isolation information about the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="f407a-109">語法</span><span class="sxs-lookup"><span data-stu-id="f407a-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a><span data-ttu-id="f407a-110">參數</span><span class="sxs-lookup"><span data-stu-id="f407a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f407a-111">*isolationInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f407a-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f407a-112">[**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex)結構指標的指標，其中包含用戶端的連線能力和擴充狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="f407a-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity and extended state information of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f407a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f407a-113">Return value</span></span>

<span data-ttu-id="f407a-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f407a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f407a-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f407a-115">Return code</span></span>                                                                                     | <span data-ttu-id="f407a-116">Description</span><span class="sxs-lookup"><span data-stu-id="f407a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f407a-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f407a-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f407a-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="f407a-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f407a-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f407a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f407a-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="f407a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f407a-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f407a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f407a-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="f407a-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f407a-123">備註</span><span class="sxs-lookup"><span data-stu-id="f407a-123">Remarks</span></span>

<span data-ttu-id="f407a-124">這項資訊是由 NapAgent 在處理 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 之後設定的，而且不得由 enforcer 設定。</span><span class="sxs-lookup"><span data-stu-id="f407a-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

<span data-ttu-id="f407a-125">SHA 必須藉由呼叫 [**FreeIsolationInfoEx**](freeisolationinfoex.md)來釋放 [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex)結構。</span><span class="sxs-lookup"><span data-stu-id="f407a-125">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f407a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f407a-126">Requirements</span></span>



| <span data-ttu-id="f407a-127">需求</span><span class="sxs-lookup"><span data-stu-id="f407a-127">Requirement</span></span> | <span data-ttu-id="f407a-128">值</span><span class="sxs-lookup"><span data-stu-id="f407a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f407a-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f407a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f407a-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f407a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f407a-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f407a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f407a-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f407a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f407a-133">標頭</span><span class="sxs-lookup"><span data-stu-id="f407a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f407a-134"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="f407a-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f407a-135">Idl</span><span class="sxs-lookup"><span data-stu-id="f407a-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f407a-136"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f407a-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="f407a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f407a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f407a-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f407a-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f407a-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f407a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f407a-140">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="f407a-140">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





