---
title: 'INapEnforcementClientConnection GetMaxSize 方法 (NapEnforcementClient .h) '
description: 取得此用戶端的 SoH 封包大小上限。
ms.assetid: 054bc783-db5d-4801-8984-6b8a131744a2
keywords:
- GetMaxSize 方法 NAP
- GetMaxSize 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetMaxSize 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d86cc71cd5da906146ab1577d58311d167d484
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685766"
---
# <a name="inapenforcementclientconnectiongetmaxsize-method"></a><span data-ttu-id="83218-106">INapEnforcementClientConnection：： GetMaxSize 方法</span><span class="sxs-lookup"><span data-stu-id="83218-106">INapEnforcementClientConnection::GetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="83218-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="83218-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="83218-108">**INapEnforcementClientConnection：： GetMaxSize** 方法會取得此用戶端的 SoH 封包大小上限。</span><span class="sxs-lookup"><span data-stu-id="83218-108">The **INapEnforcementClientConnection::GetMaxSize** method gets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="83218-109">語法</span><span class="sxs-lookup"><span data-stu-id="83218-109">Syntax</span></span>


```C++
HRESULT GetMaxSize(
  [out] ProtocolMaxSize *maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="83218-110">參數</span><span class="sxs-lookup"><span data-stu-id="83218-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83218-111">*maxSize* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="83218-111">*maxSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83218-112">指向 [**ProtocolMaxSize**](nap-datatypes.md) 的指標，指出 SoH 封包的最大大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="83218-112">A pointer to a [**ProtocolMaxSize**](nap-datatypes.md) that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83218-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="83218-113">Return value</span></span>

<span data-ttu-id="83218-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="83218-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="83218-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="83218-115">Return code</span></span>                                                                                     | <span data-ttu-id="83218-116">Description</span><span class="sxs-lookup"><span data-stu-id="83218-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="83218-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="83218-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="83218-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="83218-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="83218-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="83218-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="83218-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="83218-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="83218-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="83218-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="83218-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="83218-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="83218-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="83218-123">Requirements</span></span>



| <span data-ttu-id="83218-124">需求</span><span class="sxs-lookup"><span data-stu-id="83218-124">Requirement</span></span> | <span data-ttu-id="83218-125">值</span><span class="sxs-lookup"><span data-stu-id="83218-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83218-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83218-126">Minimum supported client</span></span><br/> | <span data-ttu-id="83218-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83218-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="83218-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83218-128">Minimum supported server</span></span><br/> | <span data-ttu-id="83218-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="83218-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="83218-130">標頭</span><span class="sxs-lookup"><span data-stu-id="83218-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="83218-131"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="83218-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="83218-132">Idl</span><span class="sxs-lookup"><span data-stu-id="83218-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="83218-133"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="83218-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="83218-134">DLL</span><span class="sxs-lookup"><span data-stu-id="83218-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83218-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83218-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="83218-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83218-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83218-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="83218-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





