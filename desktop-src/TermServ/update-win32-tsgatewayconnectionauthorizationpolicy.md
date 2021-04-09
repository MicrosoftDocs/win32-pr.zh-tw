---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 Update 方法
description: 更新目前的遠端桌面連線授權原則 (RD \ 160;端點) 。
ms.assetid: 6d13d1b7-1c7d-4d22-b42c-36e0f4446e86
ms.tgt_platform: multiple
keywords:
- Update 方法遠端桌面服務
- Update 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，Update 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b982030170e954342dc5ff99754dcb89afd0e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025170"
---
# <a name="update-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Win32 TSGatewayConnectionAuthorizationPolicy 類別的 Update 方法 \_

 (RD CAP) 更新目前的遠端桌面連線授權原則。

## <a name="syntax"></a>語法


```mof
uint32 Update(
  [in] string  Name,
  [in] string  UserGroupNames,
  [in] string  ComputerGroupNames,
  [in] boolean SmartCard,
  [in] boolean Password,
  [in] boolean SecureId,
  [in] boolean Enabled,
  [in] uint32  DeviceRedirectionType,
  [in] boolean DiskDrivesDisabled,
  [in] boolean PrintersDisabled,
  [in] boolean SerialPortsDisabled,
  [in] boolean ClipboardDisabled,
  [in] boolean PlugAndPlayDevicesDisabled,
  [in] uint32  IdleTimeout,
  [in] uint32  SessionTimeout,
  [in] uint32  SessionTimeoutAction,
  [in] boolean AllowOnlySDRServers,
  [in] boolean CookieAuthentication
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

RD CAP 的名稱。 名稱必須為64個字元或更少，) 會忽略唯一的 (大小寫，且不能包含下列保留字元：

<> ：;" / \\ \| ? \*\[TAB\]

</dd> <dt>

*UserGroupNames* \[在\]
</dt> <dd>

分號分隔的使用者組名清單。 名稱的格式為 *網域 \\ UserGroupName*。 如果使用者屬於這些使用者群組的任何一個，則會允許使用者存取 RD 閘道 server。

</dd> <dt>

*ComputerGroupNames* \[在\]
</dt> <dd>

分號分隔的電腦群組名清單。 這個值可以是空的。 名稱的格式為 *網域 \\ ComputerGroupName*。 如果指定了值，用戶端電腦必須屬於其中一個電腦群組，使用者才能存取 RD 閘道 server。

</dd> <dt>

*智慧卡* \[在\]
</dt> <dd>

指定是否可以使用智慧卡向 RD 閘道伺服器進行驗證。

</dd> <dt>

*密碼* \[在\]
</dt> <dd>

指定是否可以使用密碼向 RD 閘道伺服器進行驗證。

</dd> <dt>

*SecureId* \[在\]
</dt> <dd>

這個參數保留給未來使用。

</dd> <dt>

*已啟用* \[在\]
</dt> <dd>

指定是否啟用此 RD CAP。

</dd> <dt>

*DeviceRedirectionType* \[在\]
</dt> <dd>

指定將會重新導向的裝置類型。

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

將不會重新導向指定的裝置。 *DiskDrivesDisabled*、 *PrintersDisabled*、 *SerialPortsDisabled*、 *ClipboardDisabled* 和 *PlugAndPlayDevicesDisabled* 參數控制哪些裝置將不會被重新導向。

</dd> </dl> </dd> <dt>

*DiskDrivesDisabled* \[在\]
</dt> <dd>

指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用磁片磁碟機重新導向。

</dd> <dt>

*PrintersDisabled* \[在\]
</dt> <dd>

指定是否要在 *DeviceRedirectionType* 參數為 "2" 時，停用印表機重新導向。

</dd> <dt>

*SerialPortsDisabled* \[在\]
</dt> <dd>

指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用序列埠重新導向。

</dd> <dt>

*ClipboardDisabled* \[在\]
</dt> <dd>

指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用剪貼簿重新導向。

</dd> <dt>

*PlugAndPlayDevicesDisabled* \[在\]
</dt> <dd>

指定 *DeviceRedirectionType* 參數為 "2" 時，是否要停用隨插即用裝置的重新導向。

</dd> <dt>

*IdleTimeout* \[在\]
</dt> <dd>

閒置超時值（分鐘）

</dd> <dt>

*SessionTimeout* \[在\]
</dt> <dd>

會話超時值（分鐘）

</dd> <dt>

*SessionTimeoutAction* \[在\]
</dt> <dd>

會話超時動作（分鐘）

</dd> <dt>

*AllowOnlySDRServers* \[在\]
</dt> <dd>

連接是否只允許連線到 SDR TS 伺服器

</dd> <dt>

*CookieAuthentication* \[在\]
</dt> <dd>

指出是否可以使用 cookie 驗證來連線到 TS 閘道伺服器

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

您必須是 Administrators 群組的成員，才能呼叫這個方法。

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
</dt> </dl>

 

