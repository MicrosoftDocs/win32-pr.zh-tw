---
description: 最常呼叫的效能通常適用于大部分的情況。
ms.assetid: f665fc60-68bd-495d-a441-e3a9473f9d89
ms.tgt_platform: multiple
title: 在 VBScript 中設定非同步呼叫的安全性
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 972947e0cb4f5d385e4d2d27b7c14298771ac4e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994542"
---
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a>在 VBScript 中設定非同步呼叫的安全性

最 [*常呼叫的*](gloss-s.md) 效能通常適用于大部分的情況。 非同步呼叫通常不是腳本的建議作法。 但是，如果必須進行非同步呼叫，就可以將登錄值設定為強制 WMI 在非同步呼叫上執行存取檢查。


**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** 登錄值可控制當傳回非同步呼叫的資料時，WMI 是否會檢查是否有可接受的驗證層級。 回呼可在較低的驗證層級傳回，而不是原始的非同步呼叫。 依預設，此值設定為零，因此不會檢查回呼。 若要保護腳本中的非同步呼叫，您必須將登錄機碼設定為 1 (一個) 。

腳本可以使用登錄物件 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)的 [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)和 [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)方法來變更 **UnsecAppAccessControlDefault** 登錄值的設定。 如需遠端存取所需的驗證和模擬層級的詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。

## <a name="to-set-asynchronous-call-security-in-vbscript"></a>設定 VBScript 中的非同步呼叫安全性

下列 VBScript 程式碼範例說明如何變更登錄值，以控制回呼的 WMI 驗證。

腳本會將 **UnsecAppAccessControlDefault** 的值從零變更為1，如果值已設定，則會將值從1變更為零。 新安裝的系統上的預設值為零。 設定旗標之後，設定會在重新開機或 WMI 重新開機時持續保存。

腳本會使用 [**SWbemMethod. InParameters**](swbemmethod-inparameters.md) 物件，並 [**SWbemObject.ExeCMethod**](swbemobject-execmethod-.md) 來呼叫 [**StdRegProv. GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) 和 [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)。 如需有關設定 **InParameters** 物件中之值的詳細資訊，請參閱 [建立 InParameters 物件和剖析 OutParameters 物件](constructing-inparameters-objects-and-parsing-outparameters-objects.md)。 如需使用 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)進行登錄呼叫的範例，請參閱 [**StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)。


```VB
' Registry key value in hex
Const hklm = &h800000002  
' Subkey string 
Const Subkey = "software\\microsoft\\wbem\\cimom" 
' Asynchronous access control
Const sValueName = "UnsecAppAccessControlDefault" 

' Obtain registry object
Set objReg = GetObject("winmgmts:root\default:StdRegProv") 

' Get the initial value of the asynchronous 
'   access control registry key
' Use an InParameters object to set up the 
'   parameters for the ExecMethod call
' For more information see Constructing InParameters Objects 
'   topic and SWbemObject.ExecMethod_ topic

Set InParams = objReg.methods_("GetStringValue").InParameters.SpawnInstance_
InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName

' Get return value from OutParameters object returned by ExecMethod. 
' For more information see Parsing OutParameters Objects topic

Set OutParams = objReg.Execmethod_("GetStringValue",InParams)

If (OutParams.ReturnValue <> 0) then
   Wscript.Echo "GetStringValue returned " & OutParams.ReturnValue
   Wscript.Quit 1
End If

Svalue = OutParams.sValue
If (sValue = 0) Then
   AccessControl = "WMI not performing asynch access control"
Else 
   AccessControl = "WMI performing asynch access control"  
End If
Wscript.Echo sValueName & " = " _
    & sValue & VBNewLine & AccessControl

' Change asynchronous access control registry key value
Set InParams = objReg.methods_("SetStringValue").InParameters.SpawnInstance_

InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName
InParams.sValue = sValue XOR 1

Set OutParams = objReg.ExecMethod_("SetStringValue",InParams)

If (OutParams.Returnvalue <> 0) Then
    Wscript.Echo "SetStringValue returned " & OutParams.Returnvalue
    Wscript.Quit 1
End If

Wscript.Echo SValueName & " changed to " & (sValue XOR 1)
```



 

 
