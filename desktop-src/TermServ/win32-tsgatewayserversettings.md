---
title: Win32_TSGatewayServerSettings 類別
description: 提供方法和屬性來查看和設定遠端桌面閘道 (RD 閘道) 伺服器設定。
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings 類別遠端桌面服務
- Win32_TSGatewayServerSettings 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00c199b4b8e98832dcc8dbe65b8fc2ef636df71c8bd6e3c096670e6333f83a75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008518"
---
# <a name="win32_tsgatewayserversettings-class"></a>Win32 \_ TSGatewayServerSettings 類別

提供方法和屬性來查看和設定遠端桌面閘道 (RD 閘道) 伺服器設定。 系統管理員可以使用這個類別來設定一組通訊協定、一組將寫入事件記錄檔的事件，以及透過 RD 閘道的最大連接數目。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a>成員

**Win32 \_ TSGatewayServerSettings** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSGatewayServerSettings** 類別具有這些方法。



| 方法                                                                                                                                             | 描述                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**設定**](configure-win32-tsgatewayserversettings.md)                                                                                       | 設定 RD 閘道服務所需的 IIS 和 RPC 設定。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                               |
| [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | 啟用或停用 **CentralCAPEnabled** 屬性，此屬性會控制是否使用中央遠端桌面連線授權原則 (RD CAP) 伺服器來控制這部伺服器的連線授權原則。<br/>                    |
| [**EnableLogEvent**](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | 啟用或停用指定事件種類的記錄。<br/>                                                                                                                                                                                              |
| [**EnableOnlyConsentCapableClients**](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | 設定 **OnlyConsentCapableClients** 屬性。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                                      |
| [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | 從 Windows Server 2016 開始，不支援這個方法。<br/> **Windows Server 2012 R2、Windows Server 2012、Windows Server 2008 R2 和 Windows Server 2008：** 啟用或停用健康狀態聲明 (SoH) 的要求。<br/> <br/> |
| [**EnableTransport**](enabletransport-win32-tsgatewayserversettings.md)                                                                           | 啟用或停用指定的傳輸。<br/> **Windows server 2008 R2 和 Windows server 2008：** 此方法在 Windows Server 2012 之前無法使用。<br/>                                                                                  |
| [**EnumAuthenticationPlugins**](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | 列舉所有已註冊的驗證外掛程式。<br/> **Windows Server 2008：** 無法使用這個方法。<br/>                                                                                                                                  |
| [**EnumAuthorizationPlugins**](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | 列舉所有已註冊的授權外掛程式。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                                     |
| [**GetIPAndPort**](getipandport-win32-tsgatewayserversettings.md)                                                                                 | 取得指定傳輸的接聽 IP 位址和埠號碼。<br/> **Windows server 2008 R2 和 Windows server 2008：** 此方法在 Windows Server 2012 之前無法使用。<br/>                                                 |
| [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | 傳回指定之記錄事件索引的記錄事件名稱。<br/>                                                                                                                                                                                         |
| [**GetProtocolName**](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | 傳回指定之通訊協定索引的通訊協定名稱。<br/>                                                                                                                                                                                           |
| [**IsLogEventEnabled**](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | 指出是否已啟用指定的事件記錄檔類型。<br/>                                                                                                                                                                                            |
| [**IsTransportEnabled**](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | 判斷指定的傳輸是否已啟用。<br/> **Windows server 2008 R2 和 Windows server 2008：** 此方法在 Windows Server 2012 之前無法使用。<br/>                                                                        |
| [**QueryCertCoNtext**](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | 指出是否已安裝指定的憑證。<br/>                                                                                                                                                                                             |
| [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | 回收 IIS 中的 RPC 應用程式集區。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                                            |
| [**RefreshCertCoNtext**](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | 重新整理 RD 閘道伺服器所使用的憑證。<br/>                                                                                                                                                                                      |
| [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | 設定 RD 閘道伺服器的目前驗證外掛程式。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                    |
| [**SetAuthenticationPluginAndRecycleRpcApplicationPools**](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | 設定 RD 閘道伺服器的目前驗證外掛程式，並在 IIS 中回收 RPC 應用程式集區。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                      |
| [**SetAuthorizationPlugin**](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | 設定 RD 閘道伺服器目前的授權外掛程式。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                     |
| [**SetCertificate**](setcertificate-win32-tsgatewayserversettings.md)                                                                             | 在 IIS 中設定埠443的 HTTPS 系結憑證雜湊。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                       |
| [**SetCertificateACL**](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | 設定此伺服器 (Acl) 的憑證存取控制清單。<br/>                                                                                                                                                                                     |
| [**SetDefaultPluginsAndRecycleRpcApplicationPools**](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | 設定 RD 閘道伺服器目前的驗證和授權外掛程式，並在 IIS 中回收 RPC 應用程式集區。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                   |
| [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | 設定 **EnforceChannelBinding** 屬性。<br/> **Windows server 2008 R2 和 Windows server 2008：** 此方法在 Windows Server 2012 之前無法使用。<br/>                                                                                  |
| [**SetIPAndPort**](setipandport-win32-tsgatewayserversettings.md)                                                                                 | 設定指定傳輸的接聽 IP 位址和埠號碼。<br/> **Windows server 2008 R2 和 Windows server 2008：** 此方法在 Windows Server 2012 之前無法使用。<br/>                                                    |
| [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | 設定允許的最大連接數 RD 閘道。 這個方法會變更 **MaxConnections** 和 **UnlimitedConnections** 屬性。<br/>                                                                                                |
| [**SetSslBridging**](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | 設定 RD 閘道伺服器所使用的 SSL 橋接類型。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                    |
| [**TSGRemoveAdminMsg**](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | 移除閘道伺服器的系統管理訊息。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                            |
| [**TSGRemoveConsentMsg**](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | 移除閘道伺服器的系統管理訊息。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                            |
| [**TSGStoreAdminMsg**](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | 更新閘道伺服器的系統管理訊息。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                            |
| [**TSGStoreConsentMsg**](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | 更新閘道伺服器的同意訊息。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                                                                                   |



 

### <a name="properties"></a>屬性

**Win32 \_ TSGatewayServerSettings** 類別具有這些屬性。

<dl> <dt>

**adminMessageEndTime**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統管理訊息的結束時間。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**adminMessageStartTime**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

管理訊息開始時間。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**adminMessageText**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

系統管理郵件內文。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**AuthenticationPluginCLSID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前驗證外掛程式的 CLSID。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**AuthenticationPluginDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前驗證外掛程式的描述。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**AuthenticationPluginName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前驗證外掛程式的名稱。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**AuthorizationPluginCLSID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前授權外掛程式的 CLSID。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**AuthorizationPluginDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前授權外掛程式的描述。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**AuthorizationPluginName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前授權外掛程式的名稱。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**CentralCAPEnabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否使用中央 RD CAP 伺服器來控制這部伺服器。 您可以藉由呼叫 [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) 方法來變更這個屬性。

</dd> <dt>

**CertHash**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在 IIS 中為埠443上的 HTTPS 系結指定憑證雜湊。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**consentMessageText**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

同意郵件內文。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**EnforceChannelBinding**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否針對 HTTP 傳輸強制執行通道系結。 您可以使用 [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) 方法來變更這個屬性值。

**Windows server 2008 R2 和 Windows server 2008：** 在 Windows Server 2012 之前，無法使用此屬性。

</dd> <dt>

**IsConfigured**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否設定 RD 閘道服務所需的 IIS 和 RPC 設定。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**MaxConnections**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

傳回透過 RD 閘道允許的最大連接數目。 您可以使用 [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) 方法來設定這個屬性。

</dd> <dt>

**MaximumAllowedConnectionsBySku**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

庫存單位 (SKU) 允許的最大連接數目。

</dd> <dt>

**MaxLogEvents**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

傳回記錄事件的最大數目。

</dd> <dt>

**MaxProtocols**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD 閘道支援的通訊協定數目。

</dd> <dt>

**OnlyConsentCapableClients**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否只允許用戶端能夠同意訊息連接到 RD 閘道。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

<dt>

零
</dt> <dd>

只有同意訊息可供用戶端連接。

</dd> <dt>

零
</dt> <dd>

未同意訊息的用戶端也可以連接。

</dd> </dl>

</dd> <dt>

**RequestSOH**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

從 Windows Server 2016 開始，不支援這個屬性。

* * Windows Server 2012 R2、Windows Server 2012、Windows Server 2008 R2 和 Windows Server 2008： * *

指定伺服器是否必須要求來自用戶端的健全狀況聲明 (SoH) 。 您可以使用 [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) 方法來變更這個屬性。

</dd> <dt>

**SkuName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

SKU 的名稱。

</dd> <dt>

**SslBridging**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定 RD 閘道伺服器所使用的 SSL 橋接類型。 這可以是下列其中一個值。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

<dt>

0
</dt> <dd>

無 SSL 橋接。

</dd> <dt>

1
</dt> <dd>

HTTPS 至 HTTP 橋接。

</dd> <dt>

2
</dt> <dd>

HTTPS 至 HTTPS 橋接。

</dd> </dl>

</dd> <dt>

**UnlimitedConnections**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否允許透過 RD 閘道的連接數目不限。 您可以使用 [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) 方法來設定這個屬性。

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

[**Win32 \_ TSGatewayConnection**](win32-tsgatewayconnection.md)
</dt> <dt>

[**Win32 \_ TSGatewayConnectionAuthorizationPolicy**](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayLoadBalancer**](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[**Win32 \_ TSGatewayRADIUSServer**](win32-tsgatewayradiusserver.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceAuthorizationPolicy**](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[**Win32 \_ TSGatewayResourceGroup**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

