---
description: 將虛擬系統或虛擬系統的儲存體遷移至主機名稱所指定的目的地主機。
ms.assetid: 796b043c-5ac9-4c69-9838-0f415be5a63e
title: Msvm_VirtualSystemMigrationService 類別的 MigrateVirtualSystemToHost 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f46d32f9e1af68cd4256c4eb5adff5c32b8766e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848782"
---
# <a name="migratevirtualsystemtohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="f15d4-103">Msvm VirtualSystemMigrationService 類別的 MigrateVirtualSystemToHost 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f15d4-103">MigrateVirtualSystemToHost method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="f15d4-104">將虛擬系統或虛擬系統的儲存體遷移至主機名稱所指定的目的地主機。</span><span class="sxs-lookup"><span data-stu-id="f15d4-104">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span>

## <a name="syntax"></a><span data-ttu-id="f15d4-105">語法</span><span class="sxs-lookup"><span data-stu-id="f15d4-105">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f15d4-106">參數</span><span class="sxs-lookup"><span data-stu-id="f15d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f15d4-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="f15d4-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f15d4-108">[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表要遷移的虛擬電腦系統。</span><span class="sxs-lookup"><span data-stu-id="f15d4-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f15d4-109">*DestinationHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f15d4-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f15d4-110">要遷移的主機系統名稱。</span><span class="sxs-lookup"><span data-stu-id="f15d4-110">The name of the host system for the migration.</span></span> <span data-ttu-id="f15d4-111">這個名稱的格式是由與這個類別相關聯之 [**Msvm \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md)類別的 **DestinationHostFormatsSupported** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="f15d4-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="f15d4-112">*MigrationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f15d4-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f15d4-113">[**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)類別的內嵌實例，代表遷移作業的設定。</span><span class="sxs-lookup"><span data-stu-id="f15d4-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="f15d4-114">*NewSystemSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f15d4-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f15d4-115">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。</span><span class="sxs-lookup"><span data-stu-id="f15d4-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f15d4-116">*NewResourceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f15d4-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f15d4-117">字串陣列，其中包含 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例，表示在遷移之後，適用于虛擬系統虛擬資源的新屬性。</span><span class="sxs-lookup"><span data-stu-id="f15d4-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f15d4-118">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f15d4-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f15d4-119">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="f15d4-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f15d4-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="f15d4-120">Return value</span></span>

<span data-ttu-id="f15d4-121">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f15d4-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f15d4-122">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="f15d4-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-123">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="f15d4-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-124">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="f15d4-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-125">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="f15d4-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-126">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="f15d4-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-127">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="f15d4-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-128">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="f15d4-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-129">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="f15d4-129">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-130">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="f15d4-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-131">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="f15d4-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-132">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="f15d4-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f15d4-133">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="f15d4-133">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f15d4-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="f15d4-134">Requirements</span></span>



| <span data-ttu-id="f15d4-135">需求</span><span class="sxs-lookup"><span data-stu-id="f15d4-135">Requirement</span></span> | <span data-ttu-id="f15d4-136">值</span><span class="sxs-lookup"><span data-stu-id="f15d4-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f15d4-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f15d4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f15d4-138">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f15d4-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f15d4-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f15d4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f15d4-140">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f15d4-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f15d4-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="f15d4-141">Namespace</span></span><br/>                | <span data-ttu-id="f15d4-142">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f15d4-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f15d4-143">MOF</span><span class="sxs-lookup"><span data-stu-id="f15d4-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f15d4-144"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f15d4-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f15d4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f15d4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f15d4-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f15d4-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f15d4-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f15d4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f15d4-148">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="f15d4-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

