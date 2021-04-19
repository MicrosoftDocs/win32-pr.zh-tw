---
description: 修改虛擬機器的目前安全性設定。
ms.assetid: b3eedab6-fd69-4c54-a8bf-4e3b77207687
title: Msvm_SecurityService 類別的 ModifySecuritySettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.ModifySecuritySettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4422f04be1833d66280392704630fcb670eba810
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989998"
---
# <a name="modifysecuritysettings-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="28019-103">Msvm SecurityService 類別的 ModifySecuritySettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="28019-103">ModifySecuritySettings method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="28019-104">修改虛擬機器的目前安全性設定。</span><span class="sxs-lookup"><span data-stu-id="28019-104">Modifies the current security settings of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="28019-105">語法</span><span class="sxs-lookup"><span data-stu-id="28019-105">Syntax</span></span>


```mof
uint32 ModifySecuritySettings(
  [in]  string              SecuritySettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="28019-106">參數</span><span class="sxs-lookup"><span data-stu-id="28019-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28019-107">*SecuritySettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28019-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28019-108">新的安全性設定資料。</span><span class="sxs-lookup"><span data-stu-id="28019-108">The new security setting data.</span></span>

</dd> <dt>

<span data-ttu-id="28019-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="28019-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28019-110">用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="28019-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="28019-111">如果作業是以非同步方式執行，則傳回值為4096。</span><span class="sxs-lookup"><span data-stu-id="28019-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28019-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="28019-112">Return value</span></span>

<span data-ttu-id="28019-113">成功時，會傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="28019-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="28019-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="28019-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="28019-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="28019-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="28019-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="28019-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="28019-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="28019-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="28019-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="28019-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="28019-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="28019-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="28019-120"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="28019-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="28019-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="28019-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="28019-122">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="28019-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="28019-123">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="28019-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="28019-124">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="28019-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="28019-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="28019-125">Requirements</span></span>



| <span data-ttu-id="28019-126">需求</span><span class="sxs-lookup"><span data-stu-id="28019-126">Requirement</span></span> | <span data-ttu-id="28019-127">值</span><span class="sxs-lookup"><span data-stu-id="28019-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28019-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28019-128">Minimum supported client</span></span><br/> | <span data-ttu-id="28019-129">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28019-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="28019-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28019-130">Minimum supported server</span></span><br/> | <span data-ttu-id="28019-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="28019-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="28019-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="28019-132">Namespace</span></span><br/>                | <span data-ttu-id="28019-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="28019-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="28019-134">MOF</span><span class="sxs-lookup"><span data-stu-id="28019-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28019-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="28019-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="28019-136">DLL</span><span class="sxs-lookup"><span data-stu-id="28019-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28019-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28019-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="28019-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28019-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28019-139">**Msvm \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="28019-139">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




