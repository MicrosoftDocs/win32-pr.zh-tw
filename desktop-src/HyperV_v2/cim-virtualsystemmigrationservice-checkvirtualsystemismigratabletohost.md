---
description: 方法來執行前置檢查，以判斷虛擬系統是否可能成功地遷移至網路名稱或 IP 位址所指定的目標主機。
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: CIM_VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToHost 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5769691a792b8f74225b640b0058ad4bd0e27c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001704"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a><span data-ttu-id="cf4a6-103">CIM VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToHost 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cf4a6-103">CheckVirtualSystemIsMigratableToHost method of the CIM\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="cf4a6-104">方法來執行前置檢查，以判斷虛擬系統是否可能成功地遷移至網路名稱或 IP 位址所指定的目標主機。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-104">Method to perform a pre-check to determine whether a virtual system is likely to be successfully migrated to a target host specified by a network name or IP address.</span></span> <span data-ttu-id="cf4a6-105">這種方法不保證後續的遷移一律會成功，因為動態資源可用性。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-105">This method does not guarantee that a subsequent migration will always succeed, due to dynamic resource availability.</span></span>

<span data-ttu-id="cf4a6-106">傳回碼描述：</span><span class="sxs-lookup"><span data-stu-id="cf4a6-106">Return code description:</span></span>

<span data-ttu-id="cf4a6-107">注意：此方法只是要在叢集支援的模型可供使用時，才會成為過渡解決方案。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-107">Note: This method is intended as a transitional solution only until modeling of cluster support is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf4a6-108">語法</span><span class="sxs-lookup"><span data-stu-id="cf4a6-108">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="cf4a6-109">參數</span><span class="sxs-lookup"><span data-stu-id="cf4a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf4a6-110">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf4a6-110">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4a6-111">要遷移的來源虛擬電腦系統的 CIM 系統可參考。 [**\_**](cim-computersystem.md)</span><span class="sxs-lookup"><span data-stu-id="cf4a6-111">A [**CIM\_ComputerSystem**](cim-computersystem.md) reference to the source virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="cf4a6-112">*DestinationHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf4a6-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4a6-113">遷移的目標主機系統。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-113">Target host system for the migration.</span></span>

<span data-ttu-id="cf4a6-114">此參數可接受的格式，是透過 \[ \] [**cim \_ ElementCapabilities**](cim-elementcapabilities.md)關聯所關聯之 [**cim \_ VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md)的實例中，DestinationHostFormatsSupported 陣列屬性的元素值來傳達。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-114">Acceptable formats for this parameter are conveyed through values of elements of the **DestinationHostFormatsSupported**\[ \] array property in the instance of the [**CIM\_VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md) that is associated through the [**CIM\_ElementCapabilities**](cim-elementcapabilities.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="cf4a6-115">*MigrationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf4a6-115">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4a6-116">字串，包含 [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) 類別的內嵌實例，代表適用于遷移作業的遷移設定。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-116">String containing an embedded instance of the [**CIM\_VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) class representing migration settings applicable to the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="cf4a6-117">*NewSystemSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf4a6-117">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4a6-118">字串，包含 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-118">String containing an embedded instance of the [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) class representing new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="cf4a6-119">*NewResourceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cf4a6-119">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4a6-120">字串陣列，其中每個字串都包含 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 類別的內嵌實例，代表在遷移之後，虛擬系統範圍中適用于虛擬資源的新屬性。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-120">Array of strings each containing an embedded instance of the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) class representing new properties applicable to virtual resources in the scope of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="cf4a6-121">*IsMigratable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cf4a6-121">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4a6-122">表示是否可以成功遷移虛擬系統的遷移檢查結果。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-122">The migration check result indicating whether or not the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf4a6-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf4a6-123">Return value</span></span>

<span data-ttu-id="cf4a6-124">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-124">Returns a 0 on success; otherwise, returns an error.</span></span>



| <span data-ttu-id="cf4a6-125">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="cf4a6-125">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="cf4a6-126">Description</span><span class="sxs-lookup"><span data-stu-id="cf4a6-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf4a6-127"><dt>**已完成，沒有錯誤**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-127"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="cf4a6-128">檢查已執行;透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-128">Check performed; result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="cf4a6-129"><dt>**不支援**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-129"><dt>**Not Supported**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="cf4a6-130">實作為不支援的方法。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-130">Method not supported by implementation.</span></span> <span data-ttu-id="cf4a6-131">沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-131">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="cf4a6-132"><dt>**失敗**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-132"><dt>**Failed**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="cf4a6-133">檢查失敗的原因不明。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-133">Check failed for unspecified reasons.</span></span> <span data-ttu-id="cf4a6-134">沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-134">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="cf4a6-135"><dt>**Timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-135"><dt>**Timeout**</dt> <dt>3</dt></span></span> </dl>                    | <span data-ttu-id="cf4a6-136">檢查超時。沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-136">Check timed out. No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="cf4a6-137"><dt>**不正確參數**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-137"><dt>**Invalid Parameter**</dt> <dt>4</dt></span></span> </dl>          | <span data-ttu-id="cf4a6-138">一或多個參數正式無效。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-138">One or more parameters are formally invalid.</span></span> <span data-ttu-id="cf4a6-139">例如，您可以使用不支援的格式來指定 *DestinationHost* 參數的值。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-139">For example, the value of the *DestinationHost* parameter could have been specified in an unsupported format.</span></span> <span data-ttu-id="cf4a6-140">沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-140">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                                                                    |
| <dl> <span data-ttu-id="cf4a6-141"><dt>**狀態**</dt> <dt>5</dt>無效</span><span class="sxs-lookup"><span data-stu-id="cf4a6-141"><dt>**Invalid State**</dt> <dt>5</dt></span></span> </dl>              | <span data-ttu-id="cf4a6-142">來源虛擬系統、來源主機系統或目標主機系統處於允許起始要求的虛擬系統移轉的狀態;這可能是暫時性的狀況。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-142">The source virtual system, the source host system or the target host system are in a state that does allow initiation of the requested virtual system migration; this may be a temporary condition.</span></span> <span data-ttu-id="cf4a6-143">沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-143">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="cf4a6-144"><dt>**不相容的參數**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-144"><dt>**Incompatible Parameters**</dt> <dt>6</dt></span></span> </dl>    | <span data-ttu-id="cf4a6-145">一或多個輸入參數與一組或目標主機不相容。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-145">One or more input parameters are incompatible as a set, or with respect to the target host.</span></span> <span data-ttu-id="cf4a6-146">例如， *MigrationNewSettingData* 參數的值包含由 *DestinationHost* 參數的值所識別的目標主機系統不支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-146">For example the value of the *MigrationNewSettingData* parameter contains properties that are not supported by the target host system identified by the value of the *DestinationHost* parameter.</span></span> <span data-ttu-id="cf4a6-147">沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。</span><span class="sxs-lookup"><span data-stu-id="cf4a6-147">No result reported through the value of the \[Out\] *IsMigratable* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="cf4a6-148">已 <dt>**保留 DMTF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-148"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="cf4a6-149"><dt>**方法保留**</dt>的 <dt>4097。</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-149"><dt>**Method Reserved**</dt> <dt>4097..32767</dt></span></span> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="cf4a6-150"><dt>**廠商**</dt>專屬 <dt>的 32768. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-150"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="cf4a6-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf4a6-151">Requirements</span></span>



| <span data-ttu-id="cf4a6-152">需求</span><span class="sxs-lookup"><span data-stu-id="cf4a6-152">Requirement</span></span> | <span data-ttu-id="cf4a6-153">值</span><span class="sxs-lookup"><span data-stu-id="cf4a6-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4a6-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cf4a6-154">Minimum supported client</span></span><br/> | <span data-ttu-id="cf4a6-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cf4a6-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="cf4a6-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cf4a6-156">Minimum supported server</span></span><br/> | <span data-ttu-id="cf4a6-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="cf4a6-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="cf4a6-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="cf4a6-158">Namespace</span></span><br/>                | <span data-ttu-id="cf4a6-159">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="cf4a6-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cf4a6-160">MOF</span><span class="sxs-lookup"><span data-stu-id="cf4a6-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf4a6-161"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf4a6-162">DLL</span><span class="sxs-lookup"><span data-stu-id="cf4a6-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf4a6-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a6-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cf4a6-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf4a6-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf4a6-165">**CIM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="cf4a6-165">**CIM\_VirtualSystemMigrationService**</span></span>](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




