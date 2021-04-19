---
description: 表示外部光纖通道埠。
ms.assetid: bab3a243-5ebd-43e0-948e-ea8112e09d0a
title: Msvm_ExternalFcPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalFcPort
- Msvm_ExternalFcPort.SetPowerState
- Msvm_ExternalFcPort.EnableDevice
- Msvm_ExternalFcPort.OnlineDevice
- Msvm_ExternalFcPort.QuiesceDevice
- Msvm_ExternalFcPort.SaveProperties
- Msvm_ExternalFcPort.RestoreProperties
- Msvm_ExternalFcPort.InstanceID
- Msvm_ExternalFcPort.Caption
- Msvm_ExternalFcPort.Description
- Msvm_ExternalFcPort.ElementName
- Msvm_ExternalFcPort.InstallDate
- Msvm_ExternalFcPort.Name
- Msvm_ExternalFcPort.OperationalStatus
- Msvm_ExternalFcPort.StatusDescriptions
- Msvm_ExternalFcPort.Status
- Msvm_ExternalFcPort.HealthState
- Msvm_ExternalFcPort.CommunicationStatus
- Msvm_ExternalFcPort.DetailedStatus
- Msvm_ExternalFcPort.OperatingStatus
- Msvm_ExternalFcPort.PrimaryStatus
- Msvm_ExternalFcPort.EnabledState
- Msvm_ExternalFcPort.OtherEnabledState
- Msvm_ExternalFcPort.RequestedState
- Msvm_ExternalFcPort.EnabledDefault
- Msvm_ExternalFcPort.TimeOfLastStateChange
- Msvm_ExternalFcPort.AvailableRequestedStates
- Msvm_ExternalFcPort.TransitioningToState
- Msvm_ExternalFcPort.SystemCreationClassName
- Msvm_ExternalFcPort.SystemName
- Msvm_ExternalFcPort.CreationClassName
- Msvm_ExternalFcPort.DeviceID
- Msvm_ExternalFcPort.PowerManagementSupported
- Msvm_ExternalFcPort.PowerManagementCapabilities
- Msvm_ExternalFcPort.Availability
- Msvm_ExternalFcPort.StatusInfo
- Msvm_ExternalFcPort.LastErrorCode
- Msvm_ExternalFcPort.ErrorDescription
- Msvm_ExternalFcPort.ErrorCleared
- Msvm_ExternalFcPort.OtherIdentifyingInfo
- Msvm_ExternalFcPort.PowerOnHours
- Msvm_ExternalFcPort.TotalPowerOnHours
- Msvm_ExternalFcPort.IdentifyingDescriptions
- Msvm_ExternalFcPort.AdditionalAvailability
- Msvm_ExternalFcPort.MaxQuiesceTime
- Msvm_ExternalFcPort.Speed
- Msvm_ExternalFcPort.MaxSpeed
- Msvm_ExternalFcPort.RequestedSpeed
- Msvm_ExternalFcPort.UsageRestriction
- Msvm_ExternalFcPort.PortType
- Msvm_ExternalFcPort.OtherPortType
- Msvm_ExternalFcPort.OtherNetworkPortType
- Msvm_ExternalFcPort.PortNumber
- Msvm_ExternalFcPort.LinkTechnology
- Msvm_ExternalFcPort.OtherLinkTechnology
- Msvm_ExternalFcPort.PermanentAddress
- Msvm_ExternalFcPort.NetworkAddresses
- Msvm_ExternalFcPort.FullDuplex
- Msvm_ExternalFcPort.AutoSense
- Msvm_ExternalFcPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalFcPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalFcPort.SupportedCOS
- Msvm_ExternalFcPort.ActiveCOS
- Msvm_ExternalFcPort.SupportedFC4Types
- Msvm_ExternalFcPort.ActiveFC4Types
- Msvm_ExternalFcPort.IsHyperVCapable
- Msvm_ExternalFcPort.WWNN
- Msvm_ExternalFcPort.WWPN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f883afd2447c90c3167e8cf3145f8fd50ef2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970842"
---
# <a name="msvm_externalfcport-class"></a><span data-ttu-id="1dac6-103">Msvm \_ ExternalFcPort 類別</span><span class="sxs-lookup"><span data-stu-id="1dac6-103">Msvm\_ExternalFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="1dac6-104">本文包含「從屬」一詞的參考，Microsoft 已不再使用該字詞。</span><span class="sxs-lookup"><span data-stu-id="1dac6-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="1dac6-105">從軟體中移除該字詞時，我們也會將其從本文中移除。</span><span class="sxs-lookup"><span data-stu-id="1dac6-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="1dac6-106">表示外部光纖通道埠。</span><span class="sxs-lookup"><span data-stu-id="1dac6-106">Represents an external Fibre Channel port.</span></span>

<span data-ttu-id="1dac6-107">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1dac6-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dac6-108">語法</span><span class="sxs-lookup"><span data-stu-id="1dac6-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalFcPort : CIM_FCPort
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
  uint16   LinkTechnology;
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
  boolean  IsHyperVCapable;
  string   WWNN;
  string   WWPN;
};
```

## <a name="members"></a><span data-ttu-id="1dac6-109">成員</span><span class="sxs-lookup"><span data-stu-id="1dac6-109">Members</span></span>

<span data-ttu-id="1dac6-110">**Msvm \_ ExternalFcPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1dac6-110">The **Msvm\_ExternalFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="1dac6-111">方法</span><span class="sxs-lookup"><span data-stu-id="1dac6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="1dac6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="1dac6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1dac6-113">方法</span><span class="sxs-lookup"><span data-stu-id="1dac6-113">Methods</span></span>

<span data-ttu-id="1dac6-114">**Msvm \_ ExternalFcPort** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1dac6-114">The **Msvm\_ExternalFcPort** class has these methods.</span></span>



| <span data-ttu-id="1dac6-115">方法</span><span class="sxs-lookup"><span data-stu-id="1dac6-115">Method</span></span>                                                               | <span data-ttu-id="1dac6-116">描述</span><span class="sxs-lookup"><span data-stu-id="1dac6-116">Description</span></span>                              |
|:---------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="1dac6-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="1dac6-117">**EnableDevice**</span></span>                                                     | <span data-ttu-id="1dac6-118">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1dac6-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1dac6-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="1dac6-119">**OnlineDevice**</span></span>                                                     | <span data-ttu-id="1dac6-120">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1dac6-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1dac6-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="1dac6-121">**QuiesceDevice**</span></span>                                                    | <span data-ttu-id="1dac6-122">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1dac6-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="1dac6-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="1dac6-123">**RequestStateChange**</span></span>](msvm-externalfcport-requeststatechange.md) | <span data-ttu-id="1dac6-124">要求狀態變更</span><span class="sxs-lookup"><span data-stu-id="1dac6-124">Requests a state change</span></span><br/>       |
| [<span data-ttu-id="1dac6-125">**重設**</span><span class="sxs-lookup"><span data-stu-id="1dac6-125">**Reset**</span></span>](msvm-externalfcport-reset.md)                           | <span data-ttu-id="1dac6-126">重設虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="1dac6-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="1dac6-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="1dac6-127">**RestoreProperties**</span></span>                                                | <span data-ttu-id="1dac6-128">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1dac6-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1dac6-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="1dac6-129">**SaveProperties**</span></span>                                                   | <span data-ttu-id="1dac6-130">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1dac6-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="1dac6-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1dac6-131">**SetPowerState**</span></span>                                                    | <span data-ttu-id="1dac6-132">不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="1dac6-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1dac6-133">屬性</span><span class="sxs-lookup"><span data-stu-id="1dac6-133">Properties</span></span>

<span data-ttu-id="1dac6-134">**Msvm \_ ExternalFcPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1dac6-134">The **Msvm\_ExternalFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="1dac6-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-136">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-138">整數陣列，指出作用中服務的類別。</span><span class="sxs-lookup"><span data-stu-id="1dac6-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="1dac6-139">支援的 COS 是由 **SupportedCOS** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="1dac6-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="1dac6-140">這個屬性繼承自 **CIM \_ FCPort**。</span><span class="sxs-lookup"><span data-stu-id="1dac6-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1dac6-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-142"><span id="1"></span>**1** (1) </span><span class="sxs-lookup"><span data-stu-id="1dac6-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-143"><span id="2"></span>**2** (2) </span><span class="sxs-lookup"><span data-stu-id="1dac6-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-144"><span id="3"></span>**3** (3) </span><span class="sxs-lookup"><span data-stu-id="1dac6-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-145"><span id="4"></span>**4** (4) </span><span class="sxs-lookup"><span data-stu-id="1dac6-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-146"><span id="5"></span>**5** (5) </span><span class="sxs-lookup"><span data-stu-id="1dac6-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-147"><span id="6"></span>**6** (6) </span><span class="sxs-lookup"><span data-stu-id="1dac6-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-148"><span id="F"></span><span id="f"></span>**F** (7 ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="1dac6-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-150">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-151">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-152">整數陣列，指出目前正在執行的光纖通道 FC-4 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1dac6-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="1dac6-153">所有支援的通訊協定清單都是由 **SupportedFC4Types** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="1dac6-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="1dac6-154">這個屬性繼承自 **CIM \_ FCPort**。</span><span class="sxs-lookup"><span data-stu-id="1dac6-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1dac6-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1dac6-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4) </span><span class="sxs-lookup"><span data-stu-id="1dac6-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>透過 **FC 的 IP** (5) </span><span class="sxs-lookup"><span data-stu-id="1dac6-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8) </span><span class="sxs-lookup"><span data-stu-id="1dac6-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9) </span><span class="sxs-lookup"><span data-stu-id="1dac6-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 主要** (17) </span><span class="sxs-lookup"><span data-stu-id="1dac6-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 從屬** (18) </span><span class="sxs-lookup"><span data-stu-id="1dac6-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 對等** (19) </span><span class="sxs-lookup"><span data-stu-id="1dac6-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 主要** (21) </span><span class="sxs-lookup"><span data-stu-id="1dac6-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 從屬** (22) </span><span class="sxs-lookup"><span data-stu-id="1dac6-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 對等** (23) </span><span class="sxs-lookup"><span data-stu-id="1dac6-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25) </span><span class="sxs-lookup"><span data-stu-id="1dac6-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="1dac6-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27) </span><span class="sxs-lookup"><span data-stu-id="1dac6-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 控制單位** (28) </span><span class="sxs-lookup"><span data-stu-id="1dac6-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**光纖通道 Services (fc-gs、fc-gs-2、fc-gs-3)** (32) </span><span class="sxs-lookup"><span data-stu-id="1dac6-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34) </span><span class="sxs-lookup"><span data-stu-id="1dac6-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36) </span><span class="sxs-lookup"><span data-stu-id="1dac6-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64) </span><span class="sxs-lookup"><span data-stu-id="1dac6-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80) </span><span class="sxs-lookup"><span data-stu-id="1dac6-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI 封裝區域網路 PDU** (81) </span><span class="sxs-lookup"><span data-stu-id="1dac6-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 封裝的 LAN PDU** (82) </span><span class="sxs-lookup"><span data-stu-id="1dac6-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88) </span><span class="sxs-lookup"><span data-stu-id="1dac6-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96) </span><span class="sxs-lookup"><span data-stu-id="1dac6-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**廠商唯一** (255) </span><span class="sxs-lookup"><span data-stu-id="1dac6-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="1dac6-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-182">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1dac6-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-184">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-185">使用中或已協商的最大傳輸單位 (MTU) 可支援，以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="1dac6-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="1dac6-186">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="1dac6-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-188">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-190">裝置的任何額外可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="1dac6-191">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-192">**自動感測**</span><span class="sxs-lookup"><span data-stu-id="1dac6-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-193">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1dac6-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-195">指出埠是否能夠自動判斷連接之網路媒體的速度或其他通訊特性。</span><span class="sxs-lookup"><span data-stu-id="1dac6-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="1dac6-196">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-197">**可用性**</span><span class="sxs-lookup"><span data-stu-id="1dac6-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-198">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-199">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-200">裝置的主要可用性和狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-200">The primary availability and status of the device.</span></span> <span data-ttu-id="1dac6-201">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="1dac6-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-203">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-204">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-205">指出 **RequestStateChange** 方法的 *RequestedState* 參數可能的值。</span><span class="sxs-lookup"><span data-stu-id="1dac6-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="1dac6-206">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1dac6-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-207">**標題**</span><span class="sxs-lookup"><span data-stu-id="1dac6-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-208">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-209">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-210">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="1dac6-210">A short description of the object.</span></span> <span data-ttu-id="1dac6-211">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="1dac6-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-213">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-214">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-215">指出檢測與基礎受管理元素通訊的能力。</span><span class="sxs-lookup"><span data-stu-id="1dac6-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="1dac6-216">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1dac6-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1dac6-217">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1dac6-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="1dac6-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**通訊正常** (2) </span><span class="sxs-lookup"><span data-stu-id="1dac6-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**遺失通訊** (3) </span><span class="sxs-lookup"><span data-stu-id="1dac6-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**沒有連絡人** (4) </span><span class="sxs-lookup"><span data-stu-id="1dac6-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1dac6-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="1dac6-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1dac6-225">)</span><span class="sxs-lookup"><span data-stu-id="1dac6-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1dac6-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-227">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-228">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-229">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="1dac6-229">The scoping system's creation class name.</span></span> <span data-ttu-id="1dac6-230">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-231">**說明**</span><span class="sxs-lookup"><span data-stu-id="1dac6-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-232">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-233">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-234">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="1dac6-234">A description of the object.</span></span> <span data-ttu-id="1dac6-235">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="1dac6-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-237">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-238">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-239">補充 **PrimaryStatus** 屬性與其他狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1dac6-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="1dac6-240">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1dac6-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1dac6-241">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (0) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="1dac6-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**沒有其他資訊** (1) </span><span class="sxs-lookup"><span data-stu-id="1dac6-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**壓力** (2) </span><span class="sxs-lookup"><span data-stu-id="1dac6-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**預測性失敗** (3) </span><span class="sxs-lookup"><span data-stu-id="1dac6-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**無法復原的錯誤** (4) </span><span class="sxs-lookup"><span data-stu-id="1dac6-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**錯誤中的支援實體** (5) </span><span class="sxs-lookup"><span data-stu-id="1dac6-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1dac6-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="1dac6-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1dac6-250">)</span><span class="sxs-lookup"><span data-stu-id="1dac6-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-251">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1dac6-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-253">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-254">用來唯一命名邏輯裝置的位址或其他識別資訊。</span><span class="sxs-lookup"><span data-stu-id="1dac6-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="1dac6-255">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="1dac6-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-257">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-258">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-259">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1dac6-259">A display name for the object.</span></span> <span data-ttu-id="1dac6-260">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="1dac6-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-262">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-263">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-264">系統管理員的預設或啟動設定，適用于元素的 **EnabledState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1dac6-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="1dac6-265">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 2 (啟用) 。</span><span class="sxs-lookup"><span data-stu-id="1dac6-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="1dac6-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-267">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-268">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-269">專案的已啟用和停用狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="1dac6-270">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，它會是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1dac6-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="1dac6-271">值</span><span class="sxs-lookup"><span data-stu-id="1dac6-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="1dac6-272">意義</span><span class="sxs-lookup"><span data-stu-id="1dac6-272">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="1dac6-273"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="1dac6-274">無法判斷元素的狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="1dac6-275"><dt>**其他**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="1dac6-276"><dt>**已啟用**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="1dac6-277">元素正在執行。</span><span class="sxs-lookup"><span data-stu-id="1dac6-277">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="1dac6-278"><dt>**停用**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="1dac6-279">元素已關閉。</span><span class="sxs-lookup"><span data-stu-id="1dac6-279">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="1dac6-280">正在 <dt>**關閉**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="1dac6-281">專案正在進入已停用狀態的進程。</span><span class="sxs-lookup"><span data-stu-id="1dac6-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="1dac6-282"><dt>**不適用**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="1dac6-283">元素不支援啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="1dac6-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="1dac6-284"><dt>**已啟用但離線**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="1dac6-285">元素可能正在完成命令，而且會捨棄任何新的要求。</span><span class="sxs-lookup"><span data-stu-id="1dac6-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="1dac6-286"><dt>**在測試**</dt> <dt>7</dt>中</span><span class="sxs-lookup"><span data-stu-id="1dac6-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="1dac6-287">元素處於測試狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-287">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="1dac6-288"><dt>**延**</dt>後 <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="1dac6-289">元素可能正在完成命令，但它會將任何新的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="1dac6-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="1dac6-290"><dt>**靜止**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="1dac6-291">已啟用元素，但它處於受限模式。</span><span class="sxs-lookup"><span data-stu-id="1dac6-291">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="1dac6-292">專案的行為類似于啟用狀態 (2) ，但只會處理一組受限制的命令。</span><span class="sxs-lookup"><span data-stu-id="1dac6-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="1dac6-293">所有其他要求則會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="1dac6-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="1dac6-294"><dt>**起始**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="1dac6-295">元素正在進入啟用狀態 (2) 。</span><span class="sxs-lookup"><span data-stu-id="1dac6-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="1dac6-296">新的要求會排入佇列。</span><span class="sxs-lookup"><span data-stu-id="1dac6-296">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="1dac6-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1dac6-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-298">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1dac6-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-299">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-300">指出現在是否已清除 **LastErrorCode** 中報告的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1dac6-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="1dac6-301">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1dac6-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-303">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-304">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-305">字串，提供 **LastErrorCode** 中所記錄錯誤的詳細資訊，以及可採取之任何矯正措施的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1dac6-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="1dac6-306">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="1dac6-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-308">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1dac6-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-309">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-310">指出埠是否以全雙工模式運作。</span><span class="sxs-lookup"><span data-stu-id="1dac6-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="1dac6-311">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="1dac6-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-313">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-314">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-315">專案目前的健康情況。</span><span class="sxs-lookup"><span data-stu-id="1dac6-315">The current health of the element.</span></span> <span data-ttu-id="1dac6-316">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1dac6-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-318">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-319">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-320">自由格式字串的陣列，可提供 **OtherIdentifyingInfo** 屬性陣列中專案背後的說明和詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1dac6-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="1dac6-321">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1dac6-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-323">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1dac6-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-324">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-325">安裝物件的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="1dac6-325">The date and time when the object was installed.</span></span> <span data-ttu-id="1dac6-326">這個屬性不需要值來表示已安裝物件。</span><span class="sxs-lookup"><span data-stu-id="1dac6-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="1dac6-327">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1dac6-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-329">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-330">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-331">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="1dac6-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-332">唯一識別此類別的實例。</span><span class="sxs-lookup"><span data-stu-id="1dac6-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="1dac6-333">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-334">**IsHyperVCapable**</span><span class="sxs-lookup"><span data-stu-id="1dac6-334">**IsHyperVCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-335">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1dac6-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-336">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-337">如果此屬性為 **True**，則此光纖通道埠可以連線至交換器，因此可提供虛擬機器的連線能力。</span><span class="sxs-lookup"><span data-stu-id="1dac6-337">If this property is **True**, this Fibre Channel port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="1dac6-338">如果此屬性為 **False**，則虛擬機器無法使用此埠光纖通道架構。</span><span class="sxs-lookup"><span data-stu-id="1dac6-338">If this property is **False**, then this port cannot be used by the virtual machine Fibre Channel architecture.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-339">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1dac6-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-340">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1dac6-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-341">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-342">邏輯裝置所報告的最後一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1dac6-342">The last error code reported by the logical device.</span></span> <span data-ttu-id="1dac6-343">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-344">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="1dac6-344">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-345">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-346">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-347">指定埠的連結技術類型。</span><span class="sxs-lookup"><span data-stu-id="1dac6-347">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="1dac6-348">當設定為1時 (其他) ， **OtherLinkTechnology** 屬性會包含連結類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="1dac6-348">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="1dac6-349">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1dac6-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-351"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1dac6-351"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-352"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2) </span><span class="sxs-lookup"><span data-stu-id="1dac6-352"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-353"><span id="IB"></span><span id="ib"></span>**IB** (3) </span><span class="sxs-lookup"><span data-stu-id="1dac6-353"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-354"><span id="FC"></span><span id="fc"></span>**FC** (4) </span><span class="sxs-lookup"><span data-stu-id="1dac6-354"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-355"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5) </span><span class="sxs-lookup"><span data-stu-id="1dac6-355"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-356"><span id="ATM"></span><span id="atm"></span>**ATM** (6) </span><span class="sxs-lookup"><span data-stu-id="1dac6-356"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-357"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**權杖環** (7) </span><span class="sxs-lookup"><span data-stu-id="1dac6-357"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-358"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**框架轉送** (8) </span><span class="sxs-lookup"><span data-stu-id="1dac6-358"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-359"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**紅外線** (9) </span><span class="sxs-lookup"><span data-stu-id="1dac6-359"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-360"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**藍牙** (10) </span><span class="sxs-lookup"><span data-stu-id="1dac6-360"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-361"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**無線區域網路** (11 ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-361"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-362">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="1dac6-362">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-363">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1dac6-363">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-364">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-365">這個屬性已被取代。</span><span class="sxs-lookup"><span data-stu-id="1dac6-365">This property has been deprecated.</span></span> <span data-ttu-id="1dac6-366">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-367">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="1dac6-367">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-368">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1dac6-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-369">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-370">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-370">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-371">埠的最大頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="1dac6-371">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="1dac6-372">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1dac6-372">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-373">**名稱**</span><span class="sxs-lookup"><span data-stu-id="1dac6-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-374">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-375">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-376">已知物件的標籤。</span><span class="sxs-lookup"><span data-stu-id="1dac6-376">The label by which the object is known.</span></span> <span data-ttu-id="1dac6-377">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-378">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="1dac6-378">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-379">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-380">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-381">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-381">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-382">包含埠之 MAC 位址的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="1dac6-382">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="1dac6-383">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-383">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-384">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="1dac6-384">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-385">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-385">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-386">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-387">提供專案操作條件的目前狀態資訊，並可用於提供關於 **EnabledState** 屬性值的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1dac6-387">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="1dac6-388">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1dac6-388">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1dac6-389">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-390"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1dac6-390"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-391"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span> (1) **無法使用**</span><span class="sxs-lookup"><span data-stu-id="1dac6-391"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-392"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**服務** (2) </span><span class="sxs-lookup"><span data-stu-id="1dac6-392"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-393"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**開始** (3) </span><span class="sxs-lookup"><span data-stu-id="1dac6-393"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-394"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**停止** (4) </span><span class="sxs-lookup"><span data-stu-id="1dac6-394"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-395"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**已停止** (5) </span><span class="sxs-lookup"><span data-stu-id="1dac6-395"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-396"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>已 **中止** (6) </span><span class="sxs-lookup"><span data-stu-id="1dac6-396"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-397"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**休眠** (7) </span><span class="sxs-lookup"><span data-stu-id="1dac6-397"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-398"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**已完成** (8) </span><span class="sxs-lookup"><span data-stu-id="1dac6-398"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-399"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**遷移** (9) </span><span class="sxs-lookup"><span data-stu-id="1dac6-399"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-400"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10) </span><span class="sxs-lookup"><span data-stu-id="1dac6-400"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-401"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11) </span><span class="sxs-lookup"><span data-stu-id="1dac6-401"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-402"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**快照** (12) </span><span class="sxs-lookup"><span data-stu-id="1dac6-402"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-403"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>正在 **關閉** (13) </span><span class="sxs-lookup"><span data-stu-id="1dac6-403"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-404"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**在測試** (14) </span><span class="sxs-lookup"><span data-stu-id="1dac6-404"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-405"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**轉換** (15) </span><span class="sxs-lookup"><span data-stu-id="1dac6-405"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-406"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**在服務** (16) </span><span class="sxs-lookup"><span data-stu-id="1dac6-406"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-407"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1dac6-407"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-408"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="1dac6-408"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1dac6-409">)</span><span class="sxs-lookup"><span data-stu-id="1dac6-409">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-410">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="1dac6-410">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-411">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-412">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-413">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-413">The current statuses of the object.</span></span> <span data-ttu-id="1dac6-414">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-415">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="1dac6-415">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-416">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-417">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-418">描述當 **EnabledState** 屬性設定為 1 (其他) 時，專案已啟用或停用狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="1dac6-418">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="1dac6-419">當 **EnabledState** 屬性是1以外的任何值時，這個屬性必須設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1dac6-419">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="1dac6-420">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1dac6-420">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-421">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1dac6-421">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-422">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-422">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-423">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-424">除了裝置識別碼資訊以外的任何其他資料，可用來識別邏輯裝置。</span><span class="sxs-lookup"><span data-stu-id="1dac6-424">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="1dac6-425">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-425">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-426">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="1dac6-426">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-427">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-428">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-429">描述 **LinkTechnology** 設定為1， (其他) 的字串值。</span><span class="sxs-lookup"><span data-stu-id="1dac6-429">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="1dac6-430">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-430">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-431">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="1dac6-431">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-432">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-433">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-434">使用這個屬性會取代 **PortType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="1dac6-434">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="1dac6-435">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-435">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-436">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="1dac6-436">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-437">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-438">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-439">描述當 **PortType** 設定為1時 (其他) 的模組類型。</span><span class="sxs-lookup"><span data-stu-id="1dac6-439">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="1dac6-440">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1dac6-440">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-441">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="1dac6-441">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-442">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-443">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-444">限定詞： **MaxLen** ( 64 ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-444">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-445">硬式編碼在埠中的網路位址。</span><span class="sxs-lookup"><span data-stu-id="1dac6-445">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="1dac6-446">您可以使用固件升級或軟體設定來變更這個硬式編碼的位址。</span><span class="sxs-lookup"><span data-stu-id="1dac6-446">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="1dac6-447">進行這項變更時，應同時更新欄位。</span><span class="sxs-lookup"><span data-stu-id="1dac6-447">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="1dac6-448">如果網路介面卡沒有任何硬式編碼位址，則此屬性應為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1dac6-448">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="1dac6-449">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-449">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-450">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="1dac6-450">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-451">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-452">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-453">連接埠號碼。</span><span class="sxs-lookup"><span data-stu-id="1dac6-453">The port number.</span></span> <span data-ttu-id="1dac6-454">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-454">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-455">**PortType**</span><span class="sxs-lookup"><span data-stu-id="1dac6-455">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-456">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-457">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-458">目前為埠啟用的特定模式。</span><span class="sxs-lookup"><span data-stu-id="1dac6-458">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="1dac6-459">當設定為1時 (其他) ，相關的 **OtherPortType** 屬性會包含埠類型的字串描述。</span><span class="sxs-lookup"><span data-stu-id="1dac6-459">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="1dac6-460">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1dac6-460">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-461"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1dac6-461"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-462"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1dac6-462"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-463"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**50 銅的 10baset** (50) </span><span class="sxs-lookup"><span data-stu-id="1dac6-463"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-464"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51) </span><span class="sxs-lookup"><span data-stu-id="1dac6-464"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-465"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52) </span><span class="sxs-lookup"><span data-stu-id="1dac6-465"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-466"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53) </span><span class="sxs-lookup"><span data-stu-id="1dac6-466"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-467"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54) </span><span class="sxs-lookup"><span data-stu-id="1dac6-467"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-468"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55) </span><span class="sxs-lookup"><span data-stu-id="1dac6-468"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-469"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10gbase-t-CX4** (56) </span><span class="sxs-lookup"><span data-stu-id="1dac6-469"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-470"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**100 光纖 100base-tx-FX** (100) </span><span class="sxs-lookup"><span data-stu-id="1dac6-470"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-471"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100base-tx-SX** (101) </span><span class="sxs-lookup"><span data-stu-id="1dac6-471"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-472"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000base-t-SX** (102) </span><span class="sxs-lookup"><span data-stu-id="1dac6-472"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-473"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000base-t-LX** (103) </span><span class="sxs-lookup"><span data-stu-id="1dac6-473"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-474"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000base-t-CX** (104) </span><span class="sxs-lookup"><span data-stu-id="1dac6-474"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-475"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10gbase-t-SR** (105) </span><span class="sxs-lookup"><span data-stu-id="1dac6-475"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-476"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10gbase-t-SW** (106) </span><span class="sxs-lookup"><span data-stu-id="1dac6-476"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-477"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**LX4** (107) </span><span class="sxs-lookup"><span data-stu-id="1dac6-477"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-478"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10gbase-t-LR** (108) </span><span class="sxs-lookup"><span data-stu-id="1dac6-478"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-479"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**LW** (109) </span><span class="sxs-lookup"><span data-stu-id="1dac6-479"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-480"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10gbase-t-ER** (110) </span><span class="sxs-lookup"><span data-stu-id="1dac6-480"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-481"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span> (111) **的**</span><span class="sxs-lookup"><span data-stu-id="1dac6-481"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-482"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (16，000. 65535 ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-482"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-483">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1dac6-483">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-484">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-484">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-485">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-486">裝置的電源管理功能。</span><span class="sxs-lookup"><span data-stu-id="1dac6-486">The power management capabilities of the device.</span></span> <span data-ttu-id="1dac6-487">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-488">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1dac6-488">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-489">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1dac6-489">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-490">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-491">指出裝置是否可以受電源管理。</span><span class="sxs-lookup"><span data-stu-id="1dac6-491">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="1dac6-492">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-493">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="1dac6-493">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-494">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1dac6-494">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-495">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-496">此裝置自上一次電源週期起開啟電源的連續小時數。</span><span class="sxs-lookup"><span data-stu-id="1dac6-496">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="1dac6-497">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-498">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="1dac6-498">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-499">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-499">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-500">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-501">提供高層級的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1dac6-501">Provides high level status information.</span></span> <span data-ttu-id="1dac6-502">這個屬性應該與 **DetailedStatus** 屬性一起使用，以提供元素和其子元件的高階和詳細健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-502">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="1dac6-503">**Null** 值表示不會執行此屬性。</span><span class="sxs-lookup"><span data-stu-id="1dac6-503">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="1dac6-504">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-504">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-505"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1dac6-505"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-506"><span id="OK"></span><span id="ok"></span>**確定** (1) </span><span class="sxs-lookup"><span data-stu-id="1dac6-506"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-507"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span> (2) **降級**</span><span class="sxs-lookup"><span data-stu-id="1dac6-507"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-508"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**錯誤** (3) </span><span class="sxs-lookup"><span data-stu-id="1dac6-508"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-509"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="1dac6-509"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-510"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**廠商保留** (0x8000。</span><span class="sxs-lookup"><span data-stu-id="1dac6-510"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="1dac6-511">)</span><span class="sxs-lookup"><span data-stu-id="1dac6-511">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-512">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="1dac6-512">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-513">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1dac6-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-514">存取類型：僅限寫入</span><span class="sxs-lookup"><span data-stu-id="1dac6-514">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-515">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-515">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-516">要求的埠頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="1dac6-516">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="1dac6-517">實際的頻寬會在 [ **速度** ] 屬性中報告。</span><span class="sxs-lookup"><span data-stu-id="1dac6-517">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="1dac6-518">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1dac6-518">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-519">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="1dac6-519">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-520">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-521">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-522">上次要求或預期的專案狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-522">The last requested or desired state for the element.</span></span> <span data-ttu-id="1dac6-523">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 12 (不適用) 。</span><span class="sxs-lookup"><span data-stu-id="1dac6-523">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-524">**速度**</span><span class="sxs-lookup"><span data-stu-id="1dac6-524">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-525">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1dac6-525">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-526">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-526">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-527">限定詞： **單位** ( 「每秒位數」 ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-527">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-528">埠的頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="1dac6-528">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="1dac6-529">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1dac6-529">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-530">**狀態**</span><span class="sxs-lookup"><span data-stu-id="1dac6-530">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-531">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-532">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-533">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-533">The current status of the object.</span></span> <span data-ttu-id="1dac6-534">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-535">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1dac6-535">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-536">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-536">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-537">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-538">描述各種 **OperationalStatus** 陣列值的字串。</span><span class="sxs-lookup"><span data-stu-id="1dac6-538">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="1dac6-539">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-539">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-540">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1dac6-540">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-541">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-541">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-542">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-543">邏輯裝置的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-543">The current state of the logical device.</span></span> <span data-ttu-id="1dac6-544">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-544">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-545">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="1dac6-545">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-546">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-546">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-547">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-547">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-548">整數陣列，表示支援的光纖通道服務 (COS) 類別。</span><span class="sxs-lookup"><span data-stu-id="1dac6-548">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="1dac6-549">作用中的 COS 是由 **ActiveCOS** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="1dac6-549">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="1dac6-550">這個屬性繼承自 **CIM \_ FCPort**。</span><span class="sxs-lookup"><span data-stu-id="1dac6-550">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-551"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1dac6-551"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-552"><span id="1"></span>**1** (1) </span><span class="sxs-lookup"><span data-stu-id="1dac6-552"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-553"><span id="2"></span>**2** (2) </span><span class="sxs-lookup"><span data-stu-id="1dac6-553"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-554"><span id="3"></span>**3** (3) </span><span class="sxs-lookup"><span data-stu-id="1dac6-554"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-555"><span id="4"></span>**4** (4) </span><span class="sxs-lookup"><span data-stu-id="1dac6-555"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-556"><span id="5"></span>**5** (5) </span><span class="sxs-lookup"><span data-stu-id="1dac6-556"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-557"><span id="6"></span>**6** (6) </span><span class="sxs-lookup"><span data-stu-id="1dac6-557"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-558"><span id="F_"></span><span id="f_"></span>**F** (7 ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-558"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-559">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="1dac6-559">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-560">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="1dac6-560">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-561">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-561">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-562">整數陣列，表示支援的光纖通道 FC-4 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="1dac6-562">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="1dac6-563">作用中且正在執行的通訊協定是由 **ActiveFC4Types** 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="1dac6-563">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="1dac6-564">這個屬性繼承自 **CIM \_ FCPort**。</span><span class="sxs-lookup"><span data-stu-id="1dac6-564">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-565"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1dac6-565"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-566"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="1dac6-566"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-567"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4) </span><span class="sxs-lookup"><span data-stu-id="1dac6-567"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-568"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>透過 **FC 的 IP** (5) </span><span class="sxs-lookup"><span data-stu-id="1dac6-568"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-569"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8) </span><span class="sxs-lookup"><span data-stu-id="1dac6-569"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-570"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9) </span><span class="sxs-lookup"><span data-stu-id="1dac6-570"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-571"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI-3 主要** (17) </span><span class="sxs-lookup"><span data-stu-id="1dac6-571"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-572"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 從屬** (18) </span><span class="sxs-lookup"><span data-stu-id="1dac6-572"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-573"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 對等** (19) </span><span class="sxs-lookup"><span data-stu-id="1dac6-573"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-574"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 主要** (21) </span><span class="sxs-lookup"><span data-stu-id="1dac6-574"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-575"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 從屬** (22) </span><span class="sxs-lookup"><span data-stu-id="1dac6-575"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-576"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 對等** (23) </span><span class="sxs-lookup"><span data-stu-id="1dac6-576"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-577"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25) </span><span class="sxs-lookup"><span data-stu-id="1dac6-577"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-578"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="1dac6-578"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-579"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27) </span><span class="sxs-lookup"><span data-stu-id="1dac6-579"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-580"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 控制單位** (28) </span><span class="sxs-lookup"><span data-stu-id="1dac6-580"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-581"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**光纖通道 Services (fc-gs、fc-gs-2、fc-gs-3)** (32) </span><span class="sxs-lookup"><span data-stu-id="1dac6-581"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-582"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34) </span><span class="sxs-lookup"><span data-stu-id="1dac6-582"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-583"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36) </span><span class="sxs-lookup"><span data-stu-id="1dac6-583"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-584"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64) </span><span class="sxs-lookup"><span data-stu-id="1dac6-584"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-585"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80) </span><span class="sxs-lookup"><span data-stu-id="1dac6-585"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-586"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI 封裝區域網路 PDU** (81) </span><span class="sxs-lookup"><span data-stu-id="1dac6-586"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-587"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 封裝的 LAN PDU** (82) </span><span class="sxs-lookup"><span data-stu-id="1dac6-587"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-588"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88) </span><span class="sxs-lookup"><span data-stu-id="1dac6-588"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-589"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96) </span><span class="sxs-lookup"><span data-stu-id="1dac6-589"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-590"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**廠商唯一** (255) </span><span class="sxs-lookup"><span data-stu-id="1dac6-590"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-591">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="1dac6-591">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-592">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1dac6-592">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-593">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-594">限定詞： **單位** ( "Bytes" ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-594">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-595">可支援的最大傳輸單位 (MTU) （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1dac6-595">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="1dac6-596">這個屬性繼承自 [**CIM \_ NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-596">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-597">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1dac6-597">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-598">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-599">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-599">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-600">範圍系統的建立類別名稱。</span><span class="sxs-lookup"><span data-stu-id="1dac6-600">The scoping system's creation class name.</span></span> <span data-ttu-id="1dac6-601">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-601">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-602">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1dac6-602">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-603">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-604">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-604">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-605">範圍系統的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dac6-605">The scoping system's name.</span></span> <span data-ttu-id="1dac6-606">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)。</span><span class="sxs-lookup"><span data-stu-id="1dac6-606">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-607">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="1dac6-607">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-608">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1dac6-608">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-609">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-609">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-610">專案的已啟用狀態上次變更的日期或時間。</span><span class="sxs-lookup"><span data-stu-id="1dac6-610">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="1dac6-611">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1dac6-611">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-612">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="1dac6-612">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-613">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="1dac6-613">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-614">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-615">此裝置已獲得電源的總時數。</span><span class="sxs-lookup"><span data-stu-id="1dac6-615">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="1dac6-616">這個屬性繼承自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)，但不會使用它。</span><span class="sxs-lookup"><span data-stu-id="1dac6-616">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-617">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="1dac6-617">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-618">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-618">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-619">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-619">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-620">指出實例正在轉換的目標狀態。</span><span class="sxs-lookup"><span data-stu-id="1dac6-620">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="1dac6-621">這個屬性繼承自 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))，而且一律設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1dac6-621">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-622">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="1dac6-622">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-623">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="1dac6-623">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-624">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-624">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-625">在某些情況下，邏輯埠可能會識別為前端或後端埠。</span><span class="sxs-lookup"><span data-stu-id="1dac6-625">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="1dac6-626">這種情況的範例之一，就是可能有後端埠與磁片磁碟機和前端埠通訊以與主機通訊的存放裝置陣列。</span><span class="sxs-lookup"><span data-stu-id="1dac6-626">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="1dac6-627">如果埠的使用沒有限制，則值應該設定為 4 (不受限制的) 。</span><span class="sxs-lookup"><span data-stu-id="1dac6-627">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="1dac6-628">這個屬性繼承自 [**CIM \_ LogicalPort**](/previous-versions//cc136869(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1dac6-628">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="1dac6-629"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="1dac6-629"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-630"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**前端** (2) </span><span class="sxs-lookup"><span data-stu-id="1dac6-630"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-631"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span> (3) 的 **後端**</span><span class="sxs-lookup"><span data-stu-id="1dac6-631"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-632"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**不受限制** (4 ) </span><span class="sxs-lookup"><span data-stu-id="1dac6-632"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1dac6-633">**WWNN**</span><span class="sxs-lookup"><span data-stu-id="1dac6-633">**WWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-634">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-635">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-635">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-636">此光纖通道埠的全球節點名稱。</span><span class="sxs-lookup"><span data-stu-id="1dac6-636">The world wide node name for this Fibre Channel port.</span></span>

</dd> <dt>

<span data-ttu-id="1dac6-637">**WWPN**</span><span class="sxs-lookup"><span data-stu-id="1dac6-637">**WWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dac6-638">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1dac6-638">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1dac6-639">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1dac6-639">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dac6-640">此光纖通道埠的全球埠名稱。</span><span class="sxs-lookup"><span data-stu-id="1dac6-640">The world wide port name for this Fibre Channel port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1dac6-641">規格需求</span><span class="sxs-lookup"><span data-stu-id="1dac6-641">Requirements</span></span>



| <span data-ttu-id="1dac6-642">需求</span><span class="sxs-lookup"><span data-stu-id="1dac6-642">Requirement</span></span> | <span data-ttu-id="1dac6-643">值</span><span class="sxs-lookup"><span data-stu-id="1dac6-643">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dac6-644">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1dac6-644">Minimum supported client</span></span><br/> | <span data-ttu-id="1dac6-645">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dac6-645">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1dac6-646">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1dac6-646">Minimum supported server</span></span><br/> | <span data-ttu-id="1dac6-647">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1dac6-647">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1dac6-648">命名空間</span><span class="sxs-lookup"><span data-stu-id="1dac6-648">Namespace</span></span><br/>                | <span data-ttu-id="1dac6-649">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1dac6-649">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1dac6-650">MOF</span><span class="sxs-lookup"><span data-stu-id="1dac6-650">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1dac6-651"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-651"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1dac6-652">DLL</span><span class="sxs-lookup"><span data-stu-id="1dac6-652">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dac6-653"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1dac6-653"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

