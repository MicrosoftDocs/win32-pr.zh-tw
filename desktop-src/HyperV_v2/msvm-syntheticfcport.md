---
description: 代表綜合光纖通道埠。
ms.assetid: 6ca827b5-3ea0-4967-ba1f-b41e84c84009
title: Msvm_SyntheticFcPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPort
- Msvm_SyntheticFcPort.SetPowerState
- Msvm_SyntheticFcPort.EnableDevice
- Msvm_SyntheticFcPort.OnlineDevice
- Msvm_SyntheticFcPort.QuiesceDevice
- Msvm_SyntheticFcPort.SaveProperties
- Msvm_SyntheticFcPort.RestoreProperties
- Msvm_SyntheticFcPort.InstanceID
- Msvm_SyntheticFcPort.Caption
- Msvm_SyntheticFcPort.Description
- Msvm_SyntheticFcPort.ElementName
- Msvm_SyntheticFcPort.InstallDate
- Msvm_SyntheticFcPort.Name
- Msvm_SyntheticFcPort.OperationalStatus
- Msvm_SyntheticFcPort.StatusDescriptions
- Msvm_SyntheticFcPort.Status
- Msvm_SyntheticFcPort.HealthState
- Msvm_SyntheticFcPort.CommunicationStatus
- Msvm_SyntheticFcPort.DetailedStatus
- Msvm_SyntheticFcPort.OperatingStatus
- Msvm_SyntheticFcPort.PrimaryStatus
- Msvm_SyntheticFcPort.EnabledState
- Msvm_SyntheticFcPort.OtherEnabledState
- Msvm_SyntheticFcPort.RequestedState
- Msvm_SyntheticFcPort.EnabledDefault
- Msvm_SyntheticFcPort.TimeOfLastStateChange
- Msvm_SyntheticFcPort.AvailableRequestedStates
- Msvm_SyntheticFcPort.TransitioningToState
- Msvm_SyntheticFcPort.SystemCreationClassName
- Msvm_SyntheticFcPort.SystemName
- Msvm_SyntheticFcPort.CreationClassName
- Msvm_SyntheticFcPort.DeviceID
- Msvm_SyntheticFcPort.PowerManagementSupported
- Msvm_SyntheticFcPort.PowerManagementCapabilities
- Msvm_SyntheticFcPort.Availability
- Msvm_SyntheticFcPort.StatusInfo
- Msvm_SyntheticFcPort.LastErrorCode
- Msvm_SyntheticFcPort.ErrorDescription
- Msvm_SyntheticFcPort.ErrorCleared
- Msvm_SyntheticFcPort.OtherIdentifyingInfo
- Msvm_SyntheticFcPort.PowerOnHours
- Msvm_SyntheticFcPort.TotalPowerOnHours
- Msvm_SyntheticFcPort.IdentifyingDescriptions
- Msvm_SyntheticFcPort.AdditionalAvailability
- Msvm_SyntheticFcPort.MaxQuiesceTime
- Msvm_SyntheticFcPort.Speed
- Msvm_SyntheticFcPort.MaxSpeed
- Msvm_SyntheticFcPort.RequestedSpeed
- Msvm_SyntheticFcPort.UsageRestriction
- Msvm_SyntheticFcPort.PortType
- Msvm_SyntheticFcPort.OtherPortType
- Msvm_SyntheticFcPort.OtherNetworkPortType
- Msvm_SyntheticFcPort.PortNumber
- Msvm_SyntheticFcPort.LinkTechnology
- Msvm_SyntheticFcPort.OtherLinkTechnology
- Msvm_SyntheticFcPort.PermanentAddress
- Msvm_SyntheticFcPort.NetworkAddresses
- Msvm_SyntheticFcPort.FullDuplex
- Msvm_SyntheticFcPort.AutoSense
- Msvm_SyntheticFcPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticFcPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticFcPort.SupportedCOS
- Msvm_SyntheticFcPort.ActiveCOS
- Msvm_SyntheticFcPort.SupportedFC4Types
- Msvm_SyntheticFcPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f28614a7c885c0cfc03d546219518cda240219a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112312"
---
# <a name="msvm_syntheticfcport-class"></a><span data-ttu-id="b0442-103">Msvm \_ SyntheticFcPort 類別</span><span class="sxs-lookup"><span data-stu-id="b0442-103">Msvm\_SyntheticFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="b0442-104">本文包含「從屬」一詞的參考，Microsoft 已不再使用該字詞。</span><span class="sxs-lookup"><span data-stu-id="b0442-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="b0442-105">從軟體中移除該字詞時，我們也會將其從本文中移除。</span><span class="sxs-lookup"><span data-stu-id="b0442-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="b0442-106">代表綜合光纖通道埠。</span><span class="sxs-lookup"><span data-stu-id="b0442-106">Represents a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="b0442-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="b0442-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0442-108">語法</span><span class="sxs-lookup"><span data-stu-id="b0442-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPort : CIM_FCPort
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
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
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology = 4;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint16   SupportedCOS[];
  uint16   ActiveCOS[];
  uint16   SupportedFC4Types[];
  uint16   ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="b0442-109">成員</span><span class="sxs-lookup"><span data-stu-id="b0442-109">Members</span></span>

<span data-ttu-id="b0442-110">**Msvm \_ SyntheticFcPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b0442-110">The **Msvm\_SyntheticFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="b0442-111">方法</span><span class="sxs-lookup"><span data-stu-id="b0442-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="b0442-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b0442-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b0442-113">方法</span><span class="sxs-lookup"><span data-stu-id="b0442-113">Methods</span></span>

<span data-ttu-id="b0442-114">**Msvm \_ SyntheticFcPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b0442-114">The **Msvm\_SyntheticFcPort** class has these methods.</span></span>



| <span data-ttu-id="b0442-115">方法</span><span class="sxs-lookup"><span data-stu-id="b0442-115">Method</span></span>                                                                | <span data-ttu-id="b0442-116">描述</span><span class="sxs-lookup"><span data-stu-id="b0442-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="b0442-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="b0442-117">**EnableDevice**</span></span>                                                      | <span data-ttu-id="b0442-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b0442-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b0442-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="b0442-119">**OnlineDevice**</span></span>                                                      | <span data-ttu-id="b0442-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b0442-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b0442-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="b0442-121">**QuiesceDevice**</span></span>                                                     | <span data-ttu-id="b0442-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b0442-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="b0442-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="b0442-123">**RequestStateChange**</span></span>](msvm-syntheticfcport-requeststatechange.md) | <span data-ttu-id="b0442-124">要求狀態變更。</span><span class="sxs-lookup"><span data-stu-id="b0442-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="b0442-125">**重設**</span><span class="sxs-lookup"><span data-stu-id="b0442-125">**Reset**</span></span>](msvm-syntheticfcport-reset.md)                           | <span data-ttu-id="b0442-126">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="b0442-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="b0442-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="b0442-127">**RestoreProperties**</span></span>                                                 | <span data-ttu-id="b0442-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b0442-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b0442-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="b0442-129">**SaveProperties**</span></span>                                                    | <span data-ttu-id="b0442-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b0442-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="b0442-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b0442-131">**SetPowerState**</span></span>                                                     | <span data-ttu-id="b0442-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b0442-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b0442-133">屬性</span><span class="sxs-lookup"><span data-stu-id="b0442-133">Properties</span></span>

<span data-ttu-id="b0442-134">**Msvm \_ SyntheticFcPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b0442-134">The **Msvm\_SyntheticFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0442-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="b0442-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-136">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-138">整數陣列，指出作用中服務的類別。</span><span class="sxs-lookup"><span data-stu-id="b0442-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="b0442-139">支援的 COS 是由 **SupportedCOS** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="b0442-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="b0442-140">這個屬性繼承自 **CIM \_ FCPort**。</span><span class="sxs-lookup"><span data-stu-id="b0442-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="b0442-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b0442-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-142"><span id="1"></span>**1** (1) </span><span class="sxs-lookup"><span data-stu-id="b0442-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-143"><span id="2"></span>**2** (2) </span><span class="sxs-lookup"><span data-stu-id="b0442-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-144"><span id="3"></span>**3** (3) </span><span class="sxs-lookup"><span data-stu-id="b0442-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-145"><span id="4"></span>**4** (4) </span><span class="sxs-lookup"><span data-stu-id="b0442-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-146"><span id="5"></span>**5** (5) </span><span class="sxs-lookup"><span data-stu-id="b0442-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-147"><span id="6"></span>**6** (6) </span><span class="sxs-lookup"><span data-stu-id="b0442-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-148"><span id="F"></span><span id="f"></span>**F** (7 ) </span><span class="sxs-lookup"><span data-stu-id="b0442-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0442-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="b0442-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-150">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-152">整數陣列，指出目前正在執行的光纖通道 FC-4 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b0442-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="b0442-153">所有支援的通訊協定清單都是由 **SupportedFC4Types** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="b0442-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="b0442-154">這個屬性繼承自 **CIM \_ FCPort**。</span><span class="sxs-lookup"><span data-stu-id="b0442-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="b0442-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b0442-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b0442-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4) </span><span class="sxs-lookup"><span data-stu-id="b0442-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>透過 **FC 的 IP** (5) </span><span class="sxs-lookup"><span data-stu-id="b0442-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8) </span><span class="sxs-lookup"><span data-stu-id="b0442-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9) </span><span class="sxs-lookup"><span data-stu-id="b0442-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 主要** (17) </span><span class="sxs-lookup"><span data-stu-id="b0442-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 從屬** (18) </span><span class="sxs-lookup"><span data-stu-id="b0442-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 對等** (19) </span><span class="sxs-lookup"><span data-stu-id="b0442-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 主要** (21) </span><span class="sxs-lookup"><span data-stu-id="b0442-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 從屬** (22) </span><span class="sxs-lookup"><span data-stu-id="b0442-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 對等** (23) </span><span class="sxs-lookup"><span data-stu-id="b0442-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25) </span><span class="sxs-lookup"><span data-stu-id="b0442-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="b0442-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27) </span><span class="sxs-lookup"><span data-stu-id="b0442-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 控制單位** (28) </span><span class="sxs-lookup"><span data-stu-id="b0442-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**光纖通道 Services (fc-gs、fc-gs-2、fc-gs-3)** (32) </span><span class="sxs-lookup"><span data-stu-id="b0442-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34) </span><span class="sxs-lookup"><span data-stu-id="b0442-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36) </span><span class="sxs-lookup"><span data-stu-id="b0442-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64) </span><span class="sxs-lookup"><span data-stu-id="b0442-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80) </span><span class="sxs-lookup"><span data-stu-id="b0442-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI 封裝區域網路 PDU** (81) </span><span class="sxs-lookup"><span data-stu-id="b0442-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 封裝的 LAN PDU** (82) </span><span class="sxs-lookup"><span data-stu-id="b0442-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88) </span><span class="sxs-lookup"><span data-stu-id="b0442-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96) </span><span class="sxs-lookup"><span data-stu-id="b0442-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**廠商唯一** (255) </span><span class="sxs-lookup"><span data-stu-id="b0442-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0442-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="b0442-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-182">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b0442-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0442-184">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="b0442-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b0442-185">使用中或已協商的最大傳輸單位 (MTU) 可支援，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="b0442-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="b0442-186">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="b0442-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="b0442-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-188">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-190">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="b0442-191">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-192">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="b0442-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-193">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b0442-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-195">指出埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。</span><span class="sxs-lookup"><span data-stu-id="b0442-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="b0442-196">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="b0442-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-197">**可用性**</span><span class="sxs-lookup"><span data-stu-id="b0442-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-198">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-200">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-200">The primary availability and status of the device.</span></span> <span data-ttu-id="b0442-201">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="b0442-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-203">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-205">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="b0442-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="b0442-206">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b0442-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-207">**標題**</span><span class="sxs-lookup"><span data-stu-id="b0442-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-210">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="b0442-210">A short description of the object.</span></span> <span data-ttu-id="b0442-211">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="b0442-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-213">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-215">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="b0442-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="b0442-216">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="b0442-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b0442-217">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b0442-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b0442-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="b0442-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="b0442-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="b0442-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="b0442-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b0442-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="b0442-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b0442-225">)</span><span class="sxs-lookup"><span data-stu-id="b0442-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0442-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b0442-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-229">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="b0442-229">The scoping system's creation class name.</span></span> <span data-ttu-id="b0442-230">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b0442-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-231">**說明**</span><span class="sxs-lookup"><span data-stu-id="b0442-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-234">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="b0442-234">A description of the object.</span></span> <span data-ttu-id="b0442-235">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="b0442-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-237">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-239">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b0442-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="b0442-240">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="b0442-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b0442-241">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b0442-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="b0442-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="b0442-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="b0442-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="b0442-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="b0442-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="b0442-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b0442-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="b0442-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b0442-250">)</span><span class="sxs-lookup"><span data-stu-id="b0442-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0442-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b0442-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-254">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="b0442-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="b0442-255">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b0442-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="b0442-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-259">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b0442-259">A display name for the object.</span></span> <span data-ttu-id="b0442-260">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="b0442-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-262">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-264">系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b0442-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="b0442-265">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="b0442-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b0442-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-267">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-269">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b0442-270">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b0442-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="b0442-271">值</span><span class="sxs-lookup"><span data-stu-id="b0442-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="b0442-272">意義</span><span class="sxs-lookup"><span data-stu-id="b0442-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="b0442-273"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="b0442-274">無法判斷元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="b0442-275"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="b0442-276"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="b0442-277">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="b0442-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="b0442-278"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="b0442-279">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="b0442-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="b0442-280">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="b0442-281">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="b0442-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="b0442-282"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="b0442-283">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="b0442-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="b0442-284"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="b0442-285">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="b0442-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="b0442-286"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="b0442-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="b0442-287">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="b0442-288"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="b0442-289">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="b0442-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="b0442-290"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="b0442-291">元素已啟用但處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="b0442-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="b0442-292">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="b0442-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="b0442-293">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="b0442-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="b0442-294"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="b0442-295">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="b0442-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="b0442-296">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="b0442-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="b0442-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="b0442-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-298">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b0442-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-300">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b0442-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="b0442-301">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b0442-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-305">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b0442-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="b0442-306">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="b0442-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-308">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b0442-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-310">指出埠是否以全雙工模式運作。</span><span class="sxs-lookup"><span data-stu-id="b0442-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="b0442-311">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="b0442-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="b0442-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-313">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-315">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="b0442-315">The current health of the element.</span></span> <span data-ttu-id="b0442-316">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b0442-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-318">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-320">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b0442-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="b0442-321">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b0442-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-323">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b0442-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-325">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="b0442-325">The date and time when the object was installed.</span></span> <span data-ttu-id="b0442-326">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="b0442-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="b0442-327">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b0442-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-329">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0442-331">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="b0442-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="b0442-332">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="b0442-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="b0442-333">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b0442-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-335">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b0442-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-337">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b0442-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="b0442-338">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-339">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="b0442-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-340">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-342">指定埠的連結技術類型。</span><span class="sxs-lookup"><span data-stu-id="b0442-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="b0442-343">當設定為1時 (其他) ， **OtherLinkTechnology** 屬性會包含連結類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="b0442-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="b0442-344">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="b0442-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="b0442-345">值</span><span class="sxs-lookup"><span data-stu-id="b0442-345">Value</span></span>                                                                                                                                                                              | <span data-ttu-id="b0442-346">意義</span><span class="sxs-lookup"><span data-stu-id="b0442-346">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC"></span><span id="fc"></span><dl> <span data-ttu-id="b0442-347"><dt>**FC**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-347"><dt>**FC**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="b0442-348">光纖通道</span><span class="sxs-lookup"><span data-stu-id="b0442-348">Fibre channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b0442-349">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="b0442-349">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-350">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b0442-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-351">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-352">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="b0442-352">This property has been deprecated.</span></span> <span data-ttu-id="b0442-353">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-354">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="b0442-354">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-355">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b0442-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-356">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0442-357">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="b0442-357">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="b0442-358">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="b0442-358">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="b0442-359">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b0442-359">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-360">**名稱**</span><span class="sxs-lookup"><span data-stu-id="b0442-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-361">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-362">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-363">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="b0442-363">The label by which the object is known.</span></span> <span data-ttu-id="b0442-364">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-365">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="b0442-365">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-366">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-367">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0442-368">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="b0442-368">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="b0442-369">包含埠之 MAC 位址的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="b0442-369">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="b0442-370">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="b0442-370">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-371">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="b0442-371">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-372">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-373">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-374">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b0442-374">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="b0442-375">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="b0442-375">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b0442-376">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b0442-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b0442-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="b0442-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="b0442-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="b0442-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="b0442-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="b0442-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="b0442-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="b0442-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="b0442-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="b0442-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="b0442-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="b0442-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="b0442-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="b0442-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="b0442-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="b0442-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="b0442-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b0442-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="b0442-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b0442-396">)</span><span class="sxs-lookup"><span data-stu-id="b0442-396">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0442-397">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="b0442-397">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-398">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-399">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-400">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-400">The current statuses of the object.</span></span> <span data-ttu-id="b0442-401">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-402">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="b0442-402">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-403">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-404">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-405">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="b0442-405">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="b0442-406">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b0442-406">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="b0442-407">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b0442-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-408">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="b0442-408">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-409">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-410">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-411">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="b0442-411">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="b0442-412">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-413">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="b0442-413">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-414">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-415">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-416">描述 **LinkTechnology** 設定為1， (其他) 的字串值。</span><span class="sxs-lookup"><span data-stu-id="b0442-416">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="b0442-417">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="b0442-417">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-418">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="b0442-418">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-419">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-420">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-421">使用這個屬性會取代 **PortType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b0442-421">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="b0442-422">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="b0442-422">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-423">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="b0442-423">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-424">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-425">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-426">描述當 **PortType** 設定為1時 (其他) 的模組類型。</span><span class="sxs-lookup"><span data-stu-id="b0442-426">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="b0442-427">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b0442-427">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-428">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="b0442-428">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-429">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-430">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0442-431">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="b0442-431">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="b0442-432">硬式編碼在埠中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="b0442-432">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="b0442-433">您可以使用固件升級或軟體設定來變更這個硬式編碼的位址。</span><span class="sxs-lookup"><span data-stu-id="b0442-433">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="b0442-434">進行這項變更時，應同時更新欄位。</span><span class="sxs-lookup"><span data-stu-id="b0442-434">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="b0442-435">如果網路介面卡沒有任何硬式編碼位址，則此屬性應為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b0442-435">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="b0442-436">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="b0442-436">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-437">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="b0442-437">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-438">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-439">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-440">連接埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b0442-440">The port number.</span></span> <span data-ttu-id="b0442-441">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="b0442-441">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-442">**PortType**</span><span class="sxs-lookup"><span data-stu-id="b0442-442">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-443">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-444">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-445">目前為埠啟用的特定模式。</span><span class="sxs-lookup"><span data-stu-id="b0442-445">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="b0442-446">當設定為1時 (其他) ，相關的 **OtherPortType** 屬性會包含埠類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="b0442-446">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="b0442-447">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b0442-447">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b0442-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b0442-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b0442-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 銅的 10baset** (50) </span><span class="sxs-lookup"><span data-stu-id="b0442-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51) </span><span class="sxs-lookup"><span data-stu-id="b0442-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52) </span><span class="sxs-lookup"><span data-stu-id="b0442-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53) </span><span class="sxs-lookup"><span data-stu-id="b0442-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54) </span><span class="sxs-lookup"><span data-stu-id="b0442-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55) </span><span class="sxs-lookup"><span data-stu-id="b0442-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10gbase-t-CX4** (56) </span><span class="sxs-lookup"><span data-stu-id="b0442-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 光纖 100base-tx-FX** (100) </span><span class="sxs-lookup"><span data-stu-id="b0442-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100base-tx-SX** (101) </span><span class="sxs-lookup"><span data-stu-id="b0442-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000base-t-SX** (102) </span><span class="sxs-lookup"><span data-stu-id="b0442-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000base-t-LX** (103) </span><span class="sxs-lookup"><span data-stu-id="b0442-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000base-t-CX** (104) </span><span class="sxs-lookup"><span data-stu-id="b0442-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10gbase-t-SR** (105) </span><span class="sxs-lookup"><span data-stu-id="b0442-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10gbase-t-SW** (106) </span><span class="sxs-lookup"><span data-stu-id="b0442-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**LX4** (107) </span><span class="sxs-lookup"><span data-stu-id="b0442-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10gbase-t-LR** (108) </span><span class="sxs-lookup"><span data-stu-id="b0442-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**LW** (109) </span><span class="sxs-lookup"><span data-stu-id="b0442-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10gbase-t-ER** (110) </span><span class="sxs-lookup"><span data-stu-id="b0442-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span> (111) **的**</span><span class="sxs-lookup"><span data-stu-id="b0442-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (16，000. 65535 ) </span><span class="sxs-lookup"><span data-stu-id="b0442-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0442-470">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="b0442-470">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-471">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-471">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-472">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-473">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="b0442-473">The power management capabilities of the device.</span></span> <span data-ttu-id="b0442-474">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-474">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-475">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="b0442-475">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-476">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b0442-476">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-477">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-478">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="b0442-478">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="b0442-479">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-479">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-480">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b0442-480">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-481">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b0442-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-482">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-483">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="b0442-483">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="b0442-484">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-485">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="b0442-485">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-486">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-487">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-488">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="b0442-488">Provides high level status information.</span></span> <span data-ttu-id="b0442-489">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-489">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="b0442-490">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="b0442-490">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="b0442-491">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-491">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="b0442-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b0442-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-493"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="b0442-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="b0442-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="b0442-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="b0442-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="b0442-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="b0442-498">)</span><span class="sxs-lookup"><span data-stu-id="b0442-498">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0442-499">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="b0442-499">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-500">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b0442-500">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-501">存取類型：僅限寫入</span><span class="sxs-lookup"><span data-stu-id="b0442-501">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="b0442-502">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="b0442-502">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="b0442-503">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="b0442-503">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="b0442-504">實際的頻寬會在 [ **速度** ] 屬性中報告。</span><span class="sxs-lookup"><span data-stu-id="b0442-504">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="b0442-505">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b0442-505">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-506">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="b0442-506">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-507">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-507">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-508">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-509">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-509">The last requested or desired state for the element.</span></span> <span data-ttu-id="b0442-510">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="b0442-510">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-511">**速度**</span><span class="sxs-lookup"><span data-stu-id="b0442-511">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-512">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b0442-512">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-513">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0442-514">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="b0442-514">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="b0442-515">埠的頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="b0442-515">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="b0442-516">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b0442-516">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-517">**狀態**</span><span class="sxs-lookup"><span data-stu-id="b0442-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-518">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-519">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-520">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-520">The current status of the object.</span></span> <span data-ttu-id="b0442-521">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-521">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-522">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="b0442-522">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-523">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-523">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-524">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-524">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-525">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="b0442-525">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="b0442-526">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="b0442-526">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-527">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b0442-527">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-528">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-529">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-530">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-530">The current state of the logical device.</span></span> <span data-ttu-id="b0442-531">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-531">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-532">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="b0442-532">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-533">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-533">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-534">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-535">整數陣列，表示支援的光纖通道服務 (COS) 類別。</span><span class="sxs-lookup"><span data-stu-id="b0442-535">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="b0442-536">作用中的 COS 是由 **ActiveCOS** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="b0442-536">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="b0442-537">這個屬性繼承自 **CIM \_ FCPort**。</span><span class="sxs-lookup"><span data-stu-id="b0442-537">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="b0442-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b0442-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-539"><span id="1"></span>**1** (1) </span><span class="sxs-lookup"><span data-stu-id="b0442-539"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-540"><span id="2"></span>**2** (2) </span><span class="sxs-lookup"><span data-stu-id="b0442-540"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-541"><span id="3"></span>**3** (3) </span><span class="sxs-lookup"><span data-stu-id="b0442-541"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-542"><span id="4"></span>**4** (4) </span><span class="sxs-lookup"><span data-stu-id="b0442-542"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-543"><span id="5"></span>**5** (5) </span><span class="sxs-lookup"><span data-stu-id="b0442-543"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-544"><span id="6"></span>**6** (6) </span><span class="sxs-lookup"><span data-stu-id="b0442-544"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-545"><span id="F_"></span><span id="f_"></span>**F** (7 ) </span><span class="sxs-lookup"><span data-stu-id="b0442-545"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0442-546">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="b0442-546">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-547">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="b0442-547">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b0442-548">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-549">整數陣列，表示支援的光纖通道 FC-4 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="b0442-549">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="b0442-550">作用中且正在執行的通訊協定是由 **ActiveFC4Types** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="b0442-550">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="b0442-551">這個屬性繼承自 **CIM \_ FCPort**。</span><span class="sxs-lookup"><span data-stu-id="b0442-551">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="b0442-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b0442-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="b0442-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4) </span><span class="sxs-lookup"><span data-stu-id="b0442-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>透過 **FC 的 IP** (5) </span><span class="sxs-lookup"><span data-stu-id="b0442-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8) </span><span class="sxs-lookup"><span data-stu-id="b0442-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9) </span><span class="sxs-lookup"><span data-stu-id="b0442-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 主要** (17) </span><span class="sxs-lookup"><span data-stu-id="b0442-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 從屬** (18) </span><span class="sxs-lookup"><span data-stu-id="b0442-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 對等** (19) </span><span class="sxs-lookup"><span data-stu-id="b0442-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 主要** (21) </span><span class="sxs-lookup"><span data-stu-id="b0442-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 從屬** (22) </span><span class="sxs-lookup"><span data-stu-id="b0442-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 對等** (23) </span><span class="sxs-lookup"><span data-stu-id="b0442-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25) </span><span class="sxs-lookup"><span data-stu-id="b0442-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="b0442-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27) </span><span class="sxs-lookup"><span data-stu-id="b0442-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 控制單位** (28) </span><span class="sxs-lookup"><span data-stu-id="b0442-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**光纖通道 Services (fc-gs、fc-gs-2、fc-gs-3)** (32) </span><span class="sxs-lookup"><span data-stu-id="b0442-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34) </span><span class="sxs-lookup"><span data-stu-id="b0442-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36) </span><span class="sxs-lookup"><span data-stu-id="b0442-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64) </span><span class="sxs-lookup"><span data-stu-id="b0442-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80) </span><span class="sxs-lookup"><span data-stu-id="b0442-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI 封裝區域網路 PDU** (81) </span><span class="sxs-lookup"><span data-stu-id="b0442-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 封裝的 LAN PDU** (82) </span><span class="sxs-lookup"><span data-stu-id="b0442-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88) </span><span class="sxs-lookup"><span data-stu-id="b0442-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96) </span><span class="sxs-lookup"><span data-stu-id="b0442-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**廠商唯一** (255) </span><span class="sxs-lookup"><span data-stu-id="b0442-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b0442-578">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="b0442-578">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-579">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b0442-579">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-580">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0442-581">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="b0442-581">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b0442-582">可支援的最大傳輸單位 (MTU) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b0442-582">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="b0442-583">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="b0442-583">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-584">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b0442-584">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-585">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-586">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-587">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="b0442-587">The scoping system's creation class name.</span></span> <span data-ttu-id="b0442-588">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b0442-588">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b0442-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-590">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b0442-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-591">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-592">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0442-592">The scoping system's name.</span></span> <span data-ttu-id="b0442-593">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="b0442-593">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="b0442-594">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="b0442-594">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-595">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="b0442-595">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-596">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-596">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-597">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="b0442-597">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="b0442-598">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b0442-598">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-599">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="b0442-599">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-600">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="b0442-600">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-601">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-601">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-602">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="b0442-602">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="b0442-603">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="b0442-603">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-604">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="b0442-604">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-605">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-605">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-606">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-607">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="b0442-607">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="b0442-608">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b0442-608">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="b0442-609">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="b0442-609">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0442-610">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="b0442-610">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0442-611">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="b0442-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0442-612">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="b0442-612">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="b0442-613">這種情況的範例之一，就是可能有後端埠與磁片磁碟機和前端埠通訊以與主機通訊的存放裝置陣列。</span><span class="sxs-lookup"><span data-stu-id="b0442-613">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="b0442-614">如果埠的使用沒有限制，則值應該設定為 4 (不受限制的) 。</span><span class="sxs-lookup"><span data-stu-id="b0442-614">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="b0442-615">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b0442-615">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="b0442-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="b0442-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**前端** (2) </span><span class="sxs-lookup"><span data-stu-id="b0442-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span> (3) 的 **後端**</span><span class="sxs-lookup"><span data-stu-id="b0442-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b0442-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**不受限制** (4 ) </span><span class="sxs-lookup"><span data-stu-id="b0442-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0442-620">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0442-620">Requirements</span></span>



| <span data-ttu-id="b0442-621">需求</span><span class="sxs-lookup"><span data-stu-id="b0442-621">Requirement</span></span> | <span data-ttu-id="b0442-622">值</span><span class="sxs-lookup"><span data-stu-id="b0442-622">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0442-623">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0442-623">Minimum supported client</span></span><br/> | <span data-ttu-id="b0442-624">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0442-624">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b0442-625">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0442-625">Minimum supported server</span></span><br/> | <span data-ttu-id="b0442-626">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0442-626">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0442-627">命名空間</span><span class="sxs-lookup"><span data-stu-id="b0442-627">Namespace</span></span><br/>                | <span data-ttu-id="b0442-628">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="b0442-628">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b0442-629">MOF</span><span class="sxs-lookup"><span data-stu-id="b0442-629">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0442-630"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-630"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0442-631">DLL</span><span class="sxs-lookup"><span data-stu-id="b0442-631">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0442-632"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0442-632"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

