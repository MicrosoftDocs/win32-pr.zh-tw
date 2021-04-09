---
description: Win32ShutdownTracker 方法提供 Win32 作業系統中的 Win32Shutdown 方法所支援的一組相同關機選項 \_ ，但是它也可讓您指定批註、關機原因或超時。
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Win32_OperatingSystem 類別的 Win32ShutdownTracker 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110216"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a>Win32 作業系統類別的 Win32ShutdownTracker 方法 \_

**Win32ShutdownTracker** 方法提供 [**Win32 \_ 作業系統**](win32-operatingsystem.md)中的 [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)方法所支援的一組相同關機選項，但是它也可讓您指定批註、關機原因或超時。

## <a name="syntax"></a>語法


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Timeout* \[在\]
</dt> <dd>

發生關機之前的時間（以秒為單位）。 預設值是 0 (零)。

</dd> <dt>

*批註* \[在\]
</dt> <dd>

要在 [關閉] 對話方塊中顯示的訊息，該對話方塊也會儲存為事件記錄檔專案中的批註。

</dd> <dt>

*ReasonCode* \[在\]
</dt> <dd>

初始關機的原因。

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

用來關閉電腦的一組點陣圖旗標。 若要強制執行命令，請將 Force 旗標 (4) 新增至命令值。 在遠端電腦上使用 Force 搭配關機或重新開機，會立即關閉所有 (包括 WMI、COM 等等) ，或重新開機遠端電腦。 這會產生不定的傳回值。

<dt>

0 (0x0) 
</dt> <dd>

登出

</dd> <dt>

4 (0x4) 
</dt> <dd>

強制登出 (0 + 4) 

</dd> <dt>

1 (0x1) 
</dt> <dd>

關機

</dd> <dt>

5 (0x5) 
</dt> <dd>

強制關機 (1 + 4) 

</dd> <dt>

2 (0x2) 
</dt> <dd>

重新啟動

</dd> <dt>

6 (0x6) 
</dt> <dd>

強制重新開機 (2 + 4) 

</dd> <dt>

8 (0x8) 
</dt> <dd>

關閉電源

</dd> <dt>

12 (0xC) 
</dt> <dd>

強制關機 (8 + 4) 

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

傳回零 (0) 表示成功。 任何其他數字表示發生錯誤。 如需錯誤碼，請參閱 [**WMI 錯誤常數**](../wmisdk/wmi-error-constants.md) 或 [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](../debug/system-error-codes.md)。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**其他** (1 – 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

呼叫進程必須具有 **SE \_ SHUTDOWN \_ 名稱** 許可權。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例說明如何呼叫 **Win32ShutdownTracker**。


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
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

[**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
