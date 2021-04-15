---
title: Win32_TerminalServiceSetting 類別的 SetDisableForcibleLogoff 方法
description: 不支援這個方法。
ms.assetid: 1b7ac0f2-c242-4ca8-bc4d-8111e63851eb
ms.tgt_platform: multiple
keywords:
- SetDisableForcibleLogoff 方法遠端桌面服務
- SetDisableForcibleLogoff 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetDisableForcibleLogoff 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetDisableForcibleLogoff
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4ae62db188d0e3aa31ffd8e3993e793e9bb2bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465100"
---
# <a name="setdisableforciblelogoff-method-of-the-win32_terminalservicesetting-class"></a>Win32 TerminalServiceSetting 類別的 SetDisableForcibleLogoff 方法 \_

不支援這個方法。

**Windows Vista 和 Windows Server 2008：** 啟用或停用登入主控台的系統管理員是否可以強制登出。

## <a name="syntax"></a>語法


```mof
uint32 SetDisableForcibleLogoff(
  [in] uint32 DisableForcibleLogoff
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DisableForcibleLogoff* \[在\]
</dt> <dd>

旗標停用或啟用 **DisableForcibleLogoff** 屬性，以決定是否可以強制登出登入主控台的系統管理員。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

停用屬性。 已連線的系統管理員可以強制登出。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

啟用屬性。 無法強制登出連線的系統管理員。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回成功;否則，會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 用戶端支援結束<br/>    | Windows Vista<br/>                                                                |
| 伺服器支援結束<br/>    | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

 





