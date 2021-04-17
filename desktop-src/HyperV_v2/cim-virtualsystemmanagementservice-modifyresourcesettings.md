---
description: 修改虛擬資源設定。
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: CIM_VirtualSystemManagementService 類別的 ModifyResourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e27729429d02c2412e05344779cc40461dbd9dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469268"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="8391b-103">CIM VirtualSystemManagementService 類別的 ModifyResourceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8391b-103">ModifyResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="8391b-104">修改虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="8391b-104">Modifies virtual resource settings.</span></span>

<span data-ttu-id="8391b-105">套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用資源。</span><span class="sxs-lookup"><span data-stu-id="8391b-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="8391b-106">語法</span><span class="sxs-lookup"><span data-stu-id="8391b-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8391b-107">參數</span><span class="sxs-lookup"><span data-stu-id="8391b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8391b-108">*ResourceSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8391b-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8391b-109">字串陣列，其中每個字串都包含類別 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 的內嵌實例，以描述對現有虛擬資源的虛擬層面所做的修改。</span><span class="sxs-lookup"><span data-stu-id="8391b-109">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes modifications to the virtual aspects of an existing virtual resource.</span></span> <span data-ttu-id="8391b-110">所有實例都必須具有有效的 **InstanceID** ，才能識別要修改的虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="8391b-110">All instances must have a valid **InstanceID** in order to identify the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="8391b-111">*ResultingResourceSettings* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8391b-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8391b-112">類別 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 實例的參考陣列，代表已修改之虛擬資源的虛擬層面。</span><span class="sxs-lookup"><span data-stu-id="8391b-112">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="8391b-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8391b-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8391b-114">如果作業的執行時間很長，則選擇性地傳回作業。</span><span class="sxs-lookup"><span data-stu-id="8391b-114">If the operation is long running, then optionally a job be returned.</span></span> <span data-ttu-id="8391b-115">在此情況下，可透過代表受影響之虛擬系統設定的 [**cim \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)類別實例，透過關聯 **cim \_ ConreteComponent** ，取得代表已修改之資源設定的類別 [**cim \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)實例。</span><span class="sxs-lookup"><span data-stu-id="8391b-115">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the modified resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8391b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8391b-116">Return value</span></span>

<span data-ttu-id="8391b-117">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8391b-117">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="8391b-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="8391b-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8391b-119">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="8391b-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8391b-120">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="8391b-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8391b-121">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="8391b-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8391b-122">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="8391b-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8391b-123">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="8391b-123">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="8391b-124"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="8391b-124">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="8391b-125">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="8391b-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="8391b-126">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="8391b-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8391b-127">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="8391b-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="8391b-128">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="8391b-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8391b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="8391b-129">Requirements</span></span>



| <span data-ttu-id="8391b-130">需求</span><span class="sxs-lookup"><span data-stu-id="8391b-130">Requirement</span></span> | <span data-ttu-id="8391b-131">值</span><span class="sxs-lookup"><span data-stu-id="8391b-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8391b-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8391b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8391b-133">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8391b-133">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8391b-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8391b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8391b-135">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8391b-135">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8391b-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="8391b-136">Namespace</span></span><br/>                | <span data-ttu-id="8391b-137">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="8391b-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8391b-138">MOF</span><span class="sxs-lookup"><span data-stu-id="8391b-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8391b-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8391b-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8391b-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8391b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8391b-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8391b-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8391b-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8391b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8391b-143">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="8391b-143">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




