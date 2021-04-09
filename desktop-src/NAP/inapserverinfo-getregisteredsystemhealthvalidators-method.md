---
title: 'INapServerInfo GetRegisteredSystemHealthValidators 方法 (NapServerManagement .h) '
description: 抓取已註冊的 Shv 清單。
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- GetRegisteredSystemHealthValidators 方法 NAP
- GetRegisteredSystemHealthValidators 方法 NAP，INapServerInfo 介面
- INapServerInfo 介面 NAP，GetRegisteredSystemHealthValidators 方法
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ffdd4d363c994efbecdb57fe4ad7203393fd1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025363"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a><span data-ttu-id="0ae43-106">INapServerInfo：： GetRegisteredSystemHealthValidators 方法</span><span class="sxs-lookup"><span data-stu-id="0ae43-106">INapServerInfo::GetRegisteredSystemHealthValidators method</span></span>

> [!Note]  
> <span data-ttu-id="0ae43-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="0ae43-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0ae43-108">**INapServerInfo：： GetRegisteredSystemHealthValidators** 方法會抓取已註冊的 shv 清單。</span><span class="sxs-lookup"><span data-stu-id="0ae43-108">The **INapServerInfo::GetRegisteredSystemHealthValidators** method retrieves a list of registered SHVs.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ae43-109">語法</span><span class="sxs-lookup"><span data-stu-id="0ae43-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a><span data-ttu-id="0ae43-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ae43-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ae43-111">*計數* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0ae43-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ae43-112">[**SystemHealthEntityCount**](nap-type-constants.md)的指標，其中包含已註冊之 shv 的數目。</span><span class="sxs-lookup"><span data-stu-id="0ae43-112">A pointer to a [**SystemHealthEntityCount**](nap-type-constants.md) that contains the number of registered SHVs.</span></span>

</dd> <dt>

<span data-ttu-id="0ae43-113">*驗證* \[ 程式擴展\]</span><span class="sxs-lookup"><span data-stu-id="0ae43-113">*validators* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ae43-114">[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)結構指標的指標，其中包含 SHV 註冊資訊。</span><span class="sxs-lookup"><span data-stu-id="0ae43-114">A pointer to a pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the SHV registration information.</span></span>

</dd> <dt>

<span data-ttu-id="0ae43-115">*validatorClsids* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0ae43-115">*validatorClsids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ae43-116">註冊之 Shv 的識別碼陣列指標。</span><span class="sxs-lookup"><span data-stu-id="0ae43-116">Pointer to an array of IDs for the registered SHVs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ae43-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ae43-117">Return value</span></span>

<span data-ttu-id="0ae43-118">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0ae43-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0ae43-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0ae43-119">Return code</span></span>                                                                                     | <span data-ttu-id="0ae43-120">Description</span><span class="sxs-lookup"><span data-stu-id="0ae43-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ae43-121"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0ae43-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0ae43-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="0ae43-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0ae43-123"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0ae43-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0ae43-124">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="0ae43-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0ae43-125"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0ae43-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0ae43-126">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="0ae43-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0ae43-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ae43-127">Requirements</span></span>



| <span data-ttu-id="0ae43-128">需求</span><span class="sxs-lookup"><span data-stu-id="0ae43-128">Requirement</span></span> | <span data-ttu-id="0ae43-129">值</span><span class="sxs-lookup"><span data-stu-id="0ae43-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ae43-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ae43-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0ae43-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="0ae43-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="0ae43-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ae43-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0ae43-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ae43-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0ae43-134">標頭</span><span class="sxs-lookup"><span data-stu-id="0ae43-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ae43-135"><dt>NapServerManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ae43-135"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ae43-136">Idl</span><span class="sxs-lookup"><span data-stu-id="0ae43-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ae43-137"><dt>NapServerManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ae43-137"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="0ae43-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0ae43-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ae43-139"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ae43-139"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="0ae43-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ae43-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ae43-141">**NapComponentRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="0ae43-141">**NapComponentRegistrationInfo**</span></span>](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[<span data-ttu-id="0ae43-142">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="0ae43-142">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





