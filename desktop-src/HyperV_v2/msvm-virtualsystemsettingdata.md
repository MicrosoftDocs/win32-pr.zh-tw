---
description: 代表虛擬機器的虛擬化特定設定。
ms.assetid: BE81405E-E773-41CE-9441-33D60B63550E
title: Msvm_VirtualSystemSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingData
- Msvm_VirtualSystemSettingData.InstanceID
- Msvm_VirtualSystemSettingData.Caption
- Msvm_VirtualSystemSettingData.Description
- Msvm_VirtualSystemSettingData.ElementName
- Msvm_VirtualSystemSettingData.VirtualSystemIdentifier
- Msvm_VirtualSystemSettingData.VirtualSystemType
- Msvm_VirtualSystemSettingData.Notes
- Msvm_VirtualSystemSettingData.CreationTime
- Msvm_VirtualSystemSettingData.ConfigurationID
- Msvm_VirtualSystemSettingData.ConfigurationDataRoot
- Msvm_VirtualSystemSettingData.ConfigurationFile
- Msvm_VirtualSystemSettingData.SnapshotDataRoot
- Msvm_VirtualSystemSettingData.SuspendDataRoot
- Msvm_VirtualSystemSettingData.SwapFileDataRoot
- Msvm_VirtualSystemSettingData.LogDataRoot
- Msvm_VirtualSystemSettingData.AutomaticStartupAction
- Msvm_VirtualSystemSettingData.AutomaticStartupActionDelay
- Msvm_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualSystemSettingData.AutomaticShutdownAction
- Msvm_VirtualSystemSettingData.AutomaticRecoveryAction
- Msvm_VirtualSystemSettingData.RecoveryFile
- Msvm_VirtualSystemSettingData.BIOSGUID
- Msvm_VirtualSystemSettingData.BIOSSerialNumber
- Msvm_VirtualSystemSettingData.BaseBoardSerialNumber
- Msvm_VirtualSystemSettingData.ChassisSerialNumber
- Msvm_VirtualSystemSettingData.Architecture
- Msvm_VirtualSystemSettingData.ChassisAssetTag
- Msvm_VirtualSystemSettingData.BIOSNumLock
- Msvm_VirtualSystemSettingData.BootOrder
- Msvm_VirtualSystemSettingData.Parent
- Msvm_VirtualSystemSettingData.UserSnapshotType
- Msvm_VirtualSystemSettingData.IsSaved
- Msvm_VirtualSystemSettingData.AdditionalRecoveryInformation
- Msvm_VirtualSystemSettingData.AllowFullSCSICommandSet
- Msvm_VirtualSystemSettingData.DebugChannelId
- Msvm_VirtualSystemSettingData.DebugPortEnabled
- Msvm_VirtualSystemSettingData.DebugPort
- Msvm_VirtualSystemSettingData.Version
- Msvm_VirtualSystemSettingData.IncrementalBackupEnabled
- Msvm_VirtualSystemSettingData.VirtualNumaEnabled
- Msvm_VirtualSystemSettingData.AllowReducedFcRedundancy
- Msvm_VirtualSystemSettingData.VirtualSystemSubType
- Msvm_VirtualSystemSettingData.BootSourceOrder
- Msvm_VirtualSystemSettingData.PauseAfterBootFailure
- Msvm_VirtualSystemSettingData.NetworkBootPreferredProtocol
- Msvm_VirtualSystemSettingData.GuestControlledCacheTypes
- Msvm_VirtualSystemSettingData.AutomaticSnapshotsEnabled
- Msvm_VirtualSystemSettingData.IsAutomaticSnapshot
- Msvm_VirtualSystemSettingData.GuestStateFile
- Msvm_VirtualSystemSettingData.GuestStateDataRoot
- Msvm_VirtualSystemSettingData.LockOnDisconnect
- Msvm_VirtualSystemSettingData.ParentPackage
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorActionTimeout
- Msvm_VirtualSystemSettingData.AutomaticCriticalErrorAction
- Msvm_VirtualSystemSettingData.ConsoleMode
- Msvm_VirtualSystemSettingData.SecureBootEnabled
- Msvm_VirtualSystemSettingData.SecureBootTemplateId
- Msvm_VirtualSystemSettingData.LowMmioGapSize
- Msvm_VirtualSystemSettingData.HighMmioGapSize
- Msvm_VirtualSystemSettingData.EnhancedSessionTransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2787abbacfe4220b135544eecd3aeb7e86596c81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936649"
---
# <a name="msvm_virtualsystemsettingdata-class"></a><span data-ttu-id="56460-103">Msvm \_ VirtualSystemSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="56460-103">Msvm\_VirtualSystemSettingData class</span></span>

<span data-ttu-id="56460-104">代表虛擬機器的虛擬化特定設定。</span><span class="sxs-lookup"><span data-stu-id="56460-104">Represents the virtualization-specific settings for a virtual machine.</span></span>

<span data-ttu-id="56460-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="56460-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="56460-106">語法</span><span class="sxs-lookup"><span data-stu-id="56460-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID;
  string   Caption = "Virtual Machine Settings";
  string   Description;
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   Architecture;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
  string   Parent;
  uint16   UserSnapshotType;
  boolean  IsSaved;
  string   AdditionalRecoveryInformation;
  boolean  AllowFullSCSICommandSet;
  uint32   DebugChannelId;
  uint16   DebugPortEnabled;
  uint32   DebugPort;
  string   Version;
  boolean  IncrementalBackupEnabled;
  boolean  VirtualNumaEnabled;
  boolean  AllowReducedFcRedundancy = False;
  string   VirtualSystemSubType;
  string   BootSourceOrder[];
  boolean  PauseAfterBootFailure;
  uint16   NetworkBootPreferredProtocol;
  boolean  GuestControlledCacheTypes;
  boolean  AutomaticSnapshotsEnabled;
  boolean  IsAutomaticSnapshot;
  string   GuestStateFile;
  string   GuestStateDataRoot;
  boolean  LockOnDisconnect;
  string   ParentPackage;
  datetime AutomaticCriticalErrorActionTimeout;
  uint16   AutomaticCriticalErrorAction;
  uint16   ConsoleMode;
  boolean  SecureBootEnabled;
  string   SecureBootTemplateId;
  uint64   LowMmioGapSize;
  uint64   HighMmioGapSize;
  uint16   EnhancedSessionTransportType;
};
```

## <a name="members"></a><span data-ttu-id="56460-107">成員</span><span class="sxs-lookup"><span data-stu-id="56460-107">Members</span></span>

<span data-ttu-id="56460-108">**Msvm \_ VirtualSystemSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="56460-108">The **Msvm\_VirtualSystemSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="56460-109">屬性</span><span class="sxs-lookup"><span data-stu-id="56460-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="56460-110">屬性</span><span class="sxs-lookup"><span data-stu-id="56460-110">Properties</span></span>

<span data-ttu-id="56460-111">**Msvm \_ VirtualSystemSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="56460-111">The **Msvm\_VirtualSystemSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56460-112">**AdditionalRecoveryInformation**</span><span class="sxs-lookup"><span data-stu-id="56460-112">**AdditionalRecoveryInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-115">針對復原動作提供的任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="56460-115">Any additional information provided to the recovery action.</span></span> <span data-ttu-id="56460-116">這個屬性的意義是由 **AutomaticRecoveryAction** 中的動作所定義。</span><span class="sxs-lookup"><span data-stu-id="56460-116">The meaning of this property is defined by the action in **AutomaticRecoveryAction**.</span></span> <span data-ttu-id="56460-117">如果 **AutomaticRecoveryAction** 為 0 ( 「無」 ) 或 1 ( 「重新開機」 ) ，則此值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="56460-117">If **AutomaticRecoveryAction** is 0 ("None") or 1 ("Restart"), this value is **Null**.</span></span> <span data-ttu-id="56460-118">如果 **AutomaticRecoveryAction** 為 2 ( 「還原為快照集」 ) ，這就是在虛擬機器工作者進程失敗時應套用的快照集的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-118">If **AutomaticRecoveryAction** is 2 ("Revert to Snapshot"), this is the object path to a snapshot that should be applied on failure of the virtual machine worker process.</span></span>

</dd> <dt>

<span data-ttu-id="56460-119">**AllowFullSCSICommandSet**</span><span class="sxs-lookup"><span data-stu-id="56460-119">**AllowFullSCSICommandSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-120">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-122">如果從客體作業系統的 SCSI 命令傳遞至傳遞磁片，**則為 True** 。否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="56460-122">**True** if SCSI commands from the guest operating system are passed to pass-through disks; otherwise, **False**.</span></span> <span data-ttu-id="56460-123">若 **為 True**，則不會篩選由客體作業系統向傳遞磁片發出的 SCSI 命令。</span><span class="sxs-lookup"><span data-stu-id="56460-123">If **True**, SCSI commands emitted by the guest operating system to pass-through disks are not filtered.</span></span> <span data-ttu-id="56460-124">我們建議在生產環境部署中維持 SCSI 篩選功能。</span><span class="sxs-lookup"><span data-stu-id="56460-124">We recommend that SCSI filtering remain enabled for production deployments.</span></span>

</dd> <dt>

<span data-ttu-id="56460-125">**AllowReducedFcRedundancy**</span><span class="sxs-lookup"><span data-stu-id="56460-125">**AllowReducedFcRedundancy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-126">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-128">指定是否允許以虛擬光纖通道介面卡設定的虛擬機器進行即時移轉至目的地電腦，該目的地電腦的目標光纖通道裝置可能沒有或減少路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-128">Specifies whether live migration of a virtual machine that is configured with a virtual Fibre Channel adapter is allowed to a destination computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="56460-129">這個屬性應該在即時移轉後清除。</span><span class="sxs-lookup"><span data-stu-id="56460-129">This property should be cleared after a live migration.</span></span>



| <span data-ttu-id="56460-130">值</span><span class="sxs-lookup"><span data-stu-id="56460-130">Value</span></span>                                                                            | <span data-ttu-id="56460-131">意義</span><span class="sxs-lookup"><span data-stu-id="56460-131">Meaning</span></span>                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56460-132"><dt>False</dt></span><span class="sxs-lookup"><span data-stu-id="56460-132"><dt>False</dt></span></span> </dl> | <span data-ttu-id="56460-133">虛擬機器無法即時移轉到目的電腦上，目標光纖通道裝置可能沒有或減少路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-133">The virtual machine cannot be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="56460-134"><dt>True</dt></span><span class="sxs-lookup"><span data-stu-id="56460-134"><dt>True</dt></span></span> </dl>  | <span data-ttu-id="56460-135">虛擬機器可以即時移轉至目的電腦，而目的電腦的目標光纖通道裝置可能沒有或減少路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-135">The virtual machine can be live migrated to a target computer that may have no or reduced paths to the target Fibre Channel devices.</span></span> <span data-ttu-id="56460-136">客體作業系統可能會中斷與儲存體的連線，而且可能會以無法預期的方式運作。</span><span class="sxs-lookup"><span data-stu-id="56460-136">The guest operating system may lose connectivity to storage and may behave in an unpredictable manner.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="56460-137">**架構**</span><span class="sxs-lookup"><span data-stu-id="56460-137">**Architecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-139">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-140">此系統的架構。</span><span class="sxs-lookup"><span data-stu-id="56460-140">The architecture of this system.</span></span>

> [!Note]  
> <span data-ttu-id="56460-141">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-141">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="x64"></span><span id="X64"></span>

<span data-ttu-id="56460-142">**x64** () </span><span class="sxs-lookup"><span data-stu-id="56460-142">**x64** ()</span></span>


</dt> <dd></dd> <dt>

<span id="arm64"></span><span id="ARM64"></span>

<span data-ttu-id="56460-143">**arm64** () </span><span class="sxs-lookup"><span data-stu-id="56460-143">**arm64** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56460-144">**AutomaticCriticalErrorAction**</span><span class="sxs-lookup"><span data-stu-id="56460-144">**AutomaticCriticalErrorAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-145">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="56460-145">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56460-146">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-147">識別當發生重大錯誤（例如儲存體中斷連線）時，要在 VM 上採取的動作。</span><span class="sxs-lookup"><span data-stu-id="56460-147">Identifies the action to be taken on VM, when a critical error happens, like storage disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="56460-148">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-148">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="56460-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (0) </span><span class="sxs-lookup"><span data-stu-id="56460-149"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (0)</span></span>


</dt> <dd>

<span data-ttu-id="56460-150">對於重大錯誤狀況，並不會採取任何特定動作。</span><span class="sxs-lookup"><span data-stu-id="56460-150">No specific action will be taken for critical error conditions.</span></span>

</dd> <dt>

<span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>

<span data-ttu-id="56460-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**暫停繼續** (1) </span><span class="sxs-lookup"><span data-stu-id="56460-151"><span id="Pause_Resume"></span><span id="pause_resume"></span><span id="PAUSE_RESUME"></span>**Pause Resume** (1)</span></span>


</dt> <dd>

<span data-ttu-id="56460-152">導致 VM 暫停，並在嚴重錯誤狀況解決時自動繼續。</span><span class="sxs-lookup"><span data-stu-id="56460-152">Causes the VM to be paused and automatically resumed when the critical error condition is resolved.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56460-153">**AutomaticCriticalErrorActionTimeout**</span><span class="sxs-lookup"><span data-stu-id="56460-153">**AutomaticCriticalErrorActionTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-154">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="56460-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="56460-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="56460-156">限定詞： [**子類型**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( "interval" ) </span><span class="sxs-lookup"><span data-stu-id="56460-156">Qualifiers: [**SubType**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("interval")</span></span>
</dt> </dl>

<span data-ttu-id="56460-157">識別將執行 **AutomaticCriticalErrorAction** 以解決重大錯誤的最長持續時間。</span><span class="sxs-lookup"><span data-stu-id="56460-157">Identifies the maximum duration for which the **AutomaticCriticalErrorAction** will be performed to resolve the critical error.</span></span> <span data-ttu-id="56460-158">只有當 **AutomaticCriticalErrorAction** 屬性的值不是 0 (無) 時，才適用這種情況。</span><span class="sxs-lookup"><span data-stu-id="56460-158">This is applicable only when the value of the **AutomaticCriticalErrorAction** property is not 0 (None).</span></span> <span data-ttu-id="56460-159">當超時時間過期時，VM 將會關閉電源。</span><span class="sxs-lookup"><span data-stu-id="56460-159">Once the timeout expires, the VM will be powered off.</span></span> <span data-ttu-id="56460-160">此值會無條件進位到最接近的分鐘數。</span><span class="sxs-lookup"><span data-stu-id="56460-160">The value will be rounded up to the nearest minute.</span></span> <span data-ttu-id="56460-161">值為0表示 VM 應該在遇到重大錯誤狀況時立即關閉電源。</span><span class="sxs-lookup"><span data-stu-id="56460-161">A value of 0 implies that the VM should be powered off immediately when it encounters a critical error condition.</span></span>

> [!Note]  
> <span data-ttu-id="56460-162">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-162">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="56460-163">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="56460-163">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-164">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="56460-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56460-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-166">當虛擬機器執行的軟體失敗時，針對虛擬機器所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="56460-166">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="56460-167">在此情況下，失敗表示主機平臺偵測到失敗，例如不可中斷等候狀態條件。</span><span class="sxs-lookup"><span data-stu-id="56460-167">Failures in this case means a failure that is detectable by the host platform, such as a noninterruptible wait state condition.</span></span> <span data-ttu-id="56460-168">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="56460-169">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="56460-169">This can be one of the following values.</span></span>



| <span data-ttu-id="56460-170">值</span><span class="sxs-lookup"><span data-stu-id="56460-170">Value</span></span>                                                                               | <span data-ttu-id="56460-171">意義</span><span class="sxs-lookup"><span data-stu-id="56460-171">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="56460-172"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="56460-172"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="56460-173">無。</span><span class="sxs-lookup"><span data-stu-id="56460-173">None.</span></span><br/>               |
| <dl> <span data-ttu-id="56460-174"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="56460-174"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="56460-175">重新啟動。</span><span class="sxs-lookup"><span data-stu-id="56460-175">Restart.</span></span><br/>            |
| <dl> <span data-ttu-id="56460-176"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="56460-176"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="56460-177">還原為快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-177">Revert to snapshot.</span></span><br/> |
| <dl> <span data-ttu-id="56460-178"><dt>5. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="56460-178"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="56460-179">保留的。</span><span class="sxs-lookup"><span data-stu-id="56460-179">Reserved.</span></span><br/>           |



 

</dd> <dt>

<span data-ttu-id="56460-180">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="56460-180">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-181">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="56460-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56460-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-183">當主機關閉時，為虛擬機器採取的動作。</span><span class="sxs-lookup"><span data-stu-id="56460-183">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="56460-184">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-184">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="56460-185">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="56460-185">This can be one of the following values.</span></span>



| <span data-ttu-id="56460-186">值</span><span class="sxs-lookup"><span data-stu-id="56460-186">Value</span></span>                                                                               | <span data-ttu-id="56460-187">意義</span><span class="sxs-lookup"><span data-stu-id="56460-187">Meaning</span></span>                |
|-------------------------------------------------------------------------------------|------------------------|
| <dl> <span data-ttu-id="56460-188"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="56460-188"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="56460-189">關閉。</span><span class="sxs-lookup"><span data-stu-id="56460-189">Turn off.</span></span><br/>   |
| <dl> <span data-ttu-id="56460-190"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="56460-190"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="56460-191">儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="56460-191">Save state.</span></span><br/> |
| <dl> <span data-ttu-id="56460-192"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="56460-192"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="56460-193">關機。</span><span class="sxs-lookup"><span data-stu-id="56460-193">Shutdown.</span></span><br/>   |
| <dl> <span data-ttu-id="56460-194"><dt>5. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="56460-194"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="56460-195">保留的。</span><span class="sxs-lookup"><span data-stu-id="56460-195">Reserved.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="56460-196">**AutomaticSnapshotsEnabled**</span><span class="sxs-lookup"><span data-stu-id="56460-196">**AutomaticSnapshotsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-197">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-197">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-198">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-198">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-199">指出此虛擬機器是否應啟用自動快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-199">Indicates whether this virtual machine should have automatic snapshots enabled.</span></span>

> [!Note]  
> <span data-ttu-id="56460-200">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-200">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="56460-201">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="56460-201">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-202">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="56460-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56460-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-204">當主機啟動時，對虛擬機器採取的動作。</span><span class="sxs-lookup"><span data-stu-id="56460-204">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="56460-205">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-205">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="56460-206">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="56460-206">This can be one of the following values.</span></span>



| <span data-ttu-id="56460-207">值</span><span class="sxs-lookup"><span data-stu-id="56460-207">Value</span></span>                                                                               | <span data-ttu-id="56460-208">意義</span><span class="sxs-lookup"><span data-stu-id="56460-208">Meaning</span></span>                                  |
|-------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="56460-209"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="56460-209"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="56460-210">無。</span><span class="sxs-lookup"><span data-stu-id="56460-210">None.</span></span><br/>                         |
| <dl> <span data-ttu-id="56460-211"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="56460-211"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="56460-212">如果之前為作用中，則重新開機。</span><span class="sxs-lookup"><span data-stu-id="56460-212">Restart if previously active.</span></span><br/> |
| <dl> <span data-ttu-id="56460-213"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="56460-213"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="56460-214">永遠啟動。</span><span class="sxs-lookup"><span data-stu-id="56460-214">Always start.</span></span><br/>                 |
| <dl> <span data-ttu-id="56460-215"><dt>5. 32768</dt></span><span class="sxs-lookup"><span data-stu-id="56460-215"><dt>5..32768</dt></span></span> </dl> | <span data-ttu-id="56460-216">保留的。</span><span class="sxs-lookup"><span data-stu-id="56460-216">Reserved.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="56460-217">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="56460-217">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-218">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="56460-218">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="56460-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-220">虛擬機器自動啟動之前的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="56460-220">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="56460-221">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-221">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-222">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="56460-222">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-223">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="56460-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56460-224">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-224">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-225">數位，指出主機系統啟動時的虛擬機器啟用的相對順序。</span><span class="sxs-lookup"><span data-stu-id="56460-225">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="56460-226">較低的數位表示先前的啟用。</span><span class="sxs-lookup"><span data-stu-id="56460-226">A lower number indicates earlier activation.</span></span> <span data-ttu-id="56460-227">如果有一或多個設定顯示相同的值，則序列會相依。</span><span class="sxs-lookup"><span data-stu-id="56460-227">If one or more configurations show the same value, the sequence is implementation dependent.</span></span> <span data-ttu-id="56460-228">值為0時，表示序列與實值相依。</span><span class="sxs-lookup"><span data-stu-id="56460-228">A value of 0 indicates that the sequence is implementation dependent.</span></span> <span data-ttu-id="56460-229">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-229">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-230">**BaseBoardSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="56460-230">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-233">虛擬機器基本板的序號。</span><span class="sxs-lookup"><span data-stu-id="56460-233">The serial number of the base board for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="56460-234">**BIOSGUID**</span><span class="sxs-lookup"><span data-stu-id="56460-234">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-236">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-237">虛擬機器之 BIOS 的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="56460-237">The globally unique identifier for the BIOS of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="56460-238">**BIOSNumLock**</span><span class="sxs-lookup"><span data-stu-id="56460-238">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-239">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-240">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-241">如果 BIOS 將 num lock 鍵設為 on，則為 **True** ;如果 BIOS 將 num lock 鍵設定為 off，則 **為 False** 。</span><span class="sxs-lookup"><span data-stu-id="56460-241">**True** if the num lock key is set to on by the BIOS; **False** if the num lock key is set to off by the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="56460-242">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="56460-242">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-243">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-244">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-245">虛擬機器之 BIOS 的序號。</span><span class="sxs-lookup"><span data-stu-id="56460-245">The serial number of the BIOS for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="56460-246">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="56460-246">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-247">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="56460-247">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="56460-248">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-248">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="56460-249">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**最大**](/windows/desktop/WmiSdk/standard-qualifiers) (4) </span><span class="sxs-lookup"><span data-stu-id="56460-249">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="56460-250">在虛擬機器的 BIOS 內設定的開機順序。</span><span class="sxs-lookup"><span data-stu-id="56460-250">The boot order set within the BIOS of the virtual machine.</span></span> <span data-ttu-id="56460-251">這個屬性是值的陣列， **BootOrder** \[ 0 \] 到 **BootOrder** \[ 3 （含）， \] 其中每個值表示要開機的裝置。</span><span class="sxs-lookup"><span data-stu-id="56460-251">This property is an array of values, **BootOrder**\[0\] through **BootOrder**\[3\], inclusive, where each value indicates a device to boot from.</span></span> <span data-ttu-id="56460-252">陣列中的每個值都必須設定，而且不得與陣列中的另一個值相同。</span><span class="sxs-lookup"><span data-stu-id="56460-252">Each of the 4 values in the array must be set and must not be the same as another value in the array.</span></span> <span data-ttu-id="56460-253">虛擬機器將會先嘗試從陣列中第一個值所指示的裝置開機。</span><span class="sxs-lookup"><span data-stu-id="56460-253">The virtual machine will first attempt to boot from the device indicated by the first value within the array.</span></span> <span data-ttu-id="56460-254">如果該裝置不包含開機磁區，虛擬機器將會嘗試從 **BootOrder** 屬性所指定的下一個裝置開機，依此類推。</span><span class="sxs-lookup"><span data-stu-id="56460-254">If that device does not contain a boot sector, the virtual machine will attempt to boot from the next device specified by the **BootOrder** property and so on.</span></span> <span data-ttu-id="56460-255">如果 **BootOrder** 中未指定任何裝置包含開機磁區，則虛擬機器將無法開機。</span><span class="sxs-lookup"><span data-stu-id="56460-255">If no device specified within the **BootOrder** contains a boot sector the virtual machine will fail to boot.</span></span> <span data-ttu-id="56460-256">虛擬機器的預設值為 \[ 0、1、2、3 \] 。</span><span class="sxs-lookup"><span data-stu-id="56460-256">The default value for a virtual machine is \[0, 1, 2, 3\].</span></span>

<dt>

<span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>

<span data-ttu-id="56460-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**軟盤機** (0) </span><span class="sxs-lookup"><span data-stu-id="56460-257"><span id="Floppy"></span><span id="floppy"></span><span id="FLOPPY"></span>**Floppy** (0)</span></span>


</dt> <dd>

<span data-ttu-id="56460-258">虛擬機器會嘗試從磁片磁碟機中的磁片磁碟機開機。</span><span class="sxs-lookup"><span data-stu-id="56460-258">The virtual machine will attempt to boot from the floppy disk within the floppy drive.</span></span>

</dd> <dt>

<span id="CD-ROM"></span><span id="cd-rom"></span>

<span data-ttu-id="56460-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**Cd-rom** (1) </span><span class="sxs-lookup"><span data-stu-id="56460-259"><span id="CD-ROM"></span><span id="cd-rom"></span>**CD-ROM** (1)</span></span>


</dt> <dd>

<span data-ttu-id="56460-260">虛擬機器會嘗試從第一部 CD 或以開機磁區找到的 DVD 磁片開機。</span><span class="sxs-lookup"><span data-stu-id="56460-260">The virtual machine will attempt to boot from the first CD or DVD disk found with a boot sector.</span></span>

</dd> <dt>

<span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>

<span data-ttu-id="56460-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE 硬碟** (2) </span><span class="sxs-lookup"><span data-stu-id="56460-261"><span id="IDE_Hard_Drive"></span><span id="ide_hard_drive"></span><span id="IDE_HARD_DRIVE"></span>**IDE Hard Drive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="56460-262">虛擬機器會嘗試從開機磁區所找到的第一個硬碟機開機。</span><span class="sxs-lookup"><span data-stu-id="56460-262">The virtual machine will attempt to boot from the first hard disk drive found with a boot sector.</span></span>

</dd> <dt>

<span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>

<span data-ttu-id="56460-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE 開機** (3) </span><span class="sxs-lookup"><span data-stu-id="56460-263"><span id="PXE_Boot"></span><span id="pxe_boot"></span><span id="PXE_BOOT"></span>**PXE Boot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="56460-264">虛擬機器會嘗試從網路進行 PXE 開機。</span><span class="sxs-lookup"><span data-stu-id="56460-264">The virtual machine will attempt to PXE boot from the network.</span></span>

</dd> <dt>

<span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>

<span data-ttu-id="56460-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI 硬碟** (4) </span><span class="sxs-lookup"><span data-stu-id="56460-265"><span id="SCSI_Hard_Drive"></span><span id="scsi_hard_drive"></span><span id="SCSI_HARD_DRIVE"></span>**SCSI Hard Drive** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="56460-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**保留** (5. 65535) </span><span class="sxs-lookup"><span data-stu-id="56460-266"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (5..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56460-267">**BootSourceOrder**</span><span class="sxs-lookup"><span data-stu-id="56460-267">**BootSourceOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-268">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="56460-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="56460-269">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-270">虛擬機器的開機來源順序。</span><span class="sxs-lookup"><span data-stu-id="56460-270">The boot source order for the virtual machine.</span></span>

<span data-ttu-id="56460-271">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="56460-271">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="56460-272">**標題**</span><span class="sxs-lookup"><span data-stu-id="56460-272">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-274">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-275">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="56460-275">A short description of the object.</span></span> <span data-ttu-id="56460-276">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="56460-276">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="56460-277">**ChassisAssetTag**</span><span class="sxs-lookup"><span data-stu-id="56460-277">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-278">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-279">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-279">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-280">虛擬機器底座的資產標記。</span><span class="sxs-lookup"><span data-stu-id="56460-280">The asset tag of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="56460-281">**ChassisSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="56460-281">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-283">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-283">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-284">虛擬機器底座的序號。</span><span class="sxs-lookup"><span data-stu-id="56460-284">The serial number of the chassis for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="56460-285">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="56460-285">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-288">儲存虛擬機器設定相關資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-288">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="56460-289">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-290">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="56460-290">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-291">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-293">儲存虛擬機器設定相關資訊之檔案的相對路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="56460-293">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="56460-294">此路徑相對於 **ConfigurationDataRoot** 屬性。</span><span class="sxs-lookup"><span data-stu-id="56460-294">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="56460-295">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-295">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-296">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="56460-296">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-297">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-298">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-299">虛擬機器設定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="56460-299">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="56460-300">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-300">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-301">**ConsoleMode**</span><span class="sxs-lookup"><span data-stu-id="56460-301">**ConsoleMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-302">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="56460-302">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56460-303">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-303">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-304">識別 VM 的主控台模式。</span><span class="sxs-lookup"><span data-stu-id="56460-304">Identifies the Console Mode for the VM.</span></span>

> [!Note]  
> <span data-ttu-id="56460-305">這個屬性是在 Windows 10 和 Windows Server 2016 中新增的。</span><span class="sxs-lookup"><span data-stu-id="56460-305">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="56460-306">**預設** (0) </span><span class="sxs-lookup"><span data-stu-id="56460-306">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="COM1"></span><span id="com1"></span>

<span data-ttu-id="56460-307">**COM1** (1) </span><span class="sxs-lookup"><span data-stu-id="56460-307">**COM1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="COM2"></span><span id="com2"></span>

<span data-ttu-id="56460-308">**COM2** (2) </span><span class="sxs-lookup"><span data-stu-id="56460-308">**COM2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="56460-309">**無** (3) </span><span class="sxs-lookup"><span data-stu-id="56460-309">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56460-310">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="56460-310">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-311">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="56460-311">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="56460-312">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-313">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="56460-313">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="56460-314">如果此物件代表目前的虛擬機器設定，則此值會是系統建立的時間。</span><span class="sxs-lookup"><span data-stu-id="56460-314">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="56460-315">如果此物件代表虛擬機器的快照集設定，則此值會是拍攝快照集的時間。</span><span class="sxs-lookup"><span data-stu-id="56460-315">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="56460-316">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-316">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-317">**DebugChannelId**</span><span class="sxs-lookup"><span data-stu-id="56460-317">**DebugChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-318">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="56460-318">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56460-319">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-319">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-320">用來使用統一的偵錯工具來偵測虛擬機器的通道識別碼。</span><span class="sxs-lookup"><span data-stu-id="56460-320">The channel identifier used to debug the virtual machine using the unified debugger.</span></span>

</dd> <dt>

<span data-ttu-id="56460-321">**DebugPort**</span><span class="sxs-lookup"><span data-stu-id="56460-321">**DebugPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-322">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="56460-322">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="56460-323">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-323">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-324">用來使用綜合調試來偵測虛擬機器的 TCP/IP 通訊埠。</span><span class="sxs-lookup"><span data-stu-id="56460-324">The TCP/IP port used to debug the virtual machine using synthetic debugging.</span></span>

</dd> <dt>

<span data-ttu-id="56460-325">**DebugPortEnabled**</span><span class="sxs-lookup"><span data-stu-id="56460-325">**DebugPortEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-326">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="56460-326">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56460-327">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-327">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-328">指定虛擬機器是否正在使用綜合的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="56460-328">Specifies whether the virtual machine is using synthetic debugging.</span></span> <span data-ttu-id="56460-329">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="56460-329">This can be one of the following values.</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="56460-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Off** (0) </span><span class="sxs-lookup"><span data-stu-id="56460-330"><span id="Off"></span><span id="off"></span><span id="OFF"></span>**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="On"></span><span id="on"></span><span id="ON"></span>

<span data-ttu-id="56460-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**(1**) </span><span class="sxs-lookup"><span data-stu-id="56460-331"><span id="On"></span><span id="on"></span><span id="ON"></span>**On** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>

<span data-ttu-id="56460-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2) </span><span class="sxs-lookup"><span data-stu-id="56460-332"><span id="OnAutoAssigned"></span><span id="onautoassigned"></span><span id="ONAUTOASSIGNED"></span>**OnAutoAssigned** (2)</span></span>


</dt> <dd>

<span data-ttu-id="56460-333">自動指派</span><span class="sxs-lookup"><span data-stu-id="56460-333">Auto-assigned</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56460-334">**說明**</span><span class="sxs-lookup"><span data-stu-id="56460-334">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-335">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-337">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="56460-337">A description of the object.</span></span> <span data-ttu-id="56460-338">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="56460-338">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to one of the following values.</span></span>



| <span data-ttu-id="56460-339">值</span><span class="sxs-lookup"><span data-stu-id="56460-339">Value</span></span>                                                                                                                  | <span data-ttu-id="56460-340">意義</span><span class="sxs-lookup"><span data-stu-id="56460-340">Meaning</span></span>                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="56460-341"><dt>「虛擬機器的作用中設定」</dt></span><span class="sxs-lookup"><span data-stu-id="56460-341"><dt>"Active settings for the virtual machine"</dt></span></span> </dl>   | <span data-ttu-id="56460-342">此實例會參考虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="56460-342">This instance refers to a virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="56460-343"><dt>「虛擬機器的快照集設定」</dt></span><span class="sxs-lookup"><span data-stu-id="56460-343"><dt>"Snapshot settings for the virtual machine"</dt></span></span> </dl> | <span data-ttu-id="56460-344">此實例會參考快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-344">This instance refers to a snapshot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="56460-345">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="56460-345">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-346">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-347">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-348">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="56460-348">A display name for the object.</span></span> <span data-ttu-id="56460-349">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且一律設定為電腦的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="56460-349">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to the display name for the machine.</span></span> <span data-ttu-id="56460-350">此名稱的長度不得超過100個字元。</span><span class="sxs-lookup"><span data-stu-id="56460-350">This name may not exceed 100 characters in length.</span></span>

</dd> <dt>

<span data-ttu-id="56460-351">**EnhancedSessionTransportType**</span><span class="sxs-lookup"><span data-stu-id="56460-351">**EnhancedSessionTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-352">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="56460-352">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56460-353">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-353">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-354">表示連接到增強的會話時要使用的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="56460-354">Indicates the transport type to use when connecting to an enhanced session.</span></span>

> [!Note]  
> <span data-ttu-id="56460-355">這個屬性是在 Windows 10 1803 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="56460-355">This property was added in Windows 10, version 1803.</span></span>

 

<dt>

<span id="VMBus_Pipe"></span><span id="vmbus_pipe"></span><span id="VMBUS_PIPE"></span>

<span data-ttu-id="56460-356">**VMBus 管道** (0) </span><span class="sxs-lookup"><span data-stu-id="56460-356">**VMBus Pipe** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Hyper-V_Socket"></span><span id="hyper-v_socket"></span><span id="HYPER-V_SOCKET"></span>

<span data-ttu-id="56460-357">**Hyper-v 通訊端** (1) </span><span class="sxs-lookup"><span data-stu-id="56460-357">**Hyper-V Socket** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56460-358">**GuestControlledCacheTypes**</span><span class="sxs-lookup"><span data-stu-id="56460-358">**GuestControlledCacheTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-359">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-360">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-360">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-361">指出來賓是否可以控制快取類型。</span><span class="sxs-lookup"><span data-stu-id="56460-361">Indicates whether the guest can control cache types.</span></span>

> [!Note]  
> <span data-ttu-id="56460-362">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-362">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="56460-363">**GuestStateDataRoot**</span><span class="sxs-lookup"><span data-stu-id="56460-363">**GuestStateDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-364">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-365">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-365">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-366">儲存來賓執行時間狀態相關資訊之目錄的 Filepath。</span><span class="sxs-lookup"><span data-stu-id="56460-366">Filepath of a directory where information about the guest runtime state is stored.</span></span>

> [!Note]  
> <span data-ttu-id="56460-367">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-367">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="56460-368">**GuestStateFile**</span><span class="sxs-lookup"><span data-stu-id="56460-368">**GuestStateFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-369">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-370">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-371">儲存來賓執行時間狀態相關資訊之檔案的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-371">Filepath of a file where information about the guest runtime state is stored.</span></span> <span data-ttu-id="56460-372">相對路徑會附加至 **GuestStateDataRoot** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="56460-372">A relative path appends to the value of the **GuestStateDataRoot** property.</span></span>

> [!Note]  
> <span data-ttu-id="56460-373">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-373">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="56460-374">**HighMmioGapSize**</span><span class="sxs-lookup"><span data-stu-id="56460-374">**HighMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-375">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="56460-375">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="56460-376">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-376">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-377">高 (超過 4GB) Memory-Mapped IO 間隙（MB）的大小</span><span class="sxs-lookup"><span data-stu-id="56460-377">The size of the High (above 4GB) Memory-Mapped IO Gap in MB</span></span>

> [!Note]  
> <span data-ttu-id="56460-378">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="56460-378">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="56460-379">**IncrementalBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="56460-379">**IncrementalBackupEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-380">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-381">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-381">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-382">指出 Hyper-v VSS 寫入器是否支援採用此虛擬機器的增量備份。</span><span class="sxs-lookup"><span data-stu-id="56460-382">Indicates whether the Hyper-V VSS writer supports taking incremental backups of this virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="56460-383">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="56460-383">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-384">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-384">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-385">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56460-386">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="56460-386">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="56460-387">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="56460-387">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="56460-388">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-388">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-389">**IsAutomaticSnapshot**</span><span class="sxs-lookup"><span data-stu-id="56460-389">**IsAutomaticSnapshot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-390">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-391">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-392">指出這是否為使用者自動建立的快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-392">Indicates whether this is a snapshot created automatically for the user.</span></span>

> [!Note]  
> <span data-ttu-id="56460-393">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-393">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="56460-394">**IsSaved**</span><span class="sxs-lookup"><span data-stu-id="56460-394">**IsSaved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-395">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-396">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-397">如果設定具有已儲存狀態檔案的參考，則 **為 True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="56460-397">**True** if the configuration has a reference to a saved state file; otherwise, **False**.</span></span> <span data-ttu-id="56460-398">這並不表示這類檔案是否存在，只是設定會指定一個。</span><span class="sxs-lookup"><span data-stu-id="56460-398">This does not indicate the presence of such a file, only that the configuration specifies one.</span></span>

</dd> <dt>

<span data-ttu-id="56460-399">**LockOnDisconnect**</span><span class="sxs-lookup"><span data-stu-id="56460-399">**LockOnDisconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-400">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-401">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-401">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-402">中斷與 vmconnect 的連線時，請鎖定主控台。</span><span class="sxs-lookup"><span data-stu-id="56460-402">Lock the console when disconnecting from vmconnect.</span></span>

> [!Note]  
> <span data-ttu-id="56460-403">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-403">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="56460-404">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="56460-404">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-405">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-406">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-407">儲存虛擬機器記錄資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-407">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="56460-408">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-408">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-409">**LowMmioGapSize**</span><span class="sxs-lookup"><span data-stu-id="56460-409">**LowMmioGapSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-410">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="56460-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="56460-411">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-411">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-412">設定虛擬機器 (VM) 的第一個 MMIO 間距大小（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="56460-412">Configures the size, in megabytes, of the first MMIO gap for a virtual machine (VM).</span></span>

<span data-ttu-id="56460-413">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="56460-413">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<span data-ttu-id="56460-414">範圍： 128 3584</span><span class="sxs-lookup"><span data-stu-id="56460-414">Range: 128 3584</span></span>

</dd> <dt>

<span data-ttu-id="56460-415">**NetworkBootPreferredProtocol**</span><span class="sxs-lookup"><span data-stu-id="56460-415">**NetworkBootPreferredProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-416">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="56460-416">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56460-417">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-417">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-418">判斷 PXE 開機慣用的通訊協定是 IPv4 或 IPv6。</span><span class="sxs-lookup"><span data-stu-id="56460-418">Determines if the preferred protocol for PXE boot is IPv4 or IPv6.</span></span>

<span data-ttu-id="56460-419">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="56460-419">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="56460-420">**IPv4** (4096) </span><span class="sxs-lookup"><span data-stu-id="56460-420">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="56460-421">**IPv6** (4097) </span><span class="sxs-lookup"><span data-stu-id="56460-421">**IPv6** (4097)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56460-422">**注意事項**</span><span class="sxs-lookup"><span data-stu-id="56460-422">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-423">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="56460-423">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="56460-424">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-424">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-425">與虛擬機器相關的使用者提供的附注。</span><span class="sxs-lookup"><span data-stu-id="56460-425">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="56460-426">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-426">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-427">**父系**</span><span class="sxs-lookup"><span data-stu-id="56460-427">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-428">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-429">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-430">如果這個實例不是以虛擬機器的快照集為基礎的系統，則此屬性為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="56460-430">If this instance does not represent a system based on a snapshot of a virtual machine, this property is **Null**.</span></span> <span data-ttu-id="56460-431">否則，屬性會保存這個實例所依據之 **Msvm \_ VirtualSystemSettingData** 物件的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-431">Otherwise, the property holds the object path of the **Msvm\_VirtualSystemSettingData** object on which this instance is based.</span></span> <span data-ttu-id="56460-432">建立虛擬機器的快照集樹狀結構階層時，這個屬性會參考目前的實例所衍生的物件 (目前的實例是子節點，而且這個屬性中所參考的物件是父節點。 ) </span><span class="sxs-lookup"><span data-stu-id="56460-432">When building a snapshot tree hierarchy for the virtual machine, this property references the object from which the current instance is derived (the current instance is the child node and the object referenced in this property is the parent node.)</span></span>

</dd> <dt>

<span data-ttu-id="56460-433">**ParentPackage**</span><span class="sxs-lookup"><span data-stu-id="56460-433">**ParentPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-434">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-435">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-436">如果此系統為容器，則為 \_ 此系統所依據之 Msvm ContainerPackage 的路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-436">If this system is a container, the path to the Msvm\_ContainerPackage from which this system is based.</span></span>

> [!Note]  
> <span data-ttu-id="56460-437">新增于 Windows 10;已在 Windows 10 1703 版中移除。</span><span class="sxs-lookup"><span data-stu-id="56460-437">Added in Windows 10; removed in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="56460-438">**PauseAfterBootFailure**</span><span class="sxs-lookup"><span data-stu-id="56460-438">**PauseAfterBootFailure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-439">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-439">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-440">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-440">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-441">指出在每次開機專案失敗並等候使用者按下按鍵之後，BIOS 是否會暫停。</span><span class="sxs-lookup"><span data-stu-id="56460-441">Indicates whether the BIOS pauses after every boot entry failure waiting for the user to press a key.</span></span> <span data-ttu-id="56460-442">如果 BIOS 暫停，**則為 True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="56460-442">**True** if the BIOS pauses; otherwise, **False**.</span></span>

<span data-ttu-id="56460-443">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="56460-443">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="56460-444">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="56460-444">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-445">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-446">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-447">儲存虛擬機器修復相關資訊之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-447">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="56460-448">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-448">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-449">**SecureBootEnabled**</span><span class="sxs-lookup"><span data-stu-id="56460-449">**SecureBootEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-450">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-450">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-451">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-451">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-452">指出是否已啟用虛擬機器 (VM) 的安全開機。</span><span class="sxs-lookup"><span data-stu-id="56460-452">Indicates whether secure boot is enabled for the virtual machine (VM).</span></span> <span data-ttu-id="56460-453">如果已啟用，則 **為 True** ;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="56460-453">**True** if enabled; otherwise, **False**.</span></span>

> [!Note]  
> <span data-ttu-id="56460-454">只有第2代 Vm 才能啟用安全開機。</span><span class="sxs-lookup"><span data-stu-id="56460-454">Secure boot can only be enabled for generation 2 VMs.</span></span>

 

<span data-ttu-id="56460-455">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="56460-455">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="56460-456">**SecureBootTemplateId**</span><span class="sxs-lookup"><span data-stu-id="56460-456">**SecureBootTemplateId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-457">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-458">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-458">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-459">UEFI 安全開機相關變數的初始值之範本的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="56460-459">The globally-unique identifier of the template of intial values of UEFI Secure Boot related variables.</span></span>

<span data-ttu-id="56460-460">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="56460-460">This is a read-only property, but it can be changed using the [**ModifyVirtualSystem**](https://www.bing.com/search?q=**ModifyVirtualSystem**) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="56460-461">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-461">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="56460-462">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="56460-462">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-463">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-464">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-465">儲存虛擬機器快照集相關資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-465">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="56460-466">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-466">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-467">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="56460-467">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-468">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-469">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-469">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-470">儲存虛擬機器暫停相關資訊之相關資訊的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-470">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="56460-471">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-471">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-472">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="56460-472">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-473">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-473">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-474">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-474">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-475">儲存虛擬機器之交換檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="56460-475">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="56460-476">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="56460-476">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-477">**UserSnapshotType**</span><span class="sxs-lookup"><span data-stu-id="56460-477">**UserSnapshotType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-478">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="56460-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="56460-479">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-479">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="56460-480">表示使用者定義的快照集類型。</span><span class="sxs-lookup"><span data-stu-id="56460-480">Indicates the user-defined snapshot type.</span></span>

> [!Note]  
> <span data-ttu-id="56460-481">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="56460-481">Added in Windows 10 and Windows Server 2016.</span></span>

 

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="56460-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**停** 用 (2) </span><span class="sxs-lookup"><span data-stu-id="56460-482"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="56460-483">停用建立任何快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-483">Disable the creation of any snapshot.</span></span>

</dd> <dt>

<span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>

<span data-ttu-id="56460-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3) </span><span class="sxs-lookup"><span data-stu-id="56460-484"><span id="ProductionFallbackToTest"></span><span id="productionfallbacktotest"></span><span id="PRODUCTIONFALLBACKTOTEST"></span>**ProductionFallbackToTest** (3)</span></span>


</dt> <dd>

<span data-ttu-id="56460-485">要在生產環境中使用的資料一致性快照集。當無法使用建立資料一致快照集的功能時，執行具有應用程式狀態的快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-485">Data-consistent snapshot for use in the production environment.Performs a snapshot with application state when the ability to create data consistent snapshot is not available.</span></span>

</dd> <dt>

<span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>

<span data-ttu-id="56460-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4) </span><span class="sxs-lookup"><span data-stu-id="56460-486"><span id="ProductionNoFallback"></span><span id="productionnofallback"></span><span id="PRODUCTIONNOFALLBACK"></span>**ProductionNoFallback** (4)</span></span>


</dt> <dd>

<span data-ttu-id="56460-487">要在生產環境中使用的資料一致性快照集。如果無法建立資料一致的快照集，則不會建立具有應用程式狀態的快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-487">Data-consistent snapshot for use in the production environment.Does not create a snapshot with application state if it is not possible to create a data consistent snapshot.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="56460-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (5) </span><span class="sxs-lookup"><span data-stu-id="56460-488"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (5)</span></span>


</dt> <dd>

<span data-ttu-id="56460-489">包含適用于測試和開發用途之記憶體和裝置資訊的快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-489">Snapshot that contains memory and device information for test and development purpose.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="56460-490">**版本**</span><span class="sxs-lookup"><span data-stu-id="56460-490">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-491">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-492">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-492">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-493">虛擬機器的版本，格式為「主要. 次要」，例如 "2.0"。</span><span class="sxs-lookup"><span data-stu-id="56460-493">The version of the virtual machine in a format of "major.minor", for example "2.0".</span></span>

</dd> <dt>

<span data-ttu-id="56460-494">**VirtualNumaEnabled**</span><span class="sxs-lookup"><span data-stu-id="56460-494">**VirtualNumaEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-495">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="56460-495">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="56460-496">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="56460-496">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="56460-497">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**Msvm \_ ProcessorSettingData**](msvm-processorsettingdata.md)。**MaxProcessorsPerNumaNode**"，"[**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md)。**MaxMemoryBlocksPerNumaNode**") </span><span class="sxs-lookup"><span data-stu-id="56460-497">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ProcessorSettingData**](msvm-processorsettingdata.md).**MaxProcessorsPerNumaNode**", "[**Msvm\_MemorySettingData**](msvm-memorysettingdata.md).**MaxMemoryBlocksPerNumaNode**")</span></span>
</dt> </dl>

<span data-ttu-id="56460-498">如果虛擬的非統一記憶體存取 (NUMA) 節點投射到虛擬機器，則 **為 True** ;如果虛擬機器將會有單一節點，則 **為 False** 。</span><span class="sxs-lookup"><span data-stu-id="56460-498">**True** if virtual non-uniform memory access (NUMA) nodes are projected into the virtual machine; **False** if the virtual machine will have a single node.</span></span> <span data-ttu-id="56460-499">若 **為 True**，則會從 [**Msvm \_ ProcessorSettingData. MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) 和 [**Msvm \_ MemorySettingData. MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) 屬性的值判斷投影到虛擬機器的虛擬 NUMA 節點數目。</span><span class="sxs-lookup"><span data-stu-id="56460-499">If **True**, the number of virtual NUMA nodes projected into the virtual machine is determined from the values of the [**Msvm\_ProcessorSettingData.MaxProcessorsPerNumaNode**](msvm-processorsettingdata.md) and [**Msvm\_MemorySettingData.MaxMemoryBlocksPerNumaNode**](msvm-memorysettingdata.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="56460-500">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="56460-500">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-501">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-501">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-502">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-502">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56460-503">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "cim \_ VirtualSystemSettingData. VirtualSystemIdentifier" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**cim \_**](cim-computersystem.md)。**名稱**") </span><span class="sxs-lookup"><span data-stu-id="56460-503">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemSettingData.VirtualSystemIdentifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="56460-504">這項設定資料所屬之 CIM 非程式物件的名稱。 [**\_**](/windows/desktop/CIMWin32Prov/cim-computersystem)</span><span class="sxs-lookup"><span data-stu-id="56460-504">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="56460-505">這個屬性是 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))的覆寫。</span><span class="sxs-lookup"><span data-stu-id="56460-505">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="56460-506">**VirtualSystemSubType**</span><span class="sxs-lookup"><span data-stu-id="56460-506">**VirtualSystemSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-507">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-507">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-508">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-509">這個屬性的有效值為 Microsoft： Hyper-v：子類型：1和 Microsoft： Hyper-v：子類型：2。</span><span class="sxs-lookup"><span data-stu-id="56460-509">The valid values for this property are Microsoft:Hyper-V:SubType:1 and Microsoft:Hyper-V:SubType:2.</span></span> <span data-ttu-id="56460-510">第1代 VM 是子類型1。</span><span class="sxs-lookup"><span data-stu-id="56460-510">A  Generation 1  VM is subtype 1.</span></span> <span data-ttu-id="56460-511">第2代 VM 是子類型2。</span><span class="sxs-lookup"><span data-stu-id="56460-511">A  Generation 2  VM is subtype 2.</span></span>

<span data-ttu-id="56460-512">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="56460-512">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

<span data-ttu-id="56460-513">**Microsoft： hyper-v：子類型： 1** ( "Microsoft： Hyper-v：子類型： 1" ) </span><span class="sxs-lookup"><span data-stu-id="56460-513">**Microsoft:Hyper-V:SubType:1** ("Microsoft:Hyper-V:SubType:1")</span></span>


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

<span data-ttu-id="56460-514">**Microsoft： hyper-v：子類型： 2** ( "Microsoft： Hyper-v：子類型： 2" ) </span><span class="sxs-lookup"><span data-stu-id="56460-514">**Microsoft:Hyper-V:SubType:2** ("Microsoft:Hyper-V:SubType:2")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="56460-515">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="56460-515">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56460-516">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="56460-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56460-517">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="56460-517">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="56460-518">指定設定資料所代表的虛擬機器類型。</span><span class="sxs-lookup"><span data-stu-id="56460-518">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="56460-519">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) 類別。</span><span class="sxs-lookup"><span data-stu-id="56460-519">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) class.</span></span> <span data-ttu-id="56460-520">這會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="56460-520">This will be one of the following values.</span></span>



| <span data-ttu-id="56460-521">值</span><span class="sxs-lookup"><span data-stu-id="56460-521">Value</span></span>                                                                                                                                 | <span data-ttu-id="56460-522">意義</span><span class="sxs-lookup"><span data-stu-id="56460-522">Meaning</span></span>                                              |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="56460-523"><dt>「Microsoft： Hyper-v： System：認識」</dt></span><span class="sxs-lookup"><span data-stu-id="56460-523"><dt>"Microsoft:Hyper-V:System:Realized"</dt></span></span> </dl>                        | <span data-ttu-id="56460-524">已實現的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="56460-524">A realized virtual machine.</span></span><br/>               |
| <dl> <span data-ttu-id="56460-525"><dt>「Microsoft： Hyper-v： System：已規劃」</dt></span><span class="sxs-lookup"><span data-stu-id="56460-525"><dt>"Microsoft:Hyper-V:System:Planned"</dt></span></span> </dl>                         | <span data-ttu-id="56460-526">規劃的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="56460-526">A planned virtual machine.</span></span><br/>                |
| <dl> <span data-ttu-id="56460-527"><dt>「Microsoft： Hyper-v： Snapshot：已實現」</dt></span><span class="sxs-lookup"><span data-stu-id="56460-527"><dt>"Microsoft:Hyper-V:Snapshot:Realized"</dt></span></span> </dl>                      | <span data-ttu-id="56460-528">已實現之虛擬機器的快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-528">A snapshot of a realized virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="56460-529"><dt>「Microsoft： Hyper-v： Snapshot： Recovery」</dt></span><span class="sxs-lookup"><span data-stu-id="56460-529"><dt>"Microsoft:Hyper-V:Snapshot:Recovery"</dt></span></span> </dl>                      | <span data-ttu-id="56460-530">復原虛擬機器的快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-530">A snapshot of a recovery virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="56460-531"><dt>「Microsoft： Hyper-v：快照集：已規劃」</dt></span><span class="sxs-lookup"><span data-stu-id="56460-531"><dt>"Microsoft:Hyper-V:Snapshot:Planned"</dt></span></span> </dl>                       | <span data-ttu-id="56460-532">規劃之虛擬機器的快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-532">A snapshot of a planned virtual machine.</span></span><br/>  |
| <dl> <span data-ttu-id="56460-533"><dt>「Microsoft： Hyper-v： Snapshot：缺少」</dt></span><span class="sxs-lookup"><span data-stu-id="56460-533"><dt>"Microsoft:Hyper-V:Snapshot:Missing"</dt></span></span> </dl>                       | <span data-ttu-id="56460-534">遺漏的快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-534">A missing snapshot.</span></span><br/>                       |
| <dl> <span data-ttu-id="56460-535"><dt>"Microsoft： Hyper-v： Snapshot： Replica： Standard"</dt></span><span class="sxs-lookup"><span data-stu-id="56460-535"><dt>"Microsoft:Hyper-V:Snapshot:Replica:Standard"</dt></span></span> </dl>              | <span data-ttu-id="56460-536">以時間為基礎的複寫點快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-536">A time-based replication point snapshot.</span></span><br/>  |
| <dl> <span data-ttu-id="56460-537"><dt>"Microsoft： Hyper-v： Snapshot： Replica： ApplicationConsistent"</dt></span><span class="sxs-lookup"><span data-stu-id="56460-537"><dt>"Microsoft:Hyper-V:Snapshot:Replica:ApplicationConsistent"</dt></span></span> </dl> | <span data-ttu-id="56460-538">VSS 複寫點快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-538">A VSS replication point snapshot.</span></span><br/>         |
| <dl> <span data-ttu-id="56460-539"><dt>"Microsoft： Hyper-v： Snapshot： Replica： PlannedFailover"</dt></span><span class="sxs-lookup"><span data-stu-id="56460-539"><dt>"Microsoft:Hyper-V:Snapshot:Replica:PlannedFailover"</dt></span></span> </dl>       | <span data-ttu-id="56460-540">規劃的複寫快照集。</span><span class="sxs-lookup"><span data-stu-id="56460-540">A planned replication snapshot.</span></span><br/>           |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56460-541">備註</span><span class="sxs-lookup"><span data-stu-id="56460-541">Remarks</span></span>

<span data-ttu-id="56460-542">存取 **Msvm \_ VirtualSystemSettingData** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="56460-542">Access to the **Msvm\_VirtualSystemSettingData** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="56460-543">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="56460-543">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="56460-544">規格需求</span><span class="sxs-lookup"><span data-stu-id="56460-544">Requirements</span></span>



| <span data-ttu-id="56460-545">需求</span><span class="sxs-lookup"><span data-stu-id="56460-545">Requirement</span></span> | <span data-ttu-id="56460-546">值</span><span class="sxs-lookup"><span data-stu-id="56460-546">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56460-547">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56460-547">Minimum supported client</span></span><br/> | <span data-ttu-id="56460-548">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56460-548">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="56460-549">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56460-549">Minimum supported server</span></span><br/> | <span data-ttu-id="56460-550">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56460-550">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56460-551">命名空間</span><span class="sxs-lookup"><span data-stu-id="56460-551">Namespace</span></span><br/>                | <span data-ttu-id="56460-552">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="56460-552">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="56460-553">MOF</span><span class="sxs-lookup"><span data-stu-id="56460-553">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56460-554"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="56460-554"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="56460-555">DLL</span><span class="sxs-lookup"><span data-stu-id="56460-555">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56460-556"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="56460-556"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="56460-557">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56460-557">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56460-558">**CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="56460-558">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

<span data-ttu-id="56460-559">[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="56460-559">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="56460-560">虛擬系統類別</span><span class="sxs-lookup"><span data-stu-id="56460-560">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

