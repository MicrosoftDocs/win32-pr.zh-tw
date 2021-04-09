---
description: 將虛擬系統移動、遷移或重新放置至目標系統的方法。
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: CIM_VirtualSystemMigrationService 類別的 MigrateVirtualSystemToSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1459d80785725914cbaa5dda5b81e8d2fabad5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849019"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="f6d48-103">CIM VirtualSystemMigrationService 類別的 MigrateVirtualSystemToSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f6d48-103">MigrateVirtualSystemToSystem method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="f6d48-104">將虛擬系統移動、遷移或重新放置至目標系統的方法。</span><span class="sxs-lookup"><span data-stu-id="f6d48-104">Method to move, migrate or relocate a virtual system to a target system.</span></span>

<span data-ttu-id="f6d48-105">傳回碼描述：</span><span class="sxs-lookup"><span data-stu-id="f6d48-105">Return code description:</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d48-106">語法</span><span class="sxs-lookup"><span data-stu-id="f6d48-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f6d48-107">參數</span><span class="sxs-lookup"><span data-stu-id="f6d48-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6d48-108">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="f6d48-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d48-109">要遷移的來源虛擬電腦系統。</span><span class="sxs-lookup"><span data-stu-id="f6d48-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f6d48-110">*DestinationSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f6d48-110">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d48-111">目的地主機系統 whereto 遷移虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="f6d48-111">Destination host system whereto migrate the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="f6d48-112">*MigrationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f6d48-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d48-113">字串，包含 [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) 類別的內嵌實例，代表適用于遷移作業的遷移設定。</span><span class="sxs-lookup"><span data-stu-id="f6d48-113">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="f6d48-114">*NewSystemSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f6d48-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d48-115">字串，包含 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。</span><span class="sxs-lookup"><span data-stu-id="f6d48-115">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f6d48-116">*NewResourceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f6d48-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d48-117">字串陣列，其中每個字串都包含 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 類別的內嵌實例，代表在遷移之後，虛擬系統範圍中適用于虛擬資源的新屬性。</span><span class="sxs-lookup"><span data-stu-id="f6d48-117">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f6d48-118">*NewComputerSystem* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6d48-118">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d48-119">在遷移之後，參考代表虛擬電腦系統的 [**CIM \_**](cim-computersystem.md) 系統類型實例。</span><span class="sxs-lookup"><span data-stu-id="f6d48-119">Reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class representing the virtual computer system after it has been migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f6d48-120">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6d48-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d48-121">如果作業的執行時間很長，則可以選擇性地傳回代表作業的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 。</span><span class="sxs-lookup"><span data-stu-id="f6d48-121">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6d48-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6d48-122">Return value</span></span>

<span data-ttu-id="f6d48-123">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f6d48-123">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="f6d48-124">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f6d48-124">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="f6d48-125">Description</span><span class="sxs-lookup"><span data-stu-id="f6d48-125">Description</span></span>                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6d48-126"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-126"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="f6d48-127">虛擬系統已遷移。</span><span class="sxs-lookup"><span data-stu-id="f6d48-127">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="f6d48-128"><dt>**不支援**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-128"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="f6d48-129">實作為不支援的方法。</span><span class="sxs-lookup"><span data-stu-id="f6d48-129">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="f6d48-130"><dt>**失敗**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-130"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="f6d48-131">虛擬系統移轉失敗，原因不明。</span><span class="sxs-lookup"><span data-stu-id="f6d48-131">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="f6d48-132"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-132"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="f6d48-133">虛擬系統移轉超時;虛擬系統狀態不明。</span><span class="sxs-lookup"><span data-stu-id="f6d48-133">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="f6d48-134"><dt>**不正確參數**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-134"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="f6d48-135">一或多個參數正式無效，例如，目的地系統參數的值不包含有效的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="f6d48-135">One or more parameters are formally invalid For example, the value of the Destination System parameter does not contain a valid object path.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="f6d48-136"><dt>**狀態**</dt> <dt>5</dt>無效</span><span class="sxs-lookup"><span data-stu-id="f6d48-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="f6d48-137">來源虛擬系統、來源主機系統或目標主機系統處於允許起始要求的虛擬系統移轉的狀態;這可能是暫時性的狀況。</span><span class="sxs-lookup"><span data-stu-id="f6d48-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="f6d48-138"><dt>**不相容的參數**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="f6d48-139">一或多個輸入參數與一組或目標主機不相容。</span><span class="sxs-lookup"><span data-stu-id="f6d48-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="f6d48-140">例如， *MigrationNewSettingData* 參數的值包含由 *DestinationSystem* 參數的值所識別的目標主機系統不支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6d48-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationSystem* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="f6d48-141">已 <dt>**保留 DMTF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f6d48-142"><dt>**已檢查方法參數-作業已啟動**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f6d48-143"><dt>**方法保留**</dt>的 <dt>4097。</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="f6d48-144"><dt>**廠商**</dt>專屬 <dt>的 32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="f6d48-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6d48-145">Requirements</span></span>



| <span data-ttu-id="f6d48-146">需求</span><span class="sxs-lookup"><span data-stu-id="f6d48-146">Requirement</span></span> | <span data-ttu-id="f6d48-147">值</span><span class="sxs-lookup"><span data-stu-id="f6d48-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d48-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6d48-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f6d48-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f6d48-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f6d48-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6d48-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f6d48-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f6d48-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f6d48-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="f6d48-152">Namespace</span></span><br/>                | <span data-ttu-id="f6d48-153">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f6d48-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f6d48-154">MOF</span><span class="sxs-lookup"><span data-stu-id="f6d48-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6d48-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6d48-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f6d48-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6d48-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6d48-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6d48-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6d48-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d48-159">**CIM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="f6d48-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




