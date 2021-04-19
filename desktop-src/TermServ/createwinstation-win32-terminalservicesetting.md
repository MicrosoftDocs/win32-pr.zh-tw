---
title: Win32_TerminalServiceSetting 類別的 CreateWinstation 方法
description: 根據接聽程式名稱和 NIC 的唯一組合，建立新的接聽程式堆疊。
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- CreateWinstation 方法遠端桌面服務
- CreateWinstation 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，CreateWinstation 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 112237a00e9e92a2074ee0b95f9964d73f083e43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999601"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a>Win32 TerminalServiceSetting 類別的 CreateWinstation 方法 \_

**CreateWinstation** 方法會根據接聽程式名稱和 NIC 的唯一組合來建立新的接聽程式堆疊。

## <a name="syntax"></a>語法


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

接聽程式名稱。

</dd> <dt>

*WinstaDriverName* \[在\]
</dt> <dd>

Winstation 驅動程式名稱。

</dd> <dt>

*LanaId* \[在\]
</dt> <dd>

NIC 的 NetBIOS 局域網路介面卡 (LANA) 號碼。

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

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

