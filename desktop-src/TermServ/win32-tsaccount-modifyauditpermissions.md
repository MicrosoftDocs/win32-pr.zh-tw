---
title: Win32_TSAccount 類別的 ModifyAuditPermissions 方法
description: 準備為指定的帳號設定更細微的 audit 許可權集。
ms.assetid: 7df44a37-257d-49c6-8193-f1e1c5ebbb57
ms.tgt_platform: multiple
keywords:
- ModifyAuditPermissions 方法遠端桌面服務
- ModifyAuditPermissions 方法遠端桌面服務，Win32_TSAccount 類別
- Win32_TSAccount 類別遠端桌面服務，ModifyAuditPermissions 方法
topic_type:
- apiref
api_name:
- Win32_TSAccount.ModifyAuditPermissions
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f19337cc6110a15b206fc437fb6ec594ded60640
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844212"
---
# <a name="modifyauditpermissions-method-of-the-win32_tsaccount-class"></a>Win32 TSAccount 類別的 ModifyAuditPermissions 方法 \_

**ModifyAuditPermissions** 方法會準備為指定的帳號設定更細微的 audit 許可權集。

## <a name="syntax"></a>語法


```mof
uint32 ModifyAuditPermissions(
  [in] uint32  PermissionMask,
  [in] boolean Success
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PermissionMask* \[在\]
</dt> <dd>

要與指定的帳號相關聯的 [遠端桌面工作階段主機許可權](terminal-services-permissions.md) 集合。 此參數的值是點陣圖，而且可以選取下列任何或所有的值。

<dt>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>

<span id="WINSTATION_QUERY"></span><span id="winstation_query"></span>**WINSTATION \_查詢** (0) 


</dt> <dd>

查詢會話相關資訊的許可權。

</dd> <dt>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>

<span id="WINSTATION_SET"></span><span id="winstation_set"></span>**WINSTATION \_設定** (1) 


</dt> <dd>

修改連接參數的許可權。

</dd> <dt>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>

<span id="WINSTATION_RESET"></span><span id="winstation_reset"></span>**WINSTATION \_重設** (6) 


</dt> <dd>

重設或結束會話或連接的許可權。

</dd> <dt>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>

<span id="WINSTATION_VIRTUAL___STANDARD_RIGHTS_REQUIRED"></span><span id="winstation_virtual___standard_rights_required"></span>**WINSTATION \_\| \_ \_ 需要虛擬標準許可權** (3) 


</dt> <dd>

使用虛擬通道的許可權。 虛擬通道可讓您從伺服器程式存取用戶端裝置。

</dd> <dt>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>

<span id="WINSTATION_SHADOW"></span><span id="winstation_shadow"></span>**WINSTATION \_陰影** (4) 


</dt> <dd>

陰影或遠端控制另一個使用者會話的許可權。

</dd> <dt>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>

<span id="WINSTATION_LOGON"></span><span id="winstation_logon"></span>**WINSTATION \_登** 入 (5) 


</dt> <dd>

登入伺服器上會話的許可權。

</dd> <dt>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>

<span id="WINSTATION_LOGOFF"></span><span id="winstation_logoff"></span>**WINSTATION \_登出** (2) 


</dt> <dd>

從會話登出使用者的許可權。

</dd> <dt>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>

<span id="WINSTATION_MSG"></span><span id="winstation_msg"></span>**WINSTATION \_MSG** (7) 


</dt> <dd>

將訊息傳送至另一個使用者會話的許可權。

</dd> <dt>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>

<span id="WINSTATION_CONNECT"></span><span id="winstation_connect"></span>**WINSTATION \_連接** (8) 


</dt> <dd>

連接到另一個會話的許可權。

</dd> <dt>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>

<span id="WINSTATION_DISCONNECT"></span><span id="winstation_disconnect"></span>**WINSTATION \_中斷** (9) 的連線


</dt> <dd>

中斷會話連接的許可權。

</dd> </dl> </dd> <dt>

*成功* \[在\]
</dt> <dd>

指定是否允許或拒絕 *PermissionMask* 參數的值所指定的許可權集合。

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

允許指定的許可權集合。

</dd> <dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

已拒絕指定的許可權集合。

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
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TSAccount**](win32-tsaccount.md)
</dt> </dl>

 

