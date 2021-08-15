---
description: 此類別是網路介面卡設定事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: SystemConfig_NIC 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 822e8404137eee9731bbfcee9f5d9f4495609078c4251b53269371dd4904cea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393814"
---
# <a name="systemconfig_nic-class"></a>SystemConfig \_ NIC 類別

此類別是網路介面卡設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a>成員

**SystemConfig \_ NIC** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ NIC** 類別具有這些屬性。

<dl> <dt>

DnsServerAddresses
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (7) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

用來查詢 DNS 伺服器的 IP 位址。 地址清單會以逗號分隔。

</dd> <dt>

IpAddresses
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

與網路介面卡相關聯的 IP 位址。 地址清單會以逗號分隔。

</dd> <dt>

Ipv4Index
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

IPv4 NIC 的介面卡索引。 介面卡已停用並啟用，或在其他情況下，介面卡索引可能會變更，而且不應該被視為持續性。

</dd> <dt>

Ipv6Index
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

IPv6 NIC 的介面卡索引。 介面卡已停用並啟用，或在其他情況下，介面卡索引可能會變更，而且不應該被視為持續性。

</dd> <dt>

NICDescription
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

介面卡的描述。

</dd> <dt>

PhysicalAddr
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) ，格式 ( "x" ) 
</dt> </dl>

介面卡的硬體位址。

</dd> <dt>

PhysicalAddrLen
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

介面卡的硬體位址長度。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




