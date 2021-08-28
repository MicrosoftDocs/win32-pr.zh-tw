---
title: Win32_TSLogonSetting 類別的 SetPromptForPassword 方法
description: SetPromptForPassword 方法會設定 PromptForPassword 屬性。
ms.assetid: eeeed374-4a8a-4014-833c-d931be3ef455
ms.tgt_platform: multiple
keywords:
- SetPromptForPassword 方法遠端桌面服務
- SetPromptForPassword 方法遠端桌面服務，Win32_TSLogonSetting 類別
- Win32_TSLogonSetting 類別遠端桌面服務，SetPromptForPassword 方法
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.SetPromptForPassword
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90ea5202b0cfdfb624a05240deb042a88a8c73c8ea994cd810e1d9680ac0ddc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769518"
---
# <a name="setpromptforpassword-method-of-the-win32_tslogonsetting-class"></a>Win32 TSLogonSetting 類別的 SetPromptForPassword 方法 \_

**SetPromptForPassword** 方法會設定 **PromptForPassword** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 SetPromptForPassword(
  [in] uint32 PromptForPassword
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PromptForPassword* \[在\]
</dt> <dd>

旗標停用或啟用 **PromptForPassword** 屬性。

<dt>

0
</dt> <dd>

停用密碼提示。

</dd> <dt>

1
</dt> <dd>

啟用密碼提示。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回成功，否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

<dl> <dt>

**FALSE** (0) 
</dt> <dt>

**TRUE** (1) 
</dt> </dl>

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

 

