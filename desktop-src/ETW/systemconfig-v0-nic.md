---
description: 此類別是網路介面卡設定事件的事件種類類別。
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: SystemConfig_V0_NIC 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973648"
---
# <a name="systemconfig_v0_nic-class"></a>SystemConfig \_ V0 \_ NIC 類別

此類別是網路介面卡設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a>成員

**SystemConfig \_ V0 \_ NIC** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ V0 \_ NIC** 類別具有這些屬性。

<dl> <dt>

**資料**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (16) 
</dt> </dl>

資料欄位。

</dd> <dt>

**DhcpServer**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (8) 
</dt> </dl>

動態主機設定通訊協定 (DHCP) server 的 IP 位址。 值為255.255.255.255 表示無法連線到 DHCP 伺服器，或正在到達。 Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。

</dd> <dt>

**DnsServer1**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (12) 
</dt> </dl>

要用於查詢 DNS 伺服器的第一個伺服器 IP 位址。 Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。

</dd> <dt>

**DnsServer2**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (13) 
</dt> </dl>

用來查詢 DNS 伺服器的第二個伺服器 IP 位址。 Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。

</dd> <dt>

**DnsServer3**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (14) 
</dt> </dl>

用來查詢 DNS 伺服器的第三個伺服器 IP 位址。 Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。

</dd> <dt>

**DnsServer4**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (15) 
</dt> </dl>

用來查詢 DNS 伺服器的第四個伺服器 IP 位址。 Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。

</dd> <dt>

**閘道**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (9) 
</dt> </dl>

電腦系統使用的預設閘道 IP 位址。 Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (2) 
</dt> </dl>

介面卡索引。 介面卡已停用並啟用，或在其他情況下，介面卡索引可能會變更，而且不應該被視為持續性。

</dd> <dt>

**IpAddress**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (6) 
</dt> </dl>

與網路介面卡相關聯的 IP 位址。 Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。

</dd> <dt>

**NICName**
</dt> <dd> <dl> <dt>

資料類型： **char16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (1) ， **最大** (256) 
</dt> </dl>

網路介面卡的名稱。

</dd> <dt>

**PhysicalAddr**
</dt> <dd> <dl> <dt>

資料類型： **char16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (4) ， **最大** (8) 
</dt> </dl>

介面卡的硬體位址。

</dd> <dt>

**PhysicalAddrLen**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (3) 
</dt> </dl>

介面卡的硬體位址長度。

</dd> <dt>

**PrimaryWinsServer**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (10) 
</dt> </dl>

主要 WINS 伺服器的 IP 位址。 Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。

</dd> <dt>

**SecondaryWinsServer**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (11) 
</dt> </dl>

次要 WINS 伺服器的 IP 位址。 Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。

</dd> <dt>

**大小**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (5) 
</dt> </dl>

資料屬性的大小（以位元組為單位）。

</dd> <dt>

**SubnetMask**
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (7) 
</dt> </dl>

與網路介面卡相關聯的子網路遮罩。 Sint32 的每個位元組都代表 IP 位址的四個部分中的其中一個)  (p1. p4。 低序位位元組包含 p1 的值，下一個位元組則包含 p2 的值，依此類推。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 




