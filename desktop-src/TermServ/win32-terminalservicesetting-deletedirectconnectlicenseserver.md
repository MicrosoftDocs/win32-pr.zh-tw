---
title: Win32_TerminalServiceSetting 類別的 DeleteDirectConnectLicenseServer 方法
description: DeleteDirectConnectLicenseServer 已無法再使用。
ms.assetid: 190316ab-b8ed-4102-8346-42603d6451e6
ms.tgt_platform: multiple
keywords:
- DeleteDirectConnectLicenseServer 方法遠端桌面服務
- DeleteDirectConnectLicenseServer 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，DeleteDirectConnectLicenseServer 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.DeleteDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1929ee4294040e80ec9bb633bd70d4709b3e56b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968378"
---
# <a name="deletedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Win32 TerminalServiceSetting 類別的 DeleteDirectConnectLicenseServer 方法 \_

\[**DeleteDirectConnectLicenseServer** 不再適用于 Windows Server 2008 R2。\]

**Windows Server 2008：** 從登錄中移除授權伺服器。

## <a name="syntax"></a>語法


```mof
uint32 DeleteDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*LicenseServerName* \[在\]
</dt> <dd>

要移除之授權伺服器的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 用戶端支援結束<br/>    | 都不支援<br/>                                                               |
| 伺服器支援結束<br/>    | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

