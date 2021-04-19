---
title: 'INapEnforcementClientConnection SetFlags 方法 (NapEnforcementClient .h) '
description: '是用來區分因為 enforcers 快取的 SoHRequests 而回應的第一次回應。 |INapEnforcementClientConnection SetFlags 方法 (NapEnforcementClient .h) '
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- SetFlags 方法 NAP
- SetFlags 方法 NAP，INapEnforcementClientConnection 介面
- INapEnforcementClientConnection 介面 NAP，SetFlags 方法
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489997fb97f0e97c5a72d23646af8ae92272628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993828"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a><span data-ttu-id="fd72b-107">INapEnforcementClientConnection：： SetFlags 方法</span><span class="sxs-lookup"><span data-stu-id="fd72b-107">INapEnforcementClientConnection::SetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="fd72b-108">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="fd72b-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fd72b-109">**INapEnforcementClientConnection：： SetFlags** 方法可用來區分因為 enforcers 快取的 SoHRequests 所產生之回應的第一次回應。</span><span class="sxs-lookup"><span data-stu-id="fd72b-109">The **INapEnforcementClientConnection::SetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd72b-110">語法</span><span class="sxs-lookup"><span data-stu-id="fd72b-110">Syntax</span></span>


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a><span data-ttu-id="fd72b-111">參數</span><span class="sxs-lookup"><span data-stu-id="fd72b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd72b-112">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fd72b-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd72b-113">判斷 [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) 是否因為快取 **SoHRequest** 所造成的旗標。</span><span class="sxs-lookup"><span data-stu-id="fd72b-113">Flags that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="fd72b-114">如果 *旗標* 的值為 [**freshSoHRequest**](nap-type-constants.md)，則為新的要求;否則，它會是快取的要求。</span><span class="sxs-lookup"><span data-stu-id="fd72b-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd72b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd72b-115">Return value</span></span>

<span data-ttu-id="fd72b-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fd72b-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fd72b-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fd72b-117">Return code</span></span>                                                                                     | <span data-ttu-id="fd72b-118">Description</span><span class="sxs-lookup"><span data-stu-id="fd72b-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fd72b-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fd72b-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="fd72b-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="fd72b-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fd72b-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fd72b-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="fd72b-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="fd72b-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fd72b-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fd72b-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="fd72b-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="fd72b-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd72b-125">備註</span><span class="sxs-lookup"><span data-stu-id="fd72b-125">Remarks</span></span>

<span data-ttu-id="fd72b-126">此值是由 NapAgent 所設定。</span><span class="sxs-lookup"><span data-stu-id="fd72b-126">This value is set by the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd72b-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd72b-127">Requirements</span></span>



| <span data-ttu-id="fd72b-128">需求</span><span class="sxs-lookup"><span data-stu-id="fd72b-128">Requirement</span></span> | <span data-ttu-id="fd72b-129">值</span><span class="sxs-lookup"><span data-stu-id="fd72b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd72b-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fd72b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fd72b-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd72b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fd72b-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fd72b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fd72b-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fd72b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fd72b-134">標頭</span><span class="sxs-lookup"><span data-stu-id="fd72b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd72b-135"><dt>NapEnforcementClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="fd72b-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fd72b-136">Idl</span><span class="sxs-lookup"><span data-stu-id="fd72b-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fd72b-137"><dt>NapEnforcementClient .idl</dt></span><span class="sxs-lookup"><span data-stu-id="fd72b-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="fd72b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fd72b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd72b-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd72b-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fd72b-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd72b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd72b-141">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="fd72b-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





