---
title: Win32_TerminalServiceSetting 類別的 SetAllowTSConnections 方法
description: SetAllowTSConnections 方法會允許或拒絕新的遠端桌面連線。 這個方法會據以修改類別的 AllowTSConnections 屬性。
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- SetAllowTSConnections 方法遠端桌面服務
- SetAllowTSConnections 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，SetAllowTSConnections 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63f8e9be06a19599f578089fa979d7fd93a7bf457fcadf033ed0ab56fea4947f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127024"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a>Win32 TerminalServiceSetting 類別的 SetAllowTSConnections 方法 \_

**SetAllowTSConnections** 方法會允許或拒絕新的遠端桌面連線。 這個方法會據以修改類別的 **AllowTSConnections** 屬性。

## <a name="syntax"></a>語法


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AllowTSConnections* \[在\]
</dt> <dd>

指定是否允許新的遠端桌面連線。 這必須是下列值之一。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

不允許新的連接。 如果 *ModifyFirewallException* 參數為1，則會停用遠端桌面防火牆例外。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

允許新的連接。 如果 *ModifyFirewallException* 參數為1，則會啟用遠端桌面防火牆例外。

</dd> </dl> </dd> <dt>

*ModifyFirewallException* \[在\]
</dt> <dd>

指定是否要將遠端桌面的防火牆例外狀況設定修改為 *AllowTSConnections* 參數所指定的狀態。 這必須是下列值之一。

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

請勿修改防火牆例外狀況設定。

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

修改防火牆例外狀況設定。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回成功;否則，會傳回 WMI 錯誤碼。 如需這些值的清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md) 。 如果設定位於群組原則控制之下，則方法會傳回錯誤。

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

 

