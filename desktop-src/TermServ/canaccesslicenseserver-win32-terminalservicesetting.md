---
title: Win32_TerminalServiceSetting 類別的 CanAccessLicenseServer 方法
description: CanAccessLicenseServer 已無法再使用。
ms.assetid: b09fa901-8ae1-431e-8d97-27ee84a84779
ms.tgt_platform: multiple
keywords:
- CanAccessLicenseServer 方法遠端桌面服務
- CanAccessLicenseServer 方法遠端桌面服務，Win32_TerminalServiceSetting 類別
- Win32_TerminalServiceSetting 類別遠端桌面服務，CanAccessLicenseServer 方法
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CanAccessLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa5bd0e108c0ccceed6890adedea7901834804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094123"
---
# <a name="canaccesslicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Win32 TerminalServiceSetting 類別的 CanAccessLicenseServer 方法 \_

\[**CanAccessLicenseServer** 不再適用于 Windows Server 2008 R2。\]

* * Windows Server 2008： * *

決定是否允許遠端桌面工作階段主機 (RD 工作階段主機) 伺服器根據下列內容，向遠端桌面授權伺服器要求遠端桌面服務的用戶端存取授權 (：

-   遠端桌面授權伺服器上的 [授權伺服器安全性群組] 群組原則設定。
-   授權伺服器上終端機伺服器電腦本機群組的成員資格。

## <a name="syntax"></a>語法


```mof
uint32 CanAccessLicenseServer(
  [in]  string ServerName,
  [out] uint32 AccessAllowed
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ServerName* \[在\]
</dt> <dd>

遠端桌面授權伺服器的名稱。

</dd> <dt>

*AccessAllowed* \[擴展\]
</dt> <dd>

是否允許 RD 工作階段主機伺服器向授權伺服器要求 RDS Cal。

<dt>

0
</dt> <dd>

允許要求。

</dd> <dt>

1
</dt> <dd>

不允許此要求。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

如果 RD 工作階段主機伺服器具有授權伺服器的存取權，則會傳回 **S \_ OK** 。 如果 RD 工作階段主機伺服器無法存取授權伺服器，則傳回 **\_ FALSE** 。

## <a name="remarks"></a>備註

[授權伺服器安全性群組] 原則設定可讓您指定允許與授權伺服器連線的 RD 工作階段主機伺服器取得 RDS Cal。 如果授權伺服器上已啟用此原則設定，授權伺服器將只會回應電腦帳戶是授權伺服器上終端機伺服器電腦本機群組成員之 RD 工作階段主機伺服器的 RDS CAL 要求。

若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。 針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。 針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。 下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



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

 

