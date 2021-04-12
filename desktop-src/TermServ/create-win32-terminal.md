---
title: Win32_Terminal 類別的 Create 方法
description: 使用 Win32 TerminalSetting 類別的屬性和方法，建立具有預設設定的終端機，這些設定可以自訂 \_ 。
ms.assetid: 64c90695-72d4-42be-a37a-89b54c04a78c
ms.tgt_platform: multiple
keywords:
- 建立方法遠端桌面服務
- 建立方法遠端桌面服務、Win32_Terminal 類別
- Win32_Terminal 類別遠端桌面服務，Create 方法
topic_type:
- apiref
api_name:
- Win32_Terminal.Create
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f1edfa22893452f81cf4695a50380842fa5c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464592"
---
# <a name="create-method-of-the-win32_terminal-class"></a>Win32 終端機類別的 Create 方法 \_

**Create** 方法會建立具有預設設定的終端機，您可以使用 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)類別的屬性和方法來自訂這些設定。 函數會在成功時傳回零，並在失敗時傳回錯誤。

## <a name="syntax"></a>語法


```mof
uint32 Create(
  [in] string NewTerminalName,
  [in] string Transport,
  [in] string TerminalProtocol
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*NewTerminalName* \[在\]
</dt> <dd>

終端機的名稱。

</dd> <dt>

*傳輸* \[在\]
</dt> <dd>

終端機的傳輸。 這是 [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) 類別的屬性。

</dd> <dt>

*TerminalProtocol* \[在\]
</dt> <dd>

終端機的通訊協定。 這是 [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md) 類別的屬性。

</dd> </dl>

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

[**Win32 \_ 終端機**](win32-terminal.md)
</dt> </dl>

 

