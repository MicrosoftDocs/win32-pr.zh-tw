---
description: GetOwner&\# 8194;WMI 類別方法會抓取執行進程的使用者名稱和功能變數名稱。
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Win32_Process 類別的 GetOwner 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110489"
---
# <a name="getowner-method-of-the-win32_process-class"></a>Win32 進程類別的 GetOwner 方法 \_

**GetOwner** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會抓取進程執行時所使用的使用者名稱和功能變數名稱。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*使用者* \[擴展\]
</dt> <dd>

傳回這個進程擁有者的使用者名稱。

</dd> <dt>

*網域* \[擴展\]
</dt> <dd>

傳回執行此進程所用的功能變數名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零 (0) 表示成功。 任何其他數字表示發生錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

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

## <a name="examples"></a>範例

[監視進程的 CPU Pct （依名稱與擁有者](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) ）VBScript 範例會收集 CPU 或處理器使用率百分比，並查閱進程擁有者。

所有 explorer.exe 進程的擁有者 [都會將使用者清單的「取得所有伺服器」記錄到](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell 範例 querys WMI。

下列 VBScript 程式碼範例會取得每個正在執行之進程的擁有者。


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
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

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ 進程**](win32-process.md)
</dt> </dl>

 

