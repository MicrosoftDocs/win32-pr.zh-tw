---
title: Win32_TSLogonSetting 類別的 ExplicitLogon 方法
description: ExplicitLogon 方法會設定要用於驗證的認證。
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- ExplicitLogon 方法遠端桌面服務
- ExplicitLogon 方法遠端桌面服務，Win32_TSLogonSetting 類別
- Win32_TSLogonSetting 類別遠端桌面服務，ExplicitLogon 方法
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef72b6b0f0ede0954a6fc74030a9f0f1d4976935
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384958"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a>Win32 TSLogonSetting 類別的 ExplicitLogon 方法 \_

**ExplicitLogon** 方法會設定要用於驗證的認證。

## <a name="syntax"></a>語法


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a>參數

<dl> <dt>

使用者 *名稱* \[在\]
</dt> <dd>

使用者名稱登入認證。

</dd> <dt>

*網域* \[在\]
</dt> <dd>

網域登入認證。

</dd> <dt>

*密碼* \[在\]
</dt> <dd>

密碼登入認證。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回成功，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

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

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> </dl>

 

