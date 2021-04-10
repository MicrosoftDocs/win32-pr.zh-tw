---
title: 'INapEnforcementClientConnection GetConnectionId 方法 (NapEnforcementClient .h) '
description: 用來取得用戶端的唯一連接識別碼。
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- GetConnectionId 方法 NAP
- GetConnectionId 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetConnectionId 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3ca16aea3c77ccf78359c3cdf5ab6461bc2219e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106427"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a><span data-ttu-id="2d1e4-106">INapEnforcementClientConnection：： GetConnectionId 方法</span><span class="sxs-lookup"><span data-stu-id="2d1e4-106">INapEnforcementClientConnection::GetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="2d1e4-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="2d1e4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2d1e4-108">**INapEnforcementClientConnection：： GetConnectionId** 方法是用來取得用戶端的唯一連接識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d1e4-108">The **INapEnforcementClientConnection::GetConnectionId** method is used to get the unique connection ID of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d1e4-109">語法</span><span class="sxs-lookup"><span data-stu-id="2d1e4-109">Syntax</span></span>


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="2d1e4-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d1e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d1e4-111">*connectionId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2d1e4-111">*connectionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d1e4-112">指標，指向可唯一識別此連接的 [**ConnectionId**](nap-datatypes.md) 指標。</span><span class="sxs-lookup"><span data-stu-id="2d1e4-112">A pointer to a pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies this connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d1e4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d1e4-113">Return value</span></span>

<span data-ttu-id="2d1e4-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2d1e4-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="2d1e4-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2d1e4-115">Return code</span></span>                                                                                     | <span data-ttu-id="2d1e4-116">Description</span><span class="sxs-lookup"><span data-stu-id="2d1e4-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d1e4-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2d1e4-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="2d1e4-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="2d1e4-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2d1e4-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2d1e4-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="2d1e4-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="2d1e4-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2d1e4-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2d1e4-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="2d1e4-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="2d1e4-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2d1e4-123">備註</span><span class="sxs-lookup"><span data-stu-id="2d1e4-123">Remarks</span></span>

<span data-ttu-id="2d1e4-124">連接識別碼主要用於記錄用途。</span><span class="sxs-lookup"><span data-stu-id="2d1e4-124">The connection ID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d1e4-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d1e4-125">Requirements</span></span>



| <span data-ttu-id="2d1e4-126">需求</span><span class="sxs-lookup"><span data-stu-id="2d1e4-126">Requirement</span></span> | <span data-ttu-id="2d1e4-127">值</span><span class="sxs-lookup"><span data-stu-id="2d1e4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d1e4-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2d1e4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2d1e4-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d1e4-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2d1e4-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2d1e4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2d1e4-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2d1e4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2d1e4-132">標頭</span><span class="sxs-lookup"><span data-stu-id="2d1e4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d1e4-133"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d1e4-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d1e4-134">Idl</span><span class="sxs-lookup"><span data-stu-id="2d1e4-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d1e4-135"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d1e4-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="2d1e4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2d1e4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d1e4-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d1e4-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2d1e4-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d1e4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d1e4-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="2d1e4-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





