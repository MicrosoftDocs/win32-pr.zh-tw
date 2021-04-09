---
description: 重新開機&\# 8194;WMI 類別方法會關閉電腦系統，然後重新開機它。
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別的重新開機方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936435"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a>Win32 作業系統類別的重新開機方法 \_

**重新開機** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會關閉電腦系統，然後重新開機它。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Reboot();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回零 (0) 表示成功。 任何其他數字表示發生錯誤。 如需錯誤碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**其他** (1 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

以程式設計方式重新開機電腦的能力，可讓系統管理員從遠端執行許多電腦管理工作。

例如，如果您建立腳本來安裝軟體或進行設定變更，而需要重新開機電腦，您可以在腳本中包含 restart 命令，並從遠端執行整個作業。 **重新** 啟動方法可以用來重新開機電腦。 如同 [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) 方法， **重新開機** 方法會要求腳本使用安全性認證的使用者擁有關機許可權。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會叫用 [**Win32 \_ 作業系統**](win32-operatingsystem.md) 類別的 Reboot 方法。

> [!Note]  
> 您必須具有 Shutdown 許可權，才能成功叫用關機方法。

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



下列 Perl 程式碼會叫用 [**Win32 \_ 作業系統**](win32-operatingsystem.md) 類別的重新開機方法。

> [!Note]  
> 您必須具有 Shutdown 許可權，才能成功叫用關機方法。

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
  if (!defined $RetVal || $RetVal != 0)
  {
   print Win32::OLE->LastError, "\n"; 
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



下列 VBScript 會在遠端系統上叫用 [**Win32 \_ 作業系統**](win32-operatingsystem.md) 類別的 Reboot 方法。 以 \_ \_ 要重新開機的遠端系統名稱填入遠端系統名稱。

> [!Note]  
> 您必須具有 RemoteShutdown 許可權，才能成功叫用重新開機方法

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



他遵循 Perl 會在遠端系統上叫用 [**Win32 \_ 作業系統**](win32-operatingsystem.md) 類別的 Reboot 方法。 以 \_ \_ 要重新開機的遠端系統名稱填入遠端系統名稱。

> [!Note]  
> 您必須具有 RemoteShutdown 許可權，才能成功叫用重新開機方法。

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
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

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ 作業系統**](win32-operatingsystem.md)
</dt> <dt>

[**CIM \_ 作業系統. Shutdown 方法**](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[WMI 工作：桌面管理](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

