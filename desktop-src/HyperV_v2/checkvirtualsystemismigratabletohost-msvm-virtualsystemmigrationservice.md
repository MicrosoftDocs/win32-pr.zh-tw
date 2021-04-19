---
description: 判斷指定的虛擬系統是否可以遷移至網路名稱或 IP 位址所指定的目標主機。
ms.assetid: eacc8448-4683-48df-81b9-8599292944db
title: Msvm_VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToHost 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b81f6562f892acbaa5bf7ff7f4f3c772574bd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998093"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="e73f3-103">Msvm VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToHost 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e73f3-103">CheckVirtualSystemIsMigratableToHost method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="e73f3-104">判斷指定的虛擬系統是否可以遷移至網路名稱或 IP 位址所指定的目標主機。</span><span class="sxs-lookup"><span data-stu-id="e73f3-104">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="e73f3-105">語法</span><span class="sxs-lookup"><span data-stu-id="e73f3-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  string                  DestinationHost,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="e73f3-106">參數</span><span class="sxs-lookup"><span data-stu-id="e73f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e73f3-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="e73f3-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e73f3-108">[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表要測試其遷移能力的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e73f3-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="e73f3-109">*DestinationHost* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e73f3-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e73f3-110">要遷移的主機系統名稱。</span><span class="sxs-lookup"><span data-stu-id="e73f3-110">The name of the host system for the migration.</span></span> <span data-ttu-id="e73f3-111">這個名稱的格式是由與這個類別相關聯之 [**Msvm \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md)類別的 **DestinationHostFormatsSupported** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="e73f3-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="e73f3-112">*MigrationSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e73f3-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e73f3-113">[**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md)類別的內嵌實例，代表遷移作業的設定。</span><span class="sxs-lookup"><span data-stu-id="e73f3-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="e73f3-114">*NewSystemSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e73f3-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e73f3-115">[**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。</span><span class="sxs-lookup"><span data-stu-id="e73f3-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e73f3-116">*NewResourceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e73f3-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e73f3-117">字串陣列，其中包含 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例，表示在遷移之後，適用于虛擬系統虛擬資源的新屬性。</span><span class="sxs-lookup"><span data-stu-id="e73f3-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="e73f3-118">*IsMigratable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e73f3-118">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e73f3-119">接收遷移檢查結果，指出是否可以成功遷移虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="e73f3-119">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e73f3-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="e73f3-120">Return value</span></span>

<span data-ttu-id="e73f3-121">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e73f3-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e73f3-122">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="e73f3-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e73f3-123">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="e73f3-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e73f3-124">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="e73f3-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e73f3-125">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="e73f3-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e73f3-126">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="e73f3-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e73f3-127">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="e73f3-127">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e73f3-128"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="e73f3-128">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="e73f3-129">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="e73f3-129">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e73f3-130">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="e73f3-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e73f3-131">**廠商特定** (32768. 65535 ) </span><span class="sxs-lookup"><span data-stu-id="e73f3-131">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e73f3-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="e73f3-132">Requirements</span></span>



| <span data-ttu-id="e73f3-133">需求</span><span class="sxs-lookup"><span data-stu-id="e73f3-133">Requirement</span></span> | <span data-ttu-id="e73f3-134">值</span><span class="sxs-lookup"><span data-stu-id="e73f3-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e73f3-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e73f3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e73f3-136">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e73f3-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e73f3-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e73f3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e73f3-138">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e73f3-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e73f3-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="e73f3-139">Namespace</span></span><br/>                | <span data-ttu-id="e73f3-140">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e73f3-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e73f3-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e73f3-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e73f3-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e73f3-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e73f3-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e73f3-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e73f3-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e73f3-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e73f3-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e73f3-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e73f3-146">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="e73f3-146">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




