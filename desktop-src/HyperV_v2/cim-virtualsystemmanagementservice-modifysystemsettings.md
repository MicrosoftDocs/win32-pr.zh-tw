---
description: 修改虛擬系統設定。
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: CIM_VirtualSystemManagementService 類別的 ModifySystemSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da610d03e683b06ad743d1b6d4fe413dc5b31d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943900"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="a04c5-103">CIM VirtualSystemManagementService 類別的 ModifySystemSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a04c5-103">ModifySystemSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a04c5-104">修改虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="a04c5-104">Modifies virtual system settings.</span></span>

<span data-ttu-id="a04c5-105">套用至「目前」虛擬系統組態的系統設定時，可能會修改虛擬系統實例。</span><span class="sxs-lookup"><span data-stu-id="a04c5-105">When applied to the system settings of a "current" virtual system configuration, as a side effect the virtual system instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04c5-106">語法</span><span class="sxs-lookup"><span data-stu-id="a04c5-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a04c5-107">參數</span><span class="sxs-lookup"><span data-stu-id="a04c5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a04c5-108">*SystemSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a04c5-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a04c5-109">字串，包含用來修改虛擬系統設定之 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 類別的實例。</span><span class="sxs-lookup"><span data-stu-id="a04c5-109">String containing an instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to modify the settings of the virtual system.</span></span> <span data-ttu-id="a04c5-110">實例必須有有效的 **InstanceID** ，才能識別要修改的虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="a04c5-110">The instance must have a valid **InstanceID** in order to identify the virtual system setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="a04c5-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a04c5-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a04c5-112">如果作業的執行時間很長，則可以選擇性地傳回代表作業的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 。</span><span class="sxs-lookup"><span data-stu-id="a04c5-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a04c5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a04c5-113">Return value</span></span>

<span data-ttu-id="a04c5-114">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a04c5-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a04c5-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a04c5-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a04c5-116">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="a04c5-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a04c5-117">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="a04c5-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a04c5-118">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="a04c5-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a04c5-119">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="a04c5-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a04c5-120">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="a04c5-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a04c5-121"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="a04c5-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a04c5-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a04c5-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a04c5-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a04c5-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a04c5-124">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="a04c5-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a04c5-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a04c5-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a04c5-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a04c5-126">Requirements</span></span>



| <span data-ttu-id="a04c5-127">需求</span><span class="sxs-lookup"><span data-stu-id="a04c5-127">Requirement</span></span> | <span data-ttu-id="a04c5-128">值</span><span class="sxs-lookup"><span data-stu-id="a04c5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a04c5-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a04c5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a04c5-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a04c5-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a04c5-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a04c5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a04c5-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a04c5-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a04c5-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="a04c5-133">Namespace</span></span><br/>                | <span data-ttu-id="a04c5-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a04c5-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a04c5-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a04c5-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a04c5-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a04c5-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a04c5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a04c5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a04c5-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a04c5-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a04c5-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a04c5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a04c5-140">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a04c5-140">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




