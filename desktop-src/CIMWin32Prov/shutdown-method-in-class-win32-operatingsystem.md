---
description: 關機&\# 8194;WMI 類別方法會卸載程式和 Dll，直到可以安全地關閉電腦為止。
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別的 Shutdown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 068551ee013634bde9a42584764c36f255bf322bedb97e6ebb3a5075c113e742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800838"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a>Win32 作業系統類別的 Shutdown 方法 \_

**關機** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會卸載程式和 dll，直到可以安全地關閉電腦為止。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Shutdown();
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

電腦偶爾需要從網路中移除，也許是為了進行排程維護，因為電腦無法正常運作，或是完成設定程式。 例如，如果 DHCP 伺服器將錯誤的 IP 位址送出，您可能會想要關閉電腦，直到可以分派服務技術人員來修正問題為止。 如果您懷疑發生安全性缺口，您可能需要關閉特定伺服器，以確保在安全性問題解決之前，無法存取這些伺服器。 某些設定作業 (例如變更電腦名稱稱) 需要您重新開機電腦，變更才會生效。

如果可能的話，這個方法會立即關閉電腦。 系統會停止所有執行中的進程，並將所有檔案緩衝區排清到磁片，然後關閉系統電源。 呼叫進程必須有 **SE \_ 關機 \_ 名稱** 許可權，如下列範例所述。


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



如需設定許可權的詳細資訊，請參閱使用 VBScript [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations) 和 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)。 如需其他關機選項（例如登出或強制關機），請參閱 [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) 方法。

## <a name="examples"></a>範例

下列 VBScript 程式碼會關閉本機電腦。

> [!Note]  
> 您必須具有 Shutdown 許可權，才能成功叫用關機方法。

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



下列 Perl 程式碼會關閉本機電腦。

> [!Note]  
> 您必須具有 Shutdown 許可權，才能成功叫用關機方法。

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
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



下列 VBScript 程式碼會關閉指定的遠端電腦。 以要關機的遠端系統名稱填入 [ *遠端 \_ 系統 \_ 名稱* ]。

> [!Note]  
> 您必須具有 RemoteShutdown 許可權，才能成功叫用 **關機** 方法。

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
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

[WMI 工作：桌面管理](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[使用 VBScript 執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

