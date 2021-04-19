---
description: 將資源新增至虛擬系統設定。
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: CIM_VirtualSystemManagementService 類別的 AddResourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974396"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="36f37-103">CIM VirtualSystemManagementService 類別的 AddResourceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="36f37-103">AddResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="36f37-104">將資源新增至虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="36f37-104">Adds resources to a virtual system configuration.</span></span>

<span data-ttu-id="36f37-105">當套用至「狀態」虛擬系統設定時，將會在作用中的虛擬系統中加入副作用資源。</span><span class="sxs-lookup"><span data-stu-id="36f37-105">When applied to a "state" virtual system configuration, as a side effect resources are added to the active virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f37-106">語法</span><span class="sxs-lookup"><span data-stu-id="36f37-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="36f37-107">參數</span><span class="sxs-lookup"><span data-stu-id="36f37-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36f37-108">*AffectedConfiguration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36f37-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36f37-109">受影響之虛擬系統組態的 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="36f37-109">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="36f37-110">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="36f37-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36f37-111">字串陣列，其中每個字串都包含一個類別 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 的內嵌實例，以描述要新增至虛擬系統的虛擬資源的虛擬層面。</span><span class="sxs-lookup"><span data-stu-id="36f37-111">Array of strings each containing one embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be added to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="36f37-112">*ResultingResourceSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="36f37-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36f37-113">類別 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 實例的參考陣列，代表已新增之虛擬資源的虛擬層面。</span><span class="sxs-lookup"><span data-stu-id="36f37-113">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="36f37-114">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="36f37-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36f37-115">如果作業的執行時間很長，則可以選擇性地傳回作業。</span><span class="sxs-lookup"><span data-stu-id="36f37-115">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="36f37-116">在此情況下，可透過代表受影響之虛擬系統設定的 [**cim \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)類別實例，透過關聯 **cim \_ ConreteComponent** ，取得代表新增資源設定的類別 [**cim \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)實例。</span><span class="sxs-lookup"><span data-stu-id="36f37-116">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the added resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36f37-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="36f37-117">Return value</span></span>

<span data-ttu-id="36f37-118">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="36f37-118">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="36f37-119">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="36f37-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="36f37-120">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="36f37-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="36f37-121">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="36f37-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="36f37-122">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="36f37-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="36f37-123">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="36f37-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="36f37-124">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="36f37-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="36f37-125">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="36f37-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="36f37-126">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="36f37-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="36f37-127">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="36f37-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="36f37-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="36f37-128">Requirements</span></span>



| <span data-ttu-id="36f37-129">需求</span><span class="sxs-lookup"><span data-stu-id="36f37-129">Requirement</span></span> | <span data-ttu-id="36f37-130">值</span><span class="sxs-lookup"><span data-stu-id="36f37-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36f37-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36f37-131">Minimum supported client</span></span><br/> | <span data-ttu-id="36f37-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="36f37-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="36f37-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36f37-133">Minimum supported server</span></span><br/> | <span data-ttu-id="36f37-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="36f37-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="36f37-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="36f37-135">Namespace</span></span><br/>                | <span data-ttu-id="36f37-136">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="36f37-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="36f37-137">MOF</span><span class="sxs-lookup"><span data-stu-id="36f37-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36f37-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="36f37-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="36f37-139">DLL</span><span class="sxs-lookup"><span data-stu-id="36f37-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36f37-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="36f37-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="36f37-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="36f37-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f37-142">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="36f37-142">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




