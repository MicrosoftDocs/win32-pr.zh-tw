---
description: 啟動建立根 ResourcePool 的作業。 ResourcePool 的範圍會設定為與此服務相同的系統。
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: CIM_ResourcePoolConfigurationService 類別的 CreateResourcePool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690800"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="79dd7-104">CIM ResourcePoolConfigurationService 類別的 CreateResourcePool 方法 \_</span><span class="sxs-lookup"><span data-stu-id="79dd7-104">CreateResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="79dd7-105">啟動建立根 ResourcePool 的作業。</span><span class="sxs-lookup"><span data-stu-id="79dd7-105">Starts a job to create a root ResourcePool.</span></span> <span data-ttu-id="79dd7-106">ResourcePool 的範圍會設定為與此服務相同的系統。</span><span class="sxs-lookup"><span data-stu-id="79dd7-106">The ResourcePool will be scoped to the same System as this Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="79dd7-107">語法</span><span class="sxs-lookup"><span data-stu-id="79dd7-107">Syntax</span></span>


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="79dd7-108">參數</span><span class="sxs-lookup"><span data-stu-id="79dd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79dd7-109">*ElementName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79dd7-109">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79dd7-110">要建立之集區的終端使用者相關名稱。</span><span class="sxs-lookup"><span data-stu-id="79dd7-110">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="79dd7-111">如果是 **Null**，則可以使用系統提供的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="79dd7-111">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="79dd7-112">值會儲存在所建立集區的 **ElementName** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="79dd7-112">The value will be stored in the **ElementName** property for the created pool.</span></span>

</dd> <dt>

<span data-ttu-id="79dd7-113">*HostResources* \[在\]</span><span class="sxs-lookup"><span data-stu-id="79dd7-113">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79dd7-114">零或多個 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 裝置的陣列，用來建立集區或修改來源延伸。</span><span class="sxs-lookup"><span data-stu-id="79dd7-114">Array of zero or more [**CIM\_LogicalDevice**](cim-logicaldevice.md) devices that are used to create the Pool or modify the source extents.</span></span> <span data-ttu-id="79dd7-115">陣列中的所有元素都必須是相同的類型。</span><span class="sxs-lookup"><span data-stu-id="79dd7-115">All elements in the array must be of the same type.</span></span>

</dd> <dt>

<span data-ttu-id="79dd7-116">*ResourceType* \[in\]</span><span class="sxs-lookup"><span data-stu-id="79dd7-116">*ResourceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79dd7-117">所建立集區將管理的資源類型。</span><span class="sxs-lookup"><span data-stu-id="79dd7-117">The type of resources the created pool will manage.</span></span> <span data-ttu-id="79dd7-118">如果 *HostResources* 包含元素，此屬性必須符合其型別。</span><span class="sxs-lookup"><span data-stu-id="79dd7-118">If *HostResources* contains elements, this property must mach their type.</span></span>

</dd> <dt>

<span data-ttu-id="79dd7-119">*集* \[ 區擴展\]</span><span class="sxs-lookup"><span data-stu-id="79dd7-119">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79dd7-120">成功時，傳回所產生之 [**CIM \_ ResourcePool**](cim-resourcepool.md)的參考。</span><span class="sxs-lookup"><span data-stu-id="79dd7-120">On success, returns a reference to the resulting [**CIM\_ResourcePool**](cim-resourcepool.md).</span></span> <span data-ttu-id="79dd7-121">傳回工作時，這可能是 **Null**，在這種情況下，用戶端必須在作業完成之後，使用該作業來尋找產生的 ResourcePool。</span><span class="sxs-lookup"><span data-stu-id="79dd7-121">When a Job is returned, this may be **NULL**, in which case, the client must use the Job to find the resulting ResourcePool once the Job completes.</span></span>

</dd> <dt>

<span data-ttu-id="79dd7-122">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="79dd7-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79dd7-123">如果作業已完成) ，則參考代表作業 (的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 可能是 null。</span><span class="sxs-lookup"><span data-stu-id="79dd7-123">Reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) that represents the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79dd7-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="79dd7-124">Return value</span></span>

<span data-ttu-id="79dd7-125">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="79dd7-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="79dd7-126">**作業已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="79dd7-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-127">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="79dd7-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-128">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="79dd7-128">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-129">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="79dd7-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-130">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="79dd7-130">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-131">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="79dd7-131">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-132">**使用** (6) </span><span class="sxs-lookup"><span data-stu-id="79dd7-132">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-133">集區的 ResourceType (7) **不正確**</span><span class="sxs-lookup"><span data-stu-id="79dd7-133">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-134">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="79dd7-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-135">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="79dd7-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-136"> (4097) **不支援的大小**</span><span class="sxs-lookup"><span data-stu-id="79dd7-136">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-137">**方法保留** (4098. 32767) </span><span class="sxs-lookup"><span data-stu-id="79dd7-137">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="79dd7-138">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="79dd7-138">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="79dd7-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="79dd7-139">Requirements</span></span>



| <span data-ttu-id="79dd7-140">需求</span><span class="sxs-lookup"><span data-stu-id="79dd7-140">Requirement</span></span> | <span data-ttu-id="79dd7-141">值</span><span class="sxs-lookup"><span data-stu-id="79dd7-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79dd7-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79dd7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="79dd7-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="79dd7-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="79dd7-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79dd7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="79dd7-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="79dd7-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="79dd7-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="79dd7-146">Namespace</span></span><br/>                | <span data-ttu-id="79dd7-147">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="79dd7-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79dd7-148">MOF</span><span class="sxs-lookup"><span data-stu-id="79dd7-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79dd7-149"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="79dd7-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79dd7-150">DLL</span><span class="sxs-lookup"><span data-stu-id="79dd7-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79dd7-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79dd7-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79dd7-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79dd7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79dd7-153">**CIM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="79dd7-153">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




