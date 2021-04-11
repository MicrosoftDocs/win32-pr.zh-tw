---
title: 'INapServerManagement SetFailureCategoryMappings 方法 (NapServerManagement .h) '
description: 用來設定 SHV 的失敗類別對應。
ms.assetid: be482f82-c79c-405c-b619-9bcb9b4dc349
keywords:
- SetFailureCategoryMappings 方法 NAP
- SetFailureCategoryMappings 方法 NAP，INapServerManagement 介面
- INapServerManagement 介面 NAP，SetFailureCategoryMappings 方法
topic_type:
- apiref
api_name:
- INapServerManagement.SetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a220d6603ef5bbb49377ac0e212d5d98afa4bdd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934676"
---
# <a name="inapservermanagementsetfailurecategorymappings-method"></a><span data-ttu-id="50bed-106">INapServerManagement：： SetFailureCategoryMappings 方法</span><span class="sxs-lookup"><span data-stu-id="50bed-106">INapServerManagement::SetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="50bed-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="50bed-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="50bed-108">**INapServerManagement：： SetFailureCategoryMappings** 方法是用來設定 SHV 的失敗類別對應。</span><span class="sxs-lookup"><span data-stu-id="50bed-108">The **INapServerManagement::SetFailureCategoryMappings** method is used to set the SHV's failure category mappings.</span></span>

## <a name="syntax"></a><span data-ttu-id="50bed-109">語法</span><span class="sxs-lookup"><span data-stu-id="50bed-109">Syntax</span></span>


```C++
HRESULT SetFailureCategoryMappings(
  [in]       SystemHealthEntityId   id,
  [in] const FailureCategoryMapping mapping
);
```



## <a name="parameters"></a><span data-ttu-id="50bed-110">參數</span><span class="sxs-lookup"><span data-stu-id="50bed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50bed-111"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="50bed-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50bed-112">[**SystemHealthEntityId**](nap-type-constants.md) ，其中包含 SHV 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="50bed-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="50bed-113">*對應* \[在\]</span><span class="sxs-lookup"><span data-stu-id="50bed-113">*mapping* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50bed-114">包含失敗分類對應資料的 [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) 結構。</span><span class="sxs-lookup"><span data-stu-id="50bed-114">A [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure that contains the failure category mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50bed-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="50bed-115">Return value</span></span>

<span data-ttu-id="50bed-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="50bed-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="50bed-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="50bed-117">Return code</span></span>                                                                                     | <span data-ttu-id="50bed-118">Description</span><span class="sxs-lookup"><span data-stu-id="50bed-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="50bed-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="50bed-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="50bed-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="50bed-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="50bed-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="50bed-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="50bed-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="50bed-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="50bed-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="50bed-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="50bed-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="50bed-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="50bed-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="50bed-125">Requirements</span></span>



| <span data-ttu-id="50bed-126">需求</span><span class="sxs-lookup"><span data-stu-id="50bed-126">Requirement</span></span> | <span data-ttu-id="50bed-127">值</span><span class="sxs-lookup"><span data-stu-id="50bed-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50bed-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50bed-128">Minimum supported client</span></span><br/> | <span data-ttu-id="50bed-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="50bed-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="50bed-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50bed-130">Minimum supported server</span></span><br/> | <span data-ttu-id="50bed-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50bed-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="50bed-132">標頭</span><span class="sxs-lookup"><span data-stu-id="50bed-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="50bed-133"><dt>NapServerManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="50bed-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="50bed-134">Idl</span><span class="sxs-lookup"><span data-stu-id="50bed-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50bed-135"><dt>NapServerManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="50bed-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="50bed-136">DLL</span><span class="sxs-lookup"><span data-stu-id="50bed-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50bed-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50bed-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="50bed-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50bed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50bed-139">**INapServerManagement**</span><span class="sxs-lookup"><span data-stu-id="50bed-139">**INapServerManagement**</span></span>](inapservermanagement.md)
</dt> </dl>

 

 





