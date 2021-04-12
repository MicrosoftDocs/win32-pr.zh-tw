---
description: 移動、遷移或重新置放虛擬系統至目標系統。
ms.assetid: 3a0be791-4514-4ce2-b4e8-3735bd6ea1d7
title: Msvm_VirtualSystemMigrationService 類別的 MigrateVirtualSystemToSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a346596b094b60456af8e2b63865bec1171d99ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318964"
---
# <a name="migratevirtualsystemtosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="845a3-103">Msvm VirtualSystemMigrationService 類別的 MigrateVirtualSystemToSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="845a3-103">MigrateVirtualSystemToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="845a3-104">移動、遷移或重新置放虛擬系統至目標系統。</span><span class="sxs-lookup"><span data-stu-id="845a3-104">Moves, migrates, or relocates a virtual system to a target system.</span></span>

## <a name="syntax"></a><span data-ttu-id="845a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="845a3-105">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="845a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="845a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="845a3-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="845a3-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845a3-108">[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表要遷移的虛擬電腦系統。</span><span class="sxs-lookup"><span data-stu-id="845a3-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="845a3-109">*DestinationSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="845a3-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845a3-110">[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表要遷移到的系統。</span><span class="sxs-lookup"><span data-stu-id="845a3-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system to be migrated to.</span></span>

</dd> <dt>

<span data-ttu-id="845a3-111">*MigrationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="845a3-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845a3-112">[**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)類別的內嵌實例，代表遷移作業的設定。</span><span class="sxs-lookup"><span data-stu-id="845a3-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="845a3-113">*NewSystemSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="845a3-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845a3-114">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。</span><span class="sxs-lookup"><span data-stu-id="845a3-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="845a3-115">*NewResourceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="845a3-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845a3-116">字串陣列，其中包含 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例，表示在遷移之後，適用于虛擬系統虛擬資源的新屬性。</span><span class="sxs-lookup"><span data-stu-id="845a3-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="845a3-117">*NewComputerSystem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="845a3-117">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="845a3-118">[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表新的已遷移系統。</span><span class="sxs-lookup"><span data-stu-id="845a3-118">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the new migrated system.</span></span>

</dd> <dt>

<span data-ttu-id="845a3-119">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="845a3-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="845a3-120">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="845a3-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="845a3-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="845a3-121">Return value</span></span>

<span data-ttu-id="845a3-122">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="845a3-122">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="845a3-123">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="845a3-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="845a3-124">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="845a3-124">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="845a3-125">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="845a3-125">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="845a3-126">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="845a3-126">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="845a3-127">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="845a3-127">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="845a3-128">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="845a3-128">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="845a3-129"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="845a3-129">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="845a3-130">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="845a3-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="845a3-131">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="845a3-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="845a3-132">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="845a3-132">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="845a3-133">**廠商特定** (32768. 65535 ) </span><span class="sxs-lookup"><span data-stu-id="845a3-133">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="845a3-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="845a3-134">Requirements</span></span>



| <span data-ttu-id="845a3-135">需求</span><span class="sxs-lookup"><span data-stu-id="845a3-135">Requirement</span></span> | <span data-ttu-id="845a3-136">值</span><span class="sxs-lookup"><span data-stu-id="845a3-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="845a3-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="845a3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="845a3-138">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="845a3-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="845a3-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="845a3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="845a3-140">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="845a3-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="845a3-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="845a3-141">Namespace</span></span><br/>                | <span data-ttu-id="845a3-142">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="845a3-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="845a3-143">MOF</span><span class="sxs-lookup"><span data-stu-id="845a3-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="845a3-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="845a3-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="845a3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="845a3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="845a3-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="845a3-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="845a3-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="845a3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="845a3-148">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="845a3-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

