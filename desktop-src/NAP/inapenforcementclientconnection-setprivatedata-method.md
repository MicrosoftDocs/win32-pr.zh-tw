---
title: 'INapEnforcementClientConnection SetPrivateData 方法 (NapEnforcementClient .h) '
description: NapAgent 會使用來設定私用資料。
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- SetPrivateData 方法 NAP
- SetPrivateData 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetPrivateData 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e73248e546b1f0e48438553877f0523bd30b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024888"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a><span data-ttu-id="ec26e-106">INapEnforcementClientConnection：： SetPrivateData 方法</span><span class="sxs-lookup"><span data-stu-id="ec26e-106">INapEnforcementClientConnection::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="ec26e-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="ec26e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ec26e-108">NapAgent 會使用 **INapEnforcementClientConnection：： SetPrivateData** 方法來設定私用資料。</span><span class="sxs-lookup"><span data-stu-id="ec26e-108">The **INapEnforcementClientConnection::SetPrivateData** method is used by the NapAgent to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec26e-109">語法</span><span class="sxs-lookup"><span data-stu-id="ec26e-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="ec26e-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec26e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec26e-111">*privateData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec26e-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec26e-112">只有 NapAgent 可以解讀的 [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) 資料 blob 指標。</span><span class="sxs-lookup"><span data-stu-id="ec26e-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec26e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec26e-113">Return value</span></span>

<span data-ttu-id="ec26e-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ec26e-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ec26e-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ec26e-115">Return code</span></span>                                                                                     | <span data-ttu-id="ec26e-116">Description</span><span class="sxs-lookup"><span data-stu-id="ec26e-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec26e-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ec26e-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="ec26e-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ec26e-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ec26e-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ec26e-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="ec26e-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="ec26e-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ec26e-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ec26e-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="ec26e-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="ec26e-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ec26e-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec26e-123">Requirements</span></span>



| <span data-ttu-id="ec26e-124">需求</span><span class="sxs-lookup"><span data-stu-id="ec26e-124">Requirement</span></span> | <span data-ttu-id="ec26e-125">值</span><span class="sxs-lookup"><span data-stu-id="ec26e-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec26e-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec26e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ec26e-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec26e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ec26e-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec26e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ec26e-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec26e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ec26e-130">標頭</span><span class="sxs-lookup"><span data-stu-id="ec26e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec26e-131"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec26e-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec26e-132">Idl</span><span class="sxs-lookup"><span data-stu-id="ec26e-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ec26e-133"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ec26e-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="ec26e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ec26e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec26e-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec26e-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ec26e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec26e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec26e-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="ec26e-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





