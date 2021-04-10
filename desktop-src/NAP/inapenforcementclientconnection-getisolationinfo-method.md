---
title: 'INapEnforcementClientConnection GetIsolationInfo 方法 (NapEnforcementClient .h) '
description: 會使用取得用戶端的隔離資訊。
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- GetIsolationInfo 方法 NAP
- GetIsolationInfo 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetIsolationInfo 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890f7268801fda77a9794ed21c4d36e78a52dd5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935118"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a><span data-ttu-id="04d4a-106">INapEnforcementClientConnection：： GetIsolationInfo 方法</span><span class="sxs-lookup"><span data-stu-id="04d4a-106">INapEnforcementClientConnection::GetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="04d4a-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="04d4a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="04d4a-108">**INapEnforcementClientConnection：： GetIsolationInfo** 方法是用來取得用戶端的隔離資訊。</span><span class="sxs-lookup"><span data-stu-id="04d4a-108">The **INapEnforcementClientConnection::GetIsolationInfo** method is used get the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d4a-109">語法</span><span class="sxs-lookup"><span data-stu-id="04d4a-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="04d4a-110">參數</span><span class="sxs-lookup"><span data-stu-id="04d4a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d4a-111">*isolationInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="04d4a-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04d4a-112">[**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo)結構指標的指標，其中包含用戶端的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="04d4a-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d4a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="04d4a-113">Return value</span></span>

<span data-ttu-id="04d4a-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="04d4a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="04d4a-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="04d4a-115">Return code</span></span>                                                                                     | <span data-ttu-id="04d4a-116">Description</span><span class="sxs-lookup"><span data-stu-id="04d4a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="04d4a-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="04d4a-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="04d4a-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="04d4a-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="04d4a-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="04d4a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="04d4a-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="04d4a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="04d4a-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="04d4a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="04d4a-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="04d4a-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="04d4a-123">備註</span><span class="sxs-lookup"><span data-stu-id="04d4a-123">Remarks</span></span>

<span data-ttu-id="04d4a-124">這項資訊是由 NapAgent 在處理 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 之後設定的，而且不得由 enforcer 設定。</span><span class="sxs-lookup"><span data-stu-id="04d4a-124">This information is set by the NapAgent after processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="04d4a-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="04d4a-125">Requirements</span></span>



| <span data-ttu-id="04d4a-126">需求</span><span class="sxs-lookup"><span data-stu-id="04d4a-126">Requirement</span></span> | <span data-ttu-id="04d4a-127">值</span><span class="sxs-lookup"><span data-stu-id="04d4a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d4a-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04d4a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="04d4a-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04d4a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="04d4a-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04d4a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="04d4a-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04d4a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="04d4a-132">標頭</span><span class="sxs-lookup"><span data-stu-id="04d4a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="04d4a-133"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="04d4a-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="04d4a-134">Idl</span><span class="sxs-lookup"><span data-stu-id="04d4a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04d4a-135"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="04d4a-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="04d4a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="04d4a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04d4a-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04d4a-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="04d4a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04d4a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d4a-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="04d4a-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





