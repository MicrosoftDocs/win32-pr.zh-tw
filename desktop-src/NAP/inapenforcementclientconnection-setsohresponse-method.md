---
title: 'INapEnforcementClientConnection SetSoHResponse 方法 (NapEnforcementClient .h) '
description: 設定 SoH-Response，並在接收封包時由強制用戶端使用。
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- SetSoHResponse 方法 NAP
- SetSoHResponse 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetSoHResponse 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdc403a1ff68e28f7d262e64ebe558226741b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466185"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a><span data-ttu-id="60c91-106">INapEnforcementClientConnection：： SetSoHResponse 方法</span><span class="sxs-lookup"><span data-stu-id="60c91-106">INapEnforcementClientConnection::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="60c91-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="60c91-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="60c91-108">**INapEnforcementClientConnection：： SetSoHResponse** 方法會設定 SoH-Response，並在接收封包時由強制用戶端使用。</span><span class="sxs-lookup"><span data-stu-id="60c91-108">The **INapEnforcementClientConnection::SetSoHResponse** method sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c91-109">語法</span><span class="sxs-lookup"><span data-stu-id="60c91-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="60c91-110">參數</span><span class="sxs-lookup"><span data-stu-id="60c91-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60c91-111">*sohResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60c91-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60c91-112">唯一 [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) 結構的指標，這是 enforcer 的不透明資料 blob。</span><span class="sxs-lookup"><span data-stu-id="60c91-112">A pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60c91-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="60c91-113">Return value</span></span>

<span data-ttu-id="60c91-114">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="60c91-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="60c91-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="60c91-115">Return code</span></span>                                                                                     | <span data-ttu-id="60c91-116">Description</span><span class="sxs-lookup"><span data-stu-id="60c91-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="60c91-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="60c91-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="60c91-118">SoH 封包有效。</span><span class="sxs-lookup"><span data-stu-id="60c91-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="60c91-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="60c91-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="60c91-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="60c91-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="60c91-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="60c91-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="60c91-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="60c91-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="60c91-123">備註</span><span class="sxs-lookup"><span data-stu-id="60c91-123">Remarks</span></span>

<span data-ttu-id="60c91-124">大小為零的封包有效。</span><span class="sxs-lookup"><span data-stu-id="60c91-124">A zero-sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="60c91-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="60c91-125">Requirements</span></span>



| <span data-ttu-id="60c91-126">需求</span><span class="sxs-lookup"><span data-stu-id="60c91-126">Requirement</span></span> | <span data-ttu-id="60c91-127">值</span><span class="sxs-lookup"><span data-stu-id="60c91-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c91-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60c91-128">Minimum supported client</span></span><br/> | <span data-ttu-id="60c91-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60c91-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="60c91-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60c91-130">Minimum supported server</span></span><br/> | <span data-ttu-id="60c91-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60c91-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="60c91-132">標頭</span><span class="sxs-lookup"><span data-stu-id="60c91-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="60c91-133"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="60c91-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="60c91-134">Idl</span><span class="sxs-lookup"><span data-stu-id="60c91-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60c91-135"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="60c91-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="60c91-136">DLL</span><span class="sxs-lookup"><span data-stu-id="60c91-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60c91-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60c91-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="60c91-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60c91-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c91-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="60c91-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





