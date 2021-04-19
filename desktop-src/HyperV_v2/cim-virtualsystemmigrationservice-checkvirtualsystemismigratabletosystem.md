---
description: 深入瞭解： CIM_VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToSystem 方法
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: CIM_VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983595"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="49ea9-103">CIM VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="49ea9-103">CheckVirtualSystemIsMigratableToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="49ea9-104">執行前置檢查以判斷虛擬系統是否可能成功遷移至目標系統的方法。</span><span class="sxs-lookup"><span data-stu-id="49ea9-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target system.</span></span> <span data-ttu-id="49ea9-105">這種方法不保證後續的遷移一律會成功，因為動態資源可用性。</span><span class="sxs-lookup"><span data-stu-id="49ea9-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span> <span data-ttu-id="49ea9-106">傳回碼描述：</span><span class="sxs-lookup"><span data-stu-id="49ea9-106">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="49ea9-107">語法</span><span class="sxs-lookup"><span data-stu-id="49ea9-107">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="49ea9-108">參數</span><span class="sxs-lookup"><span data-stu-id="49ea9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ea9-109">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="49ea9-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea9-110">[**CIM \_系統實例，**](cim-computersystem.md) 參考要遷移的來源虛擬電腦系統。</span><span class="sxs-lookup"><span data-stu-id="49ea9-110">[**CIM\_ComputerSystem**](cim-computersystem.md) instance referencing the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="49ea9-111">*DestinationSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49ea9-111">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea9-112">[**CIM \_系統**](cim-system.md) 實例，參考要將虛擬系統移轉至其中的目的地系統。</span><span class="sxs-lookup"><span data-stu-id="49ea9-112">[**CIM\_System**](cim-system.md) instance referencing the destination system onto which to migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="49ea9-113">*MigrationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49ea9-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea9-114">字串，包含 [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) 類別的內嵌實例，代表適用于遷移作業的遷移設定。</span><span class="sxs-lookup"><span data-stu-id="49ea9-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="49ea9-115">*NewSystemSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49ea9-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea9-116">字串，包含 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。</span><span class="sxs-lookup"><span data-stu-id="49ea9-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="49ea9-117">*NewResourceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49ea9-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea9-118">字串陣列，其中每個字串都包含 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 類別的內嵌實例，代表在遷移之後，虛擬系統範圍中適用于虛擬資源的新屬性。</span><span class="sxs-lookup"><span data-stu-id="49ea9-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="49ea9-119">*IsMigratable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="49ea9-119">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49ea9-120">表示是否可以成功遷移虛擬系統的遷移檢查結果。</span><span class="sxs-lookup"><span data-stu-id="49ea9-120">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ea9-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="49ea9-121">Return value</span></span>

<span data-ttu-id="49ea9-122">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="49ea9-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="49ea9-123">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="49ea9-123">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="49ea9-124">Description</span><span class="sxs-lookup"><span data-stu-id="49ea9-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49ea9-125"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="49ea9-126">檢查已執行;透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="49ea9-126">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="49ea9-127"><dt>**不支援**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="49ea9-128">實作為不支援的方法。</span><span class="sxs-lookup"><span data-stu-id="49ea9-128">Method not supported by implementation.</span></span> <span data-ttu-id="49ea9-129">沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="49ea9-129">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="49ea9-130"><dt>**失敗**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="49ea9-131">檢查失敗的原因不明。</span><span class="sxs-lookup"><span data-stu-id="49ea9-131">Check failed for unspecified reasons.</span></span> <span data-ttu-id="49ea9-132">沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="49ea9-132">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="49ea9-133"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-133"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="49ea9-134">檢查超時。沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="49ea9-134">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="49ea9-135"><dt>**不正確參數**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-135"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="49ea9-136">一或多個參數正式無效。</span><span class="sxs-lookup"><span data-stu-id="49ea9-136">One or more parameters are formally invalid.</span></span> <span data-ttu-id="49ea9-137">例如， *DestinationSystem* 參數的值不包含有效的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="49ea9-137">For example, the value of the *DestinationSystem* parameter does not comprise a valid object path.</span></span> <span data-ttu-id="49ea9-138">沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="49ea9-138">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="49ea9-139"><dt>**狀態**</dt> <dt>5</dt>無效</span><span class="sxs-lookup"><span data-stu-id="49ea9-139"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="49ea9-140">來源虛擬系統、來源主機系統或目標主機系統處於允許起始要求的虛擬系統移轉的狀態;這可能是暫時性的狀況。</span><span class="sxs-lookup"><span data-stu-id="49ea9-140">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="49ea9-141">沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="49ea9-141">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="49ea9-142"><dt>**不相容的參數**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-142"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="49ea9-143">一或多個輸入參數與一組或目標主機不相容。</span><span class="sxs-lookup"><span data-stu-id="49ea9-143">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="49ea9-144">例如， *NewSettingData* 參數的值包含由 *DestinationSystem* 參數的值所識別的目標主機系統不支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="49ea9-144">For example the value of the *NewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span> <span data-ttu-id="49ea9-145">沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="49ea9-145">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="49ea9-146">已 <dt>**保留 DMTF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-146"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="49ea9-147"><dt>**方法保留**</dt>的 <dt>4097。</dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-147"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="49ea9-148"><dt>**廠商**</dt>專屬 <dt>的 32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-148"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="49ea9-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="49ea9-149">Requirements</span></span>



| <span data-ttu-id="49ea9-150">需求</span><span class="sxs-lookup"><span data-stu-id="49ea9-150">Requirement</span></span> | <span data-ttu-id="49ea9-151">值</span><span class="sxs-lookup"><span data-stu-id="49ea9-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49ea9-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49ea9-152">Minimum supported client</span></span><br/> | <span data-ttu-id="49ea9-153">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="49ea9-153">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="49ea9-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49ea9-154">Minimum supported server</span></span><br/> | <span data-ttu-id="49ea9-155">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="49ea9-155">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="49ea9-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="49ea9-156">Namespace</span></span><br/>                | <span data-ttu-id="49ea9-157">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="49ea9-157">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="49ea9-158">MOF</span><span class="sxs-lookup"><span data-stu-id="49ea9-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49ea9-159"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-159"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="49ea9-160">DLL</span><span class="sxs-lookup"><span data-stu-id="49ea9-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49ea9-161"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="49ea9-161"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="49ea9-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49ea9-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ea9-163">**CIM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="49ea9-163">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




