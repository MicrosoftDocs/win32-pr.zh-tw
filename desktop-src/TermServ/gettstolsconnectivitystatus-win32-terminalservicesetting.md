---
title: Win32_TerminalServiceSetting 類別的 GetTStoLSConnectivityStatus 方法
description: 判斷遠端桌面服務與授權伺服器之間的連接狀態。
ms.assetid: 11fc5865-47e8-4be8-a526-53e29f72d0a4
ms.tgt_platform: multiple
keywords:
- GetTStoLSConnectivityStatus 方法遠端桌面服務
- GetTStoLSConnectivityStatus 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，GetTStoLSConnectivityStatus 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTStoLSConnectivityStatus
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff79de8bc1740e659b8f0398c0fa84958c1bfcffda505f1a26322da442dcc19b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059566"
---
# <a name="gettstolsconnectivitystatus-method-of-the-win32_terminalservicesetting-class"></a>Win32 TerminalServiceSetting 類別的 GetTStoLSConnectivityStatus 方法 \_

判斷遠端桌面服務與授權伺服器之間的連接狀態。

## <a name="syntax"></a>語法


```mof
uint32 GetTStoLSConnectivityStatus(
  [in]  string ServerName,
  [out] uint32 TStoLSConnectivityStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ServerName* \[在\]
</dt> <dd>

要檢查連接狀態的授權伺服器名稱。

</dd> <dt>

*TStoLSConnectivityStatus* \[擴展\]
</dt> <dd>

值，這個值表示授權伺服器的連接狀態。 這可以是下列其中一個值。

<dt>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>

<span id="LS_CONNECTABLE_UNKNOWN"></span><span id="ls_connectable_unknown"></span>**LS \_可 \_** 連接的未知 (0) 


</dt> <dd>

無法判斷連接狀態。

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2"></span><span id="ls_connectable_valid_ws08r2"></span>**LS \_可連接的 \_ 有效 \_ WS08R2** (1) 


</dt> <dd>

遠端桌面服務可以連接到 Windows Server 2008 R2 授權伺服器。

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>

<span id="LS_CONNECTABLE_VALID_WS08"></span><span id="ls_connectable_valid_ws08"></span>**LS \_可連接的 \_ 有效 \_ WS08** (2) 


</dt> <dd>

遠端桌面服務可以連接到 Windows Server 2008 授權伺服器。

</dd> <dt>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>

<span id="LS_CONNECTABLE_BETA_RTM_MISMATCH"></span><span id="ls_connectable_beta_rtm_mismatch"></span>**LS \_可連接的 \_ BETA \_ RTM \_ 不符** (3) 


</dt> <dd>

遠端桌面服務可以連線到授權伺服器，但其中一部伺服器正在執行 Beta 版作業系統。

</dd> <dt>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>

<span id="LS_CONNECTABLE_LOWER_VERSION"></span><span id="ls_connectable_lower_version"></span>**LS \_可連接的 \_ 較低 \_ 版本** (4) 


</dt> <dd>

遠端桌面服務可以連線到授權伺服器，但授權伺服器與遠端桌面服務主機伺服器之間有不相容的情況。

</dd> <dt>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>

<span id="LS_CONNECTABLE_NOT_IN_TSCGROUP"></span><span id="ls_connectable_not_in_tscgroup"></span>**LS \_可連接 \_ 不 \_ 在 \_ TSCGROUP** (5) 


</dt> <dd>

授權伺服器中已啟用安全性群組原則，但遠端桌面服務不是群組原則的一部分。

</dd> <dt>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>

<span id="LS_NOT_CONNECTABLE"></span><span id="ls_not_connectable"></span>**LS \_無法 \_** 連接 (6) 


</dt> <dd>

遠端桌面服務無法連接至授權伺服器。

</dd> <dt>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>

<span id="LS_CONNECTABLE_UNKNOWN_VALIDITY"></span><span id="ls_connectable_unknown_validity"></span>**LS \_可連接的 \_ 未知 \_ 有效** (7) 


</dt> <dd>

授權伺服器可以連接到，但無法判斷連接的有效性。

</dd> <dt>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>

<span id="LS_CONNECTABLE_BUT_ACCESS_DENIED"></span><span id="ls_connectable_but_access_denied"></span>**LS \_可 \_ 連接 \_ 但 \_ 拒絕存取** (8) 


</dt> <dd>

遠端桌面服務可以連接到授權伺服器，但使用者帳戶沒有授權伺服器的系統管理員許可權。

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>

<span id="LS_CONNECTABLE_VALID_WS08R2_VDI"></span><span id="ls_connectable_valid_ws08r2_vdi"></span>**LS \_可連接的 \_ 有效 \_ WS08R2 \_ VDI** (9) 


</dt> <dd>

遠端桌面服務可以連接到 Windows server 2008 R2 虛擬桌面基礎結構 (VDI) 伺服器。

**Windows Server 2008 R2：** Windows Server 2012 之前，不支援這個值。

</dd> <dt>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>

<span id="LS_CONNECTABLE_FEATURE_NOT_SUPPORTED"></span><span id="ls_connectable_feature_not_supported"></span>**LS \_\_ \_ 不 \_ 支援** 可連接功能 (10) 


</dt> <dd>

這項功能不受支援。

**Windows server 2008 r2 和 Windows server 2008 r2 SP1：** Windows Server 2012 之前，不支援這個值。

</dd> <dt>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>

<span id="LS_CONNECTABLE_VALID_LS"></span><span id="ls_connectable_valid_ls"></span>**LS \_可連接的 \_ 有效 \_ LS** (11) 


</dt> <dd>

授權伺服器有效。

**Windows server 2008 r2 和 Windows server 2008 r2 SP1：** Windows Server 2012 之前，不支援這個值。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                       |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





