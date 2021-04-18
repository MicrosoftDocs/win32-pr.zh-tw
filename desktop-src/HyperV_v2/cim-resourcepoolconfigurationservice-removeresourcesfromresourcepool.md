---
description: 啟動作業，以從資源集區中移除資源。
ms.assetid: 1689ccbf-a524-45b7-bf95-6341a3b28f6c
title: CIM_ResourcePoolConfigurationService 類別的 RemoveResourcesFromResourcePool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.RemoveResourcesFromResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41c8a7d1608b9c4d5ea629aa9c053e022d59d9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511849"
---
# <a name="removeresourcesfromresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="a5126-103">CIM ResourcePoolConfigurationService 類別的 RemoveResourcesFromResourcePool 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a5126-103">RemoveResourcesFromResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="a5126-104">啟動作業，以從資源集區中移除資源。</span><span class="sxs-lookup"><span data-stu-id="a5126-104">Starts a job to remove resources from a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5126-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5126-105">Syntax</span></span>


```mof
uint32 RemoveResourcesFromResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a5126-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5126-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5126-107">*HostResources* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a5126-107">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5126-108">要從集區中移除的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 實例陣列。</span><span class="sxs-lookup"><span data-stu-id="a5126-108">Array of [**CIM\_LogicalDevice**](cim-logicaldevice.md) instances to remove from the pool.</span></span>

</dd> <dt>

<span data-ttu-id="a5126-109">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="a5126-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5126-110">[**CIM \_ ResourcePool**](cim-resourcepool.md) ，代表要從中移除資源的集區。</span><span class="sxs-lookup"><span data-stu-id="a5126-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) representing the pool to remove the resources from.</span></span>

</dd> <dt>

<span data-ttu-id="a5126-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a5126-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5126-112">如果作業已完成) ，則參考作業 (的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 可能會是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="a5126-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5126-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5126-113">Return value</span></span>

<span data-ttu-id="a5126-114">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="a5126-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="a5126-115">**作業已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a5126-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-116">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="a5126-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-117">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="a5126-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-118">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="a5126-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-119">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="a5126-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-120">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="a5126-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-121">**使用** (6) </span><span class="sxs-lookup"><span data-stu-id="a5126-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-122">集區的 ResourceType (7) **不正確**</span><span class="sxs-lookup"><span data-stu-id="a5126-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="a5126-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="a5126-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-125"> (4097) **不支援的大小**</span><span class="sxs-lookup"><span data-stu-id="a5126-125">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-126">**方法保留** (4098. 32767) </span><span class="sxs-lookup"><span data-stu-id="a5126-126">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a5126-127">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="a5126-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a5126-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5126-128">Requirements</span></span>



| <span data-ttu-id="a5126-129">需求</span><span class="sxs-lookup"><span data-stu-id="a5126-129">Requirement</span></span> | <span data-ttu-id="a5126-130">值</span><span class="sxs-lookup"><span data-stu-id="a5126-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5126-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5126-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a5126-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a5126-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="a5126-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5126-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a5126-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a5126-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="a5126-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="a5126-135">Namespace</span></span><br/>                | <span data-ttu-id="a5126-136">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="a5126-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a5126-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a5126-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5126-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a5126-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5126-139">DLL</span><span class="sxs-lookup"><span data-stu-id="a5126-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5126-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a5126-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a5126-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5126-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5126-142">**CIM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="a5126-142">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




