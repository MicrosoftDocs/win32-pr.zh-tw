---
description: 建立子資源集區。
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Msvm_ResourcePoolConfigurationService 類別的 >batchclient.pooloperations.createpool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978023"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="fbb9e-103">Msvm ResourcePoolConfigurationService 類別的 >batchclient.pooloperations.createpool 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fbb9e-103">CreatePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="fbb9e-104">建立子資源集區。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-104">Creates a child resource pool.</span></span> <span data-ttu-id="fbb9e-105">資源集區的範圍將設定為與此服務相同的系統。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-105">The resource pool will be scoped to the same System as this Service.</span></span> <span data-ttu-id="fbb9e-106">產生的集區將會是子集區。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-106">The resulting pool will be a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbb9e-107">語法</span><span class="sxs-lookup"><span data-stu-id="fbb9e-107">Syntax</span></span>


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="fbb9e-108">參數</span><span class="sxs-lookup"><span data-stu-id="fbb9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb9e-109">*PoolSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbb9e-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb9e-110">[**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)類別的內嵌實例，可用來指定非配置相關的集區設定。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the pool settings that are not allocation related.</span></span>

</dd> <dt>

<span data-ttu-id="fbb9e-111">*ParentPools* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbb9e-111">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb9e-112">[**Msvm \_ ResourcePool**](msvm-resourcepool.md)參考的陣列，代表要在其中建立新集區的集區或集區。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-112">An array of [**Msvm\_ResourcePool**](msvm-resourcepool.md) references that represent the pool or pools from which to create the new pool.</span></span>

</dd> <dt>

<span data-ttu-id="fbb9e-113">*AllocationSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fbb9e-113">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb9e-114">一或多個 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例陣列，用來指定集區配置的相關設定。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-114">An array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span> <span data-ttu-id="fbb9e-115">這個陣列必須針對 *ParentPools* 陣列中的每個元素，或只包含一個元素。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-115">This array must contain either one element for each element in the *ParentPools* array, or exactly one element.</span></span> <span data-ttu-id="fbb9e-116">如果這個陣列包含一個元素，而 *ParentPools* 包含一個以上的元素，則 *AlllocationSettings* 會指定可由任何父集區滿足的共用容量配置。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-116">If this array contains one element and *ParentPools* contains more than one element, *AlllocationSettings* specifies a shared capacity allocation that can be satisfied by any of the parent pools.</span></span>

<span data-ttu-id="fbb9e-117">這是用來將可從子系配置給集區的資源，限制為低於其父系所提供之匯總容量的限制。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-117">This is used to restrict the resources that can be allocated from the child to the pool to a lower limit than the aggregate capacity provided by its parents.</span></span> <span data-ttu-id="fbb9e-118">並非所有資源類型都支援此選項。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-118">This option is not supported by all resource types.</span></span> <span data-ttu-id="fbb9e-119">如果資源類型不支援共用容量配置，這個方法將會傳回 32770 (不支援) 。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-119">If a resource type does not support shared capacity allocation, this method will return 32770 (Not Supported).</span></span>

</dd> <dt>

<span data-ttu-id="fbb9e-120">*集* \[ 區擴展\]</span><span class="sxs-lookup"><span data-stu-id="fbb9e-120">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb9e-121">所產生集區的參考。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-121">A reference to the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="fbb9e-122">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fbb9e-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbb9e-123">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-123">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbb9e-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbb9e-124">Return value</span></span>

<span data-ttu-id="fbb9e-125">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="fbb9e-125">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="fbb9e-126">**作業已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-127">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-128">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-129">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-130">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-131">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-132">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-133">**未知** 的 (32771) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-133">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-134">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-135">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-135">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-136">**使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-136">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-137">**不正確狀態** (32775) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-137">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-138">集區 (32776) **不正確的資源類型**</span><span class="sxs-lookup"><span data-stu-id="fbb9e-138">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-139">**無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-139">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-140">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-140">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-141">**廠商保留** (32779) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-141">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-142">**資源不足** (32780) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-142">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-143">**找不到物件** (32781 32787) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-143">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-144">**物件存在** (32788) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-144">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="fbb9e-145">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="fbb9e-145">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="fbb9e-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbb9e-146">Requirements</span></span>



| <span data-ttu-id="fbb9e-147">需求</span><span class="sxs-lookup"><span data-stu-id="fbb9e-147">Requirement</span></span> | <span data-ttu-id="fbb9e-148">值</span><span class="sxs-lookup"><span data-stu-id="fbb9e-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbb9e-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbb9e-149">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb9e-150">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbb9e-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fbb9e-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbb9e-151">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb9e-152">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbb9e-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbb9e-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="fbb9e-153">Namespace</span></span><br/>                | <span data-ttu-id="fbb9e-154">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="fbb9e-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fbb9e-155">MOF</span><span class="sxs-lookup"><span data-stu-id="fbb9e-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbb9e-156"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fbb9e-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbb9e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="fbb9e-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbb9e-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbb9e-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fbb9e-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbb9e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb9e-160">**Msvm \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="fbb9e-160">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

