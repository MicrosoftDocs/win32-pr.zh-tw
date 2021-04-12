---
description: 代表虛擬機器的複寫特定設定。
ms.assetid: f6f6a413-a949-4aca-930b-37e39bdc1fdb
title: Msvm_ReplicationSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationSettingData
- Msvm_ReplicationSettingData.InstanceID
- Msvm_ReplicationSettingData.Caption
- Msvm_ReplicationSettingData.Description
- Msvm_ReplicationSettingData.ElementName
- Msvm_ReplicationSettingData.VirtualSystemIdentifier
- Msvm_ReplicationSettingData.VirtualSystemType
- Msvm_ReplicationSettingData.Notes
- Msvm_ReplicationSettingData.CreationTime
- Msvm_ReplicationSettingData.ConfigurationID
- Msvm_ReplicationSettingData.ConfigurationDataRoot
- Msvm_ReplicationSettingData.ConfigurationFile
- Msvm_ReplicationSettingData.SnapshotDataRoot
- Msvm_ReplicationSettingData.SuspendDataRoot
- Msvm_ReplicationSettingData.SwapFileDataRoot
- Msvm_ReplicationSettingData.LogDataRoot
- Msvm_ReplicationSettingData.AutomaticStartupAction
- Msvm_ReplicationSettingData.AutomaticStartupActionDelay
- Msvm_ReplicationSettingData.AutomaticStartupActionSequenceNumber
- Msvm_ReplicationSettingData.AutomaticShutdownAction
- Msvm_ReplicationSettingData.AutomaticRecoveryAction
- Msvm_ReplicationSettingData.RecoveryFile
- Msvm_ReplicationSettingData.AuthenticationType
- Msvm_ReplicationSettingData.CertificateThumbPrint
- Msvm_ReplicationSettingData.RootCertificateThumbPrint
- Msvm_ReplicationSettingData.CompressionEnabled
- Msvm_ReplicationSettingData.BypassProxyServer
- Msvm_ReplicationSettingData.RecoveryConnectionPoint
- Msvm_ReplicationSettingData.RecoveryHostSystem
- Msvm_ReplicationSettingData.PrimaryConnectionPoint
- Msvm_ReplicationSettingData.PrimaryHostSystem
- Msvm_ReplicationSettingData.RecoveryServerPortNumber
- Msvm_ReplicationSettingData.ReplicateHostKvpItems
- Msvm_ReplicationSettingData.ApplicationConsistentSnapshotInterval
- Msvm_ReplicationSettingData.RecoveryHistory
- Msvm_ReplicationSettingData.IncludedDisks
- Msvm_ReplicationSettingData.AutoResynchronizeEnabled
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalStart
- Msvm_ReplicationSettingData.AutoResynchronizeIntervalEnd
- Msvm_ReplicationSettingData.EnableWriteOrderPreservationAcrossDisks
- Msvm_ReplicationSettingData.ReplicationProvider
- Msvm_ReplicationSettingData.AdditionalSettings
- Msvm_ReplicationSettingData.ReplicationInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35bb97e531f8aca5f74801d55a71e5b3f2850c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193320"
---
# <a name="msvm_replicationsettingdata-class"></a><span data-ttu-id="11b11-103">Msvm \_ ReplicationSettingData 類別</span><span class="sxs-lookup"><span data-stu-id="11b11-103">Msvm\_ReplicationSettingData class</span></span>

<span data-ttu-id="11b11-104">代表虛擬機器的複寫特定設定。</span><span class="sxs-lookup"><span data-stu-id="11b11-104">Represents the replication-specific settings for a virtual machine.</span></span> <span data-ttu-id="11b11-105">用戶端會將這個類別的實例傳遞至 [**Msvm \_ ReplicationService >createreplicationrelationship**](createreplicationrelationship-msvm-replicationservice.md) ，以建立複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="11b11-105">The client passes an instance of this class to [**Msvm\_ReplicationService.CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) to create a replication relationship.</span></span> <span data-ttu-id="11b11-106">用戶端無法直接變更這個類別之任何屬性的值;它必須呼叫 [**Msvm \_ ReplicationService. ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) 方法來變更值。</span><span class="sxs-lookup"><span data-stu-id="11b11-106">The client can't directly change the values of any of the properties for this class; it must call the [**Msvm\_ReplicationService.ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) method to change the values.</span></span> <span data-ttu-id="11b11-107">每個複寫關聯性都有單一的設定實例。</span><span class="sxs-lookup"><span data-stu-id="11b11-107">Each replication relationship has a single instance of settings.</span></span>

<span data-ttu-id="11b11-108">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="11b11-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="11b11-109">語法</span><span class="sxs-lookup"><span data-stu-id="11b11-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationSettingData : CIM_VirtualSystemSettingData
{
  string   InstanceID = "Microsoft:Virtual Machine GUID\HVR";
  string   Caption = "Replication Settings";
  string   Description = "Virtual Machine Replication Settings Data";
  string   ElementName;
  string   VirtualSystemIdentifier;
  string   VirtualSystemType = "Microsoft:Hyper-V:Replica";
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
  uint16   AuthenticationType;
  string   CertificateThumbPrint;
  string   RootCertificateThumbPrint;
  boolean  CompressionEnabled;
  boolean  BypassProxyServer;
  string   RecoveryConnectionPoint;
  string   RecoveryHostSystem;
  string   PrimaryConnectionPoint;
  string   PrimaryHostSystem;
  uint16   RecoveryServerPortNumber = 0;
  boolean  ReplicateHostKvpItems = True;
  uint16   ApplicationConsistentSnapshotInterval;
  uint16   RecoveryHistory = 0;
  string   IncludedDisks[];
  boolean  AutoResynchronizeEnabled = False;
  datetime AutoResynchronizeIntervalStart = 00000000183000.000000:000;
  datetime AutoResynchronizeIntervalEnd = 00000000060000.000000:000;
  boolean  EnableWriteOrderPreservationAcrossDisks;
  string   ReplicationProvider;
  string   AdditionalSettings;
  uint16   ReplicationInterval = 300;
};
```

## <a name="members"></a><span data-ttu-id="11b11-110">成員</span><span class="sxs-lookup"><span data-stu-id="11b11-110">Members</span></span>

<span data-ttu-id="11b11-111">**Msvm \_ ReplicationSettingData** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="11b11-111">The **Msvm\_ReplicationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="11b11-112">屬性</span><span class="sxs-lookup"><span data-stu-id="11b11-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11b11-113">屬性</span><span class="sxs-lookup"><span data-stu-id="11b11-113">Properties</span></span>

<span data-ttu-id="11b11-114">**Msvm \_ ReplicationSettingData** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="11b11-114">The **Msvm\_ReplicationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11b11-115">**AdditionalSettings**</span><span class="sxs-lookup"><span data-stu-id="11b11-115">**AdditionalSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-118">端點提供者可以使用的其他複寫設定。</span><span class="sxs-lookup"><span data-stu-id="11b11-118">Additional replication settings that the endpoint provider can use.</span></span>

<span data-ttu-id="11b11-119">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="11b11-119">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-120">**ApplicationConsistentSnapshotInterval**</span><span class="sxs-lookup"><span data-stu-id="11b11-120">**ApplicationConsistentSnapshotInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-121">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="11b11-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-123">應用程式一致快照集之間的時間間隔，以小時為單位指定。</span><span class="sxs-lookup"><span data-stu-id="11b11-123">The time interval between application consistent snapshots, specified in hours.</span></span> <span data-ttu-id="11b11-124">有效的值為1小時到12小時。</span><span class="sxs-lookup"><span data-stu-id="11b11-124">Valid values are from 1 hour to 12 hours.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-125">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="11b11-125">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-126">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="11b11-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-128">定義用來連接到復原伺服器的驗證模式。</span><span class="sxs-lookup"><span data-stu-id="11b11-128">Define authentication mode used to connect to recover server.</span></span>

<dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="11b11-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos 驗證** (1) </span><span class="sxs-lookup"><span data-stu-id="11b11-129"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="11b11-130">Kerberos 驗證。</span><span class="sxs-lookup"><span data-stu-id="11b11-130">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="11b11-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>以 **憑證為基礎的驗證** (2) </span><span class="sxs-lookup"><span data-stu-id="11b11-131"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="11b11-132">以憑證為基礎的驗證。</span><span class="sxs-lookup"><span data-stu-id="11b11-132">Certificate based authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="11b11-133">**AutomaticRecoveryAction**</span><span class="sxs-lookup"><span data-stu-id="11b11-133">**AutomaticRecoveryAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-134">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="11b11-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-136">未使用。</span><span class="sxs-lookup"><span data-stu-id="11b11-136">Not used.</span></span>

<span data-ttu-id="11b11-137">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="11b11-137">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11b11-138">**AutomaticShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="11b11-138">**AutomaticShutdownAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="11b11-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-141">未使用。</span><span class="sxs-lookup"><span data-stu-id="11b11-141">Not used.</span></span>

<span data-ttu-id="11b11-142">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="11b11-142">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11b11-143">**AutomaticStartupAction**</span><span class="sxs-lookup"><span data-stu-id="11b11-143">**AutomaticStartupAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-144">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="11b11-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-146">未使用。</span><span class="sxs-lookup"><span data-stu-id="11b11-146">Not used.</span></span>

<span data-ttu-id="11b11-147">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="11b11-147">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11b11-148">**AutomaticStartupActionDelay**</span><span class="sxs-lookup"><span data-stu-id="11b11-148">**AutomaticStartupActionDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-149">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="11b11-149">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-151">虛擬機器自動啟動之前的延遲時間。</span><span class="sxs-lookup"><span data-stu-id="11b11-151">The delay time before the virtual machine is automatically started up.</span></span> <span data-ttu-id="11b11-152">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="11b11-152">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-153">**AutomaticStartupActionSequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="11b11-153">**AutomaticStartupActionSequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-154">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="11b11-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-155">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-156">數位，指出主機系統啟動時的虛擬機器啟用的相對順序。</span><span class="sxs-lookup"><span data-stu-id="11b11-156">A number that indicates the relative sequence of virtual machine activation when the host system is started.</span></span> <span data-ttu-id="11b11-157">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="11b11-157">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-158">**AutoResynchronizeEnabled**</span><span class="sxs-lookup"><span data-stu-id="11b11-158">**AutoResynchronizeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-159">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="11b11-159">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-160">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-161">指定是否在由於電源和硬體故障而發生複寫錯誤時，自動觸發重新同步作業。</span><span class="sxs-lookup"><span data-stu-id="11b11-161">Specifies whether resynchronization operations are automatically triggered when a replication error occurs due to power and hardware failures.</span></span> <span data-ttu-id="11b11-162">只有在 **AutoResynchronizeIntervalStart** 和 **AutoResynchronizeIntervalEnd** 屬性所指定的時間之間發生失敗時，才會觸發重新同步作業。</span><span class="sxs-lookup"><span data-stu-id="11b11-162">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="11b11-163">預設值為 **[False]** 。</span><span class="sxs-lookup"><span data-stu-id="11b11-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-164">**AutoResynchronizeIntervalEnd**</span><span class="sxs-lookup"><span data-stu-id="11b11-164">**AutoResynchronizeIntervalEnd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-165">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="11b11-165">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-167">指定要觸發自動重新同步處理作業的結束時間。</span><span class="sxs-lookup"><span data-stu-id="11b11-167">Specifies the end time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="11b11-168">這個值是當地時間。</span><span class="sxs-lookup"><span data-stu-id="11b11-168">This value is in local time.</span></span> <span data-ttu-id="11b11-169">預設值為 06:00 (6:00 A.M. ) 。</span><span class="sxs-lookup"><span data-stu-id="11b11-169">The default value is 06:00 (6:00 A.M.).</span></span>

<span data-ttu-id="11b11-170">只有在 **AutoResynchronizeIntervalStart** 和 **AutoResynchronizeIntervalEnd** 屬性所指定的時間之間發生失敗時，才會觸發重新同步作業。</span><span class="sxs-lookup"><span data-stu-id="11b11-170">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="11b11-171">重新同步處理作業也可以排程，以便在下一個間隔期間觸發。</span><span class="sxs-lookup"><span data-stu-id="11b11-171">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-172">**AutoResynchronizeIntervalStart**</span><span class="sxs-lookup"><span data-stu-id="11b11-172">**AutoResynchronizeIntervalStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-173">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="11b11-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-174">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-175">指定要觸發自動重新同步處理作業的開始時間。</span><span class="sxs-lookup"><span data-stu-id="11b11-175">Specifies the start time for automatic resynchronization operations to be triggered.</span></span> <span data-ttu-id="11b11-176">這個值是當地時間。</span><span class="sxs-lookup"><span data-stu-id="11b11-176">This value is in local time.</span></span> <span data-ttu-id="11b11-177">預設值為 18:30 (6:30 P.M. ) 。</span><span class="sxs-lookup"><span data-stu-id="11b11-177">The default value is 18:30 (6:30 P.M.).</span></span>

<span data-ttu-id="11b11-178">只有在 **AutoResynchronizeIntervalStart** 和 **AutoResynchronizeIntervalEnd** 屬性所指定的時間之間發生失敗時，才會觸發重新同步作業。</span><span class="sxs-lookup"><span data-stu-id="11b11-178">Resynchronization operations are only triggered when the failure occurs between the times specified by the **AutoResynchronizeIntervalStart** and **AutoResynchronizeIntervalEnd** properties.</span></span>

<span data-ttu-id="11b11-179">重新同步處理作業也可以排程，以便在下一個間隔期間觸發。</span><span class="sxs-lookup"><span data-stu-id="11b11-179">Resynchronization operations can also be scheduled so that they are triggered during the next interval.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-180">**BypassProxyServer**</span><span class="sxs-lookup"><span data-stu-id="11b11-180">**BypassProxyServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-181">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="11b11-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-183">指定在連接到復原伺服器時是否應略過 proxy 伺服器。</span><span class="sxs-lookup"><span data-stu-id="11b11-183">Specifies whether the proxy server should be bypassed when connecting to a recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-184">**標題**</span><span class="sxs-lookup"><span data-stu-id="11b11-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-187">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="11b11-187">A short description of the object.</span></span> <span data-ttu-id="11b11-188">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為「複寫設定」。</span><span class="sxs-lookup"><span data-stu-id="11b11-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Settings".</span></span>

</dd> <dt>

<span data-ttu-id="11b11-189">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="11b11-189">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-190">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b11-192">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128) </span><span class="sxs-lookup"><span data-stu-id="11b11-192">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="11b11-193">**AuthenticationType** 屬性為以憑證為基礎的驗證時，所要使用的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="11b11-193">Certificate thumbprint to use when the **AuthenticationType** property is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-194">**CompressionEnabled**</span><span class="sxs-lookup"><span data-stu-id="11b11-194">**CompressionEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-195">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="11b11-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-197">指定將複寫資料傳送到復原伺服器時，是否要將它壓縮。</span><span class="sxs-lookup"><span data-stu-id="11b11-197">Specifies whether replication data will be compressed while sending it to the recovery server.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-198">**ConfigurationDataRoot**</span><span class="sxs-lookup"><span data-stu-id="11b11-198">**ConfigurationDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-199">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-201">未使用。</span><span class="sxs-lookup"><span data-stu-id="11b11-201">Not used.</span></span>

<span data-ttu-id="11b11-202">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="11b11-202">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11b11-203">**ConfigurationFile**</span><span class="sxs-lookup"><span data-stu-id="11b11-203">**ConfigurationFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-205">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-206">儲存虛擬機器設定相關資訊之檔案的相對路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="11b11-206">The relative path and file name of a file where information about the virtual machine configuration is stored.</span></span> <span data-ttu-id="11b11-207">此路徑相對於 **ConfigurationDataRoot** 屬性。</span><span class="sxs-lookup"><span data-stu-id="11b11-207">This path is relative to the **ConfigurationDataRoot** property.</span></span> <span data-ttu-id="11b11-208">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="11b11-208">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-209">**ConfigurationID**</span><span class="sxs-lookup"><span data-stu-id="11b11-209">**ConfigurationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-212">虛擬機器設定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="11b11-212">The unique identifier of the virtual machine configuration.</span></span> <span data-ttu-id="11b11-213">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="11b11-213">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-214">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="11b11-214">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-215">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="11b11-215">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-216">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-217">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="11b11-217">The date and time at which the settings for the virtual machine were created.</span></span> <span data-ttu-id="11b11-218">如果此物件代表目前的虛擬機器設定，則此值會是系統建立的時間。</span><span class="sxs-lookup"><span data-stu-id="11b11-218">If this object represents the current settings for the virtual machine, this value would be the time at which the system was created.</span></span> <span data-ttu-id="11b11-219">如果此物件代表虛擬機器的快照集設定，則此值會是拍攝快照集的時間。</span><span class="sxs-lookup"><span data-stu-id="11b11-219">If this object represents the snapshot settings for the virtual machine, this value would be the time at which the snapshot was taken.</span></span> <span data-ttu-id="11b11-220">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="11b11-220">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

<span data-ttu-id="11b11-221">這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md)方法來變更。</span><span class="sxs-lookup"><span data-stu-id="11b11-221">This is a read-only property, but it can be changed by using the [**ModifySystemSettings**](modifysystemsettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="11b11-222">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="11b11-222">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11b11-223">**說明**</span><span class="sxs-lookup"><span data-stu-id="11b11-223">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-224">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-226">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="11b11-226">A description of the object.</span></span> <span data-ttu-id="11b11-227">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「虛擬機器複寫設定資料」。</span><span class="sxs-lookup"><span data-stu-id="11b11-227">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="11b11-228">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="11b11-228">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-229">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-231">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="11b11-231">A display name for the object.</span></span> <span data-ttu-id="11b11-232">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，它會設定為虛擬機器的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="11b11-232">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is set to the display name for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-233">**EnableWriteOrderPreservationAcrossDisks**</span><span class="sxs-lookup"><span data-stu-id="11b11-233">**EnableWriteOrderPreservationAcrossDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-234">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="11b11-234">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b11-236">限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「沒有值」 ) </span><span class="sxs-lookup"><span data-stu-id="11b11-236">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value")</span></span>
</dt> </dl>

<span data-ttu-id="11b11-237">指定是否將虛擬機器的所有複寫虛擬硬碟複寫到相同的時間點。</span><span class="sxs-lookup"><span data-stu-id="11b11-237">Specifies whether all replicating virtual hard disks for the virtual machine are replicated to the same point in time.</span></span> <span data-ttu-id="11b11-238">這可確保複寫在虛擬機器中接受應用程式的寫入順序。</span><span class="sxs-lookup"><span data-stu-id="11b11-238">This ensures replication honors the write-order of the applications in the virtual machine.</span></span>

<span data-ttu-id="11b11-239">**Windows 8.1：** 從 Windows 8.1 和 Windows Server 2012 R2 開始，這個屬性已被取代，而且一律設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="11b11-239">**Windows 8.1:** Beginning with Windows 8.1 and Windows Server 2012 R2, this property is deprecated and always set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-240">**IncludedDisks**</span><span class="sxs-lookup"><span data-stu-id="11b11-240">**IncludedDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-241">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="11b11-241">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="11b11-242">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b11-243">限定詞： **HyperVEmbeddedInstance** ( "CIM \_ StorageAllocationSettingData" ) ， [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) </span><span class="sxs-lookup"><span data-stu-id="11b11-243">Qualifiers: **HyperVEmbeddedInstance** ("CIM\_StorageAllocationSettingData"), [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="11b11-244">虛擬硬碟 (Vhd 的清單) 附加至複寫引擎將複寫的系統。</span><span class="sxs-lookup"><span data-stu-id="11b11-244">The list of virtual hard disks (VHDs) attached to the system that will be replicated by the replication engine.</span></span> <span data-ttu-id="11b11-245">這是字串的陣列，每個字串都包含代表 VHD 之 [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)的 **InstanceID** 。</span><span class="sxs-lookup"><span data-stu-id="11b11-245">This is an array of strings, each containing the **InstanceID** of the [**Msvm\_StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) that represents the VHD.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-246">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="11b11-246">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-247">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-248">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b11-249">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="11b11-249">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="11b11-250">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="11b11-250">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="11b11-251">這個屬性繼承自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="11b11-251">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span> <span data-ttu-id="11b11-252">針對 Windows 8，它一律會設定為 "Microsoft：*Virtual MACHINE GUID* \\ HVR"。</span><span class="sxs-lookup"><span data-stu-id="11b11-252">For Windows 8, it is always set to "Microsoft:*Virtual Machine GUID*\\HVR".</span></span> <span data-ttu-id="11b11-253">針對 Windows 8.1，它會設定為 "Microsoft：*Virtual MACHINE GUID* \\ HVR \\<0/1>"。</span><span class="sxs-lookup"><span data-stu-id="11b11-253">For Windows 8.1, it is set to "Microsoft:*Virtual Machine GUID*\\HVR\\<0/1>".</span></span> <span data-ttu-id="11b11-254">在 Windows 8.1 值中，0表示 primary，1表示擴充複寫。</span><span class="sxs-lookup"><span data-stu-id="11b11-254">In the Windows 8.1 value, 0 indicates primary and 1 indicates extended replication.</span></span> <span data-ttu-id="11b11-255">如需擴充複寫的詳細資訊，請參閱 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)。</span><span class="sxs-lookup"><span data-stu-id="11b11-255">For more info about extended replication, see [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md).</span></span>

</dd> <dt>

<span data-ttu-id="11b11-256">**LogDataRoot**</span><span class="sxs-lookup"><span data-stu-id="11b11-256">**LogDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-259">儲存虛擬機器記錄資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="11b11-259">The path of a directory where log information for the virtual machine is stored.</span></span> <span data-ttu-id="11b11-260">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="11b11-260">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-261">**注意事項**</span><span class="sxs-lookup"><span data-stu-id="11b11-261">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-262">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="11b11-262">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="11b11-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-264">未使用且無法設定。</span><span class="sxs-lookup"><span data-stu-id="11b11-264">Not used and can't be set.</span></span>

<span data-ttu-id="11b11-265">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="11b11-265">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11b11-266">**PrimaryConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="11b11-266">**PrimaryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b11-269">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="11b11-269">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="11b11-270">主要連接點的名稱。</span><span class="sxs-lookup"><span data-stu-id="11b11-270">The name of the primary connection point.</span></span> <span data-ttu-id="11b11-271">在主要叢集的案例中，這是 broker CAP 名稱。</span><span class="sxs-lookup"><span data-stu-id="11b11-271">In the case of a primary cluster, this is the broker CAP name.</span></span> <span data-ttu-id="11b11-272">在獨立主伺服器的情況下，這是主機系統名稱。</span><span class="sxs-lookup"><span data-stu-id="11b11-272">In the case of a standalone primary server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-273">**PrimaryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="11b11-273">**PrimaryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-274">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b11-276">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="11b11-276">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="11b11-277">裝載虛擬機器之主要主機系統的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b11-277">The fully qualified domain name of the primary host system that is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-278">**RecoveryConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="11b11-278">**RecoveryConnectionPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-279">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-280">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b11-281">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="11b11-281">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="11b11-282">復原連接點的名稱。</span><span class="sxs-lookup"><span data-stu-id="11b11-282">The name of the recovery connection point.</span></span> <span data-ttu-id="11b11-283">在復原叢集的情況下，這是 broker CAP 名稱。</span><span class="sxs-lookup"><span data-stu-id="11b11-283">In the case of a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="11b11-284">在獨立復原伺服器的情況下，這是主機系統名稱。</span><span class="sxs-lookup"><span data-stu-id="11b11-284">In the case of a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-285">**RecoveryFile**</span><span class="sxs-lookup"><span data-stu-id="11b11-285">**RecoveryFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-286">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-288">儲存虛擬機器修復相關資訊之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="11b11-288">The full path of a file where recovery related information for the virtual machine is stored.</span></span> <span data-ttu-id="11b11-289">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="11b11-289">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-290">**RecoveryHistory**</span><span class="sxs-lookup"><span data-stu-id="11b11-290">**RecoveryHistory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-291">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="11b11-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-292">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-293">復原伺服器上將儲存的復原快照集數目上限。</span><span class="sxs-lookup"><span data-stu-id="11b11-293">The maximum number of recovery snapshots that will be stored on the recovery server.</span></span> <span data-ttu-id="11b11-294">有效的值是從0到24。</span><span class="sxs-lookup"><span data-stu-id="11b11-294">Valid values are from 0 to 24.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-295">**RecoveryHostSystem**</span><span class="sxs-lookup"><span data-stu-id="11b11-295">**RecoveryHostSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-296">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-297">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b11-298">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="11b11-298">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="11b11-299">裝載虛擬機器之復原主機系統的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="11b11-299">The fully qualified domain name of the recovery host system which is hosting the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-300">**RecoveryServerPortNumber**</span><span class="sxs-lookup"><span data-stu-id="11b11-300">**RecoveryServerPortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-301">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="11b11-301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-302">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-302">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-303">建立安全連線以進行複寫時要使用的復原伺服器埠號碼。</span><span class="sxs-lookup"><span data-stu-id="11b11-303">The recovery server port number to use when making a secure connection for replication.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-304">**ReplicateHostKvpItems**</span><span class="sxs-lookup"><span data-stu-id="11b11-304">**ReplicateHostKvpItems**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-305">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="11b11-305">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-307">指定是否應該將主機專用的 [**Msvm \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)從主要虛擬機器複寫到復原虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="11b11-307">Specifies whether host-only [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md)s should be replicated from the primary virtual machine to the recovery virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-308">**ReplicationInterval**</span><span class="sxs-lookup"><span data-stu-id="11b11-308">**ReplicationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-309">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="11b11-309">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-310">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-311">複寫關聯性的複寫間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="11b11-311">Replication interval of a replication relationship in seconds.</span></span> <span data-ttu-id="11b11-312">有效值為：</span><span class="sxs-lookup"><span data-stu-id="11b11-312">Valid values are:</span></span>

<span data-ttu-id="11b11-313">30</span><span class="sxs-lookup"><span data-stu-id="11b11-313">30</span></span>

<span data-ttu-id="11b11-314">300</span><span class="sxs-lookup"><span data-stu-id="11b11-314">300</span></span>

<span data-ttu-id="11b11-315">900</span><span class="sxs-lookup"><span data-stu-id="11b11-315">900</span></span>

<span data-ttu-id="11b11-316">預設值為300秒。</span><span class="sxs-lookup"><span data-stu-id="11b11-316">Default value is 300 seconds.</span></span>

<span data-ttu-id="11b11-317">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="11b11-317">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-318">**ReplicationProvider**</span><span class="sxs-lookup"><span data-stu-id="11b11-318">**ReplicationProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-319">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-320">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-321">識別複寫提供者端點之 [**Msvm \_ ReplicationProvider**](msvm-replicationprovider.md) 類別實例的路徑。</span><span class="sxs-lookup"><span data-stu-id="11b11-321">The path to the instance of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class that identifies the replication provider endpoint.</span></span>

<span data-ttu-id="11b11-322">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="11b11-322">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-323">**RootCertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="11b11-323">**RootCertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-325">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="11b11-326">限定詞： [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128) </span><span class="sxs-lookup"><span data-stu-id="11b11-326">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="11b11-327">當 **AuthenticationType** 為 2 (以憑證為基礎的授權) 時，所使用之憑證的根憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="11b11-327">Root certificate thumbprint of the certificate in use when **AuthenticationType** is 2 (certificate based authorization).</span></span>

</dd> <dt>

<span data-ttu-id="11b11-328">**SnapshotDataRoot**</span><span class="sxs-lookup"><span data-stu-id="11b11-328">**SnapshotDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-329">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-331">儲存虛擬機器快照集相關資訊之目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="11b11-331">The path of a directory where information about the virtual machine snapshots is stored.</span></span> <span data-ttu-id="11b11-332">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="11b11-332">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-333">**SuspendDataRoot**</span><span class="sxs-lookup"><span data-stu-id="11b11-333">**SuspendDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-334">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-336">儲存虛擬機器暫停相關資訊之相關資訊的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="11b11-336">The path of a directory where information about the virtual machine suspend-related information is stored.</span></span> <span data-ttu-id="11b11-337">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="11b11-337">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-338">**SwapFileDataRoot**</span><span class="sxs-lookup"><span data-stu-id="11b11-338">**SwapFileDataRoot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-339">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-340">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-341">儲存虛擬機器之交換檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="11b11-341">The path of a directory where swap files for the virtual machine are stored.</span></span> <span data-ttu-id="11b11-342">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="11b11-342">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11b11-343">**VirtualSystemIdentifier**</span><span class="sxs-lookup"><span data-stu-id="11b11-343">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-344">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-346">這項設定資料所屬之 CIM 非程式物件的名稱。 [**\_**](/windows/desktop/CIMWin32Prov/cim-computersystem)</span><span class="sxs-lookup"><span data-stu-id="11b11-346">The name of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object to which this setting data belongs.</span></span> <span data-ttu-id="11b11-347">這個屬性是 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))的覆寫。</span><span class="sxs-lookup"><span data-stu-id="11b11-347">This property is an override from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11b11-348">**VirtualSystemType**</span><span class="sxs-lookup"><span data-stu-id="11b11-348">**VirtualSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11b11-349">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="11b11-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="11b11-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11b11-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11b11-351">指定設定資料所代表的虛擬機器類型。</span><span class="sxs-lookup"><span data-stu-id="11b11-351">Specifies the type of virtual machine the setting data represents.</span></span> <span data-ttu-id="11b11-352">這個屬性繼承自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))，且一律設定為 "Microsoft： hyper-v： Replica"。</span><span class="sxs-lookup"><span data-stu-id="11b11-352">This property is inherited from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)), and it is always set to "Microsoft:Hyper-V:Replica".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11b11-353">規格需求</span><span class="sxs-lookup"><span data-stu-id="11b11-353">Requirements</span></span>



| <span data-ttu-id="11b11-354">需求</span><span class="sxs-lookup"><span data-stu-id="11b11-354">Requirement</span></span> | <span data-ttu-id="11b11-355">值</span><span class="sxs-lookup"><span data-stu-id="11b11-355">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11b11-356">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11b11-356">Minimum supported client</span></span><br/> | <span data-ttu-id="11b11-357">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11b11-357">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="11b11-358">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11b11-358">Minimum supported server</span></span><br/> | <span data-ttu-id="11b11-359">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11b11-359">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11b11-360">命名空間</span><span class="sxs-lookup"><span data-stu-id="11b11-360">Namespace</span></span><br/>                | <span data-ttu-id="11b11-361">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="11b11-361">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="11b11-362">MOF</span><span class="sxs-lookup"><span data-stu-id="11b11-362">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11b11-363"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="11b11-363"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="11b11-364">DLL</span><span class="sxs-lookup"><span data-stu-id="11b11-364">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11b11-365"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="11b11-365"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="11b11-366">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11b11-366">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11b11-367">**CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="11b11-367">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> <dt>

[<span data-ttu-id="11b11-368">**ModifyReplicationSettings**</span><span class="sxs-lookup"><span data-stu-id="11b11-368">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)
</dt> </dl>

 

