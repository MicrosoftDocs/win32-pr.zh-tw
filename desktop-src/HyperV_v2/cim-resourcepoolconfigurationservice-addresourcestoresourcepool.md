---
description: 啟動將資源新增至資源集區的作業。
ms.assetid: b163619a-19bd-43d7-ba35-ec4bd8192100
title: CIM_ResourcePoolConfigurationService 類別的 AddResourcesToResourcePool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.AddResourcesToResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d3aed59267bd064e95b62431064fbd54bb9168aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967156"
---
# <a name="addresourcestoresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="71202-103">CIM ResourcePoolConfigurationService 類別的 AddResourcesToResourcePool 方法 \_</span><span class="sxs-lookup"><span data-stu-id="71202-103">AddResourcesToResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="71202-104">啟動將資源新增至資源集區的作業。</span><span class="sxs-lookup"><span data-stu-id="71202-104">Starts a job to add resources to a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="71202-105">語法</span><span class="sxs-lookup"><span data-stu-id="71202-105">Syntax</span></span>


```mof
uint32 AddResourcesToResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="71202-106">參數</span><span class="sxs-lookup"><span data-stu-id="71202-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71202-107">*HostResources* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71202-107">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71202-108">要加入集區的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 實例陣列。</span><span class="sxs-lookup"><span data-stu-id="71202-108">Array of [**CIM\_LogicalDevice**](cim-logicaldevice.md) instances to add to the pool.</span></span>

</dd> <dt>

<span data-ttu-id="71202-109">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="71202-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71202-110">[**CIM \_ ResourcePool**](cim-resourcepool.md) ，代表要新增資源的集區。</span><span class="sxs-lookup"><span data-stu-id="71202-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that represents the pool to add the resources to.</span></span>

</dd> <dt>

<span data-ttu-id="71202-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="71202-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71202-112">如果作業已完成) ，則參考作業 (的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 可能會是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="71202-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71202-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="71202-113">Return value</span></span>

<span data-ttu-id="71202-114">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="71202-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="71202-115">**作業已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="71202-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="71202-116">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="71202-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="71202-117">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="71202-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="71202-118">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="71202-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="71202-119">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="71202-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="71202-120">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="71202-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="71202-121">**使用** (6) </span><span class="sxs-lookup"><span data-stu-id="71202-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="71202-122">集區的 ResourceType (7) **不正確**</span><span class="sxs-lookup"><span data-stu-id="71202-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="71202-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="71202-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="71202-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="71202-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="71202-125"> (4097) **不支援的大小**</span><span class="sxs-lookup"><span data-stu-id="71202-125">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="71202-126">**方法保留** (4098. 32767) </span><span class="sxs-lookup"><span data-stu-id="71202-126">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="71202-127">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="71202-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="71202-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="71202-128">Requirements</span></span>



| <span data-ttu-id="71202-129">需求</span><span class="sxs-lookup"><span data-stu-id="71202-129">Requirement</span></span> | <span data-ttu-id="71202-130">值</span><span class="sxs-lookup"><span data-stu-id="71202-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71202-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71202-131">Minimum supported client</span></span><br/> | <span data-ttu-id="71202-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="71202-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="71202-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71202-133">Minimum supported server</span></span><br/> | <span data-ttu-id="71202-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="71202-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="71202-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="71202-135">Namespace</span></span><br/>                | <span data-ttu-id="71202-136">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="71202-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="71202-137">MOF</span><span class="sxs-lookup"><span data-stu-id="71202-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71202-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="71202-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="71202-139">DLL</span><span class="sxs-lookup"><span data-stu-id="71202-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71202-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71202-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="71202-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71202-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71202-142">**CIM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="71202-142">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




