---
description: 變更指派給子集區之資源的父集區資源設定。
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Msvm_ResourcePoolConfigurationService 類別的 ModifyPoolResources 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850955"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="d5ded-103">Msvm ResourcePoolConfigurationService 類別的 ModifyPoolResources 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d5ded-103">ModifyPoolResources method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="d5ded-104">變更指派給子集區之資源的父集區資源設定。</span><span class="sxs-lookup"><span data-stu-id="d5ded-104">Changes the parent pool resource settings for resources assigned to a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ded-105">語法</span><span class="sxs-lookup"><span data-stu-id="d5ded-105">Syntax</span></span>


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d5ded-106">參數</span><span class="sxs-lookup"><span data-stu-id="d5ded-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ded-107">*ChildPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5ded-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ded-108">[**CIM \_ ResourcePool**](cim-resourcepool.md)類別實例的參考，代表要修改的子集區。</span><span class="sxs-lookup"><span data-stu-id="d5ded-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="d5ded-109">*ParentPools* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5ded-109">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ded-110">[**CIM \_ ResourcePool**](cim-resourcepool.md)參考的陣列，代表要指派給子集區的新父集區。</span><span class="sxs-lookup"><span data-stu-id="d5ded-110">An array of [**CIM\_ResourcePool**](cim-resourcepool.md) references that represent the new parent pools to assign to the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="d5ded-111">*AllocationSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d5ded-111">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ded-112">一或多個 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例的選擇性陣列，用來指定集區配置的相關設定。</span><span class="sxs-lookup"><span data-stu-id="d5ded-112">An optional array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span>

</dd> <dt>

<span data-ttu-id="d5ded-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d5ded-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ded-114">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d5ded-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ded-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5ded-115">Return value</span></span>

<span data-ttu-id="d5ded-116">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d5ded-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d5ded-117">**作業已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="d5ded-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-118">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d5ded-118">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="d5ded-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-120">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="d5ded-120">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-121">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="d5ded-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-122">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="d5ded-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-123">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="d5ded-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-124">**未知** 的 (32771) </span><span class="sxs-lookup"><span data-stu-id="d5ded-124">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-125">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="d5ded-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-126">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="d5ded-126">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-127">**使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="d5ded-127">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-128">**不正確狀態** (32775) </span><span class="sxs-lookup"><span data-stu-id="d5ded-128">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-129">集區 (32776) **不正確的資源類型**</span><span class="sxs-lookup"><span data-stu-id="d5ded-129">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-130">**無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="d5ded-130">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-131">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="d5ded-131">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-132">**廠商保留** (32779) </span><span class="sxs-lookup"><span data-stu-id="d5ded-132">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-133">**資源不足** (32780) </span><span class="sxs-lookup"><span data-stu-id="d5ded-133">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-134">**找不到物件** (32781 32787) </span><span class="sxs-lookup"><span data-stu-id="d5ded-134">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-135">**物件存在** (32788) </span><span class="sxs-lookup"><span data-stu-id="d5ded-135">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="d5ded-136">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="d5ded-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d5ded-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5ded-137">Requirements</span></span>



| <span data-ttu-id="d5ded-138">需求</span><span class="sxs-lookup"><span data-stu-id="d5ded-138">Requirement</span></span> | <span data-ttu-id="d5ded-139">值</span><span class="sxs-lookup"><span data-stu-id="d5ded-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ded-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5ded-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d5ded-141">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5ded-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d5ded-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5ded-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d5ded-143">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5ded-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5ded-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="d5ded-144">Namespace</span></span><br/>                | <span data-ttu-id="d5ded-145">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d5ded-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d5ded-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d5ded-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5ded-147"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d5ded-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5ded-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d5ded-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5ded-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5ded-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d5ded-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5ded-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ded-151">**Msvm \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="d5ded-151">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

