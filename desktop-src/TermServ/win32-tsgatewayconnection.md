---
title: Win32_TSGatewayConnection 類別
description: 代表從用戶端電腦到遠端桌面閘道 (RD 閘道) server 的連接。
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnection 類別遠端桌面服務
- Win32_TSGatewayConnection 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dbaa79213282a70b2f29e6bee9f94901700dddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105833"
---
# <a name="win32_tsgatewayconnection-class"></a>Win32 \_ TSGatewayConnection 類別

代表從用戶端電腦到遠端桌面閘道 (RD 閘道) server 的連接。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a>成員

**Win32 \_ TSGatewayConnection** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSGatewayConnection** 類別具有這些方法。



| 方法                                                                     | 描述                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**CheckStatus**](checkstatus-win32-tsgatewayconnection.md)               | 檢查 RD 閘道伺服器連接的狀態，以及是否已設定目標伺服器進行負載平衡。<br/> |
| [**中斷連線**](disconnect-win32-tsgatewayconnection.md)                 | 結束連接。<br/>                                                                                                  |
| [**DisconnectProtocol**](disconnectprotocol-win32-tsgatewayconnection.md) | 結束使用指定之通訊協定的所有連接。<br/>                                                                 |
| [**DisconnectUser**](disconnectuser-win32-tsgatewayconnection.md)         | 結束指定之使用者的所有連接。<br/>                                                                           |



 

### <a name="properties"></a>屬性

**Win32 \_ TSGatewayConnection** 類別具有這些屬性。

<dl> <dt>

**ChannelId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

通道識別碼。

</dd> <dt>

**ClientAddress**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用戶端 IP 位址。

</dd> <dt>

**ConnectedPort**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

連接的資源上使用者所連線的埠。

</dd> <dt>

**ConnectedResource**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用戶端所連線之電腦 (或叢集) 的名稱。

</dd> <dt>

**ConnectedTime**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立連接時的時間戳記。 當連接重設時，會重設此時間，即使它會自動重新連線。

</dd> <dt>

**ConnectionDuration**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自連線時間以來經過的時間。

</dd> <dt>

**ConnectionKey**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

格式為 "tunnelId： channelID" 的連接識別碼。

</dd> <dt>

**FullUserName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

已連線使用者的完整使用者名稱。

</dd> <dt>

**IdleTime**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

連接的閒置時間。

</dd> <dt>

**NumberOfKilobytesReceived**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD 閘道伺服器從用戶端電腦收到的 kb 數。

</dd> <dt>

**NumberOfKilobytesSent**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD 閘道伺服器傳送給用戶端電腦的 kb 數。

</dd> <dt>

**ProtocolName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來連接 RD 閘道伺服器的通訊協定。

<dt>

RDP
</dt> <dd>

RD 閘道伺服器的通訊協定。

</dd> </dl>

</dd> <dt>

**TransportProtocol**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定連接的傳輸類型。 這必須是下列值之一。

<dt>

0
</dt> <dd>

RPC over HTTP 傳輸。

</dd> <dt>

1
</dt> <dd>

HTTP 傳輸。

</dd> <dt>

2
</dt> <dd>

UDP 傳輸。

</dd> </dl>

</dd> <dt>

**TunnelId**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

通道識別碼。

</dd> <dt>

**使用者名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

連接到 RD 閘道伺服器的使用者名稱。

</dd> </dl>

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能使用這個類別。

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[**Win32 \_ TSGatewayServerSettings**](win32-tsgatewayserversettings.md)
</dt> </dl>

 

