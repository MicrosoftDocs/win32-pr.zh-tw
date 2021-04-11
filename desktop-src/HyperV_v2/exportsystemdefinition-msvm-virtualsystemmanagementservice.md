---
description: 將虛擬機器或虛擬機器的快照集匯出到檔案。
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Msvm_VirtualSystemManagementService 類別的 ExportSystemDefinition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689496"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="1e63e-103">Msvm VirtualSystemManagementService 類別的 ExportSystemDefinition 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1e63e-103">ExportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1e63e-104">將虛擬機器或虛擬機器的快照集匯出到檔案。</span><span class="sxs-lookup"><span data-stu-id="1e63e-104">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span> <span data-ttu-id="1e63e-105">虛擬機器必須處於「已關閉電源」或「已儲存」狀態才能匯出。</span><span class="sxs-lookup"><span data-stu-id="1e63e-105">The virtual machine must be in the "powered off" or "saved" state to be exported.</span></span> <span data-ttu-id="1e63e-106">虛擬機器、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。</span><span class="sxs-lookup"><span data-stu-id="1e63e-106">The virtual machine, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e63e-107">語法</span><span class="sxs-lookup"><span data-stu-id="1e63e-107">Syntax</span></span>


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1e63e-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e63e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e63e-109">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e63e-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e63e-110">CIM 電腦的參考 [**， \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 代表要匯出的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1e63e-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="1e63e-111">*ExportDirectory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e63e-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e63e-112">要匯出虛擬機器之目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="1e63e-112">The fully qualified path of the directory to which the virtual machine is to be exported.</span></span> <span data-ttu-id="1e63e-113">如果 *ExportSettingData* 參數中 [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)類別的 **CreateVmExportSubdirectory** 屬性設定為 **True**，則可以重複使用此目錄來匯出多部虛擬機器，而此方法會將每個虛擬機器定義放在此路徑底下的個別子目錄中。</span><span class="sxs-lookup"><span data-stu-id="1e63e-113">If the **CreateVmExportSubdirectory** property of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class in the *ExportSettingData* parameter is set to **True**, then this directory can be reused for exporting multiple virtual machines and this method places each virtual machine definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="1e63e-114">*ExportSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e63e-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e63e-115">[**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)類別的內嵌實例，表示匯出作業的設定。</span><span class="sxs-lookup"><span data-stu-id="1e63e-115">An embedded instance of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="1e63e-116">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1e63e-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e63e-117">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="1e63e-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e63e-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e63e-118">Return value</span></span>

<span data-ttu-id="1e63e-119">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1e63e-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1e63e-120">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="1e63e-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-121">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="1e63e-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-122">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="1e63e-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-123">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="1e63e-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-124">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="1e63e-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-125">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="1e63e-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-126">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="1e63e-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-127">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="1e63e-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-128">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="1e63e-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-129">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="1e63e-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-130">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="1e63e-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-131">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="1e63e-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1e63e-132">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="1e63e-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1e63e-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e63e-133">Requirements</span></span>



| <span data-ttu-id="1e63e-134">需求</span><span class="sxs-lookup"><span data-stu-id="1e63e-134">Requirement</span></span> | <span data-ttu-id="1e63e-135">值</span><span class="sxs-lookup"><span data-stu-id="1e63e-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e63e-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e63e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1e63e-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e63e-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1e63e-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e63e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1e63e-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e63e-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e63e-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="1e63e-140">Namespace</span></span><br/>                | <span data-ttu-id="1e63e-141">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1e63e-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1e63e-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1e63e-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e63e-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1e63e-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e63e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1e63e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e63e-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e63e-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1e63e-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e63e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e63e-147">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="1e63e-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

