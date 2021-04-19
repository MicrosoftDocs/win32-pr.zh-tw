---
title: Win32_TerminalServiceSetting 類別的 SetTimeZoneRedirection 方法
description: SetTimeZoneRedirection 方法會設定 TimeZoneRedirection 屬性，以允許用戶端電腦將時區設定重新導向遠端桌面服務會話。
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- SetTimeZoneRedirection 方法遠端桌面服務
- SetTimeZoneRedirection 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetTimeZoneRedirection 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968344"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a>Win32 TerminalServiceSetting 類別的 SetTimeZoneRedirection 方法 \_

**SetTimeZoneRedirection** 方法會設定 **TimeZoneRedirection** 屬性，以允許用戶端電腦將時區設定重新導向遠端桌面服務會話。

## <a name="syntax"></a>語法


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TimeZoneRedirection* \[在\]
</dt> <dd>

**TimeZoneRedirection** 屬性的新值。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

停用 **TimeZoneRedirection** 屬性。 不會發生時區重新導向。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

啟用 **TimeZoneRedirection** 屬性。 用戶端的時區會重新導向至會話的時區。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="remarks"></a>備註

根據預設，遠端桌面服務會話的時區與遠端桌面工作階段主機 (RD 工作階段主機) server 的時區相同。 用戶端電腦無法重新導向時區資訊。

如果已停用時區重新導向，則新的會話會繼承伺服器的時區。 當會話重新連線時，會話會保留其中斷連線之前的時區。

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

 

