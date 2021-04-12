---
description: 管理虛擬機器的複寫。
ms.assetid: 0335fb94-5f2b-43be-bfb4-bc6811c5b507
title: Msvm_ReplicationService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService
- Msvm_ReplicationService.InstanceID
- Msvm_ReplicationService.Caption
- Msvm_ReplicationService.Description
- Msvm_ReplicationService.ElementName
- Msvm_ReplicationService.InstallDate
- Msvm_ReplicationService.Name
- Msvm_ReplicationService.OperationalStatus
- Msvm_ReplicationService.StatusDescriptions
- Msvm_ReplicationService.Status
- Msvm_ReplicationService.HealthState
- Msvm_ReplicationService.CommunicationStatus
- Msvm_ReplicationService.DetailedStatus
- Msvm_ReplicationService.OperatingStatus
- Msvm_ReplicationService.PrimaryStatus
- Msvm_ReplicationService.EnabledState
- Msvm_ReplicationService.OtherEnabledState
- Msvm_ReplicationService.RequestedState
- Msvm_ReplicationService.EnabledDefault
- Msvm_ReplicationService.TimeOfLastStateChange
- Msvm_ReplicationService.AvailableRequestedStates
- Msvm_ReplicationService.TransitioningToState
- Msvm_ReplicationService.SystemCreationClassName
- Msvm_ReplicationService.SystemName
- Msvm_ReplicationService.CreationClassName
- Msvm_ReplicationService.PrimaryOwnerName
- Msvm_ReplicationService.PrimaryOwnerContact
- Msvm_ReplicationService.StartMode
- Msvm_ReplicationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86e9140e2fe9b047c57c762be2e0fba048511993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193321"
---
# <a name="msvm_replicationservice-class"></a><span data-ttu-id="c70eb-103">Msvm \_ ReplicationService 類別</span><span class="sxs-lookup"><span data-stu-id="c70eb-103">Msvm\_ReplicationService class</span></span>

<span data-ttu-id="c70eb-104">管理虛擬機器的複寫。</span><span class="sxs-lookup"><span data-stu-id="c70eb-104">Manages the replication for a virtual machine.</span></span>

<span data-ttu-id="c70eb-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c70eb-106">語法</span><span class="sxs-lookup"><span data-stu-id="c70eb-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Replica Service";
  string   Description = "Replication Service";
  string   ElementName;
  datetime InstallDate;
  string   Name = "replicasvc";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status = "OK";
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
  string   CreationClassName = "Msvm_ReplicationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="c70eb-107">成員</span><span class="sxs-lookup"><span data-stu-id="c70eb-107">Members</span></span>

<span data-ttu-id="c70eb-108">**Msvm \_ ReplicationService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c70eb-108">The **Msvm\_ReplicationService** class has these types of members:</span></span>

-   [<span data-ttu-id="c70eb-109">方法</span><span class="sxs-lookup"><span data-stu-id="c70eb-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c70eb-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c70eb-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c70eb-111">方法</span><span class="sxs-lookup"><span data-stu-id="c70eb-111">Methods</span></span>

<span data-ttu-id="c70eb-112">**Msvm \_ ReplicationService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c70eb-112">The **Msvm\_ReplicationService** class has these methods.</span></span>



| <span data-ttu-id="c70eb-113">方法</span><span class="sxs-lookup"><span data-stu-id="c70eb-113">Method</span></span>                                                                                                 | <span data-ttu-id="c70eb-114">描述</span><span class="sxs-lookup"><span data-stu-id="c70eb-114">Description</span></span>                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c70eb-115">**AddAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c70eb-115">**AddAuthorizationEntry**</span></span>](addauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="c70eb-116">將授權專案加入至伺服器。</span><span class="sxs-lookup"><span data-stu-id="c70eb-116">Adds an authorization entry to a server.</span></span><br/>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="c70eb-117">**ChangeReplicationModeToPrimary**</span><span class="sxs-lookup"><span data-stu-id="c70eb-117">**ChangeReplicationModeToPrimary**</span></span>](changereplicationmodetoprimary-msvm-replicationservice.md)       | <span data-ttu-id="c70eb-118">將延伸複寫關聯性變更為複本虛擬機器的主要關聯性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-118">Changes the extended replication relationship to the primary relationship for a replica virtual machine.</span></span> <span data-ttu-id="c70eb-119">複本虛擬機器必須處於容錯移轉認可狀態。</span><span class="sxs-lookup"><span data-stu-id="c70eb-119">The replica virtual machine must be in a failover committed state.</span></span><br/> <span data-ttu-id="c70eb-120">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c70eb-120">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/> |
| [<span data-ttu-id="c70eb-121">**CommitFailover**</span><span class="sxs-lookup"><span data-stu-id="c70eb-121">**CommitFailover**</span></span>](commitfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="c70eb-122">認可 [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) 方法用於容錯移轉的修復快照。</span><span class="sxs-lookup"><span data-stu-id="c70eb-122">Commits the recovery snapshot that the [**InitiateFailover**](initiatefailover-msvm-replicationservice.md) method has used for a failover.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="c70eb-123">**>createreplicationrelationship**</span><span class="sxs-lookup"><span data-stu-id="c70eb-123">**CreateReplicationRelationship**</span></span>](createreplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="c70eb-124">為虛擬機器建立新的複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-124">Creates a new replication relationship for a virtual machine.</span></span><br/>                                                                                                                                                                                                                      |
| [<span data-ttu-id="c70eb-125">**GetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="c70eb-125">**GetReplicationStatistics**</span></span>](getreplicationstatistics-msvm-replicationservice.md)                   | <span data-ttu-id="c70eb-126">抓取虛擬機器的複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="c70eb-126">Retrieves replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                            |
| [<span data-ttu-id="c70eb-127">**GetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="c70eb-127">**GetReplicationStatisticsEx**</span></span>](getreplicationstatisticsex-msvm-replicationservice.md)               | <span data-ttu-id="c70eb-128">抓取與虛擬機器的指定複寫關聯性相關聯的複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="c70eb-128">Retrieves the replication statistics that are associated with specified replication relationship of the virtual machine.</span></span><br/> <span data-ttu-id="c70eb-129">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c70eb-129">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                    |
| [<span data-ttu-id="c70eb-130">**GetSystemCertificates**</span><span class="sxs-lookup"><span data-stu-id="c70eb-130">**GetSystemCertificates**</span></span>](getsystemcertificates-msvm-replicationservice.md)                         | <span data-ttu-id="c70eb-131">抓取主機系統上的系統憑證。</span><span class="sxs-lookup"><span data-stu-id="c70eb-131">Retrieves the system certificates on a host system.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="c70eb-132">**ImportInitialReplica**</span><span class="sxs-lookup"><span data-stu-id="c70eb-132">**ImportInitialReplica**</span></span>](importinitialreplica-msvm-replicationservice.md)                           | <span data-ttu-id="c70eb-133">匯入虛擬機器的初始複寫。</span><span class="sxs-lookup"><span data-stu-id="c70eb-133">Imports the initial replication for a virtual machine.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="c70eb-134">**InitiateFailback**</span><span class="sxs-lookup"><span data-stu-id="c70eb-134">**InitiateFailback**</span></span>](initiatefailback-msvm-replicationservice.md)                                   | <span data-ttu-id="c70eb-135">起始復原虛擬機器的容錯回復。</span><span class="sxs-lookup"><span data-stu-id="c70eb-135">Initiates the failback for a recovery virtual machine.</span></span> <span data-ttu-id="c70eb-136">也就是說，會將虛擬機器的容錯移轉設定為應用程式或損毀一致映射。</span><span class="sxs-lookup"><span data-stu-id="c70eb-136">That is, sets the failover for the virtual machine to an app or crash consistent image.</span></span><br/> <span data-ttu-id="c70eb-137">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c70eb-137">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                              |
| [<span data-ttu-id="c70eb-138">**InitiateFailover**</span><span class="sxs-lookup"><span data-stu-id="c70eb-138">**InitiateFailover**</span></span>](initiatefailover-msvm-replicationservice.md)                                   | <span data-ttu-id="c70eb-139">起始虛擬機器對應用程式或標準複寫點映射的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c70eb-139">Initiates a failover for a virtual machine to an application or standard replication point image.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="c70eb-140">**ModifyAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c70eb-140">**ModifyAuthorizationEntry**</span></span>](modifyauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="c70eb-141">修改伺服器上的授權專案。</span><span class="sxs-lookup"><span data-stu-id="c70eb-141">Modifies an authorization entry on a server.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="c70eb-142">**ModifyReplicationSettings**</span><span class="sxs-lookup"><span data-stu-id="c70eb-142">**ModifyReplicationSettings**</span></span>](modifyreplicationsettings-msvm-replicationservice.md)                 | <span data-ttu-id="c70eb-143">修改虛擬機器的複寫設定。</span><span class="sxs-lookup"><span data-stu-id="c70eb-143">Modifies the replication settings for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="c70eb-144">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="c70eb-144">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)                         | <span data-ttu-id="c70eb-145">修改 Hyper-v 複本服務的設定。</span><span class="sxs-lookup"><span data-stu-id="c70eb-145">Modifies the settings for the Hyper-V Replica service.</span></span><br/>                                                                                                                                                                                                                             |
| [<span data-ttu-id="c70eb-146">**RemoveAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c70eb-146">**RemoveAuthorizationEntry**</span></span>](removeauthorizationentry-msvm-replicationservice.md)                   | <span data-ttu-id="c70eb-147">從伺服器移除授權專案。</span><span class="sxs-lookup"><span data-stu-id="c70eb-147">Removes the authorization entry from a server.</span></span><br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="c70eb-148">**RemoveReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="c70eb-148">**RemoveReplicationRelationship**</span></span>](removereplicationrelationship-msvm-replicationservice.md)         | <span data-ttu-id="c70eb-149">移除虛擬機器複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-149">Removes a virtual machine replication relationship.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="c70eb-150">**RemoveReplicationRelationshipEx**</span><span class="sxs-lookup"><span data-stu-id="c70eb-150">**RemoveReplicationRelationshipEx**</span></span>](removereplicationrelationshipex-msvm-replicationservice.md)     | <span data-ttu-id="c70eb-151">移除指定的虛擬機器複寫關聯性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-151">Removes the specified virtual machine replication relationship.</span></span> <span data-ttu-id="c70eb-152">若為複本虛擬機器，如果已啟用延伸複寫，則無法移除主要複寫。</span><span class="sxs-lookup"><span data-stu-id="c70eb-152">For a replica virtual machine, primary replication can't be removed if extended replication is enabled.</span></span><br/> <span data-ttu-id="c70eb-153">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c70eb-153">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>     |
| [<span data-ttu-id="c70eb-154">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="c70eb-154">**RequestStateChange**</span></span>](msvm-replicationservice-requeststatechange.md)                               | <span data-ttu-id="c70eb-155">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="c70eb-155">Requests a state change.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="c70eb-156">**ResetReplicationStatistics**</span><span class="sxs-lookup"><span data-stu-id="c70eb-156">**ResetReplicationStatistics**</span></span>](resetreplicationstatistics-msvm-replicationservice.md)               | <span data-ttu-id="c70eb-157">重設虛擬機器的複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="c70eb-157">Resets the replication statistics for a virtual machine.</span></span><br/>                                                                                                                                                                                                                           |
| [<span data-ttu-id="c70eb-158">**ResetReplicationStatisticsEx**</span><span class="sxs-lookup"><span data-stu-id="c70eb-158">**ResetReplicationStatisticsEx**</span></span>](resetreplicationstatisticsex-msvm-replicationservice.md)           | <span data-ttu-id="c70eb-159">重設與虛擬機器的指定複寫關聯性相關聯的複寫統計資料。</span><span class="sxs-lookup"><span data-stu-id="c70eb-159">Resets replication statistics that are associated with the specified replication relationship of a virtual machine.</span></span><br/> <span data-ttu-id="c70eb-160">**Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="c70eb-160">**Windows 8.1:** This method is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span><br/>                                                         |
| [<span data-ttu-id="c70eb-161">**重新同步處理**</span><span class="sxs-lookup"><span data-stu-id="c70eb-161">**Resynchronize**</span></span>](resynchronize-msvm-replicationservice.md)                                         | <span data-ttu-id="c70eb-162">在指定的虛擬機器上執行重新同步處理操作。</span><span class="sxs-lookup"><span data-stu-id="c70eb-162">Performs a resynchronization operation on the specified virtual machine.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="c70eb-163">**ReverseReplicationRelationship**</span><span class="sxs-lookup"><span data-stu-id="c70eb-163">**ReverseReplicationRelationship**</span></span>](reversereplicationrelationship-msvm-replicationservice.md)       | <span data-ttu-id="c70eb-164">將已容錯移轉的虛擬機器複寫回主伺服器。</span><span class="sxs-lookup"><span data-stu-id="c70eb-164">Replicates a failed-over virtual machine back to the primary server.</span></span><br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="c70eb-165">**RevertFailover**</span><span class="sxs-lookup"><span data-stu-id="c70eb-165">**RevertFailover**</span></span>](revertfailover-msvm-replicationservice.md)                                       | <span data-ttu-id="c70eb-166">藉由捨棄目前的容錯移轉磁片來還原虛擬機器目前的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="c70eb-166">Reverts the current failover for a virtual machine by discarding the current failover disk.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="c70eb-167">**SetAuthorizationEntry**</span><span class="sxs-lookup"><span data-stu-id="c70eb-167">**SetAuthorizationEntry**</span></span>](setauthorizationentry-msvm-replicationservice.md)                         | <span data-ttu-id="c70eb-168">設定虛擬機器的複寫授權專案。</span><span class="sxs-lookup"><span data-stu-id="c70eb-168">Sets the replication authorization entry for a virtual machine.</span></span><br/>                                                                                                                                                                                                                    |
| [<span data-ttu-id="c70eb-169">**SetFailoverNetworkAdapterSettings**</span><span class="sxs-lookup"><span data-stu-id="c70eb-169">**SetFailoverNetworkAdapterSettings**</span></span>](setfailovernetworkadaptersettings-msvm-replicationservice.md) | <span data-ttu-id="c70eb-170">設定要在容錯移轉之後套用至虛擬機器的網路介面卡 IP 設定。</span><span class="sxs-lookup"><span data-stu-id="c70eb-170">Configures the network adapter's IP settings to be applied to a virtual machine after a failover.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="c70eb-171">**>startreplication**</span><span class="sxs-lookup"><span data-stu-id="c70eb-171">**StartReplication**</span></span>](startreplication-msvm-replicationservice.md)                                   | <span data-ttu-id="c70eb-172">啟動虛擬機器的複寫。</span><span class="sxs-lookup"><span data-stu-id="c70eb-172">Starts the replication of a virtual machine.</span></span><br/>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="c70eb-173">**StartService**</span><span class="sxs-lookup"><span data-stu-id="c70eb-173">**StartService**</span></span>](msvm-replicationservice-startservice.md)                                           | <span data-ttu-id="c70eb-174">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="c70eb-174">Starts the service.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="c70eb-175">**StopService**</span><span class="sxs-lookup"><span data-stu-id="c70eb-175">**StopService**</span></span>](msvm-replicationservice-stopservice.md)                                             | <span data-ttu-id="c70eb-176">停止服務。</span><span class="sxs-lookup"><span data-stu-id="c70eb-176">Stops the service.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="c70eb-177">**TestReplicaSystem**</span><span class="sxs-lookup"><span data-stu-id="c70eb-177">**TestReplicaSystem**</span></span>](testreplicasystem-msvm-replicationservice.md)                                 | <span data-ttu-id="c70eb-178">使用指定的快照集建立虛擬機器的新複本，以供測試之用。</span><span class="sxs-lookup"><span data-stu-id="c70eb-178">Creates a new replica of a virtual machine with the specified snapshot for testing purposes.</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="c70eb-179">**TestReplicationConnection**</span><span class="sxs-lookup"><span data-stu-id="c70eb-179">**TestReplicationConnection**</span></span>](testreplicationconnection-msvm-replicationservice.md)                 | <span data-ttu-id="c70eb-180">確認是否可以從目前的主機系統啟用複寫到指定的復原系統。</span><span class="sxs-lookup"><span data-stu-id="c70eb-180">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span><br/>                                                                                                                                                                          |



 

### <a name="properties"></a><span data-ttu-id="c70eb-181">屬性</span><span class="sxs-lookup"><span data-stu-id="c70eb-181">Properties</span></span>

<span data-ttu-id="c70eb-182">**Msvm \_ ReplicationService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-182">The **Msvm\_ReplicationService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c70eb-183">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="c70eb-183">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-184">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c70eb-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-186">指出 *RequestedState* 參數的可能值。</span><span class="sxs-lookup"><span data-stu-id="c70eb-186">Indicates the possible values for the *RequestedState* parameter.</span></span> <span data-ttu-id="c70eb-187">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c70eb-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-188">**標題**</span><span class="sxs-lookup"><span data-stu-id="c70eb-188">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-191">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="c70eb-191">A short description of the object.</span></span> <span data-ttu-id="c70eb-192">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「hyper-v 複本服務」。</span><span class="sxs-lookup"><span data-stu-id="c70eb-192">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Replica Service".</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-193">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="c70eb-193">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-194">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c70eb-194">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-196">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="c70eb-196">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="c70eb-197">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-197">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c70eb-198">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c70eb-198">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c70eb-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c70eb-199"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="c70eb-200"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="c70eb-201"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="c70eb-202"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="c70eb-203"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c70eb-204"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c70eb-205"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c70eb-206">)</span><span class="sxs-lookup"><span data-stu-id="c70eb-206">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c70eb-207">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c70eb-207">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-210">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="c70eb-210">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-211">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="c70eb-211">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="c70eb-212">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "Msvm \_ ReplicationService"。</span><span class="sxs-lookup"><span data-stu-id="c70eb-212">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ReplicationService".</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-213">**說明**</span><span class="sxs-lookup"><span data-stu-id="c70eb-213">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-214">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-215">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-216">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="c70eb-216">A description of the object.</span></span> <span data-ttu-id="c70eb-217">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為 "Replication Service"。</span><span class="sxs-lookup"><span data-stu-id="c70eb-217">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service".</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-218">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="c70eb-218">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-219">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c70eb-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-221">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c70eb-221">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="c70eb-222">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-222">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c70eb-223">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c70eb-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c70eb-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="c70eb-224"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="c70eb-225"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="c70eb-226"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="c70eb-227"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="c70eb-228"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="c70eb-229"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c70eb-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c70eb-231"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c70eb-232">)</span><span class="sxs-lookup"><span data-stu-id="c70eb-232">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c70eb-233">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c70eb-233">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-235">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-235">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-236">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c70eb-236">A display name for the object.</span></span> <span data-ttu-id="c70eb-237">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="c70eb-237">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-238">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="c70eb-238">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-239">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c70eb-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-240">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-240">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-241">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="c70eb-241">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="c70eb-242">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="c70eb-242">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="c70eb-243">值</span><span class="sxs-lookup"><span data-stu-id="c70eb-243">Value</span></span>                                                                        | <span data-ttu-id="c70eb-244">意義</span><span class="sxs-lookup"><span data-stu-id="c70eb-244">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c70eb-245"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c70eb-245"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c70eb-246">已啟用</span><span class="sxs-lookup"><span data-stu-id="c70eb-246">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c70eb-247">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="c70eb-247">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-248">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c70eb-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-249">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-250">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="c70eb-250">The enabled and disabled states of an element.</span></span> <span data-ttu-id="c70eb-251">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="c70eb-251">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="c70eb-252">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="c70eb-252">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="c70eb-253">值</span><span class="sxs-lookup"><span data-stu-id="c70eb-253">Value</span></span>                                                                        | <span data-ttu-id="c70eb-254">意義</span><span class="sxs-lookup"><span data-stu-id="c70eb-254">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="c70eb-255"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c70eb-255"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c70eb-256">已啟用</span><span class="sxs-lookup"><span data-stu-id="c70eb-256">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c70eb-257">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="c70eb-257">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-258">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c70eb-258">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-259">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-259">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-260">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="c70eb-260">The current health of the element.</span></span> <span data-ttu-id="c70eb-261">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="c70eb-261">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="c70eb-262">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="c70eb-262">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="c70eb-263">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="c70eb-263">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="c70eb-264">值</span><span class="sxs-lookup"><span data-stu-id="c70eb-264">Value</span></span>                                                                        | <span data-ttu-id="c70eb-265">意義</span><span class="sxs-lookup"><span data-stu-id="c70eb-265">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="c70eb-266"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c70eb-266"><dt>5</dt></span></span> </dl> | <span data-ttu-id="c70eb-267">健全狀況狀態為 [正常]。</span><span class="sxs-lookup"><span data-stu-id="c70eb-267">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c70eb-268">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c70eb-268">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-269">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c70eb-269">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-270">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-271">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="c70eb-271">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="c70eb-272">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c70eb-272">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-273">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c70eb-273">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-274">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-275">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-276">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="c70eb-276">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-277">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="c70eb-277">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c70eb-278">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c70eb-278">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-279">**名稱**</span><span class="sxs-lookup"><span data-stu-id="c70eb-279">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-280">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-281">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-282">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="c70eb-282">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-283">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="c70eb-283">The label by which the object is known.</span></span> <span data-ttu-id="c70eb-284">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "replicasvc"。</span><span class="sxs-lookup"><span data-stu-id="c70eb-284">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "replicasvc".</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-285">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="c70eb-285">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-286">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c70eb-286">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-287">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-288">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c70eb-288">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="c70eb-289">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-289">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c70eb-290">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c70eb-290">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c70eb-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c70eb-291"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="c70eb-292"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="c70eb-293"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="c70eb-294"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="c70eb-295"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="c70eb-296"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="c70eb-297"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="c70eb-298"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="c70eb-299"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="c70eb-300"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="c70eb-301"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="c70eb-302"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="c70eb-303"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="c70eb-304"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="c70eb-305"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="c70eb-306"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="c70eb-307"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c70eb-308"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c70eb-309"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c70eb-310">)</span><span class="sxs-lookup"><span data-stu-id="c70eb-310">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c70eb-311">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="c70eb-311">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-312">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="c70eb-312">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-314">陣列，其中包含物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c70eb-314">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="c70eb-315">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c70eb-315">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="c70eb-316">位於索引零的值將會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c70eb-316">The value at index zero will be one of the following values.</span></span>



| <span data-ttu-id="c70eb-317">值</span><span class="sxs-lookup"><span data-stu-id="c70eb-317">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="c70eb-318">意義</span><span class="sxs-lookup"><span data-stu-id="c70eb-318">Meaning</span></span>                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="c70eb-319"><dt>**確定**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c70eb-319"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                  | <span data-ttu-id="c70eb-320">複寫服務正常運作。</span><span class="sxs-lookup"><span data-stu-id="c70eb-320">The replication service is operating normally.</span></span><br/>                                                                     |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span><dl> <span data-ttu-id="c70eb-321"><dt>**錯誤**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c70eb-321"><dt>**Error**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="c70eb-322">一或多個複寫網路接聽程式未執行。</span><span class="sxs-lookup"><span data-stu-id="c70eb-322">One or more replication network listeners are not running.</span></span> <span data-ttu-id="c70eb-323">請確認複寫服務設定是否有效。</span><span class="sxs-lookup"><span data-stu-id="c70eb-323">Verify that the replication service settings are valid.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c70eb-324">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="c70eb-324">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-325">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-326">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-327">描述當 **EnabledState** 屬性設定為 1 ( "Other" ) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="c70eb-327">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="c70eb-328">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c70eb-328">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="c70eb-329">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c70eb-329">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-330">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="c70eb-330">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-331">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-332">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-333">限定詞： **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="c70eb-333">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-334">有關如何聯繫服務主要擁有者的任何資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="c70eb-334">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="c70eb-335">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c70eb-335">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-336">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="c70eb-336">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-339">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="c70eb-339">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-340">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="c70eb-340">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="c70eb-341">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="c70eb-341">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="c70eb-342">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c70eb-342">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-343">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="c70eb-343">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-344">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c70eb-344">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-345">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-345">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-346">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="c70eb-346">Provides high level status information.</span></span> <span data-ttu-id="c70eb-347">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="c70eb-347">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="c70eb-348">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-348">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="c70eb-349">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c70eb-349">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="c70eb-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="c70eb-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-351"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="c70eb-351"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="c70eb-352"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="c70eb-353"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="c70eb-354"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="c70eb-355"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="c70eb-356">)</span><span class="sxs-lookup"><span data-stu-id="c70eb-356">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c70eb-357">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="c70eb-357">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-358">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c70eb-358">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-359">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-360">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="c70eb-360">The last requested or desired state for the element.</span></span> <span data-ttu-id="c70eb-361">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="c70eb-361">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="c70eb-362">系統會提供這個屬性來比較專案的最後一個要求和目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c70eb-362">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="c70eb-363">[**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))類別的特定實例可能不支援 **RequestedState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c70eb-363">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="c70eb-364">如果發生這種情況，則會使用值 12 ( 「不適用」 ) 。</span><span class="sxs-lookup"><span data-stu-id="c70eb-364">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="c70eb-365">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="c70eb-365">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="c70eb-366">值</span><span class="sxs-lookup"><span data-stu-id="c70eb-366">Value</span></span>                                                                         | <span data-ttu-id="c70eb-367">意義</span><span class="sxs-lookup"><span data-stu-id="c70eb-367">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="c70eb-368"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c70eb-368"><dt>12</dt></span></span> </dl> | <span data-ttu-id="c70eb-369">不適用。</span><span class="sxs-lookup"><span data-stu-id="c70eb-369">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c70eb-370">**已開始**</span><span class="sxs-lookup"><span data-stu-id="c70eb-370">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-371">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="c70eb-371">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-373">指出服務目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="c70eb-373">Indicates whether the service is currently running.</span></span> <span data-ttu-id="c70eb-374">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="c70eb-374">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-375">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="c70eb-375">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-376">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-377">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-377">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-378">限定詞： **MaxLen** ( 10 ) </span><span class="sxs-lookup"><span data-stu-id="c70eb-378">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-379">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="c70eb-379">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="c70eb-380">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c70eb-380">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-381">**狀態**</span><span class="sxs-lookup"><span data-stu-id="c70eb-381">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-382">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-383">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-383">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-384">指出元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="c70eb-384">Indicates the status of the element.</span></span> <span data-ttu-id="c70eb-385">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "OK"。</span><span class="sxs-lookup"><span data-stu-id="c70eb-385">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-386">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="c70eb-386">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-387">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="c70eb-387">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-388">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-388">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-389">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="c70eb-389">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="c70eb-390">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="c70eb-390">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-391">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="c70eb-391">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-392">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-392">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-393">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-394">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="c70eb-394">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-395">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="c70eb-395">The scoping system's creation class name.</span></span> <span data-ttu-id="c70eb-396">這個屬性是從 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)繼承而來的，而且一律設定為「Msvm 的程式集」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c70eb-396">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-397">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="c70eb-397">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-398">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c70eb-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-400">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="c70eb-400">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-401">主控電腦系統的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="c70eb-401">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="c70eb-402">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="c70eb-402">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-403">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="c70eb-403">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-404">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c70eb-404">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-405">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-406">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="c70eb-406">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="c70eb-407">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c70eb-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c70eb-408">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="c70eb-408">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c70eb-409">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="c70eb-409">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c70eb-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c70eb-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c70eb-411">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="c70eb-411">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="c70eb-412">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c70eb-412">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c70eb-413">規格需求</span><span class="sxs-lookup"><span data-stu-id="c70eb-413">Requirements</span></span>



| <span data-ttu-id="c70eb-414">需求</span><span class="sxs-lookup"><span data-stu-id="c70eb-414">Requirement</span></span> | <span data-ttu-id="c70eb-415">值</span><span class="sxs-lookup"><span data-stu-id="c70eb-415">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c70eb-416">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c70eb-416">Minimum supported client</span></span><br/> | <span data-ttu-id="c70eb-417">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c70eb-417">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c70eb-418">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c70eb-418">Minimum supported server</span></span><br/> | <span data-ttu-id="c70eb-419">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c70eb-419">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c70eb-420">命名空間</span><span class="sxs-lookup"><span data-stu-id="c70eb-420">Namespace</span></span><br/>                | <span data-ttu-id="c70eb-421">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="c70eb-421">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c70eb-422">MOF</span><span class="sxs-lookup"><span data-stu-id="c70eb-422">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c70eb-423"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="c70eb-423"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c70eb-424">DLL</span><span class="sxs-lookup"><span data-stu-id="c70eb-424">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c70eb-425"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c70eb-425"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

