---
title: 'INapServerInfo GetFailureCategoryMappings 方法 (NapServerManagement .h) '
description: 抓取指定 SHA 或 SHV 的失敗類別對應。
ms.assetid: 89b89003-40b3-4763-aec8-01cd0c307649
keywords:
- GetFailureCategoryMappings 方法 NAP
- GetFailureCategoryMappings 方法 NAP，INapServerInfo 介面
- INapServerInfo 介面 NAP，GetFailureCategoryMappings 方法
topic_type:
- apiref
api_name:
- INapServerInfo.GetFailureCategoryMappings
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ba830dd8a35a2c60b14c4feec14846125223e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467057"
---
# <a name="inapserverinfogetfailurecategorymappings-method"></a><span data-ttu-id="bdfea-106">INapServerInfo：： GetFailureCategoryMappings 方法</span><span class="sxs-lookup"><span data-stu-id="bdfea-106">INapServerInfo::GetFailureCategoryMappings method</span></span>

> [!Note]  
> <span data-ttu-id="bdfea-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="bdfea-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bdfea-108">**INapServerInfo：： GetFailureCategoryMappings** 方法會抓取指定 SHA 或 SHV 的失敗類別對應。</span><span class="sxs-lookup"><span data-stu-id="bdfea-108">The **INapServerInfo::GetFailureCategoryMappings** method retrieves the failure category mappings for a specified SHA or SHV.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdfea-109">語法</span><span class="sxs-lookup"><span data-stu-id="bdfea-109">Syntax</span></span>


```C++
HRESULT GetFailureCategoryMappings(
  [in]  SystemHealthEntityId   id,
  [out] FailureCategoryMapping *mapping
);
```



## <a name="parameters"></a><span data-ttu-id="bdfea-110">參數</span><span class="sxs-lookup"><span data-stu-id="bdfea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdfea-111"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="bdfea-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdfea-112">[**SystemHealthEntityId**](nap-type-constants.md) ，其中包含 SHA 或 SHV 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="bdfea-112">A [**SystemHealthEntityId**](nap-type-constants.md) that contains the unique identifier of the SHA or the SHV.</span></span>

</dd> <dt>

<span data-ttu-id="bdfea-113">*對應* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bdfea-113">*mapping* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdfea-114">[**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping)的指標，其中包含對應資料。</span><span class="sxs-lookup"><span data-stu-id="bdfea-114">A pointer to a [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) that contains the mapping data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdfea-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bdfea-115">Return value</span></span>

<span data-ttu-id="bdfea-116">也可能傳回其他 COM 特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bdfea-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="bdfea-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bdfea-117">Return code</span></span>                                                                                     | <span data-ttu-id="bdfea-118">Description</span><span class="sxs-lookup"><span data-stu-id="bdfea-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bdfea-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bdfea-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="bdfea-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="bdfea-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bdfea-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bdfea-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="bdfea-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="bdfea-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bdfea-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bdfea-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="bdfea-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="bdfea-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bdfea-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdfea-125">Requirements</span></span>



| <span data-ttu-id="bdfea-126">需求</span><span class="sxs-lookup"><span data-stu-id="bdfea-126">Requirement</span></span> | <span data-ttu-id="bdfea-127">值</span><span class="sxs-lookup"><span data-stu-id="bdfea-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdfea-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bdfea-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bdfea-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="bdfea-129">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="bdfea-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bdfea-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bdfea-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdfea-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bdfea-132">標頭</span><span class="sxs-lookup"><span data-stu-id="bdfea-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdfea-133"><dt>NapServerManagement。h</dt></span><span class="sxs-lookup"><span data-stu-id="bdfea-133"><dt>NapServerManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdfea-134">Idl</span><span class="sxs-lookup"><span data-stu-id="bdfea-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bdfea-135"><dt>NapServerManagement .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bdfea-135"><dt>NapServerManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="bdfea-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bdfea-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdfea-137"><dt>Qsvrmgmt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdfea-137"><dt>Qsvrmgmt.dll</dt></span></span> </dl>            |



## <a name="see-also"></a><span data-ttu-id="bdfea-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdfea-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdfea-139">**INapServerInfo**</span><span class="sxs-lookup"><span data-stu-id="bdfea-139">**INapServerInfo**</span></span>](inapserverinfo.md)
</dt> </dl>

 

 





