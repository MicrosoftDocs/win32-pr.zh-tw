---
description: 可以連接到 LAN 以傳送及接收資料框架的通訊端點。 LAN 端點包括乙太網路、權杖環和 FDDI 介面。
ms.assetid: c69464cf-00a9-476d-a494-2d7d65776334
title: CIM_LANEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LANEndpoint
- CIM_LANEndpoint.LANID
- CIM_LANEndpoint.LANType
- CIM_LANEndpoint.OtherLANType
- CIM_LANEndpoint.MACAddress
- CIM_LANEndpoint.AliasAddresses
- CIM_LANEndpoint.GroupAddresses
- CIM_LANEndpoint.MaxDataSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c924d175cb48e53346daff59a6317a4a0f241f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992619"
---
# <a name="cim_lanendpoint-class"></a>CIM \_ LANEndpoint 類別

可以連接到 LAN 以傳送及接收資料框架的通訊端點。 LAN 端點包括乙太網路、權杖環和 FDDI 介面。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_LANEndpoint : CIM_ProtocolEndpoint
{
  string LANID;
  uint16 LANType;
  string OtherLANType;
  string MACAddress;
  string AliasAddresses[];
  string GroupAddresses[];
  uint32 MaxDataSize;
};
```

## <a name="members"></a>成員

**CIM \_ LANEndpoint** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ LANEndpoint** 類別具有這些屬性。

<dl> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

陣列，其中包含可用來與 LAN 端點通訊的其他單播位址。

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

陣列，包含 LAN 端點接聽的多播位址。

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "cim \_ LANConnectivitySegment. LANID，CIM \_ LANSegment. LANID" ) 
</dt> </dl>

端點所連接之 LAN 區段的標籤或識別碼。 如果端點目前未連線或此資訊未知，則 **LANID** 為 Null。

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md)」。**ProtocolType**") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ LANCONNECTIVITYSEGMENT. >connectivitytype，cim \_ LANSegment. LANType ") 
</dt> </dl>

> [!Note]  
> 已淘汰的描述： LAN 上使用的技術種類。

 

此屬性已被取代。 相反地，我們建議使用 **ProtocolType** 屬性。

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

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

**TokenRing** (3) 


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (4) 


</dt> <dd></dd> </dl>

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12) 
</dt> </dl>

LAN 端點所使用的主體單播位址。

MAC 位址的格式必須為下列特性：

-   位址包含十二個十六進位數位。
-   每一組數位代表 MAC 位址中六個八位的其中一個。
-   每一對數位都必須根據 RFC 2469 以標準的位順序表示。

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bits" ) 
</dt> </dl>

LAN 端點所傳送或接收之資料欄位的大小上限（以位元組為單位）。

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**淘汰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ( 「[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md)」。**OtherTypeDescription**") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" Cim \_ LANConnectivitySegment. OtherTypeDescription "，"**cim \_ LANEndpoint**.**LANType**") 
</dt> </dl>

> [!Note]  
> 已淘汰的描述：當 **LANType** 屬性設定為 "1" (其他) 時，LAN 所使用的技術類型。

 

此屬性已被取代。 相反地，我們建議使用 **OtherTypeDescription** 屬性。

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

[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md)
</dt> </dl>

 

