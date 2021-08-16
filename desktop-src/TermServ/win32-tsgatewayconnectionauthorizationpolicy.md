---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別
description: 描述 (RD \ 160; 的遠端桌面連線授權原則。端點) 。 RD \ 160;CAPs 可用來判斷是否允許使用者連接到遠端桌面閘道 (RD 閘道) server。
ms.assetid: 50ff3f97-0818-4e9c-9db7-a822cfed0e82
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy
- Win32_TSGatewayConnectionAuthorizationPolicy.Name
- Win32_TSGatewayConnectionAuthorizationPolicy.Order
- Win32_TSGatewayConnectionAuthorizationPolicy.SmartcardAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.PasswordAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.SecureIdAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.CookieAuthenticationAllowed
- Win32_TSGatewayConnectionAuthorizationPolicy.Enabled
- Win32_TSGatewayConnectionAuthorizationPolicy.IdleTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeout
- Win32_TSGatewayConnectionAuthorizationPolicy.SessionTimeoutAction
- Win32_TSGatewayConnectionAuthorizationPolicy.DeviceRedirectionType
- Win32_TSGatewayConnectionAuthorizationPolicy.DiskDrivesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PrintersDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.SerialPortsDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.ClipboardDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.PlugAndPlayDevicesDisabled
- Win32_TSGatewayConnectionAuthorizationPolicy.UserGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.ComputerGroupNames
- Win32_TSGatewayConnectionAuthorizationPolicy.HasNapAttributes
- Win32_TSGatewayConnectionAuthorizationPolicy.AllowOnlySDRServers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfaefb0a3062db27622afe90023928507c6d127c64edb60041347f73c1b261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349243"
---
# <a name="win32_tsgatewayconnectionauthorizationpolicy-class"></a>Win32 \_ TSGatewayConnectionAuthorizationPolicy 類別

描述 (RD CAP) 的遠端桌面連線授權原則。 RD Cap 用來判斷是否允許使用者連線至遠端桌面閘道 (RD 閘道) server。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnectionAuthorizationPolicy
{
  string  Name;
  uint32  Order;
  boolean SmartcardAllowed;
  boolean PasswordAllowed;
  boolean SecureIdAllowed;
  boolean CookieAuthenticationAllowed;
  boolean Enabled;
  uint32  IdleTimeout;
  uint32  SessionTimeout;
  uint32  SessionTimeoutAction;
  uint32  DeviceRedirectionType;
  boolean DiskDrivesDisabled;
  boolean PrintersDisabled;
  boolean SerialPortsDisabled;
  boolean ClipboardDisabled;
  boolean PlugAndPlayDevicesDisabled;
  string  UserGroupNames;
  string  ComputerGroupNames;
  boolean HasNapAttributes;
  boolean AllowOnlySDRServers;
};
```

## <a name="members"></a>成員

**Win32 \_ TSGatewayConnectionAuthorizationPolicy** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ TSGatewayConnectionAuthorizationPolicy** 類別具有這些方法。



| 方法                                                                                                                | 描述                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddComputerGroupNames**](addcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | 將指定的電腦群組名加入至 **ComputerGroupNames** 屬性。<br/>                                                                                      |
| [**AddUserGroupNames**](addusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | 將指定的使用者組名加入至 **UserGroupNames** 屬性。<br/>                                                                                              |
| [**建立**](create-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | 建立 RD CAP。<br/>                                                                                                                                                   |
| [**刪除**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | 刪除目前的 RD CAP。<br/>                                                                                                                                          |
| [**DisableClipboard**](disableclipboard-win32-tsgatewayconnectionauthorizationpolicy.md)                             | 設定 **ClipboardDisabled** 屬性。<br/>                                                                                                                             |
| [**DisableDiskDrives**](disablediskdrives-win32-tsgatewayconnectionauthorizationpolicy.md)                           | 設定 **DiskDrivesDisabled** 屬性。<br/>                                                                                                                            |
| [**DisablePlugAndPlayDevices**](disableplugandplaydevices-win32-tsgatewayconnectionauthorizationpolicy.md)           | 設定 **PlugAndPlayDevicesDisabled** 屬性。<br/>                                                                                                                    |
| [**DisablePrinters**](disableprinters-win32-tsgatewayconnectionauthorizationpolicy.md)                               | 設定 **PrintersDisabled** 屬性。<br/>                                                                                                                              |
| [**DisableSerialPorts**](disableserialports-win32-tsgatewayconnectionauthorizationpolicy.md)                         | 設定 **SerialPortsDisabled** 屬性。<br/>                                                                                                                           |
| [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md)           | 用來切換 **AllowOnlySDRServers** 屬性<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                  |
| [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)                                             | 將目前 RD CAP 在清單中向下移動一個位置。<br/>                                                                                                              |
| [**上移**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | 將目前 RD CAP 在清單中向上移動一個位置。<br/>                                                                                                                |
| [**RemoveComputerGroupNames**](removecomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)             | 從 **ComputerGroupNames** 屬性中移除指定的電腦群組名。<br/>                                                                                 |
| [**RemoveUserGroupNames**](removeusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                     | 從 **UserGroupNames** 屬性中移除指定的使用者組名。<br/>                                                                                             |
| [**SetComputerGroupNames**](setcomputergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                   | 設定 **ComputerGroupNames** 屬性。<br/>                                                                                                                            |
| [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) | 設定 **CookieAuthenticationAllowed** 屬性。<br/> **Windows Server 2008：** 無法使用這個方法。<br/>                                                 |
| [**SetDeviceRedirectionType**](setdeviceredirectiontype-win32-tsgatewayconnectionauthorizationpolicy.md)             | 設定 **DeviceRedirectionType** 屬性。<br/>                                                                                                                         |
| [**SetEnabled**](setenabled-win32-tsgatewayconnectionauthorizationpolicy.md)                                         | 啟用或停用目前的 RD CAP。<br/>                                                                                                                              |
| [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                                 | 設定 **IdleTimeout** 屬性。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/>                                   |
| [**SetName**](setname-win32-tsgatewayconnectionauthorizationpolicy.md)                                               | 為此 RD CAP 設定新的名稱。 這個方法會確保名稱是唯一的。<br/>                                                                                      |
| [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | 設定 **PasswordAllowed** 屬性。<br/>                                                                                                                               |
| [**SetSecureIdAllowed**](setsecureidallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                         | 設定 **SecureIdAllowed** 屬性。<br/> **Windows Server 2008：** 這個方法會保留供日後使用。<br/>                                                   |
| [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md)                           | 設定 **SessionTimeout** 和 **SessionTimeoutAction** 屬性。<br/> **Windows Server 2008：** Windows Server 2008 R2 之前無法使用這個方法。<br/> |
| [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md)                       | 設定 **SmartcardAllowed** 屬性。<br/>                                                                                                                              |
| [**SetUserGroupNames**](setusergroupnames-win32-tsgatewayconnectionauthorizationpolicy.md)                           | 設定 **UserGroupNames** 屬性。<br/>                                                                                                                                |
| [**更新**](update-win32-tsgatewayconnectionauthorizationpolicy.md)                                                 | 更新目前的 RD CAP。<br/>                                                                                                                                          |



 

### <a name="properties"></a>屬性

**Win32 \_ TSGatewayConnectionAuthorizationPolicy** 類別具有這些屬性。

<dl> <dt>

**AllowOnlySDRServers**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出連接是否只允許安全的裝置重新導向 (SDR) RDS 伺服器。 您可以使用 [**EnableAllowOnlySDRServers**](win32-tsgatewayconnectionauthorizationpolicy-enableallowonlysdrservers.md) 方法來設定這個屬性。

**Windows Server 2008：** Windows Server 2008 R2 之前，無法使用此屬性。

</dd> <dt>

**ClipboardDisabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否將停用剪貼簿重新導向。 只有當 **DeviceRedirectionType** 屬性的值為 "2" 時，這個屬性才會有作用。

</dd> <dt>

**ComputerGroupNames**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

分號分隔的電腦群組名清單。 這個值可以是空的。 名稱的格式為 *網域 \\ ComputerGroupName*。 如果指定了值，用戶端電腦必須屬於其中一個電腦群組，使用者才能存取 RD 閘道 server。

</dd> <dt>

**CookieAuthenticationAllowed**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否可以使用 cookie 驗證連接到 RD 閘道伺服器。 您可以使用 [**SetCookieAuthenticationAllowed**](setcookieauthenticationallowed-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來設定這個屬性。

**Windows Server 2008：** 無法使用這個屬性。

</dd> <dt>

**DeviceRedirectionType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定將會重新導向的裝置。

<dt>

0
</dt> <dd>

將會重新導向所有裝置。

</dd> <dt>

1
</dt> <dd>

將不會重新導向任何裝置。

</dd> <dt>

2
</dt> <dd>

將不會重新導向指定的裝置。 **DiskDrivesDisabled**、 **PrintersDisabled**、 **SerialPortsDisabled**、 **ClipboardDisabled** 和 **PlugAndPlayDevicesDisabled** 屬性控制哪些裝置將不會被重新導向。

</dd> </dl>

</dd> <dt>

**DiskDrivesDisabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否將停用磁片磁碟機重新導向。 只有當 **DeviceRedirectionType** 屬性的值為 "2" 時，這個屬性才會有作用。

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出此 RD CAP 是否將用來評估使用者的授權。

</dd> <dt>

**HasNapAttributes**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出 RD CAP 是否 (NAP) 屬性使用網路存取保護。

</dd> <dt>

**IdleTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

閒置的超時值（以分鐘為單位）。 值為0表示沒有任何超時時間。 您可以使用 [**SetIdleTimeout**](setidletimeout-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來設定這個屬性。

**Windows Server 2008：** 無法使用這個屬性。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

RD CAP 的名稱。

</dd> <dt>

**順序**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD CAP 的評估順序。 第一個評估 RD CAP 的值為 "1"。 呼叫 [**Create**](create-win32-tsgatewayconnectionauthorizationpolicy.md)、 [**Delete**](delete-win32-tsgatewayconnectionauthorizationpolicy.md)、[**上移**](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)或 [**MoveDown**](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)方法時，可以變更 **Order** 屬性。

</dd> <dt>

**PasswordAllowed**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否可以使用密碼連接到 RD 閘道伺服器。 您可以使用 [**SetPasswordAllowed**](setpasswordallowed-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來變更這個屬性。

</dd> <dt>

**PlugAndPlayDevicesDisabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否將停用隨插即用裝置的重新導向。 只有當 **DeviceRedirectionType** 屬性的值為 "2" 時，這個屬性才會有作用。

</dd> <dt>

**PrintersDisabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否將停用印表機重新導向。 只有當 **DeviceRedirectionType** 屬性的值為 "2" 時，這個屬性才會有作用。

</dd> <dt>

**SecureIdAllowed**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否可以使用安全識別碼來連接 RD 閘道伺服器。

**Windows Server 2008：** 未使用此屬性。

</dd> <dt>

**SerialPortsDisabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否將停用序列埠重新導向。 只有當 **DeviceRedirectionType** 屬性的值為 "2" 時，這個屬性才會有作用。

</dd> <dt>

**SessionTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

會話超時值（以分鐘為單位）。 值為0表示沒有任何超時時間。 您可以使用 [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來設定這個屬性。

**Windows Server 2008：** 無法使用這個屬性。

</dd> <dt>

**SessionTimeoutAction**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定會話超時時要採取的動作。 您可以使用 [**SetSessionTimeout**](setsessiontimeout-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來設定這個屬性。

這可以是下列其中一個值。

**Windows Server 2008：** 無法使用這個屬性。

<dt>

0
</dt> <dd>

中斷會話的連線。

</dd> <dt>

1
</dt> <dd>

嘗試重新授權會話。

</dd> </dl>

</dd> <dt>

**SmartcardAllowed**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出是否可以使用智慧卡來連接 RD 閘道伺服器。 您可以使用 [**SetSmartcardAllowed**](setsmartcardallowed-win32-tsgatewayconnectionauthorizationpolicy.md) 方法來變更這個屬性。

</dd> <dt>

**UserGroupNames**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

分號分隔的使用者組名清單。 名稱的格式為 *網域 \\ UserGroupName*。 如果使用者隸屬于這些使用者群組中的任何一項，則會允許使用者存取 RD 閘道 server。

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

 

