---
description: 做為切換內服務的預留位置，以學習 MAC 位址並作為 Msvm \_ VirtualEthernetSwitch 和 Msvm DynamicForwardingEntry 類別之間的橋樑 \_ 。
ms.assetid: E617DBC3-F5DD-4875-B3CC-E120A2218EBE
title: Msvm_TransparentBridgingService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingService
- Msvm_TransparentBridgingService.InstanceID
- Msvm_TransparentBridgingService.Caption
- Msvm_TransparentBridgingService.Description
- Msvm_TransparentBridgingService.ElementName
- Msvm_TransparentBridgingService.InstallDate
- Msvm_TransparentBridgingService.OperationalStatus
- Msvm_TransparentBridgingService.StatusDescriptions
- Msvm_TransparentBridgingService.Status
- Msvm_TransparentBridgingService.HealthState
- Msvm_TransparentBridgingService.CommunicationStatus
- Msvm_TransparentBridgingService.DetailedStatus
- Msvm_TransparentBridgingService.OperatingStatus
- Msvm_TransparentBridgingService.PrimaryStatus
- Msvm_TransparentBridgingService.EnabledState
- Msvm_TransparentBridgingService.OtherEnabledState
- Msvm_TransparentBridgingService.RequestedState
- Msvm_TransparentBridgingService.EnabledDefault
- Msvm_TransparentBridgingService.TimeOfLastStateChange
- Msvm_TransparentBridgingService.AvailableRequestedStates
- Msvm_TransparentBridgingService.TransitioningToState
- Msvm_TransparentBridgingService.SystemCreationClassName
- Msvm_TransparentBridgingService.SystemName
- Msvm_TransparentBridgingService.CreationClassName
- Msvm_TransparentBridgingService.Name
- Msvm_TransparentBridgingService.PrimaryOwnerName
- Msvm_TransparentBridgingService.PrimaryOwnerContact
- Msvm_TransparentBridgingService.StartMode
- Msvm_TransparentBridgingService.Started
- Msvm_TransparentBridgingService.Keywords
- Msvm_TransparentBridgingService.ServiceURL
- Msvm_TransparentBridgingService.StartupConditions
- Msvm_TransparentBridgingService.StartupParameters
- Msvm_TransparentBridgingService.ProtocolType
- Msvm_TransparentBridgingService.OtherProtocolType
- Msvm_TransparentBridgingService.AgingTime
- Msvm_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f5daacf42bc221fa98f56d0c5b84140e3784c2ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943681"
---
# <a name="msvm_transparentbridgingservice-class"></a><span data-ttu-id="39fa1-103">Msvm \_ TransparentBridgingService 類別</span><span class="sxs-lookup"><span data-stu-id="39fa1-103">Msvm\_TransparentBridgingService class</span></span>

<span data-ttu-id="39fa1-104">做為切換內服務的預留位置，以學習 MAC 位址並作為 [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) 和 [**Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) 類別之間的橋樑。</span><span class="sxs-lookup"><span data-stu-id="39fa1-104">Serves as a placeholder for the service inside the switch that learns MAC addresses and serves as a bridge between the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) and [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) classes.</span></span>

<span data-ttu-id="39fa1-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="39fa1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="39fa1-106">語法</span><span class="sxs-lookup"><span data-stu-id="39fa1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingService : CIM_TransparentBridgingService
{
  string   InstanceID;
  string   Caption = "Virtual Switch Transparent Bridging Service";
  string   Description = "Microsoft Virtual Switch Transparent Bridging Service";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_TransparentBridgingService";
  string   Name;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode = "Automatic";
  boolean  Started = True;
  string   Keywords[];
  string   ServiceURL;
  string   StartupConditions[];
  string   StartupParameters[];
  uint16   ProtocolType = 15;
  string   OtherProtocolType;
  uint32   AgingTime = 300;
  uint32   FID = 0;
};
```

## <a name="members"></a><span data-ttu-id="39fa1-107">成員</span><span class="sxs-lookup"><span data-stu-id="39fa1-107">Members</span></span>

<span data-ttu-id="39fa1-108">**Msvm \_ TransparentBridgingService** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="39fa1-108">The **Msvm\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="39fa1-109">方法</span><span class="sxs-lookup"><span data-stu-id="39fa1-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="39fa1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="39fa1-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="39fa1-111">方法</span><span class="sxs-lookup"><span data-stu-id="39fa1-111">Methods</span></span>

<span data-ttu-id="39fa1-112">**Msvm \_ TransparentBridgingService** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="39fa1-112">The **Msvm\_TransparentBridgingService** class has these methods.</span></span>



| <span data-ttu-id="39fa1-113">方法</span><span class="sxs-lookup"><span data-stu-id="39fa1-113">Method</span></span>                                                                           | <span data-ttu-id="39fa1-114">描述</span><span class="sxs-lookup"><span data-stu-id="39fa1-114">Description</span></span>                         |
|:---------------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="39fa1-115">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="39fa1-115">**RequestStateChange**</span></span>](msvm-transparentbridgingservice-requeststatechange.md) | <span data-ttu-id="39fa1-116">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="39fa1-116">Requests a state change.</span></span><br/> |
| [<span data-ttu-id="39fa1-117">**StartService**</span><span class="sxs-lookup"><span data-stu-id="39fa1-117">**StartService**</span></span>](msvm-transparentbridgingservice-startservice.md)             | <span data-ttu-id="39fa1-118">啟動服務。</span><span class="sxs-lookup"><span data-stu-id="39fa1-118">Starts the service.</span></span><br/>      |
| [<span data-ttu-id="39fa1-119">**StopService**</span><span class="sxs-lookup"><span data-stu-id="39fa1-119">**StopService**</span></span>](msvm-transparentbridgingservice-stopservice.md)               | <span data-ttu-id="39fa1-120">停止服務。</span><span class="sxs-lookup"><span data-stu-id="39fa1-120">Stops the service.</span></span><br/>       |



 

### <a name="properties"></a><span data-ttu-id="39fa1-121">屬性</span><span class="sxs-lookup"><span data-stu-id="39fa1-121">Properties</span></span>

<span data-ttu-id="39fa1-122">**Msvm \_ TransparentBridgingService** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="39fa1-122">The **Msvm\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39fa1-123">**AgingTime**</span><span class="sxs-lookup"><span data-stu-id="39fa1-123">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-124">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="39fa1-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-126">以秒為單位的逾時間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="39fa1-126">The time-out period, in seconds, for aging out dynamically learned MAC addresses.</span></span> <span data-ttu-id="39fa1-127">這個屬性繼承自 [**CIM \_ TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-127">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-128">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="39fa1-128">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-129">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="39fa1-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-131">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="39fa1-131">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="39fa1-132">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="39fa1-132">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-133">**標題**</span><span class="sxs-lookup"><span data-stu-id="39fa1-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-134">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-135">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-136">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="39fa1-136">A short description of the object.</span></span> <span data-ttu-id="39fa1-137">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律為「虛擬交換器透明橋接服務」。</span><span class="sxs-lookup"><span data-stu-id="39fa1-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always "Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-138">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="39fa1-138">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-139">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39fa1-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-141">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="39fa1-141">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="39fa1-142">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="39fa1-142">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="39fa1-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-143">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="39fa1-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="39fa1-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="39fa1-145"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="39fa1-146"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="39fa1-147"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="39fa1-148"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="39fa1-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="39fa1-150"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="39fa1-151">)</span><span class="sxs-lookup"><span data-stu-id="39fa1-151">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39fa1-152">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="39fa1-152">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-155">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="39fa1-155">A short description of the object.</span></span> <span data-ttu-id="39fa1-156">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-156">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-157">**說明**</span><span class="sxs-lookup"><span data-stu-id="39fa1-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-160">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="39fa1-160">A description of the object.</span></span> <span data-ttu-id="39fa1-161">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)，一律設定為「Microsoft 虛擬交換器透明橋接服務」。</span><span class="sxs-lookup"><span data-stu-id="39fa1-161">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Virtual Switch Transparent Bridging Service".</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-162">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="39fa1-162">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-163">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39fa1-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-164">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-165">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="39fa1-165">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="39fa1-166">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="39fa1-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="39fa1-167">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="39fa1-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="39fa1-168"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="39fa1-169"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="39fa1-170"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="39fa1-171"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="39fa1-172"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="39fa1-173"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="39fa1-174"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="39fa1-175"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="39fa1-176">)</span><span class="sxs-lookup"><span data-stu-id="39fa1-176">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39fa1-177">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="39fa1-177">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-178">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-179">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-180">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="39fa1-180">A display name for the object.</span></span> <span data-ttu-id="39fa1-181">除了索引鍵屬性、身分識別資料和描述資訊之外，此屬性還可讓每個實例定義顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="39fa1-181">This property allows each instance to define a display name in addition to its key properties, identity data, and description information.</span></span> <span data-ttu-id="39fa1-182">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-182">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-183">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="39fa1-183">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-184">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39fa1-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-185">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-186">系統管理員的預設或啟動設定，適用于元素的啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="39fa1-186">An administrator's default or startup configuration for the Enabled State of an element.</span></span> <span data-ttu-id="39fa1-187">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="39fa1-187">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-188">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="39fa1-188">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-189">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39fa1-189">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-190">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-191">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="39fa1-191">The enabled and disabled states of an element.</span></span> <span data-ttu-id="39fa1-192">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="39fa1-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-193">**裂**</span><span class="sxs-lookup"><span data-stu-id="39fa1-193">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-194">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="39fa1-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-195">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-196">支援 VLAN 且擁有多個篩選資料庫的參數所使用的篩選資料庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="39fa1-196">The filtering database identifier used by switches that support VLAN and that have more than one filtering database.</span></span> <span data-ttu-id="39fa1-197">這個屬性繼承自 [**CIM \_ TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-197">This property is inherited from [**CIM\_TransparentBridgingService**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-198">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="39fa1-198">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-199">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39fa1-199">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-201">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="39fa1-201">The current health of the element.</span></span> <span data-ttu-id="39fa1-202">這個屬性會表示此元素的健全狀況，但不一定是它的子元件。</span><span class="sxs-lookup"><span data-stu-id="39fa1-202">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="39fa1-203">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-203">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-204">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="39fa1-204">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-205">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="39fa1-205">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-206">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-207">指定物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="39fa1-207">Specifies the time when the object was installed.</span></span> <span data-ttu-id="39fa1-208">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="39fa1-208">Lack of a value does not indicate that the object is not installed.</span></span> <span data-ttu-id="39fa1-209">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，而且不會使用它。</span><span class="sxs-lookup"><span data-stu-id="39fa1-209">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-210">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="39fa1-210">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-211">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-212">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-213">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="39fa1-213">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-214">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="39fa1-214">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="39fa1-215">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-215">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-216">**關鍵字**</span><span class="sxs-lookup"><span data-stu-id="39fa1-216">**Keywords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-217">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="39fa1-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-219">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="39fa1-219">Do not use.</span></span> <span data-ttu-id="39fa1-220">字串的自由格式陣列，提供可在查詢中使用的描述性單字和片語。</span><span class="sxs-lookup"><span data-stu-id="39fa1-220">A free-form array of strings that provide descriptive words and phrases that can be used in queries.</span></span> <span data-ttu-id="39fa1-221">因為未標準化，所以不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="39fa1-221">This property is not implemented because it is not standardized.</span></span> <span data-ttu-id="39fa1-222">如果這個屬性是必要的查詢結構，則在繼承階層中需要較高的版本。</span><span class="sxs-lookup"><span data-stu-id="39fa1-222">If this property were a necessary query construct, then it would be required higher in the inheritance hierarchy.</span></span> <span data-ttu-id="39fa1-223">這個屬性繼承自 [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="39fa1-223">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-224">**名稱**</span><span class="sxs-lookup"><span data-stu-id="39fa1-224">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-227">可唯一識別服務的名稱，並提供所管理功能的指示。</span><span class="sxs-lookup"><span data-stu-id="39fa1-227">A name that uniquely identifies the service and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="39fa1-228">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-228">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-229">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="39fa1-229">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-230">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39fa1-230">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-231">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-232">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="39fa1-232">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="39fa1-233">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="39fa1-233">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="39fa1-234">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-234">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="39fa1-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="39fa1-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="39fa1-236"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="39fa1-237"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="39fa1-238"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="39fa1-239"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="39fa1-240"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="39fa1-241"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="39fa1-242"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="39fa1-243"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="39fa1-244"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="39fa1-245"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="39fa1-246"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="39fa1-247"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="39fa1-248"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="39fa1-249"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="39fa1-250"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="39fa1-251"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="39fa1-252"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="39fa1-253"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="39fa1-254">)</span><span class="sxs-lookup"><span data-stu-id="39fa1-254">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39fa1-255">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="39fa1-255">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-256">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="39fa1-256">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-257">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-258">專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="39fa1-258">The current status of the element.</span></span> <span data-ttu-id="39fa1-259">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-260">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="39fa1-260">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-262">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-263">當 **EnabledState** 屬性設定為 1 (其他) 時，元素的啟用或停用狀態。</span><span class="sxs-lookup"><span data-stu-id="39fa1-263">The enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="39fa1-264">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且不會使用它。</span><span class="sxs-lookup"><span data-stu-id="39fa1-264">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-265">**OtherProtocolType**</span><span class="sxs-lookup"><span data-stu-id="39fa1-265">**OtherProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-266">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-267">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-268">當 **ProtocolType** 的值為 1 (其他) 時，所轉送的通訊協定類型。</span><span class="sxs-lookup"><span data-stu-id="39fa1-268">The type of protocol that is being forwarded when the value of **ProtocolType** is 1 (Other).</span></span> <span data-ttu-id="39fa1-269">這個屬性繼承自 [**CIM \_ ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-269">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-270">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="39fa1-270">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-271">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-272">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-273">提供有關如何聯繫服務主要擁有者之資訊的字串。</span><span class="sxs-lookup"><span data-stu-id="39fa1-273">A string that provides information about how the primary owner of the Service can be reached.</span></span> <span data-ttu-id="39fa1-274">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-274">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-275">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="39fa1-275">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-277">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-278">服務的主要擁有者名稱（如果有定義的話）。</span><span class="sxs-lookup"><span data-stu-id="39fa1-278">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="39fa1-279">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-279">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-280">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="39fa1-280">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-281">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39fa1-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-282">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-283">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="39fa1-283">Provides high level status information.</span></span> <span data-ttu-id="39fa1-284">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="39fa1-284">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="39fa1-285">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="39fa1-285">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="39fa1-286">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-286">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="39fa1-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="39fa1-287"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-288"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="39fa1-288"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="39fa1-289"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="39fa1-290"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="39fa1-291"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="39fa1-292"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="39fa1-293">)</span><span class="sxs-lookup"><span data-stu-id="39fa1-293">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="39fa1-294">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="39fa1-294">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-295">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39fa1-295">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-296">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-297">正在轉送的通訊協定類型。</span><span class="sxs-lookup"><span data-stu-id="39fa1-297">The type of protocol that is being forwarded.</span></span> <span data-ttu-id="39fa1-298">這個屬性繼承自 [**CIM \_ ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-298">This property is inherited from [**CIM\_ForwardingService**](/previous-versions/windows/desktop/clushyperv/cim-forwardingservice).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-299">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="39fa1-299">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-300">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39fa1-300">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-301">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-302">上次要求或預期的管理服務狀態。</span><span class="sxs-lookup"><span data-stu-id="39fa1-302">The last requested or desired state for the management service.</span></span> <span data-ttu-id="39fa1-303">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="39fa1-303">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-304">**ServiceURL**</span><span class="sxs-lookup"><span data-stu-id="39fa1-304">**ServiceURL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-305">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-306">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-307">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="39fa1-307">Do not use.</span></span> <span data-ttu-id="39fa1-308">提供存取服務所需的通訊協定、網路位置和其他服務特定資訊的 URL。</span><span class="sxs-lookup"><span data-stu-id="39fa1-308">A URL that provides the protocol, network location, and other service-specific information required to access the service.</span></span> <span data-ttu-id="39fa1-309">相反地，請使用 **ServiceAccessURI** 類別，它會正確地放置服務存取的語法，並說明資訊的格式。</span><span class="sxs-lookup"><span data-stu-id="39fa1-309">Instead, use the **ServiceAccessURI** class, which correctly positions the semantics of the service access, and clarifies the format of the information.</span></span> <span data-ttu-id="39fa1-310">這個屬性繼承自 [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="39fa1-310">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-311">**已開始**</span><span class="sxs-lookup"><span data-stu-id="39fa1-311">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-312">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="39fa1-312">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-313">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-313">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-314">指出服務是否已啟動 (**True**) ，或停止 (**False**) 。</span><span class="sxs-lookup"><span data-stu-id="39fa1-314">Indicates whether the service has been started (**True**), or stopped (**False**).</span></span> <span data-ttu-id="39fa1-315">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-315">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-316">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="39fa1-316">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-317">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-318">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-319">指出服務是否由系統自動啟動、作業系統等，或只在要求時才啟動。</span><span class="sxs-lookup"><span data-stu-id="39fa1-319">Indicates whether the service is automatically started by a system, an operating system, and so on, or is started only upon request.</span></span> <span data-ttu-id="39fa1-320">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-320">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-321">**StartupConditions**</span><span class="sxs-lookup"><span data-stu-id="39fa1-321">**StartupConditions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-322">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="39fa1-322">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-323">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-323">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-324">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="39fa1-324">Do not use.</span></span> <span data-ttu-id="39fa1-325">字串的自由格式陣列，指定必須符合才能正確啟動此服務的任何特定前置條件。</span><span class="sxs-lookup"><span data-stu-id="39fa1-325">A free-form array of strings that specify any specific preconditions that must be met for this service to start correctly.</span></span> <span data-ttu-id="39fa1-326">這個屬性不會很有用，因為它不是標準化的。</span><span class="sxs-lookup"><span data-stu-id="39fa1-326">This property is not useful because it is not standardized.</span></span> <span data-ttu-id="39fa1-327">如果這個屬性是必要的結構，則在服務) 上 (的繼承階層架構中需要較高層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="39fa1-327">If this property were a necessary construct, then it would be required higher in the inheritance hierarchy (on Service).</span></span> <span data-ttu-id="39fa1-328">這個屬性繼承自 [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="39fa1-328">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-329">**StartupParameters**</span><span class="sxs-lookup"><span data-stu-id="39fa1-329">**StartupParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-330">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="39fa1-330">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-331">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-332">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="39fa1-332">Do not use.</span></span> <span data-ttu-id="39fa1-333">字串的自由格式陣列，指定必須提供給 **StartService** 方法的任何特定參數，才能讓此服務正確啟動。</span><span class="sxs-lookup"><span data-stu-id="39fa1-333">A free-form array of strings that specify any specific parameters that must be supplied to the **StartService** method for this service to start correctly.</span></span> <span data-ttu-id="39fa1-334">如果這個方法經過調整，則其參數會更正式地傳達這項資訊。</span><span class="sxs-lookup"><span data-stu-id="39fa1-334">If this method were refined, then its parameters would more formally convey this information.</span></span> <span data-ttu-id="39fa1-335">這個屬性繼承自 [**CIM \_ NetworkService**](/previous-versions//cc136875(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="39fa1-335">This property is inherited from [**CIM\_NetworkService**](/previous-versions//cc136875(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-336">**狀態**</span><span class="sxs-lookup"><span data-stu-id="39fa1-336">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-337">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-338">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-339">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="39fa1-339">The current status of the object.</span></span> <span data-ttu-id="39fa1-340">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-340">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-341">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="39fa1-341">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-342">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="39fa1-342">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-343">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-344">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="39fa1-344">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="39fa1-345">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-345">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-346">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="39fa1-346">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-347">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-348">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-348">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-349">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="39fa1-349">The creation class name of the scoping system.</span></span> <span data-ttu-id="39fa1-350">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-350">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-351">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="39fa1-351">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-352">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="39fa1-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-353">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-354">主控電腦系統的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="39fa1-354">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="39fa1-355">這個屬性繼承自 [**CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-355">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-356">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="39fa1-356">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-357">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="39fa1-357">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-358">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-359">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="39fa1-359">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="39fa1-360">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且不會使用它。</span><span class="sxs-lookup"><span data-stu-id="39fa1-360">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="39fa1-361">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="39fa1-361">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39fa1-362">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="39fa1-362">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="39fa1-363">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="39fa1-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39fa1-364">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="39fa1-364">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="39fa1-365">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="39fa1-365">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39fa1-366">備註</span><span class="sxs-lookup"><span data-stu-id="39fa1-366">Remarks</span></span>

<span data-ttu-id="39fa1-367">存取 **Msvm \_ TransparentBridgingService** 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="39fa1-367">Access to the **Msvm\_TransparentBridgingService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="39fa1-368">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="39fa1-368">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="39fa1-369">規格需求</span><span class="sxs-lookup"><span data-stu-id="39fa1-369">Requirements</span></span>



| <span data-ttu-id="39fa1-370">需求</span><span class="sxs-lookup"><span data-stu-id="39fa1-370">Requirement</span></span> | <span data-ttu-id="39fa1-371">值</span><span class="sxs-lookup"><span data-stu-id="39fa1-371">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39fa1-372">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39fa1-372">Minimum supported client</span></span><br/> | <span data-ttu-id="39fa1-373">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39fa1-373">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="39fa1-374">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39fa1-374">Minimum supported server</span></span><br/> | <span data-ttu-id="39fa1-375">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39fa1-375">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39fa1-376">命名空間</span><span class="sxs-lookup"><span data-stu-id="39fa1-376">Namespace</span></span><br/>                | <span data-ttu-id="39fa1-377">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="39fa1-377">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="39fa1-378">MOF</span><span class="sxs-lookup"><span data-stu-id="39fa1-378">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39fa1-379"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="39fa1-379"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39fa1-380">DLL</span><span class="sxs-lookup"><span data-stu-id="39fa1-380">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39fa1-381"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39fa1-381"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="39fa1-382">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39fa1-382">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39fa1-383">**CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="39fa1-383">**CIM\_TransparentBridgingService**</span></span>](cim-transparentbridgingservice.md)
</dt> <dt>

[<span data-ttu-id="39fa1-384">**CIM \_ TransparentBridgingService**</span><span class="sxs-lookup"><span data-stu-id="39fa1-384">**CIM\_TransparentBridgingService**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingservice)
</dt> </dl>

 

