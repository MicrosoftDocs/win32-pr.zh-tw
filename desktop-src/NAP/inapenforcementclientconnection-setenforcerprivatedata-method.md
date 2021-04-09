---
title: 'INapEnforcementClientConnection SetEnforcerPrivateData 方法 (NapEnforcementClient .h) '
description: Enforcer 會使用來設定私用資料。
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- SetEnforcerPrivateData 方法 NAP
- SetEnforcerPrivateData 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetEnforcerPrivateData 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5773294e229a59ff07db8ef546d9d691b369b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024890"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a><span data-ttu-id="c5b34-106">INapEnforcementClientConnection：： SetEnforcerPrivateData 方法</span><span class="sxs-lookup"><span data-stu-id="c5b34-106">INapEnforcementClientConnection::SetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="c5b34-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="c5b34-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c5b34-108">Enforcer 會使用 **INapEnforcementClientConnection：： SetEnforcerPrivateData** 方法來設定私用資料。</span><span class="sxs-lookup"><span data-stu-id="c5b34-108">The **INapEnforcementClientConnection::SetEnforcerPrivateData** method is used by the enforcer to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b34-109">語法</span><span class="sxs-lookup"><span data-stu-id="c5b34-109">Syntax</span></span>


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="c5b34-110">參數</span><span class="sxs-lookup"><span data-stu-id="c5b34-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b34-111">*privateData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5b34-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b34-112">只有 enforcer 可以解讀的 [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) 不透明資料 blob 指標。</span><span class="sxs-lookup"><span data-stu-id="c5b34-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b34-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5b34-113">Return value</span></span>

<span data-ttu-id="c5b34-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c5b34-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c5b34-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c5b34-115">Return code</span></span>                                                                                     | <span data-ttu-id="c5b34-116">Description</span><span class="sxs-lookup"><span data-stu-id="c5b34-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5b34-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c5b34-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c5b34-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="c5b34-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c5b34-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c5b34-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c5b34-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="c5b34-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c5b34-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c5b34-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c5b34-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="c5b34-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c5b34-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5b34-123">Requirements</span></span>



| <span data-ttu-id="c5b34-124">需求</span><span class="sxs-lookup"><span data-stu-id="c5b34-124">Requirement</span></span> | <span data-ttu-id="c5b34-125">值</span><span class="sxs-lookup"><span data-stu-id="c5b34-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b34-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5b34-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b34-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5b34-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c5b34-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5b34-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b34-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5b34-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c5b34-130">標頭</span><span class="sxs-lookup"><span data-stu-id="c5b34-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5b34-131"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5b34-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c5b34-132">Idl</span><span class="sxs-lookup"><span data-stu-id="c5b34-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c5b34-133"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c5b34-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="c5b34-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c5b34-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5b34-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5b34-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c5b34-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5b34-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b34-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="c5b34-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





