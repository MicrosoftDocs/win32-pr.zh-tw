---
description: 要求將虛擬機器的狀態變更為指定的值。
ms.assetid: 87BE4C7D-604B-4F8D-B4DC-89BD563E3999
title: Msvm_ComputerSystem 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f3851d32b43bc7ebd170a1179ecda1e25f86e43ddaf819453a4af6998e2f7efc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014346"
---
# <a name="requeststatechange-method-of-the-msvm_computersystem-class"></a>Msvm it 類別的 RequestStateChange 方法 \_

要求將虛擬機器的狀態變更為指定的值。 多次叫用 **RequestStateChange** 方法可能會導致較早的要求被覆寫或遺失。 只有代表虛擬機器的 Msvm 同機類別 [**\_**](msvm-computersystem.md) 實例才支援這個方法。

當狀態變更正在進行時，會將 **requestedstate** 屬性變更為 *requestedstate* 參數的值。

## <a name="syntax"></a>語法


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RequestedState* \[在\]
</dt> <dd>

類型： **uint16**

新狀態。 大於32767的值為 **DMTF** 建議的值，可能會變更。

以下是可能的值：

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

對應至 [**CIM \_ EnabledLogicalElement。**](/previous-versions//cc136818(v=vs.85))

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**已啟用** (2) 


</dt> <dd>

對應至 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) = Enabled。

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** (3) 


</dt> <dd>

對應至 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) = Disabled。

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**關機** (4) 


</dt> <dd>

僅適用于第1版 (V1) 的 Hyper-v。 虛擬機器正在透過關機服務關閉。 對應至 [**CIM \_ EnabledLogicalElement。 EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown。

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**離線** (6) 


</dt> <dd>

對應至 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) = 已啟用但離線。

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**測試** (7) 


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**延** 後 (8) 


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**靜止** (9) 


</dt> <dd>

對應至 [**CIM \_ EnabledLogicalElement。 EnabledState**](/previous-versions//cc136818(v=vs.85)) = 靜止、已啟用但已暫停。

</dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**重新開機** (10) 


</dt> <dd>

狀態從 **Off** 轉換或 **儲存** 為 **執行中。**

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**重設** (11) 


</dt> <dd>

重設虛擬機器。 對應至 [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) = Reset。

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**正在儲存** (32773) 


</dt> <dd>

在第1版 (V1) 的 Hyper-v 中，對應于 **EnabledStateSaving**。

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**暫停** (32776) 


</dt> <dd>

在第1版 (V1) 的 Hyper-v 中，對應于 **EnabledStatePausing**。

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**繼續** (32777) 


</dt> <dd>

在第1版 (V1) 的 Hyper-v 中，對應于 **EnabledStateResuming**。 狀態從 **暫停****轉換成執行中。**

</dd> <dt>

<span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>

<span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779) 


</dt> <dd>

對應至 **EnabledStateFastSuspend**。

</dd> <dt>

<span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>

<span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780) 


</dt> <dd>

對應至 **EnabledStateFastSuspending**。 從執行到 **FastSaved****的狀態** 轉換。

</dd> </dl>

這些值代表重大狀態：

<dt>

<span id="RunningCritical"></span><span id="runningcritical"></span><span id="RUNNINGCRITICAL"></span>

**RunningCritical** (32781) 


</dt> <dd></dd> <dt>

<span id="OffCritical"></span><span id="offcritical"></span><span id="OFFCRITICAL"></span>

**OffCritical** (32782) 


</dt> <dd></dd> <dt>

<span id="StoppingCritical"></span><span id="stoppingcritical"></span><span id="STOPPINGCRITICAL"></span>

**StoppingCritical** (32783) 


</dt> <dd></dd> <dt>

<span id="SavedCritical"></span><span id="savedcritical"></span><span id="SAVEDCRITICAL"></span>

**SavedCritical** (32784) 


</dt> <dd></dd> <dt>

<span id="PausedCritical"></span><span id="pausedcritical"></span><span id="PAUSEDCRITICAL"></span>

**PausedCritical** (32785) 


</dt> <dd></dd> <dt>

<span id="StartingCritical"></span><span id="startingcritical"></span><span id="STARTINGCRITICAL"></span>

**StartingCritical** (32786) 


</dt> <dd></dd> <dt>

<span id="ResetCritical"></span><span id="resetcritical"></span><span id="RESETCRITICAL"></span>

**ResetCritical** (32787) 


</dt> <dd></dd> <dt>

<span id="SavingCritical"></span><span id="savingcritical"></span><span id="SAVINGCRITICAL"></span>

**SavingCritical** (32788) 


</dt> <dd></dd> <dt>

<span id="PausingCritical"></span><span id="pausingcritical"></span><span id="PAUSINGCRITICAL"></span>

**PausingCritical** (32789) 


</dt> <dd></dd> <dt>

<span id="ResumingCritical"></span><span id="resumingcritical"></span><span id="RESUMINGCRITICAL"></span>

**ResumingCritical** (32790) 


</dt> <dd></dd> <dt>

<span id="FastSavedCritical"></span><span id="fastsavedcritical"></span><span id="FASTSAVEDCRITICAL"></span>

**FastSavedCritical** (32791) 


</dt> <dd></dd> <dt>

<span id="FastSavingCritical"></span><span id="fastsavingcritical"></span><span id="FASTSAVINGCRITICAL"></span>

**FastSavingCritical** (32792) 


</dt> <dd></dd> </dl> </dd> <dt>

*作業* \[擴展\]
</dt> <dd>

類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

如果以非同步方式執行作業，則為所傳回之 [**Msvm \_ ConcreteJob**](msvm-concretejob.md) 物件的選擇性參考。 如果有，則會使用傳回的參考來監視進度，並取得方法的結果。

</dd> <dt>

*TimeoutPeriod* \[在\]
</dt> <dd>

類型： **datetime**

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個值。



| 傳回碼/值                                                                                                                                                                       | 描述                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**已完成，沒有錯誤**</dt> <dt>0</dt> </dl>                           | 成功。<br/>                                                                |
| <dl> <dt>**方法參數檢查-轉換已啟動**</dt> <dt>4096</dt> </dl> | 轉換是非同步。<br/>                                         |
| <dl> <dt>**拒絕存取**</dt> <dt>32769</dt> </dl>                                 | 拒絕存取。<br/>                                                          |
| <dl> <dt></dt><dt>32768</dt> </dl>                                                  |                                                                                    |
| <dl> <dt></dt><dt>32770</dt> </dl>                                                  |                                                                                    |
| <dl> <dt></dt><dt>32771</dt> </dl>                                                  |                                                                                    |
| <dl> <dt></dt><dt>32772</dt> </dl>                                                  |                                                                                    |
| <dl> <dt></dt><dt>32773</dt> </dl>                                                  |                                                                                    |
| <dl> <dt></dt><dt>32774</dt> </dl>                                                  |                                                                                    |
| <dl> <dt>**此操作的狀態無效**</dt> <dt>32775</dt> </dl>              | 不支援在 *RequestedState* 參數中指定的值。<br/> |
| <dl> <dt></dt><dt>32776</dt> </dl>                                                  |                                                                                    |
| <dl> <dt></dt><dt>32777</dt> </dl>                                                  |                                                                                    |
| <dl> <dt></dt><dt>32778</dt> </dl>                                                  |                                                                                    |



 

## <a name="remarks"></a>備註

UAC 篩選可能會限制對 Msvm 的 [未使用] 類別的存取。 [**\_**](msvm-computersystem.md) 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="examples"></a>範例

下列 c # 範例會啟動或停用虛擬機器。 您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。

> [!IMPORTANT]
> 若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    public class RequestStateChangeClass
    {
        public static void RequestStateChange(string vmName, string action)
        {
            ManagementScope scope = new ManagementScope(@"\\.\root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);

            if (null == vm)
            {
                throw new ArgumentException(
                    string.Format(
                    "The virtual machine '{0}' could not be found.", 
                    vmName));
            }

            ManagementBaseObject inParams = vm.GetMethodParameters("RequestStateChange");

            const int Enabled = 2;
            const int Disabled = 3;

            if (action.ToLower() == "start")
            {
                inParams["RequestedState"] = Enabled;
            }
            else if (action.ToLower() == "stop")
            {
                inParams["RequestedState"] = Disabled;
            }
            else
            {
                throw new Exception("Wrong action is specified");
            }

            ManagementBaseObject outParams = vm.InvokeMethod(
                "RequestStateChange", 
                inParams, 
                null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine(
                        "{0} state was changed successfully.", 
                        vmName);
                }
                else
                {
                    Console.WriteLine("Failed to change virtual system state");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine(
                    "{0} state was changed successfully.", 
                    vmName);
            }
            else
            {
                Console.WriteLine(
                    "Change virtual system state failed with error {0}", 
                    outParams["ReturnValue"]);
            }

        }

        public static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: <application> vmName action");
                Console.WriteLine("action: start|stop");
                return;
            }

            RequestStateChange(args[0], args[1]);
        }

    }
}
```



下列 Visual Basic 腳本撰寫版 (VBScript) 範例會啟動或停用虛擬機器。

> [!IMPORTANT]
> 若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。

 


```VB
dim objWMIService
dim fileSystem

const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const Enabled = 2
const Disabled = 3



Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    strComputer = "."
    set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       action = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript StartVM.vbs vmName start|stop"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)

    if RequestStateChange(computerSystem, action) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "RequestStateChange failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Turn on a virtual machine
'-----------------------------------------------------------------
Function RequestStateChange(computerSystem, action)
    WriteLog Format2("RequestStateChange({0}, {1})", computerSystem.ElementName, action)

    RequestStateChange = false
    set objInParam = computerSystem.Methods_("RequestStateChange").InParameters.SpawnInstance_()
    
    if action = "start" then
        objInParam.RequestedState = Enabled
    else
        objInParam.RequestedState = Disabled
    end if

    set objOutParams = computerSystem.ExecMethod_("RequestStateChange", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VM {0} was started successfully", computerSystem.ElementName)
            RequestStateChange = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)

    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        end if

    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    dim WMIJob

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting

        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState

    wend


    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\StartVM.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_**](msvm-computersystem.md)
</dt> </dl>

 

