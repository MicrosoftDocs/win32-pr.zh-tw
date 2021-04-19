---
description: 表示光纖通道 (FC) 埠裝置的功能和管理。
ms.assetid: 32a11971-9e18-410d-a3cd-4921a7e986f0
title: CIM_FCPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FCPort
- CIM_FCPort.PortType
- CIM_FCPort.SupportedCOS
- CIM_FCPort.ActiveCOS
- CIM_FCPort.SupportedFC4Types
- CIM_FCPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6a858cbb4603743e1ddd11cac71500a9e39325a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973804"
---
# <a name="cim_fcport-class"></a><span data-ttu-id="10ca7-103">CIM \_ FCPort 類別</span><span class="sxs-lookup"><span data-stu-id="10ca7-103">CIM\_FCPort class</span></span>

> [!NOTE]
> <span data-ttu-id="10ca7-104">本文包含「從屬」一詞的參考，Microsoft 已不再使用該字詞。</span><span class="sxs-lookup"><span data-stu-id="10ca7-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="10ca7-105">從軟體中移除該字詞時，我們也會將其從本文中移除。</span><span class="sxs-lookup"><span data-stu-id="10ca7-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="10ca7-106">表示光纖通道 (FC) 埠裝置的功能和管理。</span><span class="sxs-lookup"><span data-stu-id="10ca7-106">Represents the capabilities and management of a fibre channel (FC) port device.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ca7-107">語法</span><span class="sxs-lookup"><span data-stu-id="10ca7-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::FC"), AMENDMENT]
class CIM_FCPort : CIM_NetworkPort
{
  uint16 PortType;
  uint16 SupportedCOS[];
  uint16 ActiveCOS[];
  uint16 SupportedFC4Types[];
  uint16 ActiveFC4Types[];
};
```

## <a name="members"></a><span data-ttu-id="10ca7-108">成員</span><span class="sxs-lookup"><span data-stu-id="10ca7-108">Members</span></span>

> [!NOTE]
> <span data-ttu-id="10ca7-109">本文包含「從屬」一詞的參考，Microsoft 已不再使用該字詞。</span><span class="sxs-lookup"><span data-stu-id="10ca7-109">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="10ca7-110">從軟體中移除該字詞時，我們也會將其從本文中移除。</span><span class="sxs-lookup"><span data-stu-id="10ca7-110">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="10ca7-111">**CIM \_ FCPort** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="10ca7-111">The **CIM\_FCPort** class has these types of members:</span></span>

-   [<span data-ttu-id="10ca7-112">屬性</span><span class="sxs-lookup"><span data-stu-id="10ca7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10ca7-113">屬性</span><span class="sxs-lookup"><span data-stu-id="10ca7-113">Properties</span></span>

<span data-ttu-id="10ca7-114">**CIM \_ FCPort** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="10ca7-114">The **CIM\_FCPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10ca7-115">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="10ca7-115">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ca7-116">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="10ca7-116">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10ca7-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10ca7-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ca7-118">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ FCPort**.**SupportedCOS**") </span><span class="sxs-lookup"><span data-stu-id="10ca7-118">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedCOS**")</span></span>
</dt> </dl>

<span data-ttu-id="10ca7-119">服務的使用中類別 (為光纖通道設定的 COS) 。</span><span class="sxs-lookup"><span data-stu-id="10ca7-119">The active class of service (COS) settings for the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10ca7-120">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="10ca7-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="10ca7-121">**1** (1) </span><span class="sxs-lookup"><span data-stu-id="10ca7-121">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="10ca7-122">**2** (2) </span><span class="sxs-lookup"><span data-stu-id="10ca7-122">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="10ca7-123">**3** (3) </span><span class="sxs-lookup"><span data-stu-id="10ca7-123">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="10ca7-124">**4** (4) </span><span class="sxs-lookup"><span data-stu-id="10ca7-124">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="10ca7-125">**5** (5) </span><span class="sxs-lookup"><span data-stu-id="10ca7-125">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="10ca7-126">**6** (6) </span><span class="sxs-lookup"><span data-stu-id="10ca7-126">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="10ca7-127">**F** (7) </span><span class="sxs-lookup"><span data-stu-id="10ca7-127">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10ca7-128">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="10ca7-128">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ca7-129">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="10ca7-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10ca7-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10ca7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ca7-131">限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ FCPort**.**SupportedFC4Types**") </span><span class="sxs-lookup"><span data-stu-id="10ca7-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedFC4Types**")</span></span>
</dt> </dl>

<span data-ttu-id="10ca7-132">光纖通道上執行的 FC 4 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="10ca7-132">The FC-4 protocols that are running on the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10ca7-133">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="10ca7-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10ca7-134">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="10ca7-134">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="10ca7-135">**ISO/IEC 8802-2 LLC** (4) </span><span class="sxs-lookup"><span data-stu-id="10ca7-135">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="10ca7-136">透過 **FC 的 IP** (5) </span><span class="sxs-lookup"><span data-stu-id="10ca7-136">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="10ca7-137">**SCSI-FCP** (8) </span><span class="sxs-lookup"><span data-stu-id="10ca7-137">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="10ca7-138">**SCSI-GPP** (9) </span><span class="sxs-lookup"><span data-stu-id="10ca7-138">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="10ca7-139">**IPI-3 主要** (17) </span><span class="sxs-lookup"><span data-stu-id="10ca7-139">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="10ca7-140">**IPI-3 從屬** (18) </span><span class="sxs-lookup"><span data-stu-id="10ca7-140">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="10ca7-141">**IPI-3 對等** (19) </span><span class="sxs-lookup"><span data-stu-id="10ca7-141">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="10ca7-142">**CP IPI-3 主要** (21) </span><span class="sxs-lookup"><span data-stu-id="10ca7-142">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="10ca7-143">**CP IPI-3 從屬** (22) </span><span class="sxs-lookup"><span data-stu-id="10ca7-143">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="10ca7-144">**CP IPI-3 對等** (23) </span><span class="sxs-lookup"><span data-stu-id="10ca7-144">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="10ca7-145">**SBCCS Channel** (25) </span><span class="sxs-lookup"><span data-stu-id="10ca7-145">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="10ca7-146">**SBCCS Control Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="10ca7-146">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="10ca7-147">**FC-SB-2 Channel** (27) </span><span class="sxs-lookup"><span data-stu-id="10ca7-147">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="10ca7-148">**FC-SB-2 控制單位** (28) </span><span class="sxs-lookup"><span data-stu-id="10ca7-148">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="10ca7-149">**光纖通道 Services (fc-gs、fc-gs-2、fc-gs-3)** (32) </span><span class="sxs-lookup"><span data-stu-id="10ca7-149">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="10ca7-150">**FC-SW** (34) </span><span class="sxs-lookup"><span data-stu-id="10ca7-150">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="10ca7-151">**FC-SNMP** (36) </span><span class="sxs-lookup"><span data-stu-id="10ca7-151">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="10ca7-152">**HIPPI-FP** (64) </span><span class="sxs-lookup"><span data-stu-id="10ca7-152">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="10ca7-153">**BBL Control** (80) </span><span class="sxs-lookup"><span data-stu-id="10ca7-153">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="10ca7-154">**BBL FDDI 封裝區域網路 PDU** (81) </span><span class="sxs-lookup"><span data-stu-id="10ca7-154">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="10ca7-155">**BBL 802.3 封裝的 LAN PDU** (82) </span><span class="sxs-lookup"><span data-stu-id="10ca7-155">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="10ca7-156">**FC-VI** (88) </span><span class="sxs-lookup"><span data-stu-id="10ca7-156">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="10ca7-157">**FC-AV** (96) </span><span class="sxs-lookup"><span data-stu-id="10ca7-157">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="10ca7-158">**廠商唯一** (255) </span><span class="sxs-lookup"><span data-stu-id="10ca7-158">**Vendor Unique** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10ca7-159">**PortType**</span><span class="sxs-lookup"><span data-stu-id="10ca7-159">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ca7-160">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="10ca7-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10ca7-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10ca7-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10ca7-162">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PortType" ) </span><span class="sxs-lookup"><span data-stu-id="10ca7-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="10ca7-163">埠的啟用模式。</span><span class="sxs-lookup"><span data-stu-id="10ca7-163">The enabled mode for the port.</span></span> <span data-ttu-id="10ca7-164">埠模式是由 ANSI X3 標準所定義。</span><span class="sxs-lookup"><span data-stu-id="10ca7-164">The port modes are defined by ANSI X3 standards.</span></span> <span data-ttu-id="10ca7-165">如果埠已登入，則這會是協商的埠類型，否則會回報設定的埠類型。</span><span class="sxs-lookup"><span data-stu-id="10ca7-165">If the port is logged in, this will be the negotiated port type, otherwise the configured port type will be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10ca7-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="10ca7-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10ca7-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="10ca7-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="10ca7-168">相關的屬性 **OtherPortType** 包含埠類型的字串描述</span><span class="sxs-lookup"><span data-stu-id="10ca7-168">The related property **OtherPortType** contains a string description of the type of port</span></span>

</dd> <dt>

<span id="N"></span><span id="n"></span>

<span data-ttu-id="10ca7-169"><span id="N"></span><span id="n"></span>**N** (10) </span><span class="sxs-lookup"><span data-stu-id="10ca7-169"><span id="N"></span><span id="n"></span>**N** (10)</span></span>


</dt> <dd>

<span data-ttu-id="10ca7-170">節點埠</span><span class="sxs-lookup"><span data-stu-id="10ca7-170">Node Port</span></span>

</dd> <dt>

<span id="NL"></span><span id="nl"></span>

<span data-ttu-id="10ca7-171"><span id="NL"></span><span id="nl"></span>**NL** (11) </span><span class="sxs-lookup"><span data-stu-id="10ca7-171"><span id="NL"></span><span id="nl"></span>**NL** (11)</span></span>


</dt> <dd>

<span data-ttu-id="10ca7-172">支援 FC 仲裁迴圈的節點埠</span><span class="sxs-lookup"><span data-stu-id="10ca7-172">Node Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="F_NL"></span><span id="f_nl"></span>

<span data-ttu-id="10ca7-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12) </span><span class="sxs-lookup"><span data-stu-id="10ca7-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>

<span data-ttu-id="10ca7-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**Nx** (13) </span><span class="sxs-lookup"><span data-stu-id="10ca7-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**Nx** (13)</span></span>


</dt> <dd>

<span data-ttu-id="10ca7-175">埠可能會協商為節點埠 (N) 或支援 FC 仲裁迴圈 (NL 的節點埠) </span><span class="sxs-lookup"><span data-stu-id="10ca7-175">Port may negotiate to become either a node port (N) or a node port supporting FC arbitrated loop (NL)</span></span>

</dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="10ca7-176"><span id="E"></span><span id="e"></span>**E** (14) </span><span class="sxs-lookup"><span data-stu-id="10ca7-176"><span id="E"></span><span id="e"></span>**E** (14)</span></span>


</dt> <dd>

<span data-ttu-id="10ca7-177">連接網狀架構元素的擴充埠 (例如 FC 交換器) </span><span class="sxs-lookup"><span data-stu-id="10ca7-177">Expansion Port connecting fabric elements (for example, FC switches)</span></span>

</dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="10ca7-178"><span id="F"></span><span id="f"></span>**F** (15) </span><span class="sxs-lookup"><span data-stu-id="10ca7-178"><span id="F"></span><span id="f"></span>**F** (15)</span></span>


</dt> <dd>

<span data-ttu-id="10ca7-179">網狀架構 (元素) 埠</span><span class="sxs-lookup"><span data-stu-id="10ca7-179">Fabric (element) Port</span></span>

</dd> <dt>

<span id="FL"></span><span id="fl"></span>

<span data-ttu-id="10ca7-180"><span id="FL"></span><span id="fl"></span>**FL** (16) </span><span class="sxs-lookup"><span data-stu-id="10ca7-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span></span>


</dt> <dd>

<span data-ttu-id="10ca7-181">支援 FC 仲裁迴圈的網狀架構 (元素) 埠</span><span class="sxs-lookup"><span data-stu-id="10ca7-181">Fabric (element) Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="10ca7-182"><span id="B"></span><span id="b"></span>**B** (17) </span><span class="sxs-lookup"><span data-stu-id="10ca7-182"><span id="B"></span><span id="b"></span>**B** (17)</span></span>


</dt> <dd>

<span data-ttu-id="10ca7-183">橋接器埠</span><span class="sxs-lookup"><span data-stu-id="10ca7-183">Bridge port</span></span>

</dd> <dt>

<span id="G"></span><span id="g"></span>

<span data-ttu-id="10ca7-184"><span id="G"></span><span id="g"></span>**G** (18) </span><span class="sxs-lookup"><span data-stu-id="10ca7-184"><span id="G"></span><span id="g"></span>**G** (18)</span></span>


</dt> <dd>

<span data-ttu-id="10ca7-185">埠可能會進行協商，以成為 (E) 的擴充埠，或 (F 的網狀架構埠) </span><span class="sxs-lookup"><span data-stu-id="10ca7-185">Port may negotiate to become either an expansion port (E), or a fabric port (F)</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="10ca7-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (16，000. 65535) </span><span class="sxs-lookup"><span data-stu-id="10ca7-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10ca7-187">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="10ca7-187">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ca7-188">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="10ca7-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10ca7-189">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10ca7-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ca7-190">服務的類別 (光纖通道所支援的 COS) 設定。</span><span class="sxs-lookup"><span data-stu-id="10ca7-190">The class of service (COS) settings that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10ca7-191">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="10ca7-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="10ca7-192">**1** (1) </span><span class="sxs-lookup"><span data-stu-id="10ca7-192">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="10ca7-193">**2** (2) </span><span class="sxs-lookup"><span data-stu-id="10ca7-193">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="10ca7-194">**3** (3) </span><span class="sxs-lookup"><span data-stu-id="10ca7-194">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="10ca7-195">**4** (4) </span><span class="sxs-lookup"><span data-stu-id="10ca7-195">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="10ca7-196">**5** (5) </span><span class="sxs-lookup"><span data-stu-id="10ca7-196">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="10ca7-197">**6** (6) </span><span class="sxs-lookup"><span data-stu-id="10ca7-197">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="10ca7-198">**F** (7) </span><span class="sxs-lookup"><span data-stu-id="10ca7-198">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10ca7-199">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="10ca7-199">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10ca7-200">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="10ca7-200">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10ca7-201">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="10ca7-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10ca7-202">光纖通道支援的 FC-4 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="10ca7-202">The FC-4 protocols that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10ca7-203">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="10ca7-203">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10ca7-204">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="10ca7-204">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="10ca7-205">**ISO/IEC 8802-2 LLC** (4) </span><span class="sxs-lookup"><span data-stu-id="10ca7-205">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="10ca7-206">透過 **FC 的 IP** (5) </span><span class="sxs-lookup"><span data-stu-id="10ca7-206">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="10ca7-207">**SCSI-FCP** (8) </span><span class="sxs-lookup"><span data-stu-id="10ca7-207">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="10ca7-208">**SCSI-GPP** (9) </span><span class="sxs-lookup"><span data-stu-id="10ca7-208">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="10ca7-209">**IPI-3 主要** (17) </span><span class="sxs-lookup"><span data-stu-id="10ca7-209">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="10ca7-210">**IPI-3 從屬** (18) </span><span class="sxs-lookup"><span data-stu-id="10ca7-210">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="10ca7-211">**IPI-3 對等** (19) </span><span class="sxs-lookup"><span data-stu-id="10ca7-211">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="10ca7-212">**CP IPI-3 主要** (21) </span><span class="sxs-lookup"><span data-stu-id="10ca7-212">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="10ca7-213">**CP IPI-3 從屬** (22) </span><span class="sxs-lookup"><span data-stu-id="10ca7-213">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="10ca7-214">**CP IPI-3 對等** (23) </span><span class="sxs-lookup"><span data-stu-id="10ca7-214">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="10ca7-215">**SBCCS Channel** (25) </span><span class="sxs-lookup"><span data-stu-id="10ca7-215">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="10ca7-216">**SBCCS Control Unit** (26) </span><span class="sxs-lookup"><span data-stu-id="10ca7-216">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="10ca7-217">**FC-SB-2 Channel** (27) </span><span class="sxs-lookup"><span data-stu-id="10ca7-217">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="10ca7-218">**FC-SB-2 控制單位** (28) </span><span class="sxs-lookup"><span data-stu-id="10ca7-218">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="10ca7-219">**光纖通道 Services (fc-gs、fc-gs-2、fc-gs-3)** (32) </span><span class="sxs-lookup"><span data-stu-id="10ca7-219">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="10ca7-220">**FC-SW** (34) </span><span class="sxs-lookup"><span data-stu-id="10ca7-220">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="10ca7-221">**FC-SNMP** (36) </span><span class="sxs-lookup"><span data-stu-id="10ca7-221">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="10ca7-222">**HIPPI-FP** (64) </span><span class="sxs-lookup"><span data-stu-id="10ca7-222">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="10ca7-223">**BBL Control** (80) </span><span class="sxs-lookup"><span data-stu-id="10ca7-223">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="10ca7-224">**BBL FDDI 封裝區域網路 PDU** (81) </span><span class="sxs-lookup"><span data-stu-id="10ca7-224">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="10ca7-225">**BBL 802.3 封裝的 LAN PDU** (82) </span><span class="sxs-lookup"><span data-stu-id="10ca7-225">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="10ca7-226">**FC-VI** (88) </span><span class="sxs-lookup"><span data-stu-id="10ca7-226">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="10ca7-227">**FC-AV** (96) </span><span class="sxs-lookup"><span data-stu-id="10ca7-227">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="10ca7-228">**廠商唯一** (255) </span><span class="sxs-lookup"><span data-stu-id="10ca7-228">**Vendor Unique** (255)</span></span>


<span data-ttu-id="10ca7-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="10ca7-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="10ca7-230">規格需求</span><span class="sxs-lookup"><span data-stu-id="10ca7-230">Requirements</span></span>



| <span data-ttu-id="10ca7-231">需求</span><span class="sxs-lookup"><span data-stu-id="10ca7-231">Requirement</span></span> | <span data-ttu-id="10ca7-232">值</span><span class="sxs-lookup"><span data-stu-id="10ca7-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10ca7-233">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10ca7-233">Minimum supported client</span></span><br/> | <span data-ttu-id="10ca7-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="10ca7-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="10ca7-235">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10ca7-235">Minimum supported server</span></span><br/> | <span data-ttu-id="10ca7-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10ca7-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="10ca7-237">命名空間</span><span class="sxs-lookup"><span data-stu-id="10ca7-237">Namespace</span></span><br/>                | <span data-ttu-id="10ca7-238">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="10ca7-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="10ca7-239">MOF</span><span class="sxs-lookup"><span data-stu-id="10ca7-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10ca7-240"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="10ca7-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="10ca7-241">DLL</span><span class="sxs-lookup"><span data-stu-id="10ca7-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10ca7-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="10ca7-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="10ca7-243">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10ca7-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ca7-244">**CIM \_ NetworkPort**</span><span class="sxs-lookup"><span data-stu-id="10ca7-244">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

