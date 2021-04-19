---
description: 判斷指定的虛擬系統是否可以遷移到目的地系統。
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Msvm_VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973610"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="f7763-103">Msvm VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToSystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f7763-103">CheckVirtualSystemIsMigratableToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="f7763-104">判斷指定的虛擬系統是否可以遷移到目的地系統。</span><span class="sxs-lookup"><span data-stu-id="f7763-104">Determines whether the specified virtual system can be migrated to a destination system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7763-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7763-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="f7763-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7763-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7763-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7763-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7763-108">[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表要測試其遷移能力的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f7763-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="f7763-109">*DestinationSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7763-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7763-110">[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表要測試遷移能力的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f7763-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability to.</span></span>

</dd> <dt>

<span data-ttu-id="f7763-111">*MigrationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7763-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7763-112">[**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)類別的內嵌實例，代表遷移作業的設定。</span><span class="sxs-lookup"><span data-stu-id="f7763-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="f7763-113">*NewSystemSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7763-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7763-114">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。</span><span class="sxs-lookup"><span data-stu-id="f7763-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f7763-115">*NewResourceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7763-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7763-116">字串陣列，其中包含 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例，表示在遷移之後，適用于虛擬系統虛擬資源的新屬性。</span><span class="sxs-lookup"><span data-stu-id="f7763-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="f7763-117">*IsMigratable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f7763-117">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7763-118">接收遷移檢查結果，指出是否可以成功遷移虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="f7763-118">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7763-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7763-119">Return value</span></span>

<span data-ttu-id="f7763-120">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f7763-120">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f7763-121">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="f7763-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f7763-122">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="f7763-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f7763-123">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="f7763-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f7763-124">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="f7763-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f7763-125">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="f7763-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f7763-126">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="f7763-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f7763-127"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="f7763-127">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f7763-128">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f7763-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f7763-129">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="f7763-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f7763-130">**廠商特定** (32768. 65535 ) </span><span class="sxs-lookup"><span data-stu-id="f7763-130">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f7763-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7763-131">Requirements</span></span>



| <span data-ttu-id="f7763-132">需求</span><span class="sxs-lookup"><span data-stu-id="f7763-132">Requirement</span></span> | <span data-ttu-id="f7763-133">值</span><span class="sxs-lookup"><span data-stu-id="f7763-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7763-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7763-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f7763-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7763-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f7763-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7763-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f7763-137">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7763-137">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7763-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="f7763-138">Namespace</span></span><br/>                | <span data-ttu-id="f7763-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f7763-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f7763-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f7763-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7763-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f7763-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7763-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f7763-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7763-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f7763-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f7763-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7763-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7763-145">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="f7763-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




