---
title: 'INapSystemHealthValidationRequest GetMachineName 方法 (NapSystemHealthValidator .h) '
description: 系統健康狀態驗證 (Shv) 用來取出 NAP 用戶端的電腦名稱稱。 然後，SHV 會記錄這些資訊。
ms.assetid: 2ea6a65d-1579-4a05-b5bc-aebf6421e46a
keywords:
- GetMachineName 方法 NAP
- GetMachineName 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，GetMachineName 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetMachineName
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1c3e264d7d2d6e4d93e3ad71d7f3adc92ff8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106506"
---
# <a name="inapsystemhealthvalidationrequestgetmachinename-method"></a><span data-ttu-id="1fc99-107">INapSystemHealthValidationRequest：： GetMachineName 方法</span><span class="sxs-lookup"><span data-stu-id="1fc99-107">INapSystemHealthValidationRequest::GetMachineName method</span></span>

> [!Note]  
> <span data-ttu-id="1fc99-108">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="1fc99-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1fc99-109">**INapSystemHealthValidationRequest：： GetMachineName** 方法是由系統健康狀態驗證 (shv) 用來取出 NAP 用戶端的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="1fc99-109">The **INapSystemHealthValidationRequest::GetMachineName** method is used by System Health Validators (SHVs) to retrieve the machine name of the NAP client.</span></span> <span data-ttu-id="1fc99-110">然後，SHV 會記錄這些資訊。</span><span class="sxs-lookup"><span data-stu-id="1fc99-110">The SHV then logs this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc99-111">語法</span><span class="sxs-lookup"><span data-stu-id="1fc99-111">Syntax</span></span>


```C++
HRESULT GetMachineName(
  [out] CountedString **machineName
);
```



## <a name="parameters"></a><span data-ttu-id="1fc99-112">參數</span><span class="sxs-lookup"><span data-stu-id="1fc99-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc99-113">*machineName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1fc99-113">*machineName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc99-114">[**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring)結構指標的指標，其中包含 NAP 用戶端的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="1fc99-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fc99-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1fc99-115">Return value</span></span>

<span data-ttu-id="1fc99-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1fc99-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1fc99-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1fc99-117">Return code</span></span>                                                                                     | <span data-ttu-id="1fc99-118">Description</span><span class="sxs-lookup"><span data-stu-id="1fc99-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1fc99-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1fc99-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1fc99-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="1fc99-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1fc99-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1fc99-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1fc99-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="1fc99-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1fc99-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1fc99-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1fc99-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="1fc99-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1fc99-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1fc99-125">Requirements</span></span>



| <span data-ttu-id="1fc99-126">需求</span><span class="sxs-lookup"><span data-stu-id="1fc99-126">Requirement</span></span> | <span data-ttu-id="1fc99-127">值</span><span class="sxs-lookup"><span data-stu-id="1fc99-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc99-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1fc99-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc99-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="1fc99-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="1fc99-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1fc99-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc99-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1fc99-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1fc99-132">標頭</span><span class="sxs-lookup"><span data-stu-id="1fc99-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fc99-133"><dt>NapSystemHealthValidator。h</dt></span><span class="sxs-lookup"><span data-stu-id="1fc99-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fc99-134">Idl</span><span class="sxs-lookup"><span data-stu-id="1fc99-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1fc99-135"><dt>NapSystemHealthValidator .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1fc99-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="1fc99-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1fc99-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fc99-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fc99-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="1fc99-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1fc99-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc99-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="1fc99-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





