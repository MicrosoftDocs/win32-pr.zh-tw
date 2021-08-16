---
description: 將電腦系統加入網域或工作組。
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Win32_ComputerSystem 類別的 JoinDomainOrWorkgroup 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9faf923cf6c771e95a7dfb4f0b04f896c54d79c6b5548e97850d867057b065b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834645"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Win32 JoinDomainOrWorkgroup 類別的方法 \_

**JoinDomainOrWorkgroup** 方法會將電腦系統加入網域或工作組。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

指定要加入的網域或工作組。 不可以是 **Null**。

</dd> <dt>

*密碼* \[在\]
</dt> <dd>

如果 *UserName* 參數指定帳戶名稱， *password* 參數必須指向連接到網域控制站時要使用的密碼。 否則，此參數必須為 **Null**。

</dd> <dt>

使用者 *名稱* \[在\]
</dt> <dd>

指向以 **null** 終止的常數位符串指標，指定連接到網域控制站時要使用的帳戶名稱。 必須指定網域 NetBIOS 名稱和使用者帳戶，例如網域 \\ 使用者。 如果此參數為 **Null**，則會使用呼叫端資訊。

您也可以在表單中使用使用者主體名稱 (UPPED) user@domain 。

</dd> <dt>

*AccountOU* \[在\]
</dt> <dd>

指定常數以 **null** 終止的字元字串指標，其中包含電腦帳戶 (OU) 之組織單位的 [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) 格式名稱。 如果您指定這個參數，字串就必須包含完整的路徑，否則 *輔色* 必須是 **Null**。

範例： "OU = testOU;DC = 網域;DC = 網域;DC = com "

</dd> <dt>

*Joindomainorworkgroup* \[在\]
</dt> <dd>

定義聯結選項的位旗標集合。

<dt>



  (0)


</dt> <dd>

預設值。 沒有聯結選項。

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP \_加入 \_ 網域** (0x00000001) 


</dt> <dd>

將電腦加入網域。 如果未指定此值，則會將電腦加入工作組。

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP \_\_建立** (0x00000002) 的帳戶


</dt> <dd>

在網域上建立帳戶。

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP \_ (\_** 0x00000010) 的 WIN9X 升級


</dt> <dd>

聯結作業會在升級過程中發生。

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP \_\_ \_ \_ 加入** (0x00000020 的網域聯結) 


</dt> <dd>

即使電腦已經加入網域，也允許加入新網域。

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP \_加入不 \_ 安全** 的 (0x00000040) 


</dt> <dd>

執行非安全性加入。

此選項會向預先建立的帳戶要求加入網域，而不需使用網域使用者認證進行驗證。 此選項可與 **NETSETUP \_ MACHINE \_ PWD \_ 傳遞** 的選項搭配使用。 在此情況下， *password* 是預先建立之電腦帳戶的密碼。

在 Windows Vista SP1 和 Windows Server 2008 之前，不安全的聯結不會驗證網域控制站。 所有通訊都是使用 null (未經驗證的) 會話來執行。 從 Windows Vista SP1 和 Windows Server 2008 開始，電腦帳戶名稱和密碼會用來驗證網域控制站。

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP \_電腦 \_ PWD 已 \_ 通過** (0x00000080) 


</dt> <dd>

指出 *password* 參數指定本機電腦帳戶密碼，而不是使用者密碼。 此旗標只適用于不安全的聯結，您也必須設定 NETSETUP 聯結不 \_ 安全旗標來指出此旗標 \_ 。

如果設定此旗標，則在聯結作業成功之後，如果該值為有效的電腦密碼，電腦密碼將會設定為 [ *密碼*] 的值。

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP \_延遲 \_ SPN \_ 設定** (0x00000100) 


</dt> <dd>

指出服務主體名稱 (SPN) ，而且電腦物件上的 DnsHostName 屬性目前不應更新。

一般而言，這些屬性會在聯結操作期間更新。 相反地，您應該在後續呼叫 [**重新命名**](rename-method-in-class-win32-computersystem.md) 方法時更新這些屬性。 在重新命名作業期間，一律會更新這些屬性。

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP \_加入 \_ DC \_ 帳戶** (0x00000200) 


</dt> <dd>

如果現有的帳戶是網域控制站，則允許加入網域。

> [!Note]  
> Windows Vista 和更新版本支援此旗標。

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP \_不明確的 \_ DC** (0x00001000) 


</dt> <dd>

加入網域時，請勿嘗試在登錄中設定慣用的網域控制站。

> [!Note]  
> Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP \_沒有 \_ NETLOGON \_** 快取 (0x00002000) 


</dt> <dd>

加入網域時，不要建立 Netlogon 快取。

> [!Note]  
> Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP \_不要 \_ 控制 \_ 服務** (0x00004000) 


</dt> <dd>

加入網域時，不會強制啟動 Netlogon 服務。

> [!Note]  
> Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP \_設定 \_ 電腦 \_ 名稱** (0x00008000) 


</dt> <dd>

加入網域以進行離線聯結時，請設定目的電腦主機名稱和 NetBIOS 名稱。

> [!Note]  
> Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP \_強制 \_ SPN \_ 設定** (0x00010000) 


</dt> <dd>

加入網域時，請在加入網域時覆寫其他設定，並將服務主體名稱設 (SPN) 。

> [!Note]  
> Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP \_沒有任何 (0x00020000 的 \_ 帳戶 \_ 重複使用**) 


</dt> <dd>

加入網域時，請勿重複使用現有的帳戶。

> [!Note]  
> Windows 7、Windows Server 2008 R2 及更新版本支援此旗標。

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP \_略過 \_ 不支援的 \_ 旗標** (0x10000000) 


</dt> <dd>

如果設定此位， **JoinDomainOrWorkgroup** 函式將會忽略無法辨識的旗標，且 [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) 的行為會如同未設定旗標。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

傳回 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)，此錯誤碼可能包含下列其中一個數值。 任何其他數字表示發生錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。

<dl> <dt>

「成功」
</dt> <dd>

0

</dd> <dt>

**5**
</dt> <dd>

存取遭到拒絕。

</dd> <dt>

**87**
</dt> <dd>

參數錯誤。

</dd> <dt>

**110**
</dt> <dd>

他的系統無法開啟指定的物件。

</dd> <dt>

**1323**
</dt> <dd>

無法更新密碼。

</dd> <dt>

**1326**
</dt> <dd>

登入失敗：未知的使用者名稱或密碼不正確。

</dd> <dt>

**1355**
</dt> <dd>

指定的網域可能不存在或無法連絡。

</dd> <dt>

**2224**
</dt> <dd>

帳戶已存在。

</dd> <dt>

**2691**
</dt> <dd>

電腦已加入網域。

</dd> <dt>

**2692**
</dt> <dd>

電腦目前未加入網域。

</dd> <dt>

**\_需要 WBEM E \_ 加密 \_ 連接 \_**
</dt> <dd>

0x80041087

已指定 *密碼* 和使用者 *名稱*，但驗證層級不是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權**。 若為 Visual Basic，則會傳回 **wbemErrEncryptedConnectionRequired** 。

</dd> <dt>

**其他**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>備註

當您將電腦從網域移到工作組時，必須先呼叫 [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) ，將電腦從網域 (移除，然後再呼叫這個方法，將工作組 (與 **JoinDomainOrWorkgroup**) 的呼叫聯結。 呼叫此方法之後，請重新開機受影響的電腦以套用變更。

使用者 *名稱* 和 *密碼* 可以保留 **null**。 不過，在 Visual Basic 的腳本或 **WbemAuthenticationLevelPktPrivacy** 中，對 WMI 的連線驗證必須是6，而且可以使用 [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library)程式庫的其他語言。 如需詳細資訊，請參閱 [使用 VBScript 設定預設進程安全性層級](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript)。

在 c + + 中，在 [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)、整個進程或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)中，針對 [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) proxy 的連接，設定 **RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 隱私權** 的驗證。 如需詳細資訊，請參閱 [使用 c + + 設定驗證](/windows/desktop/WmiSdk/setting-authentication-using-c-) 和 [設定 IWbemServices 和其他 proxy 的安全性](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies)。

## <a name="examples"></a>範例

將 [電腦加入網域](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell 範例會將電腦加入網域。

下列 VBScript 程式碼範例會將電腦加入網域，並在 Active Directory 中建立電腦的帳戶。


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 未進行**](win32-computersystem.md)
</dt> <dt>

[**UnjoinDomainOrWorkgroup 方法**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

