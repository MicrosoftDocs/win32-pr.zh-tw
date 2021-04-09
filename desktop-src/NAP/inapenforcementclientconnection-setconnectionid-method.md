---
title: 'INapEnforcementClientConnection SetConnectionId 方法 (NapEnforcementClient .h) '
description: 是用來設定連接的唯一識別碼，而且必須在建立連接之後，強制用戶端設定此識別碼。
ms.assetid: 69d1a891-bc86-4c8a-b614-ebcdaa4a9057
keywords:
- SetConnectionId 方法 NAP
- SetConnectionId 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetConnectionId 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9749be304170ec7706b637429f577e77411ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934163"
---
# <a name="inapenforcementclientconnectionsetconnectionid-method"></a><span data-ttu-id="925c8-106">INapEnforcementClientConnection：： SetConnectionId 方法</span><span class="sxs-lookup"><span data-stu-id="925c8-106">INapEnforcementClientConnection::SetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="925c8-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="925c8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="925c8-108">**INapEnforcementClientConnection：： SetConnectionId** 方法是用來設定連接的唯一識別碼，而且必須在建立連接之後，強制用戶端設定此識別碼。</span><span class="sxs-lookup"><span data-stu-id="925c8-108">The **INapEnforcementClientConnection::SetConnectionId** method is used to set the unique ID of the connection and must be set by the enforcement client as soon as the connection is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="925c8-109">語法</span><span class="sxs-lookup"><span data-stu-id="925c8-109">Syntax</span></span>


```C++
HRESULT SetConnectionId(
  [in] const ConnectionId *connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="925c8-110">參數</span><span class="sxs-lookup"><span data-stu-id="925c8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="925c8-111">*connectionId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="925c8-111">*connectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="925c8-112">可唯一識別連接之 [**ConnectionId**](nap-datatypes.md) 的指標。</span><span class="sxs-lookup"><span data-stu-id="925c8-112">A pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="925c8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="925c8-113">Return value</span></span>

<span data-ttu-id="925c8-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="925c8-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="925c8-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="925c8-115">Return code</span></span>                                                                                     | <span data-ttu-id="925c8-116">Description</span><span class="sxs-lookup"><span data-stu-id="925c8-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="925c8-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="925c8-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="925c8-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="925c8-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="925c8-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="925c8-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="925c8-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="925c8-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="925c8-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="925c8-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="925c8-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="925c8-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="925c8-123">備註</span><span class="sxs-lookup"><span data-stu-id="925c8-123">Remarks</span></span>

<span data-ttu-id="925c8-124">此 ConnectionID 主要用於記錄用途。</span><span class="sxs-lookup"><span data-stu-id="925c8-124">This ConnectionID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="925c8-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="925c8-125">Requirements</span></span>



| <span data-ttu-id="925c8-126">需求</span><span class="sxs-lookup"><span data-stu-id="925c8-126">Requirement</span></span> | <span data-ttu-id="925c8-127">值</span><span class="sxs-lookup"><span data-stu-id="925c8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="925c8-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="925c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="925c8-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="925c8-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="925c8-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="925c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="925c8-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="925c8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="925c8-132">標頭</span><span class="sxs-lookup"><span data-stu-id="925c8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="925c8-133"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="925c8-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="925c8-134">Idl</span><span class="sxs-lookup"><span data-stu-id="925c8-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="925c8-135"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="925c8-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="925c8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="925c8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="925c8-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="925c8-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="925c8-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="925c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="925c8-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="925c8-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





