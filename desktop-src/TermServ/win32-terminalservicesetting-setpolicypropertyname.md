---
title: Win32_TerminalServiceSetting 類別的 SetPolicyPropertyName 方法
description: SetPolicyPropertyName 方法會設定類別的 DeleteTempFolders、UseTempFolders 或 Help 屬性。
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- SetPolicyPropertyName 方法遠端桌面服務
- SetPolicyPropertyName 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetPolicyPropertyName 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a9009a05cb1c8de210c3e274af0e8c21297e9e01ed28dbc0c01d38edc06fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769978"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a>Win32 TerminalServiceSetting 類別的 SetPolicyPropertyName 方法 \_

**SetPolicyPropertyName** 方法會設定類別的 **DeleteTempFolders**、 **UseTempFolders** 或 **Help** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PropertyName* \[在\]
</dt> <dd>

指定方法設定的原則屬性。

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**


</dt> <dd>

方法正在設定 **DeleteTempFolders** 屬性。

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**


</dt> <dd>

方法正在設定 **UseTempFolders** 屬性。

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>**説明**


</dt> <dd>

方法正在設定 **Help** 屬性。

**注意：**  **不支援** 說明

</dd> </dl> </dd> <dt>

*值* \[在\]
</dt> <dd>

值，指出是否要啟用或停用 *PropertyName* 參數所指定的屬性。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

停用屬性。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

啟用屬性。

</dd> </dl> </dd> </dl>

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

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

