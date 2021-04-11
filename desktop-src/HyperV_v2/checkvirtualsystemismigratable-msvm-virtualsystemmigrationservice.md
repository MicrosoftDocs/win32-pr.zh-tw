---
description: 判斷指定的虛擬系統是否可以遷移。
ms.assetid: 1bf1b385-162e-41c9-a408-f7ee755a9646
title: Msvm_VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratable 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratable
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1aed843f3f0f4c6c30eb6125cdd5859cdba902d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847771"
---
# <a name="checkvirtualsystemismigratable-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="c377d-103">Msvm VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratable 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c377d-103">CheckVirtualSystemIsMigratable method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="c377d-104">判斷指定的虛擬系統是否可以遷移。</span><span class="sxs-lookup"><span data-stu-id="c377d-104">Determines whether the specified virtual system can be migrated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c377d-105">語法</span><span class="sxs-lookup"><span data-stu-id="c377d-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratable(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c377d-106">參數</span><span class="sxs-lookup"><span data-stu-id="c377d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c377d-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="c377d-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c377d-108">[**CIM \_**](cim-computersystem.md)系統類型實例的參考，代表要測試其遷移能力的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c377d-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="c377d-109">*DestinationHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c377d-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c377d-110">要遷移的主機系統名稱。</span><span class="sxs-lookup"><span data-stu-id="c377d-110">The name of the host system for the migration.</span></span> <span data-ttu-id="c377d-111">這個名稱的格式是由與這個類別相關聯之 [**Msvm \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md)類別的 **DestinationHostFormatsSupported** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="c377d-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="c377d-112">*MigrationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c377d-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c377d-113">[**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)類別的內嵌實例，代表遷移作業的設定。</span><span class="sxs-lookup"><span data-stu-id="c377d-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="c377d-114">*NewSystemSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c377d-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c377d-115">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。</span><span class="sxs-lookup"><span data-stu-id="c377d-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="c377d-116">*NewResourceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c377d-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c377d-117">字串陣列，其中包含 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例，表示在遷移之後，適用于虛擬系統虛擬資源的新屬性。</span><span class="sxs-lookup"><span data-stu-id="c377d-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="c377d-118">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c377d-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c377d-119">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="c377d-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c377d-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c377d-120">Return value</span></span>

<span data-ttu-id="c377d-121">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c377d-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c377d-122">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="c377d-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-123">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="c377d-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-124">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="c377d-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-125">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="c377d-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-126">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="c377d-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-127">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="c377d-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-128">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="c377d-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-129">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="c377d-129">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-130">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="c377d-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-131">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="c377d-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-132">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="c377d-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c377d-133">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="c377d-133">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c377d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="c377d-134">Requirements</span></span>



| <span data-ttu-id="c377d-135">需求</span><span class="sxs-lookup"><span data-stu-id="c377d-135">Requirement</span></span> | <span data-ttu-id="c377d-136">值</span><span class="sxs-lookup"><span data-stu-id="c377d-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c377d-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c377d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c377d-138">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c377d-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c377d-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c377d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c377d-140">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c377d-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c377d-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="c377d-141">Namespace</span></span><br/>                | <span data-ttu-id="c377d-142">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="c377d-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c377d-143">MOF</span><span class="sxs-lookup"><span data-stu-id="c377d-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c377d-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c377d-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c377d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c377d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c377d-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c377d-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c377d-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c377d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c377d-148">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="c377d-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

