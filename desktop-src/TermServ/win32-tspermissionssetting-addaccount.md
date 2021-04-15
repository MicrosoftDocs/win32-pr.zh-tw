---
title: 'Win32_TSPermissionsSetting 類別的 AddAccount 方法 (Faxcomex) '
description: AddAccount 方法會準備將帳戶新增至具有指定許可權集合的終端機。 您可以新增使用者、群組或電腦。
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- AddAccount 方法遠端桌面服務
- AddAccount 方法遠端桌面服務，Win32_TSPermissionsSetting 類別
- Win32_TSPermissionsSetting 類別遠端桌面服務，AddAccount 方法
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465961"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a>Win32 TSPermissionsSetting 類別的 AddAccount 方法 \_

**AddAccount** 方法會準備將帳戶新增至具有指定許可權集合的終端機。 您可以新增使用者、群組或電腦。

## <a name="syntax"></a>語法


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AccountName* \[在\]
</dt> <dd>

要新增至終端機的帳戶名稱。

</dd> <dt>

*PermissionPreSet* \[在\]
</dt> <dd>

要與指定的帳號相關聯的許可權集合。 這個參數可以是下列任何一個或所有的值。 如需詳細資訊，請參閱 [遠端桌面服務許可權](terminal-services-permissions.md)。

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION \_來賓 \_ 存取** (0) 


</dt> <dd>

帳戶具有登入許可權。

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION \_使用者 \_ 存取** (1) 


</dt> <dd>

帳戶具有下列許可權： Logon、Query Information、Send Message 和 Connect。

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION \_所有 \_ 存取** (2) 


</dt> <dd>

此帳戶具有所有的遠端桌面服務許可權。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| 標頭<br/>                   | <dl> <dt>Faxcomex。h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)
</dt> </dl>

 

