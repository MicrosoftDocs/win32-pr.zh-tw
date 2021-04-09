---
description: 從網域或工作組移除電腦系統。
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Win32_ComputerSystem 類別的 UnjoinDomainOrWorkgroup 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847532"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Win32 UnjoinDomainOrWorkgroup 類別的方法 \_

**UnjoinDomainOrWorkgroup** 方法會從網域或工作組移除電腦系統。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*密碼* \[在\]
</dt> <dd>

如果 *UserName* 參數指定帳戶名稱， *password* 參數必須指向連接到網域控制站時要使用的密碼。 否則，此參數必須為 **Null**。

> [!Note]  
> 連接到 IWbemServices 或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices)指標時，*密碼* 必須使用高驗證層級，而不是低於 **RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權**。 如果是本機到 Winmgmt，這就不是問題所在。

 

</dd> <dt>

使用者 *名稱* \[在\]
</dt> <dd>

指向以 null 終止的常數位符串指標，指定連接到網域控制站時要使用的帳戶名稱。 必須指定網域和使用者帳戶，例如「網域使用者」或「」 \\ user@domain 。 如果這個參數為 **Null**，則會使用呼叫端內容。

> [!Note]  
> 連線到 [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices)指標上的 Winmgmt 或 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)時，使用者 *名稱* 必須使用高驗證層級，而非小於 **RPC \_ C \_ 驗證 \_ 層級的 \_ PKT \_ 隱私權**。 如果是本機到 Winmgmt，這就不是問題所在。

 

</dd> <dt>

*FUnjoinOptions* \[在\]
</dt> <dd>

定義退出選項的位旗標集合。

<dt>



  (0)


</dt> <dd>

預設值。 沒有選項。

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP \_ (\_** 4) 的帳戶刪除


</dt> <dd>

在退出作業之後停用 Active Directory 帳戶，但不要刪除帳戶。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

**UnjoinDomainOrWorkgroup** 方法會在成功時傳回 0 (零) ，或不涉及任何選項時傳回。 任何其他值則表示錯誤。 如需錯誤碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**其他** (1 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

呼叫此方法之後，請重新開機受影響的電腦以套用變更。

## <a name="examples"></a>範例

[從網域退出電腦](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) VBScript 範例會從目前的網域 unjoins 本機電腦，並停用電腦帳戶。

[使用 VBS 腳本範例從網域退出電腦](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1)從網域 unjoins 指定的電腦。 .

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

[**JoinDomainOrWorkgroup 方法**](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

