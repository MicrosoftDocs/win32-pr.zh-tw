---
title: 'Session. Timeout 屬性 (WSManDisp .h) '
description: 設定並取得用戶端應用程式等候 Windows 遠端管理完成其作業的最大時間量（以毫秒為單位）。
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Timeout 屬性 Windows 遠端管理
- Timeout 屬性 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Timeout 屬性
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731e4f76ee890bc925a14b69c8ffb3d50e47406939b76183359021242a5fadc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743239"
---
# <a name="sessiontimeout-property"></a>Session. Timeout 屬性

設定並取得用戶端應用程式等候 Windows 遠端管理完成其作業的最大時間量（以毫秒為單位）。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Session.Timeout As long
```



## <a name="property-value"></a>屬性值

超時值（以毫秒為單位）。 當超過超時值時，就會發生執行階段錯誤。

## <a name="remarks"></a>備註

您可以在代理程式執行的每個作業之前設定超時值。 如果未指定超時值，代理程式會設定超時值。

在列舉作業期間，當列舉資源時，無法重設超時值。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會使用 WMI [**Win32 \_ process**](/windows/desktop/CIMWin32Prov/win32-process)類別的 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法來啟動 Calc.exe 進程。 *StrInputParameters* 參數包含 XML 格式的輸入參數。 腳本會指定會話的超時時間。


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**會話**](session.md)
</dt> </dl>

 

