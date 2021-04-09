---
description: Win32Shutdown &\# 8194;WMI 類別方法提供 Win32 作業系統所支援的一組完整關機選項。 這些包括登出、關機、重新開機，以及強制登出、關機或重新開機。
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別的 Win32Shutdown 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847517"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a>Win32 作業系統類別的 Win32Shutdown 方法 \_

**Win32Shutdown**   [WMI 類別](../wmisdk/retrieving-a-class.md)方法提供 Win32 作業系統所支援的一組完整關機選項。 這些包括登出、關機、重新開機，以及強制登出、關機或重新開機。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](../wmisdk/calling-a-method.md)。

## <a name="syntax"></a>語法


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

用來關閉電腦的一組點陣圖旗標。 若要強制執行命令，請將 Force 旗標 (4) 新增至命令值。 在遠端電腦上使用 Force 搭配關機或重新開機，會立即關閉所有 (包括 WMI、COM 等等) ，或重新開機遠端電腦。 這會產生不定的傳回值。

<dt>

0 (0x0) 
</dt> <dd>

**登出-登出** 電腦的使用者。 登出會停止所有與呼叫 exit 函式之進程的安全性內容相關聯的處理常式、將目前的使用者登出系統，並顯示 [登入] 對話方塊。

</dd> <dt>

4 (0x4) 
</dt> <dd>

**強制登出 (0 + 4)** -立即將使用者登出電腦，而且不會通知應用程式登入會話即將結束。 這可能會導致資料遺失。

</dd> <dt>

1 (0x1) 
</dt> <dd>

**關機** -將電腦關機至關閉電源的安全點。  (所有的檔案緩衝區都會排清至磁片，並停止所有執行中的處理常式。 ) 使用者會看到訊息， `It is now safe to turn off your computer.`

在關機期間，系統會將訊息傳送至每個執行中的應用程式。 應用程式會在處理訊息時執行任何清除，並傳回 True 以表示可以終止它們。

</dd> <dt>

5 (0x5) 
</dt> <dd>

**強制關機 (1 + 4)** -將電腦關閉，以關閉電源的安全點。  (所有的檔案緩衝區都會排清至磁片，並停止所有執行中的處理常式。 ) 使用者會看到訊息，` It is now safe to turn off your computer.`

使用強制關機方法時，所有服務（包括 WMI）都會立即關閉。 因此，如果您在遠端電腦上執行腳本，您將無法接收傳回值。

</dd> <dt>

2 (0x2) 
</dt> <dd>

**重新開機** -關機，然後重新開機電腦。

</dd> <dt>

6 (0x6) 
</dt> <dd>

**強制重新開機 (2 + 4)** -關閉然後重新開機電腦。

使用強制重新開機方法時，所有服務（包括 WMI）都會立即關閉。 因此，如果您在遠端電腦上執行腳本，您將無法接收傳回值。

</dd> <dt>

8 (0x8) 
</dt> <dd>

**關閉電腦電源** ，並關閉電源 (（如果有) 問題的電腦支援的話）。

</dd> <dt>

12 (0xC) 
</dt> <dd>

**強制關閉 (8 + 4)** -關閉電腦並關閉電源 (（如果有) 問題的電腦支援的話）。

使用強制關機方法時，所有服務（包括 WMI）都會立即關閉。 因此，如果您在遠端電腦上執行腳本，您將無法接收傳回值。

</dd> </dl> </dd> <dt>

*保留* \[在\]
</dt> <dd>

擴充 **Win32Shutdown** 的方法。 目前， *保留* 的參數會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零 (0) 表示成功。 任何其他數字表示發生錯誤。 如需錯誤碼，請參閱 [**WMI 錯誤常數**](../wmisdk/wmi-error-constants.md) 或 [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](../debug/system-error-codes.md)。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**其他** (1 – 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

若要更有效率地管理組織中的電腦，系統管理員必須能夠從遠端關機或重新開機電腦，或是從遠端登出使用者。 執行這些工作的能力可讓系統管理員安裝軟體、重新設定電腦設定、從網路移除電腦，以及執行其他工作，而不需要手動將每部電腦關機或重新開機。

例如，若要執行網路升級，您可能需要關閉在特定網路區段上執行的所有電腦。 若要強制群組原則升級，您需要將使用者登出其電腦。 如果您組織中的任何地方都有電腦病毒，您可能會想要盡可能關閉電腦的數量，然後才能讓病毒擴散。 關閉和重新開機電腦，並以程式設計方式（而不是手動）登出使用者的能力，可能是相當耗時的時間。

呼叫進程必須具有 **SE \_ SHUTDOWN \_ 名稱** 許可權。

[**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md)方法提供 [**Win32 \_ 作業系統**](win32-operatingsystem.md)中的 **Win32Shutdown** 方法所支援的一組相同關機選項，但是它也可讓您指定批註、關機原因或超時。

Win32Shutdown 方法沒有鎖定工作站的參數，讓使用者登入。 不過，您可以使用下列命令，從命令列鎖定工作站：

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a>範例

在 TechNet 資源庫上 [登出、重新開機或關機多部電腦](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) VBScript 範例會使用 Win32Shutdown 來登出、關機、重新開機或關閉 (，視伺服器陣列中列出的電腦) 選取專案而定。

TechNet 元件庫上的 [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell 範例包含一個方法，該方法會在遠端電腦上呼叫 Win32Shutdown。

下列 PowerShell 範例會使用 Win32Shutdown 方法來關閉指定的電腦。


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



下列 PowerShell 程式碼範例會使用 EnableAllPrivileges from >get-wmiobject Cmdlet 來完成適當的許可權。


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



下列 VB.NET 範例程式碼會使用 Shutdown 方法來重新開機或登出系統。


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
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

[作業系統類別](./operating-system-classes.md)
</dt> <dt>

[**Win32 \_ 作業系統**](win32-operatingsystem.md)
</dt> <dt>

[**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[WMI 工作：桌面管理](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[使用 VBScript 執行特殊許可權作業](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
