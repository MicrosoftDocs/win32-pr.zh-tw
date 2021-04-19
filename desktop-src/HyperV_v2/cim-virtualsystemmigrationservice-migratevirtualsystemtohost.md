---
description: 將虛擬系統移動、遷移或重新放置到網路名稱或 IP 位址所指定之目標主機的方法。
ms.assetid: 09fdc0b2-641c-47f5-b270-e26e3acf7ea5
title: CIM_VirtualSystemMigrationService 類別的 MigrateVirtualSystemToHost 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1a90e3adadbb5efc5f9cae3b7710e07c1e05000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979109"
---
# <a name="migratevirtualsystemtohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="fdc04-103">CIM VirtualSystemMigrationService 類別的 MigrateVirtualSystemToHost 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fdc04-103">MigrateVirtualSystemToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="fdc04-104">將虛擬系統移動、遷移或重新放置到網路名稱或 IP 位址所指定之目標主機的方法。</span><span class="sxs-lookup"><span data-stu-id="fdc04-104">Method to move, migrate or relocate a virtual system to a target host specified by a network name or IP address.</span></span>

> [!Note]  
> <span data-ttu-id="fdc04-105">這種方法的目的是要在叢集支援模型可用之前，才使用過渡解決方案。</span><span class="sxs-lookup"><span data-stu-id="fdc04-105">This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="fdc04-106">語法</span><span class="sxs-lookup"><span data-stu-id="fdc04-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fdc04-107">參數</span><span class="sxs-lookup"><span data-stu-id="fdc04-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdc04-108">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdc04-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdc04-109">要遷移的來源虛擬電腦系統。</span><span class="sxs-lookup"><span data-stu-id="fdc04-109">Source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="fdc04-110">*DestinationHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdc04-110">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdc04-111">遷移的目標主機系統。</span><span class="sxs-lookup"><span data-stu-id="fdc04-111">Target host system for the migration.</span></span>

<span data-ttu-id="fdc04-112">此參數可接受的格式，是透過 \[ \] [**cim \_ ElementCapabilities**](cim-elementcapabilities.md)關聯所關聯之 [**cim \_ VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md)的實例中，DestinationHostFormatsSupported 陣列屬性的元素值來傳達。</span><span class="sxs-lookup"><span data-stu-id="fdc04-112">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="fdc04-113">*MigrationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdc04-113">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdc04-114">字串，包含 [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) 類別的內嵌實例，代表適用于遷移作業的遷移設定。</span><span class="sxs-lookup"><span data-stu-id="fdc04-114">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="fdc04-115">*NewSystemSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdc04-115">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdc04-116">字串，包含 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。</span><span class="sxs-lookup"><span data-stu-id="fdc04-116">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="fdc04-117">*NewResourceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fdc04-117">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdc04-118">字串陣列，其中每個字串都包含 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 類別的內嵌實例，代表在遷移之後，虛擬系統範圍中適用于虛擬資源的新屬性。</span><span class="sxs-lookup"><span data-stu-id="fdc04-118">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="fdc04-119">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fdc04-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fdc04-120">如果作業的執行時間很長，則可以選擇性地傳回代表作業的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 。</span><span class="sxs-lookup"><span data-stu-id="fdc04-120">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdc04-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="fdc04-121">Return value</span></span>

<span data-ttu-id="fdc04-122">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="fdc04-122">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="fdc04-123">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="fdc04-123">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="fdc04-124">Description</span><span class="sxs-lookup"><span data-stu-id="fdc04-124">Description</span></span>                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fdc04-125"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-125"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="fdc04-126">虛擬系統已遷移。</span><span class="sxs-lookup"><span data-stu-id="fdc04-126">Virtual system was migrated.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="fdc04-127"><dt>**不支援**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-127"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="fdc04-128">實作為不支援的方法。</span><span class="sxs-lookup"><span data-stu-id="fdc04-128">Method not supported by implementation.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="fdc04-129"><dt>**失敗**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-129"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                                     | <span data-ttu-id="fdc04-130">虛擬系統移轉失敗，原因不明。</span><span class="sxs-lookup"><span data-stu-id="fdc04-130">Virtual system migration failed for unspecified reasons.</span></span><br/>                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="fdc04-131"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-131"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                                    | <span data-ttu-id="fdc04-132">虛擬系統移轉超時;虛擬系統狀態不明。</span><span class="sxs-lookup"><span data-stu-id="fdc04-132">Virtual system migration time out; the virtual system state is unknown.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="fdc04-133"><dt>**不正確參數**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-133"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="fdc04-134">一或多個參數正式無效。</span><span class="sxs-lookup"><span data-stu-id="fdc04-134">One or more parameters are formally invalid.</span></span> <span data-ttu-id="fdc04-135">例如，您可以使用不支援的格式來指定 *DestinationHost* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="fdc04-135">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="fdc04-136"><dt>**狀態**</dt> <dt>5</dt>無效</span><span class="sxs-lookup"><span data-stu-id="fdc04-136"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>                              | <span data-ttu-id="fdc04-137">來源虛擬系統、來源主機系統或目標主機系統處於允許起始要求的虛擬系統移轉的狀態;這可能是暫時性的狀況。</span><span class="sxs-lookup"><span data-stu-id="fdc04-137">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="fdc04-138"><dt>**不相容的參數**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-138"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>                    | <span data-ttu-id="fdc04-139">一或多個輸入參數與一組或目標主機不相容。</span><span class="sxs-lookup"><span data-stu-id="fdc04-139">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="fdc04-140">例如， *MigrationNewSettingData* 參數的值包含由 *DestinationHost* 參數的值所識別的目標主機系統不支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="fdc04-140">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="fdc04-141">已 <dt>**保留 DMTF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-141"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="fdc04-142"><dt>**已檢查方法參數-作業已啟動**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-142"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="fdc04-143"><dt>**方法保留**</dt>的 <dt>4097。</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-143"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="fdc04-144"><dt>**廠商**</dt>專屬 <dt>的 32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-144"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="fdc04-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="fdc04-145">Requirements</span></span>



| <span data-ttu-id="fdc04-146">需求</span><span class="sxs-lookup"><span data-stu-id="fdc04-146">Requirement</span></span> | <span data-ttu-id="fdc04-147">值</span><span class="sxs-lookup"><span data-stu-id="fdc04-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdc04-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fdc04-148">Minimum supported client</span></span><br/> | <span data-ttu-id="fdc04-149">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fdc04-149">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fdc04-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fdc04-150">Minimum supported server</span></span><br/> | <span data-ttu-id="fdc04-151">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fdc04-151">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fdc04-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="fdc04-152">Namespace</span></span><br/>                | <span data-ttu-id="fdc04-153">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="fdc04-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fdc04-154">MOF</span><span class="sxs-lookup"><span data-stu-id="fdc04-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fdc04-155"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fdc04-156">DLL</span><span class="sxs-lookup"><span data-stu-id="fdc04-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdc04-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fdc04-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fdc04-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdc04-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdc04-159">**CIM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="fdc04-159">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




