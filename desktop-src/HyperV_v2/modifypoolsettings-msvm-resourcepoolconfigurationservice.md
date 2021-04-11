---
description: 變更非配置相關的子集區設定。
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Msvm_ResourcePoolConfigurationService 類別的 ModifyPoolSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: edc5f48dabfb84554954cc80d9c4e8a20678d34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193929"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="d2855-103">Msvm ResourcePoolConfigurationService 類別的 ModifyPoolSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d2855-103">ModifyPoolSettings method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="d2855-104">變更非配置相關的子集區設定。</span><span class="sxs-lookup"><span data-stu-id="d2855-104">Changes the settings of a child pool that are not allocation related.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2855-105">語法</span><span class="sxs-lookup"><span data-stu-id="d2855-105">Syntax</span></span>


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d2855-106">參數</span><span class="sxs-lookup"><span data-stu-id="d2855-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2855-107">*ChildPool* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2855-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2855-108">[**CIM \_ ResourcePool**](cim-resourcepool.md)類別實例的參考，代表要修改的子集區。</span><span class="sxs-lookup"><span data-stu-id="d2855-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="d2855-109">*PoolSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2855-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2855-110">[**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)類別的內嵌實例，可用來指定集區的新設定。</span><span class="sxs-lookup"><span data-stu-id="d2855-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the new settings for the pool.</span></span>

</dd> <dt>

<span data-ttu-id="d2855-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d2855-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2855-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d2855-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2855-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2855-113">Return value</span></span>

<span data-ttu-id="d2855-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d2855-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d2855-115">**作業已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="d2855-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-116">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="d2855-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="d2855-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-118">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="d2855-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="d2855-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="d2855-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="d2855-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-122">**未知** 的 (32771) </span><span class="sxs-lookup"><span data-stu-id="d2855-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="d2855-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="d2855-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-125">**使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="d2855-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-126">**不正確狀態** (32775) </span><span class="sxs-lookup"><span data-stu-id="d2855-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-127">集區 (32776) **不正確的資源類型**</span><span class="sxs-lookup"><span data-stu-id="d2855-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-128">**無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="d2855-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="d2855-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-130">**廠商保留** (32779) </span><span class="sxs-lookup"><span data-stu-id="d2855-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-131">**資源不足** (32780) </span><span class="sxs-lookup"><span data-stu-id="d2855-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-132">**找不到物件** (32781 32787) </span><span class="sxs-lookup"><span data-stu-id="d2855-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-133">**物件存在** (32788) </span><span class="sxs-lookup"><span data-stu-id="d2855-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="d2855-134">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="d2855-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d2855-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2855-135">Requirements</span></span>



| <span data-ttu-id="d2855-136">需求</span><span class="sxs-lookup"><span data-stu-id="d2855-136">Requirement</span></span> | <span data-ttu-id="d2855-137">值</span><span class="sxs-lookup"><span data-stu-id="d2855-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2855-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d2855-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d2855-139">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2855-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d2855-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d2855-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d2855-141">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d2855-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2855-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="d2855-142">Namespace</span></span><br/>                | <span data-ttu-id="d2855-143">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d2855-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d2855-144">MOF</span><span class="sxs-lookup"><span data-stu-id="d2855-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2855-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d2855-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2855-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d2855-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2855-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2855-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d2855-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2855-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2855-149">**Msvm \_ ResourcePoolConfigurationService**</span><span class="sxs-lookup"><span data-stu-id="d2855-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

