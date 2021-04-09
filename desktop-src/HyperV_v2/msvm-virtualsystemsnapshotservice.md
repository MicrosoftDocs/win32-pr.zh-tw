---
description: 用來建立、套用和終結虛擬機器快照集的服務。
ms.assetid: 34efe124-d198-4bad-a3c9-e8457a5faa5e
title: Msvm_VirtualSystemSnapshotService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService
- Msvm_VirtualSystemSnapshotService.StartService
- Msvm_VirtualSystemSnapshotService.StopService
- Msvm_VirtualSystemSnapshotService.InstanceID
- Msvm_VirtualSystemSnapshotService.Caption
- Msvm_VirtualSystemSnapshotService.Description
- Msvm_VirtualSystemSnapshotService.ElementName
- Msvm_VirtualSystemSnapshotService.InstallDate
- Msvm_VirtualSystemSnapshotService.Name
- Msvm_VirtualSystemSnapshotService.OperationalStatus
- Msvm_VirtualSystemSnapshotService.StatusDescriptions
- Msvm_VirtualSystemSnapshotService.Status
- Msvm_VirtualSystemSnapshotService.HealthState
- Msvm_VirtualSystemSnapshotService.CommunicationStatus
- Msvm_VirtualSystemSnapshotService.DetailedStatus
- Msvm_VirtualSystemSnapshotService.OperatingStatus
- Msvm_VirtualSystemSnapshotService.PrimaryStatus
- Msvm_VirtualSystemSnapshotService.EnabledState
- Msvm_VirtualSystemSnapshotService.OtherEnabledState
- Msvm_VirtualSystemSnapshotService.RequestedState
- Msvm_VirtualSystemSnapshotService.EnabledDefault
- Msvm_VirtualSystemSnapshotService.TimeOfLastStateChange
- Msvm_VirtualSystemSnapshotService.AvailableRequestedStates
- Msvm_VirtualSystemSnapshotService.TransitioningToState
- Msvm_VirtualSystemSnapshotService.SystemCreationClassName
- Msvm_VirtualSystemSnapshotService.SystemName
- Msvm_VirtualSystemSnapshotService.CreationClassName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerName
- Msvm_VirtualSystemSnapshotService.PrimaryOwnerContact
- Msvm_VirtualSystemSnapshotService.StartMode
- Msvm_VirtualSystemSnapshotService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be84d70dd9478012e747626a9a566464d7587789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847757"
---
# <a name="msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="31116-103">Msvm \_ VirtualSystemSnapshotService 類別</span><span class="sxs-lookup"><span data-stu-id="31116-103">Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="31116-104">用來建立、套用和終結虛擬機器快照集的服務。</span><span class="sxs-lookup"><span data-stu-id="31116-104">Service to create, apply, and destroy snapshots of virtual machines.</span></span>

<span data-ttu-id="31116-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="31116-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31116-106">語法</span><span class="sxs-lookup"><span data-stu-id="31116-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSnapshotService : CIM_VirtualSystemSnapshotService
{
  string   InstanceID;
  string   Caption = "Hyper-V Virtual System Snapshot Service";
  string   Description = "Service for creating, destroying, and applying virtual machine snapshots";
  string   ElementName;
  datetime InstallDate;
  string   Name = "vssnapsvc";
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
  uint16   TransitioningToState = 12;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemSnapshotService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="31116-107">成員</span><span class="sxs-lookup"><span data-stu-id="31116-107">Members</span></span>

<span data-ttu-id="31116-108">**Msvm \_ VirtualSystemSnapshotService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="31116-108">The **Msvm\_VirtualSystemSnapshotService** class has these types of members:</span></span>

-   [<span data-ttu-id="31116-109">方法</span><span class="sxs-lookup"><span data-stu-id="31116-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="31116-110">屬性</span><span class="sxs-lookup"><span data-stu-id="31116-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="31116-111">方法</span><span class="sxs-lookup"><span data-stu-id="31116-111">Methods</span></span>

<span data-ttu-id="31116-112">**Msvm \_ VirtualSystemSnapshotService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="31116-112">The **Msvm\_VirtualSystemSnapshotService** class has these methods.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="31116-113">方法</span><span class="sxs-lookup"><span data-stu-id="31116-113">Method</span></span></th>
<th style="text-align: left;"><span data-ttu-id="31116-114">描述</span><span class="sxs-lookup"><span data-stu-id="31116-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="31116-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="31116-115"><a href="applysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>ApplySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="31116-116">將虛擬機器快照集套用至其建立來源的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="31116-116">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="31116-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span><span class="sxs-lookup"><span data-stu-id="31116-117"><a href="clearsnapshotstate-msvm-virtualsystemsnapshotservice.md"><strong>ClearSnapshotState</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="31116-118">清除現有快照集的儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="31116-118">Clears save state from an existing snapshot.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="31116-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="31116-119"><a href="msvm-virtualsystemsnapshotservice-converttoreferencepoint.md"><strong>ConvertToReferencePoint</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="31116-120">將現有的虛擬系統快照集轉換為參考點。</span><span class="sxs-lookup"><span data-stu-id="31116-120">Convert an existing virtual system snapshot to a reference point.</span></span> <span data-ttu-id="31116-121">快照集會被刪除做為副作用。</span><span class="sxs-lookup"><span data-stu-id="31116-121">The snapshot gets deleted as a side effect.</span></span> <span data-ttu-id="31116-122">只有修復快照集可以轉換成參考點。</span><span class="sxs-lookup"><span data-stu-id="31116-122">Only recovery snapshots can be converted to reference points.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="31116-123">已將此方法的支援新增至 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="31116-123">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="31116-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>>icloudblob.createsnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="31116-124"><a href="createsnapshot-msvm-virtualsystemsnapshotservice.md"><strong>CreateSnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="31116-125">建立虛擬機器的快照集。</span><span class="sxs-lookup"><span data-stu-id="31116-125">Creates a snapshot of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="31116-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span><span class="sxs-lookup"><span data-stu-id="31116-126"><a href="destroysnapshot-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshot</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="31116-127">終結現有的虛擬機器快照集。</span><span class="sxs-lookup"><span data-stu-id="31116-127">Destroy an existing virtual machine snapshot.</span></span> <span data-ttu-id="31116-128">這個方法可能會損毀其他相依于受影響快照集的快照集。</span><span class="sxs-lookup"><span data-stu-id="31116-128">This method may, as a side effect, destroy other snapshots that are dependent on the affected snapshot.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="31116-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span><span class="sxs-lookup"><span data-stu-id="31116-129"><a href="destroysnapshottree-msvm-virtualsystemsnapshotservice.md"><strong>DestroySnapshotTree</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="31116-130">移除虛擬機器的現有快照集及其所有子系。</span><span class="sxs-lookup"><span data-stu-id="31116-130">Removes an existing snapshot, and all its children, of a virtual machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="31116-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span><span class="sxs-lookup"><span data-stu-id="31116-131"><a href="msvm-virtualsystemsnapshotservice-requeststatechange.md"><strong>RequestStateChange</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="31116-132">要求元素的狀態變更。</span><span class="sxs-lookup"><span data-stu-id="31116-132">Requests a state change for the element.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="31116-133">已將此方法的支援新增至 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="31116-133">Support for this method was added in Windows 10.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="31116-134"><strong>StartService</strong></span><span class="sxs-lookup"><span data-stu-id="31116-134"><strong>StartService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="31116-135">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="31116-135">This method is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="31116-136"><strong>StopService</strong></span><span class="sxs-lookup"><span data-stu-id="31116-136"><strong>StopService</strong></span></span></td>
<td style="text-align: left;"><span data-ttu-id="31116-137">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="31116-137">This method is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a><span data-ttu-id="31116-138">屬性</span><span class="sxs-lookup"><span data-stu-id="31116-138">Properties</span></span>

<span data-ttu-id="31116-139">**Msvm \_ VirtualSystemSnapshotService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="31116-139">The **Msvm\_VirtualSystemSnapshotService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31116-140">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="31116-140">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-141">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="31116-141">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="31116-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-143">指出用於起始狀態變更之 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="31116-143">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method used to initiate a state change.</span></span> <span data-ttu-id="31116-144">列出的值將會是與 **cim \_ EnabledLogicalElementCapabilities** 相關聯的實例之 **RequestedStatesSupported** 屬性中所含值的子集，其中選取的值是 [**cim \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))物件目前狀態的函式。</span><span class="sxs-lookup"><span data-stu-id="31116-144">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="31116-145">如果實作為目前狀態的函式，則這個屬性可以是非 **Null** 的值。</span><span class="sxs-lookup"><span data-stu-id="31116-145">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="31116-146">如果實作為目前狀態的函式無法判斷可能的值集，這個屬性將會是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="31116-146">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="31116-147">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="31116-147">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="31116-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) </span><span class="sxs-lookup"><span data-stu-id="31116-148"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="31116-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) </span><span class="sxs-lookup"><span data-stu-id="31116-149"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="31116-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) </span><span class="sxs-lookup"><span data-stu-id="31116-150"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="31116-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) </span><span class="sxs-lookup"><span data-stu-id="31116-151"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="31116-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) </span><span class="sxs-lookup"><span data-stu-id="31116-152"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="31116-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) </span><span class="sxs-lookup"><span data-stu-id="31116-153"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="31116-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) </span><span class="sxs-lookup"><span data-stu-id="31116-154"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="31116-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) </span><span class="sxs-lookup"><span data-stu-id="31116-155"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="31116-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) </span><span class="sxs-lookup"><span data-stu-id="31116-156"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="31116-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="31116-157"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="31116-158">)</span><span class="sxs-lookup"><span data-stu-id="31116-158">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31116-159">**標題**</span><span class="sxs-lookup"><span data-stu-id="31116-159">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-160">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-162">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="31116-162">A short description of the object.</span></span> <span data-ttu-id="31116-163">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Hyper-v 虛擬系統快照集服務」。</span><span class="sxs-lookup"><span data-stu-id="31116-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Snapshot Service".</span></span>

</dd> <dt>

<span data-ttu-id="31116-164">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="31116-164">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-165">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="31116-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31116-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-167">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="31116-167">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="31116-168">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="31116-168">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="31116-169">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="31116-169">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="31116-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="31116-170"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="31116-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="31116-171"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="31116-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="31116-172"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="31116-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="31116-173"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="31116-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="31116-174"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="31116-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="31116-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="31116-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="31116-176"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="31116-177">)</span><span class="sxs-lookup"><span data-stu-id="31116-177">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31116-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="31116-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-179">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-180">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31116-181">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="31116-181">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="31116-182">建立實例時所使用之類別或子類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="31116-182">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="31116-183">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 "Msvm \_ VirtualSystemSnapshotService"。</span><span class="sxs-lookup"><span data-stu-id="31116-183">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemSnapshotService".</span></span>

</dd> <dt>

<span data-ttu-id="31116-184">**說明**</span><span class="sxs-lookup"><span data-stu-id="31116-184">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-185">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-186">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-187">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="31116-187">A description of the object.</span></span> <span data-ttu-id="31116-188">這個屬性是從 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)繼承而來，而且一律設定為「服務以建立、終結及套用虛擬機器快照集」。</span><span class="sxs-lookup"><span data-stu-id="31116-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, destroying, and applying virtual machine snapshots".</span></span>

</dd> <dt>

<span data-ttu-id="31116-189">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="31116-189">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-190">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="31116-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31116-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-192">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="31116-192">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="31116-193">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="31116-193">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="31116-194">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="31116-194">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="31116-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="31116-195"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="31116-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="31116-196"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="31116-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="31116-197"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="31116-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="31116-198"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="31116-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="31116-199"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="31116-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="31116-200"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="31116-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="31116-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="31116-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="31116-202"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="31116-203">)</span><span class="sxs-lookup"><span data-stu-id="31116-203">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31116-204">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="31116-204">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-205">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-207">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="31116-207">A display name for the object.</span></span> <span data-ttu-id="31116-208">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="31116-208">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="31116-209">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="31116-209">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-210">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="31116-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31116-211">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-212">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="31116-212">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="31116-213">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="31116-213">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="31116-214">值</span><span class="sxs-lookup"><span data-stu-id="31116-214">Value</span></span>                                                                        | <span data-ttu-id="31116-215">意義</span><span class="sxs-lookup"><span data-stu-id="31116-215">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="31116-216"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="31116-216"><dt>2</dt></span></span> </dl> | <span data-ttu-id="31116-217">已啟用</span><span class="sxs-lookup"><span data-stu-id="31116-217">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="31116-218">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="31116-218">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-219">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="31116-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31116-220">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-221">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="31116-221">The enabled and disabled states of an element.</span></span> <span data-ttu-id="31116-222">也可以指出這些要求狀態之間的轉換。</span><span class="sxs-lookup"><span data-stu-id="31116-222">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="31116-223">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="31116-223">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="31116-224">值</span><span class="sxs-lookup"><span data-stu-id="31116-224">Value</span></span>                                                                        | <span data-ttu-id="31116-225">意義</span><span class="sxs-lookup"><span data-stu-id="31116-225">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="31116-226"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="31116-226"><dt>2</dt></span></span> </dl> | <span data-ttu-id="31116-227">已啟用</span><span class="sxs-lookup"><span data-stu-id="31116-227">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="31116-228">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="31116-228">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-229">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="31116-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31116-230">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-231">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="31116-231">The current health of the element.</span></span> <span data-ttu-id="31116-232">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="31116-232">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="31116-233">可能的值為0到30，其中5表示元素完全狀況良好，而30表示元素完全無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="31116-233">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="31116-234">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 5 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="31116-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="31116-235">值</span><span class="sxs-lookup"><span data-stu-id="31116-235">Value</span></span>                                                                        | <span data-ttu-id="31116-236">意義</span><span class="sxs-lookup"><span data-stu-id="31116-236">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="31116-237"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="31116-237"><dt>5</dt></span></span> </dl> | <span data-ttu-id="31116-238">健全狀況狀態為 [正常]。</span><span class="sxs-lookup"><span data-stu-id="31116-238">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="31116-239">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="31116-239">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-240">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="31116-240">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31116-241">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-242">建立虛擬機器設定的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="31116-242">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="31116-243">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="31116-243">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="31116-244">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="31116-244">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-245">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-246">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31116-247">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="31116-247">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="31116-248">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="31116-248">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="31116-249">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="31116-249">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="31116-250">**名稱**</span><span class="sxs-lookup"><span data-stu-id="31116-250">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-251">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-252">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31116-253">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="31116-253">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="31116-254">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="31116-254">The label by which the object is known.</span></span> <span data-ttu-id="31116-255">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且一律設定為 "vssnapsvc"。</span><span class="sxs-lookup"><span data-stu-id="31116-255">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vssnapsvc".</span></span>

</dd> <dt>

<span data-ttu-id="31116-256">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="31116-256">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-257">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="31116-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31116-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-259">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="31116-259">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="31116-260">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="31116-260">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="31116-261">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="31116-261">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="31116-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="31116-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="31116-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="31116-263"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="31116-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="31116-264"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="31116-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="31116-265"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="31116-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="31116-266"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="31116-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="31116-267"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="31116-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="31116-268"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="31116-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="31116-269"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="31116-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="31116-270"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="31116-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="31116-271"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="31116-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="31116-272"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="31116-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="31116-273"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="31116-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="31116-274"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="31116-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="31116-275"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="31116-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="31116-276"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="31116-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="31116-277"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="31116-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="31116-278"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="31116-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="31116-279"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="31116-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="31116-280"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="31116-281">)</span><span class="sxs-lookup"><span data-stu-id="31116-281">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31116-282">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="31116-282">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-283">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="31116-283">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="31116-284">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-285">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="31116-285">The current statuses of the object.</span></span> <span data-ttu-id="31116-286">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為 2 (確定) 。</span><span class="sxs-lookup"><span data-stu-id="31116-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="31116-287">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="31116-287">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-289">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-290">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="31116-290">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="31116-291">當 **EnabledState** 是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="31116-291">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="31116-292">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="31116-292">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="31116-293">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="31116-293">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-294">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-295">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31116-296">限定詞： **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="31116-296">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="31116-297">有關如何聯繫服務主要擁有者的任何資訊 (例如電話號碼、電子郵件地址等等) 。</span><span class="sxs-lookup"><span data-stu-id="31116-297">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="31116-298">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="31116-298">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="31116-299">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="31116-299">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-301">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31116-302">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="31116-302">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="31116-303">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="31116-303">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="31116-304">主要擁有者是服務的初始支援連絡人。</span><span class="sxs-lookup"><span data-stu-id="31116-304">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="31116-305">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="31116-305">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="31116-306">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="31116-306">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-307">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="31116-307">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31116-308">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-309">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="31116-309">Provides high level status information.</span></span> <span data-ttu-id="31116-310">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="31116-310">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="31116-311">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="31116-311">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="31116-312">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="31116-312">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="31116-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="31116-313"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="31116-314"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="31116-314"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="31116-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="31116-315"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="31116-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="31116-316"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="31116-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="31116-317"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="31116-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="31116-318"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="31116-319">)</span><span class="sxs-lookup"><span data-stu-id="31116-319">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31116-320">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="31116-320">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-321">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="31116-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31116-322">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-323">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="31116-323">The last requested or desired state for the element.</span></span> <span data-ttu-id="31116-324">元素的實際狀態是由 **EnabledState** 表示。</span><span class="sxs-lookup"><span data-stu-id="31116-324">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="31116-325">系統會提供這個屬性來比較專案的最後一個要求和目前狀態。</span><span class="sxs-lookup"><span data-stu-id="31116-325">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="31116-326">[**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))類別的特定實例可能不支援 **RequestedState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="31116-326">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="31116-327">如果發生這種情況，則會使用值 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="31116-327">If this occurs, the value 12 (Not Applicable) is used.</span></span> <span data-ttu-id="31116-328">這個屬性繼承自 **CIM \_ EnabledLogicalElement**，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="31116-328">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="31116-329">值</span><span class="sxs-lookup"><span data-stu-id="31116-329">Value</span></span>                                                                         | <span data-ttu-id="31116-330">意義</span><span class="sxs-lookup"><span data-stu-id="31116-330">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="31116-331"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="31116-331"><dt>12</dt></span></span> </dl> | <span data-ttu-id="31116-332">不適用。</span><span class="sxs-lookup"><span data-stu-id="31116-332">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="31116-333">**已開始**</span><span class="sxs-lookup"><span data-stu-id="31116-333">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-334">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="31116-334">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="31116-335">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-336">指出服務目前是否正在執行。</span><span class="sxs-lookup"><span data-stu-id="31116-336">Indicates whether the service is currently running.</span></span> <span data-ttu-id="31116-337">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="31116-337">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="31116-338">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="31116-338">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-339">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-339">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-340">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31116-341">限定詞： **MaxLen** ( 10 ) </span><span class="sxs-lookup"><span data-stu-id="31116-341">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="31116-342">字串值，表示服務是由系統自動啟動、作業系統還是只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="31116-342">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="31116-343">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)，一律設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="31116-343">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="31116-344">**狀態**</span><span class="sxs-lookup"><span data-stu-id="31116-344">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-345">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-347">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="31116-347">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="31116-348">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="31116-348">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-349">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="31116-349">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="31116-350">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-351">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="31116-351">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="31116-352">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且每個陣列元素一律設定為「服務正在正常執行」。</span><span class="sxs-lookup"><span data-stu-id="31116-352">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="31116-353">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="31116-353">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-354">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-355">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31116-356">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="31116-356">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="31116-357">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="31116-357">The scoping system's creation class name.</span></span> <span data-ttu-id="31116-358">這個屬性是從 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)繼承而來的，而且一律設定為「Msvm 的程式集」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="31116-358">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="31116-359">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="31116-359">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-360">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="31116-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31116-361">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31116-362">限定詞： **Key**、 **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="31116-362">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="31116-363">主控電腦系統的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="31116-363">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="31116-364">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="31116-364">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="31116-365">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="31116-365">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-366">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="31116-366">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="31116-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-368">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="31116-368">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="31116-369">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="31116-369">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="31116-370">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="31116-370">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31116-371">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="31116-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="31116-372">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="31116-372">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31116-373">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="31116-373">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="31116-374">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="31116-374">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="31116-375">值</span><span class="sxs-lookup"><span data-stu-id="31116-375">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="31116-376">意義</span><span class="sxs-lookup"><span data-stu-id="31116-376">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="31116-377"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31116-377"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="31116-378"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="31116-378"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="31116-379"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="31116-379"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="31116-380"><dt>**關機**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="31116-380"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="31116-381"><dt>**無變更**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="31116-381"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="31116-382">沒有進行中的轉換。</span><span class="sxs-lookup"><span data-stu-id="31116-382">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="31116-383"><dt>**離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="31116-383"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="31116-384"><dt>**測試**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="31116-384"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="31116-385"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="31116-385"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="31116-386"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="31116-386"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="31116-387"><dt>**重新開機**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="31116-387"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="31116-388"><dt>**重設**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="31116-388"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="31116-389"><dt>**不適用**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="31116-389"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="31116-390">此執行不支援表示進行中的轉換。</span><span class="sxs-lookup"><span data-stu-id="31116-390">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="31116-391">已 <dt>**保留 DMTF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="31116-391"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31116-392">規格需求</span><span class="sxs-lookup"><span data-stu-id="31116-392">Requirements</span></span>



| <span data-ttu-id="31116-393">需求</span><span class="sxs-lookup"><span data-stu-id="31116-393">Requirement</span></span> | <span data-ttu-id="31116-394">值</span><span class="sxs-lookup"><span data-stu-id="31116-394">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31116-395">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31116-395">Minimum supported client</span></span><br/> | <span data-ttu-id="31116-396">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31116-396">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="31116-397">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31116-397">Minimum supported server</span></span><br/> | <span data-ttu-id="31116-398">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31116-398">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31116-399">命名空間</span><span class="sxs-lookup"><span data-stu-id="31116-399">Namespace</span></span><br/>                | <span data-ttu-id="31116-400">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="31116-400">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="31116-401">MOF</span><span class="sxs-lookup"><span data-stu-id="31116-401">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31116-402"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="31116-402"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="31116-403">DLL</span><span class="sxs-lookup"><span data-stu-id="31116-403">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31116-404"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="31116-404"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

