---
title: 'INapEnforcementClientConnection GetSoHRequest 方法 (NapEnforcementClient .h) '
description: 取得目前的 SoH 要求。
ms.assetid: 21397a0d-ef18-494e-9c5a-43d7f6216a67
keywords:
- GetSoHRequest 方法 NAP
- GetSoHRequest 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6115e607f810aef67911ec7d7800d35207368e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934164"
---
# <a name="inapenforcementclientconnectiongetsohrequest-method"></a><span data-ttu-id="60209-106">INapEnforcementClientConnection：： GetSoHRequest 方法</span><span class="sxs-lookup"><span data-stu-id="60209-106">INapEnforcementClientConnection::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="60209-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="60209-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="60209-108">**INapEnforcementClientConnection：： GetSoHRequest** 方法會取得目前的 SoH 要求。</span><span class="sxs-lookup"><span data-stu-id="60209-108">The **INapEnforcementClientConnection::GetSoHRequest** method gets the current SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="60209-109">語法</span><span class="sxs-lookup"><span data-stu-id="60209-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] NetworkSoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="60209-110">參數</span><span class="sxs-lookup"><span data-stu-id="60209-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60209-111">*sohRequest* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="60209-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60209-112">指向 [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) 結構指標的指標，這是 enforcer 的不透明資料 blob。</span><span class="sxs-lookup"><span data-stu-id="60209-112">A pointer to a pointer to a [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60209-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="60209-113">Return value</span></span>

<span data-ttu-id="60209-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="60209-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="60209-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="60209-115">Return code</span></span>                                                                                     | <span data-ttu-id="60209-116">Description</span><span class="sxs-lookup"><span data-stu-id="60209-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="60209-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="60209-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="60209-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="60209-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="60209-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="60209-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="60209-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="60209-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="60209-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="60209-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="60209-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="60209-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60209-123">備註</span><span class="sxs-lookup"><span data-stu-id="60209-123">Remarks</span></span>

<span data-ttu-id="60209-124">這是由 NapAgent 所設定，並由 enforcers 查詢，以在網路上傳送。</span><span class="sxs-lookup"><span data-stu-id="60209-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="60209-125">零位元組長度的 SoH 封包無效。</span><span class="sxs-lookup"><span data-stu-id="60209-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="60209-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="60209-126">Requirements</span></span>



| <span data-ttu-id="60209-127">需求</span><span class="sxs-lookup"><span data-stu-id="60209-127">Requirement</span></span> | <span data-ttu-id="60209-128">值</span><span class="sxs-lookup"><span data-stu-id="60209-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60209-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60209-129">Minimum supported client</span></span><br/> | <span data-ttu-id="60209-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60209-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="60209-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60209-131">Minimum supported server</span></span><br/> | <span data-ttu-id="60209-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60209-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="60209-133">標頭</span><span class="sxs-lookup"><span data-stu-id="60209-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="60209-134"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="60209-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="60209-135">Idl</span><span class="sxs-lookup"><span data-stu-id="60209-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60209-136"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="60209-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="60209-137">DLL</span><span class="sxs-lookup"><span data-stu-id="60209-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60209-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60209-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="60209-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60209-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60209-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="60209-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





