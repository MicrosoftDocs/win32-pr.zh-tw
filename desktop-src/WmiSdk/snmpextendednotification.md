---
description: SnmpExtendedNotification 類別是 SNMP 提供者從通知類型宏對應到 CIM 類別之任何類別的基類。
ms.assetid: 207966c1-14cf-4a47-8176-0f58838cfa1e
ms.tgt_platform: multiple
title: SnmpExtendedNotification 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SnmpExtendedNotification
- SnmpExtendedNotification.SECURITY_DESCRIPTOR
- SnmpExtendedNotification.TIME_CREATED
- SnmpExtendedNotification.AgentAddress
- SnmpExtendedNotification.AgentTransport
- SnmpExtendedNotification.AgentTransportAddress
- SnmpExtendedNotification.Community
- SnmpExtendedNotification.Identification
- SnmpExtendedNotification.TimeStamp
- SnmpExtendedNotification.AgentTransportProtocol
api_type:
- Schema
api_location:
- Root\snmp\SMIR
ms.openlocfilehash: e21fcc32976c42f41cd33a519e5fa6c684acdfc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981490"
---
# <a name="snmpextendednotification-class"></a>SnmpExtendedNotification 類別

**SnmpExtendedNotification** 類別是 [SNMP 提供者](snmp-provider.md)從 [通知類型](notification-type-macro.md)宏對應到 CIM 類別之任何類別的基類。

> [!Note]  
> 如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class SnmpExtendedNotification : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  string AgentAddress;
  string AgentTransport;
  string AgentTransportAddress;
  string Community;
  string Identification;
  string TimeStamp;
  string AgentTransportProtocol;
};
```

## <a name="members"></a>成員

**SnmpExtendedNotification** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SnmpExtendedNotification** 類別具有這些屬性。

<dl> <dt>

**AgentAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立通知之實體的網路位址。 這是裝置的實際位址。 當管理實體使用 SNMP over UDP 時，傳輸位址會參考 IP 位址。 當管理實體使用 SNMP over IPX 時，傳輸位址會設定為 **Null**。 這個屬性僅適用于 SNMPv1。

</dd> <dt>

**AgentTransport**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

傳送實體所使用的傳輸通訊協定。 這個屬性對 SNMPv1 和 SNMPv2C 有效。

</dd> <dt>

**AgentTransportAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

傳送通知之實體的網路位址。 這是轉送通知的最後一個實體的位址。 當管理實體使用 SNMP over UDP 時，傳輸位址會參考 IP 位址。 當管理實體將 SNMP 用於 IPX 時，傳輸位址會參考 IPX 位址。 這個屬性對 SNMPv1 和 SNMPv2C 有效。

</dd> <dt>

**AgentTransportProtocol**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

傳送實體所使用的傳輸通訊協定。

</dd> <dt>

**社群**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與 PDU 實例相關聯的群體名稱。 群體名稱會驗證 PDU 的建立者。 這個屬性對 SNMPv1 和 SNMPv2C 都有效。

</dd> <dt>

**識別**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **文字 \_ 慣例** ( "OBJECTIDENTIFIER" ) ， **編碼** ( "OBJECTIDENTIFIER" ) ， **物件 \_ 語法** ( "OBJECTIDENTIFIER" ) ， **物件 \_ 識別碼** ( "1.3.6.1.6.3.1.1.4.1" ) 
</dt> </dl>

此通知的授權識別。 直接對應到 MIB 專案 SnmpTrapOID 變數系結。 這個屬性僅適用于 SNMPv2C。

</dd> <dt>

**安全 \_ 描述項**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

事件提供者用來判斷哪些使用者可以接收事件的描述項。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。 如需有關用來設定此安全描述項之常數的詳細資訊，請參閱 [WMI 安全性常數](wmi-security-constants.md)。

</dd> <dt>

**\_建立時間**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

唯一值，指出產生事件的時間。 這是64位值，代表1601年1月1日之後的 100-毫微秒間隔數目。 此資訊採用國際標準時間 (UTC) 格式。 這個屬性繼承自 [**\_ \_ 事件**](--event.md)。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

</dd> <dt>

**時間 戳**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **文字 \_ 慣例** ( "TimeTicks" ) ， **編碼** ( "TimeTicks" ) ， **物件 \_ 語法** ( "TimeTicks" ) ， **物件 \_ 識別碼** ( "1.3.6.1.2.1.1.3" ) 
</dt> </dl>

上次重新初始化代理程式的網路管理部分之後的時間（百分之一秒）。 這會對應到 MIB 變數 sysUptime 0，其類型為 **INTEGER32**。 這個屬性會對應至屬於 **uint32** 類型的 CIM 類別屬性 **時間戳記**。 這個屬性僅適用于 SNMPv2C。

</dd> </dl>

## <a name="remarks"></a>備註

包含名為 **TimeStamp** 或 **識別** 之 [物件類型](object-type-macro.md)宏參考的 [通知類型](notification-type-macro.md)宏會導致對應衝突。 如果發生這種衝突，就會優先使用必要的屬性，而且必須重新命名衝突的參考。

包含名為「**社區**」之 [物件類型](object-type-macro.md)宏參考的 [通知類型](notification-type-macro.md)宏會導致對應衝突。 如果發生這種衝突，就會優先使用必要的屬性，而且必須重新命名衝突的參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ snmp \\ SMIR<br/>                                                             |
| MOF<br/>                      | <dl> <dt>SnmpSmiR mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_ExtrinsicEvent**](--extrinsicevent.md)
</dt> <dt>

[通知類型宏](notification-type-macro.md)
</dt> </dl>

 

