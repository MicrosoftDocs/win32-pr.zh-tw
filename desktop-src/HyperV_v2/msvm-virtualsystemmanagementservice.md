---
description: 代表存在於單一主機系統上的虛擬化服務。
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Msvm_VirtualSystemManagementService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ee79b9690f1eacdf7dc57a2ebfc2133091a1d55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689763"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6f66b-103">Msvm \_ VirtualSystemManagementService 類別</span><span class="sxs-lookup"><span data-stu-id="6f66b-103">Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6f66b-104">代表存在於單一主機系統上的虛擬化服務。</span><span class="sxs-lookup"><span data-stu-id="6f66b-104">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="6f66b-105">**Msvm \_VirtualSystemManagementService** 可用來控制虛擬機器的定義、修改和刪除。</span><span class="sxs-lookup"><span data-stu-id="6f66b-105">**Msvm\_VirtualSystemManagementService** is used to control the definition, modification, and deletion of virtual machines.</span></span> <span data-ttu-id="6f66b-106">它也有方法可在虛擬機器上執行作業，例如複製、快照，以及匯入或匯出虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6f66b-106">It also has methods for performing operations on virtual machines, such as cloning, snapshotting, and the importing or exporting of virtual machines.</span></span> <span data-ttu-id="6f66b-107">若要取得每個虛擬機器資訊，請使用 [**Msvm \_**](msvm-computersystem.md)。</span><span class="sxs-lookup"><span data-stu-id="6f66b-107">To retrieve per-virtual machine information, use [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="6f66b-108">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6f66b-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f66b-109">語法</span><span class="sxs-lookup"><span data-stu-id="6f66b-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="6f66b-110">成員</span><span class="sxs-lookup"><span data-stu-id="6f66b-110">Members</span></span>

<span data-ttu-id="6f66b-111">**Msvm \_ VirtualSystemManagementService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6f66b-111">The **Msvm\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="6f66b-112">方法</span><span class="sxs-lookup"><span data-stu-id="6f66b-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="6f66b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="6f66b-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6f66b-114">方法</span><span class="sxs-lookup"><span data-stu-id="6f66b-114">Methods</span></span>

<span data-ttu-id="6f66b-115">**Msvm \_ VirtualSystemManagementService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6f66b-115">The **Msvm\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="6f66b-116">方法</span><span class="sxs-lookup"><span data-stu-id="6f66b-116">Method</span></span>                                                                                                                 | <span data-ttu-id="6f66b-117">描述</span><span class="sxs-lookup"><span data-stu-id="6f66b-117">Description</span></span>                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f66b-118">**AddBootSourceSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-118">**AddBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | <span data-ttu-id="6f66b-119">在套用至「狀態」虛擬系統設定時，將開機來源新增至虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-119">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="6f66b-120">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-120">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | <span data-ttu-id="6f66b-121">將乙太網路功能設定新增至虛擬機器 Ethernet 連接的設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-121">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="6f66b-122">**AddFibreChannelChap**</span><span class="sxs-lookup"><span data-stu-id="6f66b-122">**AddFibreChannelChap**</span></span>](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="6f66b-123">將 DH-CHAP 參數新增到虛擬機器中的綜合光纖通道埠。</span><span class="sxs-lookup"><span data-stu-id="6f66b-123">Adds DH-CHAP parameters to a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="6f66b-124">**AddGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-124">**AddGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | <span data-ttu-id="6f66b-125">將來賓服務設定新增至虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-125">Adds guest service settings to a virtual system configuration.</span></span><br/> <span data-ttu-id="6f66b-126">套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用來賓服務。</span><span class="sxs-lookup"><span data-stu-id="6f66b-126">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>              |
| [<span data-ttu-id="6f66b-127">**AddKvpItems**</span><span class="sxs-lookup"><span data-stu-id="6f66b-127">**AddKvpItems**</span></span>](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="6f66b-128">將機碼/值組加入至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6f66b-128">Adds key-value pairs to a virtual machine.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="6f66b-129">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-129">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="6f66b-130">將資源新增至虛擬機器設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-130">Adds resources to a virtual machine configuration.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="6f66b-131">**AddSystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-131">**AddSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | <span data-ttu-id="6f66b-132">將一般設定新增至虛擬系統設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-132">Adds generic settings to a virtual system configuration.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="6f66b-133">**DefinePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="6f66b-133">**DefinePlannedSystem**</span></span>](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | <span data-ttu-id="6f66b-134">定義已規劃的虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="6f66b-134">Defines a planned virtual system.</span></span><br/> <span data-ttu-id="6f66b-135">未完全指定的輸入可能會以預設值填入。</span><span class="sxs-lookup"><span data-stu-id="6f66b-135">Input that is not completely specified may be filled out with default values.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="6f66b-136">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="6f66b-136">**DefineSystem**</span></span>](definesystem-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="6f66b-137">建立新的虛擬機器定義。</span><span class="sxs-lookup"><span data-stu-id="6f66b-137">Creates a new virtual machine definition.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="6f66b-138">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="6f66b-138">**DestroySystem**</span></span>](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | <span data-ttu-id="6f66b-139">刪除現有的虛擬機器定義。</span><span class="sxs-lookup"><span data-stu-id="6f66b-139">Deletes an existing virtual machine definition.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="6f66b-140">**DiagnoseNetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="6f66b-140">**DiagnoseNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | <span data-ttu-id="6f66b-141">在 Windows 網路虛擬化環境中診斷 VM 的網路連線能力。</span><span class="sxs-lookup"><span data-stu-id="6f66b-141">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="6f66b-142">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="6f66b-142">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="6f66b-143">將虛擬機器或虛擬機器的快照集匯出到檔案。</span><span class="sxs-lookup"><span data-stu-id="6f66b-143">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="6f66b-144">**FormatError**</span><span class="sxs-lookup"><span data-stu-id="6f66b-144">**FormatError**</span></span>](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="6f66b-145">針對指定的內嵌 [**Msvm \_ 錯誤**](msvm-error.md) 實例陣列，傳回格式化的錯誤訊息字串。</span><span class="sxs-lookup"><span data-stu-id="6f66b-145">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="6f66b-146">**GenerateWwpn**</span><span class="sxs-lookup"><span data-stu-id="6f66b-146">**GenerateWwpn**</span></span>](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="6f66b-147">產生一組全球通訊埠名稱 (WWPNs) 。</span><span class="sxs-lookup"><span data-stu-id="6f66b-147">Generates a set of World Wide Port Names (WWPNs).</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="6f66b-148">**GetCurrentWwpnFromGenerator**</span><span class="sxs-lookup"><span data-stu-id="6f66b-148">**GetCurrentWwpnFromGenerator**</span></span>](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | <span data-ttu-id="6f66b-149">提供在不保留 WWPN 的情況下，預覽目前全球埠名稱 (WWPN) 的功能。</span><span class="sxs-lookup"><span data-stu-id="6f66b-149">Provides the ability to preview the current World Wide Port Name (WWPN) without the WWPN being reserved.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="6f66b-150">**GetDefinitionFileSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="6f66b-150">**GetDefinitionFileSummaryInformation**</span></span>](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="6f66b-151">傳回指定之虛擬機器定義檔的虛擬機器摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="6f66b-151">Returns virtual machine summary information for the specified virtual machine definition files.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="6f66b-152">**GetSizeOfSystemFiles**</span><span class="sxs-lookup"><span data-stu-id="6f66b-152">**GetSizeOfSystemFiles**</span></span>](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="6f66b-153">抓取虛擬機器的系統檔案大小總計。</span><span class="sxs-lookup"><span data-stu-id="6f66b-153">Retrieves the total size of the system files of virtual machine.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="6f66b-154">**GetSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="6f66b-154">**GetSummaryInformation**</span></span>](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="6f66b-155">傳回虛擬機器摘要資訊。</span><span class="sxs-lookup"><span data-stu-id="6f66b-155">Returns virtual machine summary information.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="6f66b-156">**GetVirtualSystemThumbnailImage**</span><span class="sxs-lookup"><span data-stu-id="6f66b-156">**GetVirtualSystemThumbnailImage**</span></span>](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | <span data-ttu-id="6f66b-157">抓取現有虛擬機器的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="6f66b-157">Retrieves a thumbnail image of an existing virtual machine.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="6f66b-158">**ImportSnapshotDefinitions**</span><span class="sxs-lookup"><span data-stu-id="6f66b-158">**ImportSnapshotDefinitions**</span></span>](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | <span data-ttu-id="6f66b-159">搜尋指定的資料夾中是否有任何與指定之規劃的電腦系統相關聯的快照集定義檔案，並針對此位置中的每個關聯定義檔，在規劃的電腦系統上建立新的快照集。</span><span class="sxs-lookup"><span data-stu-id="6f66b-159">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span><br/> |
| [<span data-ttu-id="6f66b-160">**ImportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="6f66b-160">**ImportSystemDefinition**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="6f66b-161">根據指定的虛擬機器定義，建立新的規劃的電腦系統。</span><span class="sxs-lookup"><span data-stu-id="6f66b-161">Creates a new planned computer system based on the specified virtual machine definition.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="6f66b-162">**ModifyDiskMergeSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-162">**ModifyDiskMergeSettings**</span></span>](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | <span data-ttu-id="6f66b-163">修改磁片合併設定資料。</span><span class="sxs-lookup"><span data-stu-id="6f66b-163">Modifies the disk merge setting data.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="6f66b-164">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-164">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="6f66b-165">修改虛擬機器乙太網路連接的目前功能設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-165">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="6f66b-166">**ModifyGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-166">**ModifyGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | <span data-ttu-id="6f66b-167">修改來賓服務設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-167">Modifies guest service settings.</span></span><br/> <span data-ttu-id="6f66b-168">套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用來賓服務。</span><span class="sxs-lookup"><span data-stu-id="6f66b-168">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>                                            |
| [<span data-ttu-id="6f66b-169">**ModifyKvpItems**</span><span class="sxs-lookup"><span data-stu-id="6f66b-169">**ModifyKvpItems**</span></span>](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="6f66b-170">修改虛擬機器上現有的機碼值組。</span><span class="sxs-lookup"><span data-stu-id="6f66b-170">Modifies existing key-value pairs on a virtual machine.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="6f66b-171">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-171">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="6f66b-172">修改虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-172">Modifies virtual resource settings.</span></span><br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="6f66b-173">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-173">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="6f66b-174">修改服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="6f66b-174">Modifies the service's setting data.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="6f66b-175">**ModifySystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-175">**ModifySystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | <span data-ttu-id="6f66b-176">修改一般系統元件設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-176">Modifies generic system component settings.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="6f66b-177">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-177">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="6f66b-178">修改虛擬機器設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-178">Modifies virtual machine settings.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="6f66b-179">**RealizePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="6f66b-179">**RealizePlannedSystem**</span></span>](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="6f66b-180">驗證已規劃的虛擬機器設定，並將其轉換為實現的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6f66b-180">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="6f66b-181">**RemoveBootSourceSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-181">**RemoveBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | <span data-ttu-id="6f66b-182">從虛擬系統組態移除虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-182">Removes virtual resource settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="6f66b-183">套用至「目前」虛擬系統設定的元件時，可能會移除作用中虛擬系統的副作用資源。</span><span class="sxs-lookup"><span data-stu-id="6f66b-183">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span><br/>            |
| [<span data-ttu-id="6f66b-184">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-184">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="6f66b-185">從虛擬機器乙太網路連接移除功能設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-185">Removes feature settings from a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="6f66b-186">**RemoveFibreChannelChap**</span><span class="sxs-lookup"><span data-stu-id="6f66b-186">**RemoveFibreChannelChap**</span></span>](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="6f66b-187">從虛擬機器中的綜合光纖通道埠移除 DH CHAP 參數。</span><span class="sxs-lookup"><span data-stu-id="6f66b-187">Removes DH-CHAP parameters from a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="6f66b-188">**RemoveGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-188">**RemoveGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | <span data-ttu-id="6f66b-189">從虛擬系統組態中移除來賓服務設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-189">Removes guest service settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="6f66b-190">套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用來賓服務。</span><span class="sxs-lookup"><span data-stu-id="6f66b-190">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>         |
| [<span data-ttu-id="6f66b-191">**RemoveKvpItems**</span><span class="sxs-lookup"><span data-stu-id="6f66b-191">**RemoveKvpItems**</span></span>](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="6f66b-192">從虛擬機器移除現有的機碼值組。</span><span class="sxs-lookup"><span data-stu-id="6f66b-192">Removes existing key-value pairs from a virtual machine.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="6f66b-193">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-193">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="6f66b-194">從虛擬機器設定移除虛擬資源設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-194">Removes virtual resource settings from a virtual machine configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="6f66b-195">**RemoveSystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="6f66b-195">**RemoveSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | <span data-ttu-id="6f66b-196">從虛擬系統組態中移除一般元件設定。</span><span class="sxs-lookup"><span data-stu-id="6f66b-196">Removes generic component settings from a virtual system configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="6f66b-197">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="6f66b-197">**RequestStateChange**</span></span>](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | <span data-ttu-id="6f66b-198">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="6f66b-198">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="6f66b-199">**SetGuestNetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="6f66b-199">**SetGuestNetworkAdapterConfiguration**</span></span>](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="6f66b-200">設定客體作業系統內的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="6f66b-200">Configures the network adapters within the guest operating system.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="6f66b-201">**SetInitialMachineConfigurationData**</span><span class="sxs-lookup"><span data-stu-id="6f66b-201">**SetInitialMachineConfigurationData**</span></span>](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | <span data-ttu-id="6f66b-202">設定 VM 的初始電腦設定資料。</span><span class="sxs-lookup"><span data-stu-id="6f66b-202">Sets a VM's initial machine configuration data.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="6f66b-203">**StartService**</span><span class="sxs-lookup"><span data-stu-id="6f66b-203">**StartService**</span></span>](msvm-virtualsystemmanagementservice-startservice.md)                                               | <span data-ttu-id="6f66b-204">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="6f66b-204">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="6f66b-205">**StopService**</span><span class="sxs-lookup"><span data-stu-id="6f66b-205">**StopService**</span></span>](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | <span data-ttu-id="6f66b-206">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="6f66b-206">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="6f66b-207">**TestNetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="6f66b-207">**TestNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | <span data-ttu-id="6f66b-208">在 Windows 網路虛擬化環境中測試 VM 的網路連線能力。</span><span class="sxs-lookup"><span data-stu-id="6f66b-208">Tests the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="6f66b-209">**UpgradeSystemVersion**</span><span class="sxs-lookup"><span data-stu-id="6f66b-209">**UpgradeSystemVersion**</span></span>](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | <span data-ttu-id="6f66b-210">升級虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="6f66b-210">Upgrades the virtual system.</span></span><br/> <span data-ttu-id="6f66b-211">套用至「目前」虛擬系統組態的系統設定時</span><span class="sxs-lookup"><span data-stu-id="6f66b-211">When applied to the system settings of a "current" virtual system configuration</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="6f66b-212">**ValidatePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="6f66b-212">**ValidatePlannedSystem**</span></span>](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="6f66b-213">驗證指定的計畫系統。</span><span class="sxs-lookup"><span data-stu-id="6f66b-213">Validates the specified planned system.</span></span><br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="6f66b-214">屬性</span><span class="sxs-lookup"><span data-stu-id="6f66b-214">Properties</span></span>

<span data-ttu-id="6f66b-215">**Msvm \_ VirtualSystemManagementService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6f66b-215">The **Msvm\_VirtualSystemManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f66b-216">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="6f66b-216">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-217">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="6f66b-217">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-219">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="6f66b-219">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="6f66b-220">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f66b-220">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-221">**標題**</span><span class="sxs-lookup"><span data-stu-id="6f66b-221">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-223">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-224">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="6f66b-224">A short description of the object.</span></span> <span data-ttu-id="6f66b-225">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 虛擬系統管理服務」。</span><span class="sxs-lookup"><span data-stu-id="6f66b-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-226">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="6f66b-226">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-227">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f66b-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-229">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="6f66b-229">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="6f66b-230">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="6f66b-230">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f66b-231">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="6f66b-231">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6f66b-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6f66b-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="6f66b-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="6f66b-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="6f66b-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="6f66b-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="6f66b-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="6f66b-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6f66b-239">)</span><span class="sxs-lookup"><span data-stu-id="6f66b-239">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f66b-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6f66b-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-241">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-243">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="6f66b-243">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-244">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f66b-244">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6f66b-245">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "Msvm \_ VirtualSystemManagementService"。</span><span class="sxs-lookup"><span data-stu-id="6f66b-245">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-246">**說明**</span><span class="sxs-lookup"><span data-stu-id="6f66b-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-249">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="6f66b-249">A description of the object.</span></span> <span data-ttu-id="6f66b-250">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律會設定為「用於建立、操作及管理虛擬機器的服務」。</span><span class="sxs-lookup"><span data-stu-id="6f66b-250">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, manipulating, and managing virtual machines".</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-251">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="6f66b-251">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-252">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f66b-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-254">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6f66b-254">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="6f66b-255">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="6f66b-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f66b-256">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="6f66b-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6f66b-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="6f66b-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="6f66b-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="6f66b-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="6f66b-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="6f66b-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="6f66b-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="6f66b-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="6f66b-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6f66b-265">)</span><span class="sxs-lookup"><span data-stu-id="6f66b-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f66b-266">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="6f66b-266">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-269">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="6f66b-269">A display name for the object.</span></span> <span data-ttu-id="6f66b-270">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 虛擬系統管理服務」。</span><span class="sxs-lookup"><span data-stu-id="6f66b-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-271">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="6f66b-271">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-272">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f66b-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-273">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-274">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="6f66b-274">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="6f66b-275">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="6f66b-275">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="6f66b-276">值</span><span class="sxs-lookup"><span data-stu-id="6f66b-276">Value</span></span>                                                                        | <span data-ttu-id="6f66b-277">意義</span><span class="sxs-lookup"><span data-stu-id="6f66b-277">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="6f66b-278"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6f66b-278"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6f66b-279">已啟用</span><span class="sxs-lookup"><span data-stu-id="6f66b-279">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6f66b-280">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="6f66b-280">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-281">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f66b-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-283">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="6f66b-283">The enabled and disabled states of an element.</span></span> <span data-ttu-id="6f66b-284">這個屬性也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="6f66b-284">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="6f66b-285">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="6f66b-285">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="6f66b-286">值</span><span class="sxs-lookup"><span data-stu-id="6f66b-286">Value</span></span>                                                                        | <span data-ttu-id="6f66b-287">意義</span><span class="sxs-lookup"><span data-stu-id="6f66b-287">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="6f66b-288"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6f66b-288"><dt>2</dt></span></span> </dl> | <span data-ttu-id="6f66b-289">已啟用</span><span class="sxs-lookup"><span data-stu-id="6f66b-289">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6f66b-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="6f66b-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-291">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f66b-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-293">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="6f66b-293">The current health of the element.</span></span> <span data-ttu-id="6f66b-294">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="6f66b-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="6f66b-295">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="6f66b-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="6f66b-296">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="6f66b-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="6f66b-297">值</span><span class="sxs-lookup"><span data-stu-id="6f66b-297">Value</span></span>                                                                        | <span data-ttu-id="6f66b-298">意義</span><span class="sxs-lookup"><span data-stu-id="6f66b-298">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="6f66b-299"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6f66b-299"><dt>5</dt></span></span> </dl> | <span data-ttu-id="6f66b-300">健全狀況狀態為 [正常]。</span><span class="sxs-lookup"><span data-stu-id="6f66b-300">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6f66b-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6f66b-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-302">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="6f66b-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-303">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-304">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="6f66b-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="6f66b-305">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="6f66b-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6f66b-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-307">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-309">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="6f66b-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-310">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="6f66b-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="6f66b-311">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="6f66b-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-312">**名稱**</span><span class="sxs-lookup"><span data-stu-id="6f66b-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-313">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-315">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="6f66b-315">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-316">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="6f66b-316">The label by which the object is known.</span></span> <span data-ttu-id="6f66b-317">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "vmms"。</span><span class="sxs-lookup"><span data-stu-id="6f66b-317">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-318">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="6f66b-318">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-319">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f66b-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-321">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6f66b-321">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="6f66b-322">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="6f66b-322">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f66b-323">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="6f66b-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6f66b-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6f66b-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="6f66b-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="6f66b-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="6f66b-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="6f66b-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="6f66b-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="6f66b-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="6f66b-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="6f66b-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="6f66b-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="6f66b-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="6f66b-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="6f66b-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="6f66b-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="6f66b-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="6f66b-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="6f66b-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="6f66b-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="6f66b-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6f66b-343">)</span><span class="sxs-lookup"><span data-stu-id="6f66b-343">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f66b-344">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="6f66b-344">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-345">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="6f66b-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-347">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="6f66b-347">The current statuses of the object.</span></span> <span data-ttu-id="6f66b-348">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="6f66b-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-349">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="6f66b-349">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-350">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-352">描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="6f66b-352">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="6f66b-353">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="6f66b-353">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="6f66b-354">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f66b-354">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-355">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="6f66b-355">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-356">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-357">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-358">限定詞： **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="6f66b-358">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-359">有關如何聯繫服務主要擁有者的任何資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="6f66b-359">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="6f66b-360">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f66b-360">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-361">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="6f66b-361">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-362">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-364">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="6f66b-364">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-365">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="6f66b-365">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="6f66b-366">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="6f66b-366">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="6f66b-367">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f66b-367">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-368">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="6f66b-368">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-369">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f66b-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-371">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="6f66b-371">Provides high level status information.</span></span> <span data-ttu-id="6f66b-372">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="6f66b-372">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="6f66b-373">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="6f66b-373">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="6f66b-374">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="6f66b-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="6f66b-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="6f66b-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-376"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="6f66b-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="6f66b-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="6f66b-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="6f66b-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="6f66b-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="6f66b-381">)</span><span class="sxs-lookup"><span data-stu-id="6f66b-381">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6f66b-382">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="6f66b-382">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-383">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f66b-383">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-384">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-385">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="6f66b-385">The last requested or desired state for the element.</span></span> <span data-ttu-id="6f66b-386">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="6f66b-386">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="6f66b-387">系統會提供這個屬性來比較專案的最後一個要求和目前狀態。</span><span class="sxs-lookup"><span data-stu-id="6f66b-387">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="6f66b-388">[**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))類別的特定實例可能不支援 **RequestedState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6f66b-388">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="6f66b-389">如果發生這種情況，則會使用值 12 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="6f66b-389">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="6f66b-390">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="6f66b-390">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="6f66b-391">值</span><span class="sxs-lookup"><span data-stu-id="6f66b-391">Value</span></span>                                                                         | <span data-ttu-id="6f66b-392">意義</span><span class="sxs-lookup"><span data-stu-id="6f66b-392">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="6f66b-393"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="6f66b-393"><dt>12</dt></span></span> </dl> | <span data-ttu-id="6f66b-394">不適用。</span><span class="sxs-lookup"><span data-stu-id="6f66b-394">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6f66b-395">**已開始**</span><span class="sxs-lookup"><span data-stu-id="6f66b-395">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-396">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6f66b-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-397">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-398">指出服務目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="6f66b-398">Indicates whether the service is currently running.</span></span> <span data-ttu-id="6f66b-399">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="6f66b-399">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-400">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="6f66b-400">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-401">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-402">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-403">限定詞： **MaxLen** ( 10 ) </span><span class="sxs-lookup"><span data-stu-id="6f66b-403">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-404">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="6f66b-404">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="6f66b-405">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f66b-405">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-406">**狀態**</span><span class="sxs-lookup"><span data-stu-id="6f66b-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-407">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-408">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-409">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="6f66b-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-410">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6f66b-410">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-411">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="6f66b-411">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-412">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-413">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="6f66b-413">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="6f66b-414">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為「服務正在正常執行」。</span><span class="sxs-lookup"><span data-stu-id="6f66b-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-415">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6f66b-415">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-416">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-417">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-418">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="6f66b-418">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-419">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="6f66b-419">The scoping system's creation class name.</span></span> <span data-ttu-id="6f66b-420">這個屬性是從 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)繼承而來的，而且一律設定為「Msvm 的程式集」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6f66b-420">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-421">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="6f66b-421">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-422">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6f66b-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-423">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-424">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="6f66b-424">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-425">主控電腦系統的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="6f66b-425">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="6f66b-426">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="6f66b-426">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-427">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="6f66b-427">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-428">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="6f66b-428">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-430">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="6f66b-430">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="6f66b-431">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6f66b-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="6f66b-432">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="6f66b-432">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f66b-433">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="6f66b-433">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-434">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="6f66b-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6f66b-435">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="6f66b-435">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="6f66b-436">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6f66b-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f66b-437">備註</span><span class="sxs-lookup"><span data-stu-id="6f66b-437">Remarks</span></span>

<span data-ttu-id="6f66b-438">存取 **Msvm \_ VirtualSystemManagementService** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="6f66b-438">Access to the **Msvm\_VirtualSystemManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6f66b-439">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="6f66b-439">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f66b-440">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f66b-440">Requirements</span></span>



| <span data-ttu-id="6f66b-441">需求</span><span class="sxs-lookup"><span data-stu-id="6f66b-441">Requirement</span></span> | <span data-ttu-id="6f66b-442">值</span><span class="sxs-lookup"><span data-stu-id="6f66b-442">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f66b-443">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f66b-443">Minimum supported client</span></span><br/> | <span data-ttu-id="6f66b-444">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f66b-444">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6f66b-445">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f66b-445">Minimum supported server</span></span><br/> | <span data-ttu-id="6f66b-446">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f66b-446">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f66b-447">命名空間</span><span class="sxs-lookup"><span data-stu-id="6f66b-447">Namespace</span></span><br/>                | <span data-ttu-id="6f66b-448">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="6f66b-448">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6f66b-449">MOF</span><span class="sxs-lookup"><span data-stu-id="6f66b-449">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f66b-450"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6f66b-450"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f66b-451">DLL</span><span class="sxs-lookup"><span data-stu-id="6f66b-451">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f66b-452"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f66b-452"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6f66b-453">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f66b-453">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f66b-454">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6f66b-454">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="6f66b-455">[**CIM \_ VirtualSystemManagementService**](/previous-versions//cc136952(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6f66b-455">[**CIM\_VirtualSystemManagementService**](/previous-versions//cc136952(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6f66b-456">[**Msvm \_ VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6f66b-456">[**Msvm\_VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6f66b-457">虛擬系統管理類別</span><span class="sxs-lookup"><span data-stu-id="6f66b-457">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

