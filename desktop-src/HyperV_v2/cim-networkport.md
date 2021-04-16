---
description: 網路裝置上網路埠的邏輯標記法。
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: CIM_NetworkPort 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e3ac64b55e17d0526527ebbaca168c3f7b289f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194559"
---
# <a name="cim_networkport-class"></a>CIM \_ NetworkPort 類別

網路裝置上網路埠的邏輯標記法。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a>成員

**CIM \_ NetworkPort** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ NetworkPort** 類別具有這些屬性。

<dl> <dt>

**ActiveMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) 
</dt> </dl>

埠支援的作用中或已協商的最大傳輸單位 (MTU) 。

</dd> <dt>

**自動感測**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果埠可以自動判斷連接之網路媒體的速度或其他通訊特性，則 **為 true** ;否則 **為 false**。

</dd> <dt>

**FullDuplex**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果埠是以全雙工模式運作，則為 **true** ;否則 **為 false**。

</dd> <dt>

**LinkTechnology**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ NetworkPort**.**OtherLinkTechnology**") 
</dt> </dl>

埠所使用的連結技術。 當設定為 "1" (其他) 時， **OtherLinkTechnology** 屬性會包含連結類型的描述。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (2) 


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

**IB** (3) 


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

**FC** (4) 


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (5) 


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (6) 


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**權杖環** (7) 


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**框架轉送** (8) 


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

**紅外線** (9) 


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

**藍牙** (10) 


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

**無線區域網路** (11) 


</dt> <dd></dd> </dl>

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 網路介面卡802埠 \| 001.3 ") 
</dt> </dl>

陣列，其中包含埠的網路位址。

</dd> <dt>

**OtherLinkTechnology**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ NetworkPort**.**LinkTechnology**") 
</dt> </dl>

當 **LinkTechnology** 設定為 "1" 時，連結技術 (其他) 。

</dd> <dt>

**OtherNetworkPortType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「**CIM \_ NetworkPort**。**OtherPortType**") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalPort**](cim-logicalport.md)。**PortType**") 
</dt> </dl>

> [!Note]  
> 已淘汰的描述：當 **PortType** 屬性包含 1 (其他) 時，埠的模組類型。

 

此屬性已被取代。 相反地，我們建議 [**CIM \_ LogicalPort**](cim-logicalport.md)類別中的 **PortType** 屬性。

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 網路介面卡802埠 \| 001.2 ") 
</dt> </dl>

硬式編碼在埠中的網路位址。 您可以使用固件升級或軟體設定來變更硬式編碼的位址。 進行這項變更時，應同時更新此屬性。 如果位址不存在， **PermanentAddress** 應該保留空白。

</dd> <dt>

**PortNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

網路埠的埠號碼。 網路埠的編號通常相對於邏輯模組或網路元素。

</dd> <dt>

**速度**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "速度" ) 、 [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "每秒位數" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIB。IETF \| Mib-ii ifSpeed "，" MIF。DMTF \| Network Adapter 802 Port \| 001.5 ") ， **PUnit** (" bit/second ") 
</dt> </dl>

埠目前的頻寬（以位/秒為單位）。 針對因頻寬而異的埠，或無法進行準確估計的埠，此屬性應該包含名義頻寬。

</dd> <dt>

**SupportedMaximumTransmissionUnit**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) 
</dt> </dl>

埠所支援的最大傳輸單位 (MTU) 。

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

[**CIM \_ LogicalPort**](cim-logicalport.md)
</dt> </dl>

 

