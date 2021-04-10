---
title: 'INapEnforcementClientConnection GetEnforcerPrivateData 方法 (NapEnforcementClient .h) '
description: Enforcer 用來取得私用資料。
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- GetEnforcerPrivateData 方法 NAP
- GetEnforcerPrivateData 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetEnforcerPrivateData 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592ad0b11abf2b349b0810d67b05f2ee4086060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106421"
---
# <a name="inapenforcementclientconnectiongetenforcerprivatedata-method"></a><span data-ttu-id="5c78e-106">INapEnforcementClientConnection：： GetEnforcerPrivateData 方法</span><span class="sxs-lookup"><span data-stu-id="5c78e-106">INapEnforcementClientConnection::GetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="5c78e-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="5c78e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5c78e-108">Enforcer 會使用 **INapEnforcementClientConnection：： GetEnforcerPrivateData** 方法來取得私用資料。</span><span class="sxs-lookup"><span data-stu-id="5c78e-108">The **INapEnforcementClientConnection::GetEnforcerPrivateData** method is used by the enforcer to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c78e-109">語法</span><span class="sxs-lookup"><span data-stu-id="5c78e-109">Syntax</span></span>


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="5c78e-110">參數</span><span class="sxs-lookup"><span data-stu-id="5c78e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c78e-111">*privateData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5c78e-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c78e-112">[**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata)不透明資料 blob 指標的指標，而這些指標只有 enforcer 可以解讀。</span><span class="sxs-lookup"><span data-stu-id="5c78e-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c78e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5c78e-113">Return value</span></span>

<span data-ttu-id="5c78e-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5c78e-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5c78e-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5c78e-115">Return code</span></span>                                                                                     | <span data-ttu-id="5c78e-116">Description</span><span class="sxs-lookup"><span data-stu-id="5c78e-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c78e-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5c78e-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5c78e-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="5c78e-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5c78e-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5c78e-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5c78e-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="5c78e-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5c78e-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5c78e-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5c78e-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="5c78e-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5c78e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c78e-123">Requirements</span></span>



| <span data-ttu-id="5c78e-124">需求</span><span class="sxs-lookup"><span data-stu-id="5c78e-124">Requirement</span></span> | <span data-ttu-id="5c78e-125">值</span><span class="sxs-lookup"><span data-stu-id="5c78e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c78e-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c78e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5c78e-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c78e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5c78e-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c78e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5c78e-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c78e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5c78e-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5c78e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c78e-131"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="5c78e-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c78e-132">Idl</span><span class="sxs-lookup"><span data-stu-id="5c78e-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5c78e-133"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5c78e-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="5c78e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5c78e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c78e-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c78e-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5c78e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c78e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c78e-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="5c78e-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





