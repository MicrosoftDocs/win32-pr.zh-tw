---
title: 'INapEnforcementClientConnection SetSoHRequest 方法 (NapEnforcementClient .h) '
description: 設定 SoH 要求。
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- SetSoHRequest 方法 NAP
- SetSoHRequest 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetSoHRequest 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92559d532e99bfa29d7f62fd29b279db20f2c0a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685760"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a><span data-ttu-id="9a6b6-106">INapEnforcementClientConnection：： SetSoHRequest 方法</span><span class="sxs-lookup"><span data-stu-id="9a6b6-106">INapEnforcementClientConnection::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="9a6b6-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="9a6b6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9a6b6-108">**INapEnforcementClientConnection：： SetSoHRequest** 方法會設定 SoH 要求。</span><span class="sxs-lookup"><span data-stu-id="9a6b6-108">The **INapEnforcementClientConnection::SetSoHRequest** method sets the SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a6b6-109">語法</span><span class="sxs-lookup"><span data-stu-id="9a6b6-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="9a6b6-110">參數</span><span class="sxs-lookup"><span data-stu-id="9a6b6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a6b6-111">*sohRequest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9a6b6-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a6b6-112">唯一 [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) 結構的指標，這是 enforcer 的不透明資料 blob。</span><span class="sxs-lookup"><span data-stu-id="9a6b6-112">A pointer to a unique [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a6b6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9a6b6-113">Return value</span></span>

<span data-ttu-id="9a6b6-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9a6b6-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="9a6b6-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9a6b6-115">Return code</span></span>                                                                                     | <span data-ttu-id="9a6b6-116">Description</span><span class="sxs-lookup"><span data-stu-id="9a6b6-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a6b6-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9a6b6-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9a6b6-118">SoH 封包有效。</span><span class="sxs-lookup"><span data-stu-id="9a6b6-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="9a6b6-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="9a6b6-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9a6b6-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="9a6b6-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9a6b6-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9a6b6-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9a6b6-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="9a6b6-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9a6b6-123">備註</span><span class="sxs-lookup"><span data-stu-id="9a6b6-123">Remarks</span></span>

<span data-ttu-id="9a6b6-124">這是由 NapAgent 所設定，並由 enforcers 查詢，以在網路上傳送。</span><span class="sxs-lookup"><span data-stu-id="9a6b6-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="9a6b6-125">零位元組長度的 SoH 封包無效。</span><span class="sxs-lookup"><span data-stu-id="9a6b6-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a6b6-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a6b6-126">Requirements</span></span>



| <span data-ttu-id="9a6b6-127">需求</span><span class="sxs-lookup"><span data-stu-id="9a6b6-127">Requirement</span></span> | <span data-ttu-id="9a6b6-128">值</span><span class="sxs-lookup"><span data-stu-id="9a6b6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a6b6-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a6b6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9a6b6-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a6b6-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9a6b6-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a6b6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9a6b6-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a6b6-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9a6b6-133">標頭</span><span class="sxs-lookup"><span data-stu-id="9a6b6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a6b6-134"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a6b6-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a6b6-135">Idl</span><span class="sxs-lookup"><span data-stu-id="9a6b6-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a6b6-136"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a6b6-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="9a6b6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="9a6b6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a6b6-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a6b6-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="9a6b6-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a6b6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a6b6-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="9a6b6-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





