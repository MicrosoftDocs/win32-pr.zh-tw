---
title: 'INapEnforcementClientConnection GetFlags 方法 (NapEnforcementClient .h) '
description: '是用來區分因為 enforcers 快取的 SoHRequests 而回應的第一次回應。 |INapEnforcementClientConnection GetFlags 方法 (NapEnforcementClient .h) '
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- GetFlags 方法 NAP
- GetFlags 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，GetFlags 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a35e183b5d4f606d21f4afce8cca68135732a35c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976654"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a><span data-ttu-id="17080-107">INapEnforcementClientConnection：： GetFlags 方法</span><span class="sxs-lookup"><span data-stu-id="17080-107">INapEnforcementClientConnection::GetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="17080-108">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="17080-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="17080-109">**INapEnforcementClientConnection：： GetFlags** 方法可用來區分因為 enforcers 快取的 SoHRequests 所產生之回應的第一次回應。</span><span class="sxs-lookup"><span data-stu-id="17080-109">The **INapEnforcementClientConnection::GetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="17080-110">語法</span><span class="sxs-lookup"><span data-stu-id="17080-110">Syntax</span></span>


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a><span data-ttu-id="17080-111">參數</span><span class="sxs-lookup"><span data-stu-id="17080-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17080-112">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="17080-112">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17080-113">旗標的指標，可判斷 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 是否因為快取 **SoHRequest** 所造成。</span><span class="sxs-lookup"><span data-stu-id="17080-113">A pointer to a flag that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="17080-114">如果 *旗標* 的值為 [**freshSoHRequest**](nap-type-constants.md)，則為新的要求;否則，它會是快取的要求。</span><span class="sxs-lookup"><span data-stu-id="17080-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17080-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="17080-115">Return value</span></span>

<span data-ttu-id="17080-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="17080-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="17080-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="17080-117">Return code</span></span>                                                                                     | <span data-ttu-id="17080-118">Description</span><span class="sxs-lookup"><span data-stu-id="17080-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="17080-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="17080-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="17080-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="17080-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="17080-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="17080-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="17080-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="17080-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="17080-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="17080-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="17080-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="17080-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="17080-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="17080-125">Requirements</span></span>



| <span data-ttu-id="17080-126">需求</span><span class="sxs-lookup"><span data-stu-id="17080-126">Requirement</span></span> | <span data-ttu-id="17080-127">值</span><span class="sxs-lookup"><span data-stu-id="17080-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17080-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17080-128">Minimum supported client</span></span><br/> | <span data-ttu-id="17080-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17080-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="17080-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17080-130">Minimum supported server</span></span><br/> | <span data-ttu-id="17080-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17080-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="17080-132">標頭</span><span class="sxs-lookup"><span data-stu-id="17080-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="17080-133"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="17080-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="17080-134">Idl</span><span class="sxs-lookup"><span data-stu-id="17080-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17080-135"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="17080-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="17080-136">DLL</span><span class="sxs-lookup"><span data-stu-id="17080-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17080-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17080-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="17080-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17080-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17080-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="17080-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





