---
description: Create&\# 8194;WMI 類別方法會建立新的進程。
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Win32_Process 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42c675f61fc8b42790aeb811ec275554b355a392
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970320"
---
# <a name="create-method-of-the-win32_process-class"></a>Win32 進程類別的 Create 方法 \_

**建立** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會建立新的進程。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*命令列* \[在\]
</dt> <dd>

要執行的命令列。 系統會將 null 字元新增至命令列，並視需要修剪字串，以指出實際使用的檔案。

</dd> <dt>

*CurrentDirectory* \[在\]
</dt> <dd>

子進程的目前磁片磁碟機和目錄。 字串要求目前的目錄解析為已知的路徑。 使用者可以指定絕對路徑或相對於目前工作目錄的路徑。 如果這個參數為 **Null**，則新的進程會有與呼叫進程相同的路徑。 此選項主要是針對必須啟動應用程式，並指定應用程式初始磁片磁碟機和工作目錄的 shell 所提供。

</dd> <dt>

*ProcessStartupInformation* \[在\]
</dt> <dd>

Windows 進程的啟動設定。 如需詳細資訊，請參閱 [**Win32 \_ ProcessStartup**](win32-processstartup.md)。

</dd> <dt>

*ProcessId* \[擴展\]
</dt> <dd>

可以用來識別進程的全域處理序識別碼。 此值是從建立程式到進程結束之前的有效時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功建立進程，則傳回 0 (零) ，以及表示錯誤的其他任何數位。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功完成** (0) 
</dt> <dt>

**拒絕存取** (2) 
</dt> <dt>

**許可權不足** (3) 
</dt> <dt>

**未知的失敗** (8) 
</dt> <dt>

 (9) **找不到路徑**
</dt> <dt>

**不正確參數** (21) 
</dt> <dt>

**其他** (22 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

您可以建立 [**Win32 \_ ProcessStartup**](win32-processstartup.md) 類別的實例，以在呼叫這個方法之前設定處理常式。

如果要啟動的程式不在 Winmgmt.exe 的搜尋路徑中，就必須指定完整路徑。 如果新建立的進程嘗試與目標系統上的物件進行互動，但沒有適當的存取權限，它就會終止，而不會通知這個方法。

基於安全性理由， **Win32 \_ 進程** 無法使用 Create 方法從遠端啟動互動式進程。

使用 **Win32 \_ 進程** 建立的進程。除非指定了 **create \_ BREAKAWAY \_ FROM \_ job** 旗標，否則 create 方法會受到工作物件的限制。 如需詳細資訊，請參閱 [**Win32 \_ ProcessStartup**](win32-processstartup.md)和 [**\_ \_ ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration)。

## <a name="examples"></a>範例

下列 VBScript 範例示範如何叫用 CIM 方法，如同它是 SWbemObject 的自動化方法。


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



下列 Perl 範例示範如何叫用 CIM 方法，如同它是 SWbemObject 的自動化方法。


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



下列 VBScript 程式碼範例會在本機電腦上建立「記事本」處理常式。 [**Win32 \_ProcessStartup**](win32-processstartup.md) 用來設定處理常式設定。


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
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

[**Win32 \_ 進程**](win32-process.md)
</dt> <dt>

[WMI 工作：進程](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

