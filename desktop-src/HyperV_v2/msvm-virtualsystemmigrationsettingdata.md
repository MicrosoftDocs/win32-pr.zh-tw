---
description: 代表遷移虛擬系統和附加至虛擬系統之存放裝置的遷移設定。
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Msvm_VirtualSystemMigrationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847759"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a><span data-ttu-id="431ed-103">Msvm \_ VirtualSystemMigrationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="431ed-103">Msvm\_VirtualSystemMigrationSettingData class</span></span>

<span data-ttu-id="431ed-104">代表遷移虛擬系統和附加至虛擬系統之存放裝置的遷移設定。</span><span class="sxs-lookup"><span data-stu-id="431ed-104">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span>

<span data-ttu-id="431ed-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="431ed-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="431ed-106">語法</span><span class="sxs-lookup"><span data-stu-id="431ed-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a><span data-ttu-id="431ed-107">成員</span><span class="sxs-lookup"><span data-stu-id="431ed-107">Members</span></span>

<span data-ttu-id="431ed-108">**Msvm \_ VirtualSystemMigrationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="431ed-108">The **Msvm\_VirtualSystemMigrationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="431ed-109">屬性</span><span class="sxs-lookup"><span data-stu-id="431ed-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="431ed-110">屬性</span><span class="sxs-lookup"><span data-stu-id="431ed-110">Properties</span></span>

<span data-ttu-id="431ed-111">**Msvm \_ VirtualSystemMigrationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="431ed-111">The **Msvm\_VirtualSystemMigrationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="431ed-112">**AllowOverwriteExistingFile**</span><span class="sxs-lookup"><span data-stu-id="431ed-112">**AllowOverwriteExistingFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-113">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="431ed-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-114">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="431ed-115">允許儲存體遷移作業覆寫現有的 .vhdx 檔案。</span><span class="sxs-lookup"><span data-stu-id="431ed-115">Allow the storage migration operation to overwrite existing .vhdx files.</span></span>

> [!Note]  
> <span data-ttu-id="431ed-116">這個屬性是在 Windows 10 1703 版中加入的。</span><span class="sxs-lookup"><span data-stu-id="431ed-116">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="431ed-117">**AvoidRemovingVHDs**</span><span class="sxs-lookup"><span data-stu-id="431ed-117">**AvoidRemovingVHDs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-118">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="431ed-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="431ed-120">請勿在遷移期間移除任何 Vhd，也就是在目的地的 successand Vhd 中，來源的 Vhd 失敗。</span><span class="sxs-lookup"><span data-stu-id="431ed-120">Do not remove any VHDs during the migration, i.e. VHDs on the source in successand VHDs on the destination in failure.</span></span>

> [!Note]  
> <span data-ttu-id="431ed-121">已在 Windows 10、1703版和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="431ed-121">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="431ed-122">**頻寬**</span><span class="sxs-lookup"><span data-stu-id="431ed-122">**Bandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-123">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="431ed-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="431ed-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="431ed-125">指定指派給或要求進行虛擬系統移轉作業的頻寬。</span><span class="sxs-lookup"><span data-stu-id="431ed-125">Specifies the bandwidth assigned to or requested for a virtual system migration operation.</span></span> <span data-ttu-id="431ed-126">頻寬單位是由 **BandwidthUnit** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="431ed-126">The bandwidth units are specified by the **BandwidthUnit** property.</span></span> <span data-ttu-id="431ed-127">在遷移期間，0值表示預設頻寬。</span><span class="sxs-lookup"><span data-stu-id="431ed-127">Within a migration, a value of 0 indicates the default bandwidth.</span></span> <span data-ttu-id="431ed-128">否則，值為0表示不支援頻寬。</span><span class="sxs-lookup"><span data-stu-id="431ed-128">Otherwise, a value of 0 indicates that bandwidths are not supported.</span></span>

<span data-ttu-id="431ed-129">**頻寬** 和 **優先順序** 可以搭配使用。</span><span class="sxs-lookup"><span data-stu-id="431ed-129">**Bandwidth** and **Priority** can be used in conjunction.</span></span> <span data-ttu-id="431ed-130">具有最高相等優先權值的遷移程式會根據其要求的頻寬共用可用的頻寬。</span><span class="sxs-lookup"><span data-stu-id="431ed-130">Migration processes that have the highest equal priority value share the available bandwidth based on their requested bandwidth.</span></span> <span data-ttu-id="431ed-131">如果並非所有的頻寬都是由這組進程取用，則下一個較低優先順序的遷移程式會共用剩餘的頻寬。</span><span class="sxs-lookup"><span data-stu-id="431ed-131">If not all bandwidth is consumed by this set of processes, migration processes with the next lower equal priority share the remaining bandwidth.</span></span> <span data-ttu-id="431ed-132">如果仍然有更多頻寬，則會考慮下一個較低優先順序的遷移程式等等。</span><span class="sxs-lookup"><span data-stu-id="431ed-132">If still more bandwidth remains, migration processes with the next lower equal priority are considered, and so forth.</span></span>

<span data-ttu-id="431ed-133">這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="431ed-133">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="431ed-134">**BandwidthUnit**</span><span class="sxs-lookup"><span data-stu-id="431ed-134">**BandwidthUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="431ed-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-136">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="431ed-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="431ed-137">指定 **頻寬** 屬性所使用的單位。</span><span class="sxs-lookup"><span data-stu-id="431ed-137">Specifies the units used by the **Bandwidth** property.</span></span> <span data-ttu-id="431ed-138">這個屬性的值必須是程式設計單位辨識符號的合法值，如 DSP0004 2.4 或更新版本的附錄 C. 1 中所定義。</span><span class="sxs-lookup"><span data-stu-id="431ed-138">The value of this property must be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

<span data-ttu-id="431ed-139">如果這個屬性的值是 "percent"， **頻寬** 屬性的值必須介於0到100之間，且值越高，表示較高的頻寬。</span><span class="sxs-lookup"><span data-stu-id="431ed-139">If the value of this property is "percent", the value of the **Bandwidth** property must be between 0 and 100, with higher values indicating a higher bandwidth.</span></span> <span data-ttu-id="431ed-140">值為100時，表示用來執行虛擬系統移轉作業的總可用頻寬。</span><span class="sxs-lookup"><span data-stu-id="431ed-140">A value of 100 indicates the total available bandwidth for performing virtual system migration operations.</span></span> <span data-ttu-id="431ed-141">介於1和100之間的值應與可用的頻寬範圍呈線性關聯。</span><span class="sxs-lookup"><span data-stu-id="431ed-141">Values between 1 and 100 should linearly correlate with the available bandwidth range.</span></span> <span data-ttu-id="431ed-142">例如，值為50時，應要求一半的可用頻寬。</span><span class="sxs-lookup"><span data-stu-id="431ed-142">For example, a value of 50 should request half of the available bandwidth.</span></span>

<span data-ttu-id="431ed-143">這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="431ed-143">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="431ed-144">**CancelIfBlackoutThresholdExceeded**</span><span class="sxs-lookup"><span data-stu-id="431ed-144">**CancelIfBlackoutThresholdExceeded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-145">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="431ed-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-146">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="431ed-147">如果超過掉電閾值時間，則取消遷移。</span><span class="sxs-lookup"><span data-stu-id="431ed-147">Cancels migration if the blackout threshold time is exceeded.</span></span>

> [!Note]  
> <span data-ttu-id="431ed-148">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="431ed-148">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="431ed-149">**標題**</span><span class="sxs-lookup"><span data-stu-id="431ed-149">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="431ed-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="431ed-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="431ed-152">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="431ed-152">A short description of the object.</span></span> <span data-ttu-id="431ed-153">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="431ed-153">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="431ed-154">**CPUCappingMagnitude**</span><span class="sxs-lookup"><span data-stu-id="431ed-154">**CPUCappingMagnitude**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-155">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="431ed-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-156">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-156">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="431ed-157">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CPUCappingMagnitude" ) </span><span class="sxs-lookup"><span data-stu-id="431ed-157">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")</span></span>
</dt> </dl>

<span data-ttu-id="431ed-158">遷移期間 CPU 限定的程度。</span><span class="sxs-lookup"><span data-stu-id="431ed-158">Degree of CPU capping during migration.</span></span>

> [!Note]  
> <span data-ttu-id="431ed-159">在 Windows 10 1709 版中新增。</span><span class="sxs-lookup"><span data-stu-id="431ed-159">Added in Windows 10, version 1709.</span></span>

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="431ed-160">**一般** (0) </span><span class="sxs-lookup"><span data-stu-id="431ed-160">**Normal** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="431ed-161">**低** (1) </span><span class="sxs-lookup"><span data-stu-id="431ed-161">**Low** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="431ed-162">**高** (2) </span><span class="sxs-lookup"><span data-stu-id="431ed-162">**High** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="431ed-163">**說明**</span><span class="sxs-lookup"><span data-stu-id="431ed-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="431ed-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-165">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="431ed-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="431ed-166">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="431ed-166">A description of the object.</span></span> <span data-ttu-id="431ed-167">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="431ed-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="431ed-168">**DestinationIPAddressList**</span><span class="sxs-lookup"><span data-stu-id="431ed-168">**DestinationIPAddressList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-169">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="431ed-169">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="431ed-170">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="431ed-171">儲存體遷移將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="431ed-171">This will be **Null** for storage migration.</span></span> <span data-ttu-id="431ed-172">若為虛擬系統移轉，這可以包含目的地主機的 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="431ed-172">For virtual system migration, this can contain a list of IP addresses of the destination host.</span></span>

</dd> <dt>

<span data-ttu-id="431ed-173">**DestinationPlannedVirtualSystemId**</span><span class="sxs-lookup"><span data-stu-id="431ed-173">**DestinationPlannedVirtualSystemId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="431ed-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="431ed-176">如果已規劃的虛擬機器存在於遷移目的地，則此屬性會設定為虛擬機器需要遷移的目的地已規劃虛擬機器的 GUID。</span><span class="sxs-lookup"><span data-stu-id="431ed-176">If a planned virtual machine exists at the migration destination, this property will be set to the GUID of the destination planned virtual machine where the virtual machine needs to migrate.</span></span> <span data-ttu-id="431ed-177">當使用者已在目的地建立計畫的虛擬機器，以及資源設定，並想要讓來源的虛擬機器遷移到此計畫的虛擬機器時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="431ed-177">This is useful for cases where a user has created a planned virtual machine at the destination, along with resource setup, and wants a virtual machine from the source to migrate into this planned virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="431ed-178">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="431ed-178">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="431ed-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="431ed-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="431ed-181">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="431ed-181">A display name for the object.</span></span> <span data-ttu-id="431ed-182">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="431ed-182">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="431ed-183">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="431ed-183">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-184">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="431ed-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-185">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="431ed-186">指出是否壓縮即時移轉流量。</span><span class="sxs-lookup"><span data-stu-id="431ed-186">Indicates whether to compress the live migration traffic.</span></span> <span data-ttu-id="431ed-187">**True** 表示要壓縮;否則 **為 False**。</span><span class="sxs-lookup"><span data-stu-id="431ed-187">**True** indicates to compress; otherwise **False**.</span></span>

<span data-ttu-id="431ed-188">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="431ed-188">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="431ed-189">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="431ed-189">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="431ed-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="431ed-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="431ed-192">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="431ed-192">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="431ed-193">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="431ed-193">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="431ed-194">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="431ed-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="431ed-195">**MigrationType**</span><span class="sxs-lookup"><span data-stu-id="431ed-195">**MigrationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-196">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="431ed-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-197">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="431ed-198">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MigrationType" ) </span><span class="sxs-lookup"><span data-stu-id="431ed-198">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")</span></span>
</dt> </dl>

<span data-ttu-id="431ed-199">指定要執行的遷移操作類型。</span><span class="sxs-lookup"><span data-stu-id="431ed-199">Specifies the type of migration operation to be performed.</span></span> <span data-ttu-id="431ed-200">這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="431ed-200">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="431ed-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="431ed-201"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span data-ttu-id="431ed-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768) </span><span class="sxs-lookup"><span data-stu-id="431ed-202"><span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="431ed-203">將虛擬系統移轉至目的地主機。</span><span class="sxs-lookup"><span data-stu-id="431ed-203">Migrates the virtual system to the destination host.</span></span>

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="431ed-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**儲存體** (32769) </span><span class="sxs-lookup"><span data-stu-id="431ed-204"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (32769)</span></span>


</dt> <dd>

<span data-ttu-id="431ed-205">只遷移虛擬系統的儲存體資源。</span><span class="sxs-lookup"><span data-stu-id="431ed-205">Migrates only the storage resources of the virtual system.</span></span>

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span data-ttu-id="431ed-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**暫存** (32770) </span><span class="sxs-lookup"><span data-stu-id="431ed-206"><span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Staged** (32770)</span></span>


</dt> <dd>

<span data-ttu-id="431ed-207">使用虛擬系統設定，在目的地主機上建立已規劃的虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="431ed-207">Using the virtual system configuration, creates a planned virtual system at the destination host.</span></span>

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span data-ttu-id="431ed-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771) </span><span class="sxs-lookup"><span data-stu-id="431ed-208"><span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)</span></span>


</dt> <dd>

<span data-ttu-id="431ed-209">將虛擬系統及其存放裝置遷移至目的地主機。</span><span class="sxs-lookup"><span data-stu-id="431ed-209">Migrates the virtual system and its storage to the destination host.</span></span>

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span data-ttu-id="431ed-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772) </span><span class="sxs-lookup"><span data-stu-id="431ed-210"><span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)</span></span>


</dt> <dd>

<span data-ttu-id="431ed-211">在目的地主機上執行虛擬系統儲存體資源遷移功能檢查。</span><span class="sxs-lookup"><span data-stu-id="431ed-211">Performs a virtual system storage resource migration ability check at the destination host.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="431ed-212">**OtherTransportType**</span><span class="sxs-lookup"><span data-stu-id="431ed-212">**OtherTransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="431ed-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="431ed-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="431ed-215">如果 **TransportType** 的值為 1 (其他) ，則指定要套用的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="431ed-215">Specifies the type of transport to be applied if the value of **TransportType** is 1 (Other).</span></span> <span data-ttu-id="431ed-216">這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="431ed-216">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="431ed-217">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="431ed-217">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-218">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="431ed-218">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-219">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="431ed-219">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="431ed-220">指定相對遷移的重要性，讓遷移系統可以用來排序，或在多個擱置中的遷移要求之間提供喜好設定。</span><span class="sxs-lookup"><span data-stu-id="431ed-220">Specifies a relative migration importance, which the migration system may use to order or otherwise give preference among multiple pending migration requests.</span></span> <span data-ttu-id="431ed-221">值愈低，優先順序愈高。</span><span class="sxs-lookup"><span data-stu-id="431ed-221">The lower the value, the higher the priority.</span></span> <span data-ttu-id="431ed-222">在遷移期間，0值表示預設優先權。</span><span class="sxs-lookup"><span data-stu-id="431ed-222">Within a migration, a value of 0 indicates the default priority.</span></span> <span data-ttu-id="431ed-223">否則，值為0表示不支援優先權。</span><span class="sxs-lookup"><span data-stu-id="431ed-223">Otherwise, a value of 0 indicates that priorities are not supported.</span></span>

<span data-ttu-id="431ed-224">這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="431ed-224">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

</dd> <dt>

<span data-ttu-id="431ed-225">**RemoveSourceUnmanagedVhds**</span><span class="sxs-lookup"><span data-stu-id="431ed-225">**RemoveSourceUnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-226">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="431ed-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-227">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-227">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="431ed-228">移除來源非受控 Vhd。</span><span class="sxs-lookup"><span data-stu-id="431ed-228">Remove source unmanaged VHDs.</span></span>

> [!Note]  
> <span data-ttu-id="431ed-229">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="431ed-229">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="431ed-230">**RetainVhdCopiesOnSource**</span><span class="sxs-lookup"><span data-stu-id="431ed-230">**RetainVhdCopiesOnSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-231">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="431ed-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-232">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="431ed-233">針對儲存體遷移，這會指定在完成遷移之後是否應移除來源主機上的唯讀 Vhd。</span><span class="sxs-lookup"><span data-stu-id="431ed-233">For a storage migration, this specifies whether the read-only VHDs on the source host should be removed after the migration is completed.</span></span>

</dd> <dt>

<span data-ttu-id="431ed-234">**TransportType**</span><span class="sxs-lookup"><span data-stu-id="431ed-234">**TransportType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-235">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="431ed-235">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="431ed-236">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-236">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="431ed-237">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "TransportType" ) </span><span class="sxs-lookup"><span data-stu-id="431ed-237">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")</span></span>
</dt> </dl>

<span data-ttu-id="431ed-238">指定要套用至虛擬系統移轉作業的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="431ed-238">Specifies the type of transport to be applied for a virtual system migration operation.</span></span> <span data-ttu-id="431ed-239">這個屬性繼承自 **CIM \_ VirtualSystemMigrationSettingData**。</span><span class="sxs-lookup"><span data-stu-id="431ed-239">This property is inherited from **CIM\_VirtualSystemMigrationSettingData**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="431ed-240">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="431ed-240">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="431ed-241">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="431ed-241">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

<span data-ttu-id="431ed-242">**SSH** (2) </span><span class="sxs-lookup"><span data-stu-id="431ed-242">**SSH** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

<span data-ttu-id="431ed-243">**TLS** (3) </span><span class="sxs-lookup"><span data-stu-id="431ed-243">**TLS** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

<span data-ttu-id="431ed-244">**TLS Strict** (4) </span><span class="sxs-lookup"><span data-stu-id="431ed-244">**TLS Strict** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="431ed-245">**TCP** (5) </span><span class="sxs-lookup"><span data-stu-id="431ed-245">**TCP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="431ed-246">**IPC** (6) </span><span class="sxs-lookup"><span data-stu-id="431ed-246">**IPC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="431ed-247">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="431ed-247">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="431ed-248">**廠商保留** (32768 ) </span><span class="sxs-lookup"><span data-stu-id="431ed-248">**Vendor Reserved** (32768..)</span></span>


<span data-ttu-id="431ed-249"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="431ed-249"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="431ed-250">針對即時移轉，此屬性會指定要用來將虛擬系統狀態傳送至目的地主機的傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="431ed-250">For live migration, this property specifies the transport type to be used for transferring virtual system state to the destination host.</span></span> <span data-ttu-id="431ed-251">支援的值為：</span><span class="sxs-lookup"><span data-stu-id="431ed-251">The supported values are:</span></span>

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span data-ttu-id="431ed-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5) </span><span class="sxs-lookup"><span data-stu-id="431ed-252"><span id="TCP"></span><span id="tcp"></span>**TCP** (5)</span></span>


</dt> <dd>

<span data-ttu-id="431ed-253">指出 TCP 傳輸類型。</span><span class="sxs-lookup"><span data-stu-id="431ed-253">Indicates the TCP transport type.</span></span>

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span data-ttu-id="431ed-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768) </span><span class="sxs-lookup"><span data-stu-id="431ed-254"><span id="SMB"></span><span id="smb"></span>**SMB** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="431ed-255">指出傳輸虛擬機器狀態的傳輸類型為 SMB。</span><span class="sxs-lookup"><span data-stu-id="431ed-255">Indicates the transport type for transferring the virtual machine state is SMB.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="431ed-256">**UnmanagedVhds**</span><span class="sxs-lookup"><span data-stu-id="431ed-256">**UnmanagedVhds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431ed-257">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="431ed-257">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="431ed-258">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="431ed-258">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="431ed-259">限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， **HyperVEmbeddedInstance** ( "Msvm \_ MoveUnmanagedVhd" ) </span><span class="sxs-lookup"><span data-stu-id="431ed-259">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), **HyperVEmbeddedInstance** ("Msvm\_MoveUnmanagedVhd")</span></span>
</dt> </dl>

<span data-ttu-id="431ed-260">內嵌 [**Msvm \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) 實例的陣列，其中包含未受管理的 vhd 資訊。</span><span class="sxs-lookup"><span data-stu-id="431ed-260">An array of embedded [**Msvm\_MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) instances which contain unmanaged VHDs information.</span></span>

> [!Note]  
> <span data-ttu-id="431ed-261">在 Windows 10 和 Windows Server 2016 中新增。</span><span class="sxs-lookup"><span data-stu-id="431ed-261">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="431ed-262">規格需求</span><span class="sxs-lookup"><span data-stu-id="431ed-262">Requirements</span></span>



| <span data-ttu-id="431ed-263">需求</span><span class="sxs-lookup"><span data-stu-id="431ed-263">Requirement</span></span> | <span data-ttu-id="431ed-264">值</span><span class="sxs-lookup"><span data-stu-id="431ed-264">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="431ed-265">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="431ed-265">Minimum supported client</span></span><br/> | <span data-ttu-id="431ed-266">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="431ed-266">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="431ed-267">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="431ed-267">Minimum supported server</span></span><br/> | <span data-ttu-id="431ed-268">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="431ed-268">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="431ed-269">命名空間</span><span class="sxs-lookup"><span data-stu-id="431ed-269">Namespace</span></span><br/>                | <span data-ttu-id="431ed-270">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="431ed-270">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="431ed-271">MOF</span><span class="sxs-lookup"><span data-stu-id="431ed-271">MOF</span></span><br/>                      | <dl> <span data-ttu-id="431ed-272"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="431ed-272"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="431ed-273">DLL</span><span class="sxs-lookup"><span data-stu-id="431ed-273">DLL</span></span><br/>                      | <dl> <span data-ttu-id="431ed-274"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="431ed-274"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="431ed-275">另請參閱</span><span class="sxs-lookup"><span data-stu-id="431ed-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431ed-276">**CIM \_ VirtualSystemMigrationSettingData**</span><span class="sxs-lookup"><span data-stu-id="431ed-276">**CIM\_VirtualSystemMigrationSettingData**</span></span>](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[<span data-ttu-id="431ed-277">**MigrateVirtualSystemToHost**</span><span class="sxs-lookup"><span data-stu-id="431ed-277">**MigrateVirtualSystemToHost**</span></span>](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

