---
title: 'INapEnforcementClientConnection GetStringCorrelationId 方法 (NapEnforcementClient .h) '
description: 取得用來讓要求和回應相互關聯的識別碼字串版本。
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- GetStringCorrelationId 方法 NAP
- GetStringCorrelationId 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetStringCorrelationId 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508443"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a><span data-ttu-id="e17eb-106">INapEnforcementClientConnection：： GetStringCorrelationId 方法</span><span class="sxs-lookup"><span data-stu-id="e17eb-106">INapEnforcementClientConnection::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="e17eb-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="e17eb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e17eb-108">**INapEnforcementClientConnection：： GetStringCorrelationId** 方法會取得用來讓要求和回應相互關聯的識別碼字串版本。</span><span class="sxs-lookup"><span data-stu-id="e17eb-108">The **INapEnforcementClientConnection::GetStringCorrelationId** method gets the string version of the ID used to correlate requests and responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="e17eb-109">語法</span><span class="sxs-lookup"><span data-stu-id="e17eb-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="e17eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="e17eb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e17eb-111">*correlationId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e17eb-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e17eb-112">[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構的指標，其中包含連接 [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)的字串版本。</span><span class="sxs-lookup"><span data-stu-id="e17eb-112">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the string version of the connection's [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e17eb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e17eb-113">Return value</span></span>

<span data-ttu-id="e17eb-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e17eb-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e17eb-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e17eb-115">Return code</span></span>                                                                                     | <span data-ttu-id="e17eb-116">Description</span><span class="sxs-lookup"><span data-stu-id="e17eb-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e17eb-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e17eb-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e17eb-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e17eb-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e17eb-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e17eb-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e17eb-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="e17eb-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e17eb-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e17eb-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e17eb-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="e17eb-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e17eb-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e17eb-123">Requirements</span></span>



| <span data-ttu-id="e17eb-124">需求</span><span class="sxs-lookup"><span data-stu-id="e17eb-124">Requirement</span></span> | <span data-ttu-id="e17eb-125">值</span><span class="sxs-lookup"><span data-stu-id="e17eb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e17eb-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e17eb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e17eb-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e17eb-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e17eb-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e17eb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e17eb-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e17eb-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e17eb-130">標頭</span><span class="sxs-lookup"><span data-stu-id="e17eb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e17eb-131"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="e17eb-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e17eb-132">Idl</span><span class="sxs-lookup"><span data-stu-id="e17eb-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e17eb-133"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="e17eb-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="e17eb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e17eb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e17eb-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e17eb-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e17eb-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e17eb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e17eb-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="e17eb-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





