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
ms.openlocfilehash: 071a3b606d4fcb9845073877eb52dcf61b9a732a3046cf255229c6ea05451a14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046918"
---
# <a name="cim_fcport-class"></a>CIM \_ FCPort 類別

> [!NOTE]
> 本文包含「從屬」一詞的參考，Microsoft 已不再使用該字詞。 從軟體中移除該字詞時，我們也會將其從本文中移除。

表示光纖通道 (FC) 埠裝置的功能和管理。

## <a name="syntax"></a>語法

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

## <a name="members"></a>成員

> [!NOTE]
> 本文包含「從屬」一詞的參考，Microsoft 已不再使用該字詞。 從軟體中移除該字詞時，我們也會將其從本文中移除。

**CIM \_ FCPort** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ FCPort** 類別具有這些屬性。

<dl> <dt>

**ActiveCOS**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ FCPort**.**SupportedCOS**") 
</dt> </dl>

服務的使用中類別 (為光纖通道設定的 COS) 。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="1"></span>

**1** (1) 


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** (2) 


</dt> <dd></dd> <dt>

<span id="3"></span>

**3** (3) 


</dt> <dd></dd> <dt>

<span id="4"></span>

**4** (4) 


</dt> <dd></dd> <dt>

<span id="5"></span>

**5** (5) 


</dt> <dd></dd> <dt>

<span id="6"></span>

**6** (6) 


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

**F** (7) 


</dt> <dd></dd> </dl>

</dd> <dt>

**ActiveFC4Types**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ FCPort**.**SupportedFC4Types**") 
</dt> </dl>

光纖通道上執行的 FC 4 通訊協定。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

**ISO/IEC 8802-2 LLC** (4) 


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

透過 **FC 的 IP** (5) 


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

**SCSI-FCP** (8) 


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

**SCSI-GPP** (9) 


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

**IPI-3 主要** (17) 


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

**IPI-3 從屬** (18) 


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

**IPI-3 對等** (19) 


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

**CP IPI-3 主要** (21) 


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

**CP IPI-3 從屬** (22) 


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

**CP IPI-3 對等** (23) 


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

**SBCCS Channel** (25) 


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

**SBCCS Control Unit** (26) 


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

**FC-SB-2 Channel** (27) 


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

**FC-SB-2 控制單位** (28) 


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

**光纖通道 Services (fc-gs、fc-gs-2、fc-gs-3)** (32) 


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

**FC-SW** (34) 


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

**FC-SNMP** (36) 


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

**HIPPI-FP** (64) 


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

**BBL Control** (80) 


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

**BBL FDDI 封裝區域網路 PDU** (81) 


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

**BBL 802.3 封裝的 LAN PDU** (82) 


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

**FC-VI** (88) 


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

**FC-AV** (96) 


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

**廠商唯一** (255) 


</dt> <dd></dd> </dl>

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PortType" ) 
</dt> </dl>

埠的啟用模式。 埠模式是由 ANSI X3 標準所定義。 如果埠已登入，則這會是協商的埠類型，否則會回報設定的埠類型。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

相關的屬性 **OtherPortType** 包含埠類型的字串描述

</dd> <dt>

<span id="N"></span><span id="n"></span>

<span id="N"></span><span id="n"></span>**N** (10) 


</dt> <dd>

節點埠

</dd> <dt>

<span id="NL"></span><span id="nl"></span>

<span id="NL"></span><span id="nl"></span>**NL** (11) 


</dt> <dd>

支援 FC 仲裁迴圈的節點埠

</dd> <dt>

<span id="F_NL"></span><span id="f_nl"></span>

<span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12) 


</dt> <dd></dd> <dt>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>**Nx** (13) 


</dt> <dd>

埠可能會協商為節點埠 (N) 或支援 FC 仲裁迴圈 (NL 的節點埠) 

</dd> <dt>

<span id="E"></span><span id="e"></span>

<span id="E"></span><span id="e"></span>**E** (14) 


</dt> <dd>

連接網狀架構元素的擴充埠 (例如 FC 交換器) 

</dd> <dt>

<span id="F"></span><span id="f"></span>

<span id="F"></span><span id="f"></span>**F** (15) 


</dt> <dd>

網狀架構 (元素) 埠

</dd> <dt>

<span id="FL"></span><span id="fl"></span>

<span id="FL"></span><span id="fl"></span>**FL** (16) 


</dt> <dd>

支援 FC 仲裁迴圈的網狀架構 (元素) 埠

</dd> <dt>

<span id="B"></span><span id="b"></span>

<span id="B"></span><span id="b"></span>**B** (17) 


</dt> <dd>

橋接器埠

</dd> <dt>

<span id="G"></span><span id="g"></span>

<span id="G"></span><span id="g"></span>**G** (18) 


</dt> <dd>

埠可能會進行協商，以成為 (E) 的擴充埠，或 (F 的網狀架構埠) 

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (16，000. 65535) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedCOS**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

服務的類別 (光纖通道所支援的 COS) 設定。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="1"></span>

**1** (1) 


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** (2) 


</dt> <dd></dd> <dt>

<span id="3"></span>

**3** (3) 


</dt> <dd></dd> <dt>

<span id="4"></span>

**4** (4) 


</dt> <dd></dd> <dt>

<span id="5"></span>

**5** (5) 


</dt> <dd></dd> <dt>

<span id="6"></span>

**6** (6) 


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

**F** (7) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedFC4Types**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

光纖通道支援的 FC-4 通訊協定。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

**ISO/IEC 8802-2 LLC** (4) 


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

透過 **FC 的 IP** (5) 


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

**SCSI-FCP** (8) 


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

**SCSI-GPP** (9) 


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

**IPI-3 主要** (17) 


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

**IPI-3 從屬** (18) 


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

**IPI-3 對等** (19) 


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

**CP IPI-3 主要** (21) 


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

**CP IPI-3 從屬** (22) 


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

**CP IPI-3 對等** (23) 


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

**SBCCS Channel** (25) 


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

**SBCCS Control Unit** (26) 


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

**FC-SB-2 Channel** (27) 


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

**FC-SB-2 控制單位** (28) 


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

**光纖通道 Services (fc-gs、fc-gs-2、fc-gs-3)** (32) 


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

**FC-SW** (34) 


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

**FC-SNMP** (36) 


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

**HIPPI-FP** (64) 


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

**BBL Control** (80) 


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

**BBL FDDI 封裝區域網路 PDU** (81) 


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

**BBL 802.3 封裝的 LAN PDU** (82) 


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

**FC-VI** (88) 


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

**FC-AV** (96) 


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

**廠商唯一** (255) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ NetworkPort**](cim-networkport.md)
</dt> </dl>

 

