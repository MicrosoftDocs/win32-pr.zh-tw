---
description: 使用指定的配置設定開始作業，以變更父集區。
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: CIM_ResourcePoolConfigurationService 類別的 ChangeParentResourcePool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6ef852d6af8f0973b6b3f29fca5fcd90e9ce726a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973092"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="7cd09-103">CIM ResourcePoolConfigurationService 類別的 ChangeParentResourcePool 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7cd09-103">ChangeParentResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="7cd09-104">使用指定的配置設定開始作業，以變更父集區。</span><span class="sxs-lookup"><span data-stu-id="7cd09-104">Start a job to change a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd09-105">語法</span><span class="sxs-lookup"><span data-stu-id="7cd09-105">Syntax</span></span>


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7cd09-106">參數</span><span class="sxs-lookup"><span data-stu-id="7cd09-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd09-107">*ChildPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7cd09-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd09-108">參考子集區的 [**CIM \_ ResourcePool**](cim-resourcepool.md) 。</span><span class="sxs-lookup"><span data-stu-id="7cd09-108">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="7cd09-109">*ParentPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7cd09-109">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd09-110"> (s) 參考父集區的 [**CIM \_ ResourcePool**](cim-resourcepool.md) 陣列。</span><span class="sxs-lookup"><span data-stu-id="7cd09-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) array that references the parent pool(s).</span></span>

</dd> <dt>

<span data-ttu-id="7cd09-111">*設定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7cd09-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd09-112">選擇性字串，其中包含用來指定父集區設定的 [**CIM \_ SettingData**](cim-settingdata.md) 實例標記法。</span><span class="sxs-lookup"><span data-stu-id="7cd09-112">Optional string containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the parent pool.</span></span>

</dd> <dt>

<span data-ttu-id="7cd09-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7cd09-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd09-114">如果作業已完成) ，則參考作業 (的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 可能會是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="7cd09-114">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd09-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7cd09-115">Return value</span></span>

<span data-ttu-id="7cd09-116">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="7cd09-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="7cd09-117">**作業已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="7cd09-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-118">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="7cd09-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-119">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="7cd09-119">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-120">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="7cd09-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-121">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="7cd09-121">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-122">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="7cd09-122">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-123">**使用** (6) </span><span class="sxs-lookup"><span data-stu-id="7cd09-123">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-124">集區的 ResourceType (7) **不正確**</span><span class="sxs-lookup"><span data-stu-id="7cd09-124">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-125">**資源不足** (8) </span><span class="sxs-lookup"><span data-stu-id="7cd09-125">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-126">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="7cd09-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-127">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="7cd09-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-128"> (4097) **不支援的大小**</span><span class="sxs-lookup"><span data-stu-id="7cd09-128">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-129">**方法保留** (4098. 32767) </span><span class="sxs-lookup"><span data-stu-id="7cd09-129">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7cd09-130">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="7cd09-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7cd09-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cd09-131">Requirements</span></span>



| <span data-ttu-id="7cd09-132">需求</span><span class="sxs-lookup"><span data-stu-id="7cd09-132">Requirement</span></span> | <span data-ttu-id="7cd09-133">值</span><span class="sxs-lookup"><span data-stu-id="7cd09-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd09-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7cd09-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd09-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7cd09-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="7cd09-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7cd09-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd09-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7cd09-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="7cd09-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="7cd09-138">Namespace</span></span><br/>                | <span data-ttu-id="7cd09-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="7cd09-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7cd09-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7cd09-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cd09-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7cd09-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cd09-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd09-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cd09-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7cd09-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7cd09-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cd09-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd09-145">**CIM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="7cd09-145">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




