---
description: 刪除資源集區。
ms.assetid: bc3111a4-9687-49ec-890e-190358230c53
title: Msvm_ResourcePoolConfigurationService 類別的 DeletePool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.DeletePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 84273daa0aa30dca8722d90d4fcec22b88325bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987702"
---
# <a name="deletepool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="0bcd8-103">Msvm ResourcePoolConfigurationService 類別的 DeletePool 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0bcd8-103">DeletePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="0bcd8-104">刪除資源集區。</span><span class="sxs-lookup"><span data-stu-id="0bcd8-104">Deletes a resource pool.</span></span> <span data-ttu-id="0bcd8-105">若要成功刪除資源集區，則不會有任何配置無法完成，或刪除將會失敗，並出現 32774 (使用中) 。</span><span class="sxs-lookup"><span data-stu-id="0bcd8-105">To successfully delete a resource pool, no allocations can be outstanding or the delete will fail with 32774 (In Use).</span></span> <span data-ttu-id="0bcd8-106">如果資源集區是根資源集區，則會傳回任何主機資源給基礎系統。</span><span class="sxs-lookup"><span data-stu-id="0bcd8-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcd8-107">語法</span><span class="sxs-lookup"><span data-stu-id="0bcd8-107">Syntax</span></span>


```mof
uint32 DeletePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0bcd8-108">參數</span><span class="sxs-lookup"><span data-stu-id="0bcd8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bcd8-109">*集* \[ 區在\]</span><span class="sxs-lookup"><span data-stu-id="0bcd8-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bcd8-110">[**CIM \_ ResourcePool**](cim-resourcepool.md)類別實例的參考，代表要刪除的集區。</span><span class="sxs-lookup"><span data-stu-id="0bcd8-110">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="0bcd8-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0bcd8-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bcd8-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="0bcd8-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bcd8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0bcd8-113">Return value</span></span>

<span data-ttu-id="0bcd8-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0bcd8-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0bcd8-115">**作業已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-116">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-118">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-122">**未知** 的 (32771) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-125">**使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-126">**不正確狀態** (32775) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-127">集區 (32776) **不正確的資源類型**</span><span class="sxs-lookup"><span data-stu-id="0bcd8-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-128">**無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-130">**廠商保留** (32779) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-131">**資源不足** (32780) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-132">**找不到物件** (32781 32787) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-133">**物件存在** (32788) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="0bcd8-134">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="0bcd8-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0bcd8-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bcd8-135">Requirements</span></span>



| <span data-ttu-id="0bcd8-136">需求</span><span class="sxs-lookup"><span data-stu-id="0bcd8-136">Requirement</span></span> | <span data-ttu-id="0bcd8-137">值</span><span class="sxs-lookup"><span data-stu-id="0bcd8-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcd8-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0bcd8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0bcd8-139">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bcd8-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0bcd8-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0bcd8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0bcd8-141">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0bcd8-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0bcd8-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="0bcd8-142">Namespace</span></span><br/>                | <span data-ttu-id="0bcd8-143">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="0bcd8-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0bcd8-144">MOF</span><span class="sxs-lookup"><span data-stu-id="0bcd8-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bcd8-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0bcd8-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bcd8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0bcd8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bcd8-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0bcd8-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0bcd8-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bcd8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcd8-149">**Msvm \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="0bcd8-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

