---
title: Win32_TerminalServiceSetting 類別的 ChangeMode 方法
description: ChangeMode 方法會設定目前遠端桌面工作階段主機 (RD 工作階段主機) server 的授權類型。
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- ChangeMode 方法遠端桌面服務
- ChangeMode 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，ChangeMode 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2812dd459e13922b1745e55355972092091b4fd9521bc41a46da40769c02021d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604037"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a>Win32 TerminalServiceSetting 類別的 ChangeMode 方法 \_

**ChangeMode** 方法會設定目前遠端桌面工作階段主機 (RD 工作階段主機) server 的授權類型。

## <a name="syntax"></a>語法


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*LicensingType* \[在\]
</dt> <dd>

要根據 RD 工作階段主機伺服器模式設定的授權類型。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

個人 RD 工作階段主機 server。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

用於系統管理的遠端桌面。

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**二級**


</dt> <dd>

每一裝置/每基座。 適用于應用程式伺服器。

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**億**


</dt> <dd>

每個使用者。 適用于應用程式伺服器。

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

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

