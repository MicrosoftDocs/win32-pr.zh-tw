---
description: 使用指定的配置設定啟動作業，以從父集區建立子集區。
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: CIM_ResourcePoolConfigurationService 類別的 CreateChildResourcePool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998073"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="8fbad-103">CIM ResourcePoolConfigurationService 類別的 CreateChildResourcePool 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8fbad-103">CreateChildResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="8fbad-104">使用指定的配置設定啟動作業，以從父集區建立子集區。</span><span class="sxs-lookup"><span data-stu-id="8fbad-104">Start a job to create a sub-pool from a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fbad-105">語法</span><span class="sxs-lookup"><span data-stu-id="8fbad-105">Syntax</span></span>


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8fbad-106">參數</span><span class="sxs-lookup"><span data-stu-id="8fbad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fbad-107">*ElementName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fbad-107">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbad-108">要建立之集區的終端使用者相關名稱。</span><span class="sxs-lookup"><span data-stu-id="8fbad-108">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="8fbad-109">如果是 **Null**，則可以使用系統提供的預設名稱。</span><span class="sxs-lookup"><span data-stu-id="8fbad-109">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="8fbad-110">值會儲存在所建立專案的 **ElementName** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="8fbad-110">The value will be stored in the **ElementName** property for the created element.</span></span>

</dd> <dt>

<span data-ttu-id="8fbad-111">*設定* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fbad-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbad-112">字串，包含用來指定子集區設定的 [**CIM \_ SettingData**](cim-settingdata.md) 實例表示。</span><span class="sxs-lookup"><span data-stu-id="8fbad-112">String containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the child Pool.</span></span>

</dd> <dt>

<span data-ttu-id="8fbad-113">*ParentPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8fbad-113">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbad-114">用來建立新集區的 [**CIM \_ ResourcePool**](cim-resourcepool.md) 。</span><span class="sxs-lookup"><span data-stu-id="8fbad-114">A [**CIM\_ResourcePool**](cim-resourcepool.md) from which to create the new Pool.</span></span>

</dd> <dt>

<span data-ttu-id="8fbad-115">*集* \[ 區擴展\]</span><span class="sxs-lookup"><span data-stu-id="8fbad-115">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbad-116">參考所產生集區的 [**CIM \_ ResourcePool**](cim-resourcepool.md) 。</span><span class="sxs-lookup"><span data-stu-id="8fbad-116">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="8fbad-117">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8fbad-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fbad-118">如果作業已完成) ，則作業 (的參考可能會是 null。</span><span class="sxs-lookup"><span data-stu-id="8fbad-118">Reference to the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fbad-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="8fbad-119">Return value</span></span>

<span data-ttu-id="8fbad-120">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8fbad-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8fbad-121">**作業已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="8fbad-121">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-122">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="8fbad-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-123">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="8fbad-123">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-124">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="8fbad-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-125">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="8fbad-125">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-126">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="8fbad-126">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-127">**使用** (6) </span><span class="sxs-lookup"><span data-stu-id="8fbad-127">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-128">集區的 ResourceType (7) **不正確**</span><span class="sxs-lookup"><span data-stu-id="8fbad-128">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-129">**資源不足** (8) </span><span class="sxs-lookup"><span data-stu-id="8fbad-129">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-130">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8fbad-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-131">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="8fbad-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-132"> (4097) **不支援的大小**</span><span class="sxs-lookup"><span data-stu-id="8fbad-132">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-133">**方法保留** (4098. 32767) </span><span class="sxs-lookup"><span data-stu-id="8fbad-133">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8fbad-134">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="8fbad-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8fbad-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fbad-135">Requirements</span></span>



| <span data-ttu-id="8fbad-136">需求</span><span class="sxs-lookup"><span data-stu-id="8fbad-136">Requirement</span></span> | <span data-ttu-id="8fbad-137">值</span><span class="sxs-lookup"><span data-stu-id="8fbad-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbad-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fbad-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8fbad-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8fbad-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8fbad-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fbad-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8fbad-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8fbad-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8fbad-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="8fbad-142">Namespace</span></span><br/>                | <span data-ttu-id="8fbad-143">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="8fbad-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8fbad-144">MOF</span><span class="sxs-lookup"><span data-stu-id="8fbad-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fbad-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8fbad-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fbad-146">DLL</span><span class="sxs-lookup"><span data-stu-id="8fbad-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fbad-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8fbad-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8fbad-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fbad-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fbad-149">**CIM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="8fbad-149">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




