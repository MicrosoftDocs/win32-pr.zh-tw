---
description: 啟動工作以刪除資源集區。
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: CIM_ResourcePoolConfigurationService 類別的 DeleteResourcePool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cab27df07a6a3a9679cb5e6595b6ba558d8b05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972881"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="2c29e-103">CIM ResourcePoolConfigurationService 類別的 DeleteResourcePool 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2c29e-103">DeleteResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="2c29e-104">啟動工作以刪除資源集區。</span><span class="sxs-lookup"><span data-stu-id="2c29e-104">Start a job to delete a resource pool.</span></span> <span data-ttu-id="2c29e-105">沒有任何配置可能未完成，或刪除會失敗並出現「使用中」。</span><span class="sxs-lookup"><span data-stu-id="2c29e-105">No allocations may be outstanding or the delete will fail with "In Use."</span></span> <span data-ttu-id="2c29e-106">如果資源集區是根資源集區，則會傳回任何主機資源給基礎系統。</span><span class="sxs-lookup"><span data-stu-id="2c29e-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c29e-107">語法</span><span class="sxs-lookup"><span data-stu-id="2c29e-107">Syntax</span></span>


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2c29e-108">參數</span><span class="sxs-lookup"><span data-stu-id="2c29e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c29e-109">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="2c29e-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c29e-110">參考要刪除之集區的 [**CIM \_ ResourcePool**](cim-resourcepool.md) 。</span><span class="sxs-lookup"><span data-stu-id="2c29e-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references to the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="2c29e-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2c29e-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c29e-112">如果作業已完成) ，則參考作業 (的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 可能會是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="2c29e-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c29e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c29e-113">Return value</span></span>

<span data-ttu-id="2c29e-114">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2c29e-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2c29e-115">**作業已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="2c29e-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-116">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="2c29e-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-117">**未知** 的 (2) </span><span class="sxs-lookup"><span data-stu-id="2c29e-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-118">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="2c29e-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-119">**失敗** (4) </span><span class="sxs-lookup"><span data-stu-id="2c29e-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-120">**不正確參數** (5) </span><span class="sxs-lookup"><span data-stu-id="2c29e-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-121">**使用** (6) </span><span class="sxs-lookup"><span data-stu-id="2c29e-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-122">集區的 ResourceType (7) **不正確**</span><span class="sxs-lookup"><span data-stu-id="2c29e-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="2c29e-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="2c29e-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="2c29e-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2c29e-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="2c29e-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2c29e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c29e-127">Requirements</span></span>



| <span data-ttu-id="2c29e-128">需求</span><span class="sxs-lookup"><span data-stu-id="2c29e-128">Requirement</span></span> | <span data-ttu-id="2c29e-129">值</span><span class="sxs-lookup"><span data-stu-id="2c29e-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c29e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c29e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c29e-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2c29e-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2c29e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c29e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c29e-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2c29e-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2c29e-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="2c29e-134">Namespace</span></span><br/>                | <span data-ttu-id="2c29e-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2c29e-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2c29e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2c29e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c29e-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2c29e-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c29e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2c29e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c29e-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2c29e-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2c29e-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c29e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c29e-141">**CIM \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="2c29e-141">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




