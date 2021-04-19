---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 SetUserGroupNames 方法
description: 將此遠端桌面連線授權原則的 UserGroupNames 屬性設定 (RD \ 160;端點) 。
ms.assetid: 03c9b2c5-8769-46f2-941f-302d798dd3a1
ms.tgt_platform: multiple
keywords:
- SetUserGroupNames 方法遠端桌面服務
- SetUserGroupNames 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，SetUserGroupNames 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ca948b63cd106e7284b00c2c5f9e54c6dfa86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966343"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a>Win32 TSGatewayConnectionAuthorizationPolicy 類別的 SetUserGroupNames 方法 \_

將此遠端桌面連線授權原則的 **UserGroupNames** 屬性設定 (RD CAP) 。

## <a name="syntax"></a>語法


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*UserGroupNames* \[在\]
</dt> <dd>

分號分隔的使用者組名清單。 名稱的格式為 *網域 \\ UserGroupName*。 如果使用者隸屬于這些使用者群組中的任何一項，則會允許使用者存取 RD 閘道 server。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則會傳回零。 如果方法失敗，則會傳回非零值。 如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。

## <a name="remarks"></a>備註

如果 *UserGroupNames* 參數中有多個使用者組名，而且其中一個名稱無法處理，則不會處理任何名稱。

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

 

