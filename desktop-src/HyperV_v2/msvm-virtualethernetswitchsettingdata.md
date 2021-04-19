---
description: 代表虛擬乙太網路交換器的目前設定。
ms.assetid: a7c03517-332d-47ce-8e04-c2187bcb2977
title: Msvm_VirtualEthernetSwitchSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingData
- Msvm_VirtualEthernetSwitchSettingData.InstanceID
- Msvm_VirtualEthernetSwitchSettingData.Caption
- Msvm_VirtualEthernetSwitchSettingData.Description
- Msvm_VirtualEthernetSwitchSettingData.ElementName
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemIdentifier
- Msvm_VirtualEthernetSwitchSettingData.VirtualSystemType
- Msvm_VirtualEthernetSwitchSettingData.Notes
- Msvm_VirtualEthernetSwitchSettingData.CreationTime
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationID
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationDataRoot
- Msvm_VirtualEthernetSwitchSettingData.ConfigurationFile
- Msvm_VirtualEthernetSwitchSettingData.SnapshotDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SuspendDataRoot
- Msvm_VirtualEthernetSwitchSettingData.SwapFileDataRoot
- Msvm_VirtualEthernetSwitchSettingData.LogDataRoot
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionDelay
- Msvm_VirtualEthernetSwitchSettingData.AutomaticStartupActionSequenceNumber
- Msvm_VirtualEthernetSwitchSettingData.AutomaticShutdownAction
- Msvm_VirtualEthernetSwitchSettingData.AutomaticRecoveryAction
- Msvm_VirtualEthernetSwitchSettingData.RecoveryFile
- Msvm_VirtualEthernetSwitchSettingData.VLANConnection
- Msvm_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- Msvm_VirtualEthernetSwitchSettingData.MaxNumMACAddress
- Msvm_VirtualEthernetSwitchSettingData.IOVPreferred
- Msvm_VirtualEthernetSwitchSettingData.ExtensionOrder
- Msvm_VirtualEthernetSwitchSettingData.BandwidthReservationMode
- Msvm_VirtualEthernetSwitchSettingData.TeamingEnabled
- Msvm_VirtualEthernetSwitchSettingData.PacketDirectEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3eccbd9dabe853f01c54c78ca651d590afc49f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974605"
---
# <a name="msvm_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="3b4e9-103">Msvm \_ VirtualEthernetSwitchSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="3b4e9-103">Msvm\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="3b4e9-104">代表虛擬乙太網路交換器的目前設定。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-104">Represents the current configuration of a virtual Ethernet switch.</span></span>

<span data-ttu-id="3b4e9-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b4e9-106">語法</span><span class="sxs-lookup"><span data-stu-id="3b4e9-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingData : CIM_VirtualEthernetSwitchSettingData
{
  string   InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string   Caption = "Virtual Ethernet Switch Settings";
  string   Description = "Active settings for the virtual Ethernet switch";
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
  string   VLANConnection[];
  string   AssociatedResourcePool[];
  uint32   MaxNumMACAddress;
  boolean  IOVPreferred = FALSE;
  string   ExtensionOrder[];
  uint32   BandwidthReservationMode = 0;
  boolean  TeamingEnabled = FALSE;
  boolean  PacketDirectEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="3b4e9-107">成員</span><span class="sxs-lookup"><span data-stu-id="3b4e9-107">Members</span></span>

<span data-ttu-id="3b4e9-108">**Msvm \_ VirtualEthernetSwitchSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3b4e9-108">The **Msvm\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3b4e9-109">屬性</span><span class="sxs-lookup"><span data-stu-id="3b4e9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b4e9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="3b4e9-110">Properties</span></span>

<span data-ttu-id="3b4e9-111">**Msvm \_ VirtualEthernetSwitchSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-111">The **Msvm\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b4e9-112">**AssociatedResourcePool**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-112">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-113">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3b4e9-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-115">要關聯的主機資源集區清單，或目前與乙太網路交換器相關聯的主機資源集區，目的是要在虛擬機器與乙太網路交換器之間配置乙太網路連接。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-115">A list of host resource pools to be associated or that are currently associated with the Ethernet switch for the purpose of the allocation of Ethernet connections between a virtual machine and an Ethernet switch.</span></span> <span data-ttu-id="3b4e9-116">每個值都必須符合 \_ DSP0207 中定義的生產 WBEM URI \_ UntypedInstancePath。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-116">Each value must conform to the production WBEM\_URI\_UntypedInstancePath as defined in DSP0207.</span></span> <span data-ttu-id="3b4e9-117">這個屬性繼承自 **CIM \_ VirtualEthernetSwitchSettingData**。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-117">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-118">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-118">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-119">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-121">當虛擬機器執行的軟體失敗時，針對虛擬機器所採取的動作。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-121">Action to take for the virtual machine when the software executed by the virtual machine fails.</span></span> <span data-ttu-id="3b4e9-122">在此情況下，失敗表示主機平臺偵測到失敗，例如無法中斷的等候狀態條件。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-122">Failures in this case means a failure that is detectable by the host platform, such as a non-interruptible wait state condition.</span></span> <span data-ttu-id="3b4e9-123">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-123">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-124">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-124">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-125">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-127">當主機關閉時，為虛擬機器採取的動作。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-127">Action to take for the virtual machine when the host is shut down.</span></span> <span data-ttu-id="3b4e9-128">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-128">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-129">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-129">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-130">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-132">當主機啟動時，對虛擬機器採取的動作。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-132">Action to take for the virtual machine when the host is started.</span></span> <span data-ttu-id="3b4e9-133">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-133">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-134">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-134">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-135">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-137">虛擬機器自動啟動之前的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-137">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="3b4e9-138">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-138">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-139">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-139">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-140">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-142">數位，指出主機系統啟動時的虛擬機器啟用的相對順序。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-142">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="3b4e9-143">較低的數位表示先前的啟用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-143">A lower number indicates earlier activation.</span></span> <span data-ttu-id="3b4e9-144">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-144">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-145">**BandwidthReservationMode**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-145">**BandwidthReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-146">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-147">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3b4e9-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-148">頻寬保留模式。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-148">The bandwidth reservation mode.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="3b4e9-149">**預設** (0) </span><span class="sxs-lookup"><span data-stu-id="3b4e9-149">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="3b4e9-150">**權數** (1) </span><span class="sxs-lookup"><span data-stu-id="3b4e9-150">**Weight** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="3b4e9-151">**絕對** (2) </span><span class="sxs-lookup"><span data-stu-id="3b4e9-151">**Absolute** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="3b4e9-152">**無** (3) </span><span class="sxs-lookup"><span data-stu-id="3b4e9-152">**None** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3b4e9-153">**標題**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-153">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-154">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-156">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-156">A short description of the object.</span></span> <span data-ttu-id="3b4e9-157">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「虛擬乙太網路交換器設定」。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Ethernet Switch Settings".</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-158">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-158">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-161">儲存虛擬機器設定相關資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-161">The path of a directory where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="3b4e9-162">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-162">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-163">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-163">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-166">儲存虛擬機器設定相關資訊之檔案的相對路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-166">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="3b4e9-167">此路徑相對於 **ConfigurationDataRoot** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-167">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="3b4e9-168">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-168">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-169">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-169">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-170">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-171">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-172">虛擬機器設定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-172">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="3b4e9-173">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-173">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-174">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-174">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-175">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-175">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-177">建立設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-177">The date and time at which the settings were created.</span></span> <span data-ttu-id="3b4e9-178">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-178">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-179">**說明**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-179">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-181">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-182">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-182">A description of the object.</span></span> <span data-ttu-id="3b4e9-183">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「虛擬乙太網路交換器的作用中設定」。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Active settings for the virtual Ethernet switch".</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-187">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-187">A display name for the object.</span></span> <span data-ttu-id="3b4e9-188">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-188">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-189">**ExtensionOrder**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-189">**ExtensionOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-190">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3b4e9-190">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-191">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3b4e9-191">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-192">[**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)類別的內嵌實例陣列，代表系結至此參數的 switch 擴充功能（依照套用的順序）。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-192">An array of embedded instances of the [**Msvm\_EthernetSwitchExtension**](msvm-ethernetswitchextension.md) class that represent the switch extensions bound to this switch, in the order in which they are applied.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-193">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-193">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-194">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-196">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-196">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-197">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-197">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3b4e9-198">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) ，一律設定為 "Microsoft：*GUID* \\ *DeviceSpecificData*"。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-198">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-199">**IOVPreferred**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-199">**IOVPreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-200">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-201">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3b4e9-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-202">指定基礎介面卡上是否偏好使用單一根 IO 虛擬化 (SR-IOV) （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-202">Specifies whether single root IO virtualization (SR-IOV) is preferred or not, if available, on the underlying adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-203">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-203">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-206">儲存虛擬機器記錄資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-206">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="3b4e9-207">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-207">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-208">**MaxNumMACAddress**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-208">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-209">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-210">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-211">指定可由交換器提供的唯一 MAC 位址數目上限，以支援 MAC 位址學習（如 IEEE 802.1 標準所定義）。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-211">Specifies the maximum number of unique MAC addresses that can be learned by the switch to support MAC Address Learning, as defined in the IEEE 802.1 standard.</span></span> <span data-ttu-id="3b4e9-212">這個屬性繼承自 **CIM \_ VirtualEthernetSwitchSettingData**。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-212">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-213">**注意事項**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-213">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-214">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3b4e9-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-216">與虛擬機器相關的使用者提供的附注。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-216">User supplied notes that are related to the virtual machine.</span></span> <span data-ttu-id="3b4e9-217">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-217">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-218">**PacketDirectEnabled**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-218">**PacketDirectEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-219">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3b4e9-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-221">指定是否應該使用 PacketDirect （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-221">Specifies whether PacketDirect should be used, if available.</span></span> <span data-ttu-id="3b4e9-222">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-222">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="3b4e9-223">這個屬性是在 Windows 10 和 Windows Server 2016 中新增的。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-223">This property was added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="3b4e9-224">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-224">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-227">儲存虛擬機器修復相關資訊之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-227">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="3b4e9-228">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-228">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-229">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-229">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-230">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-232">儲存虛擬機器快照集相關資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-232">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="3b4e9-233">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-233">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-234">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-234">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-235">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-235">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-236">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-237">儲存虛擬機器暫停相關資訊之相關資訊的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-237">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="3b4e9-238">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-238">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-239">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-239">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-242">儲存虛擬機器之交換檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-242">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="3b4e9-243">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，而且不會使用。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-243">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-244">**TeamingEnabled**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-244">**TeamingEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-245">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-245">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-246">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3b4e9-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-247">指定是否應該使用「NIC 小組」。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-247">Specifies whether NIC Teaming should be used.</span></span> <span data-ttu-id="3b4e9-248">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-248">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="3b4e9-249">此屬性已新增至 Windows 10 和 Windows Server 2016。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-249">This property was added inWindows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="3b4e9-250">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-250">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-253">這項設定資料所屬之 CIM 非程式物件的名稱。 [**\_**](/windows/desktop/CIMWin32Prov/cim-computersystem)</span><span class="sxs-lookup"><span data-stu-id="3b4e9-253">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="3b4e9-254">這個屬性是 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))的覆寫。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-254">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-255">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-255">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-256">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-258">指定設定資料所代表的虛擬機器類型。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-258">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="3b4e9-259">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-259">This property is inherited from the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3b4e9-260">**VLANConnection**</span><span class="sxs-lookup"><span data-stu-id="3b4e9-260">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b4e9-261">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="3b4e9-261">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3b4e9-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3b4e9-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b4e9-263">此交換器可以存取的 VLAN 識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-263">A list of VLAN identifiers that this switch can access.</span></span> <span data-ttu-id="3b4e9-264">這個屬性繼承自 **CIM \_ VirtualEthernetSwitchSettingData**。</span><span class="sxs-lookup"><span data-stu-id="3b4e9-264">This property is inherited from **CIM\_VirtualEthernetSwitchSettingData**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b4e9-265">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b4e9-265">Requirements</span></span>



| <span data-ttu-id="3b4e9-266">需求</span><span class="sxs-lookup"><span data-stu-id="3b4e9-266">Requirement</span></span> | <span data-ttu-id="3b4e9-267">值</span><span class="sxs-lookup"><span data-stu-id="3b4e9-267">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b4e9-268">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b4e9-268">Minimum supported client</span></span><br/> | <span data-ttu-id="3b4e9-269">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b4e9-269">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3b4e9-270">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b4e9-270">Minimum supported server</span></span><br/> | <span data-ttu-id="3b4e9-271">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b4e9-271">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b4e9-272">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b4e9-272">Namespace</span></span><br/>                | <span data-ttu-id="3b4e9-273">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="3b4e9-273">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3b4e9-274">MOF</span><span class="sxs-lookup"><span data-stu-id="3b4e9-274">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b4e9-275"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="3b4e9-275"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b4e9-276">DLL</span><span class="sxs-lookup"><span data-stu-id="3b4e9-276">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b4e9-277"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b4e9-277"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

