---
title: 'Invoke 方法 (WSManDisp) '
description: 叫用方法並傳回方法呼叫的結果。
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Invoke 方法 Windows 遠端管理
- Invoke 方法 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Invoke 方法
topic_type:
- apiref
api_name:
- Session.Invoke
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117c688b616f377730524a09234b1dc38a4996c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686338"
---
# <a name="sessioninvoke-method"></a>Invoke 方法

叫用方法並傳回方法呼叫的結果。

## <a name="syntax"></a>語法


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*actionUri* \[在\]
</dt> <dd>

要叫用之方法的 URI。

</dd> <dt>

*resourceUri* \[在\]
</dt> <dd>

要取出的資源識別碼。

此參數可包含下列其中一項：

-   具有或不含 [*選取器*](windows-remote-management-glossary.md)的 URI。 在下列 Visual Basic Scripting Edition (VBScript) 範例中，是由指定索引鍵 `Win32_Service?Name=winmgmt` 。

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   可能包含選取器、[*片段*](windows-remote-management-glossary.md)或 [*選項*](windows-remote-management-glossary.md)的 [**ResourceLocator**](resourcelocator.md)物件。
-   [*Ws-addressing*](windows-remote-management-glossary.md) 端點參考，如 [WS-Management 通訊協定](ws-management-protocol.md) standard 所述。 如需 WS-Management 通訊協定之公用規格的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。

</dd> <dt>

*參數* \[在\]
</dt> <dd>

方法之輸入的 XML 表示。 必須提供這個字串，否則這個方法將會失敗。

</dd> <dt>

*旗標* \[在中，選擇性\]
</dt> <dd>

保留的。 必須設定為 0。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法輸出的 XML 標記法。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會啟動 Calc.exe 進程。 *StrInputParameters* 參數包含 XML 格式的輸入參數。 WMI [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)類別的 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法唯一必要的輸入參數是要執行的命令列。


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



下列 VBScript 程式碼範例會呼叫 **Session （Invoke** ）方法來執行 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)的 [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)方法。 **StopService** 方法沒有輸入參數。 不過， **Invoke** 方法需要 *parameters* 參數中的 XML 字串。


```VB
Option Explicit

Dim objWsman
Dim objSession
Dim strResponse
Dim strActionURI
Dim strInputXml
Dim strResourceURI
Dim strMethodName

set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession
strResourceURI = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=w32time"
strMethodName = "StopService"
strActionURI = strMethodName                                      

strInputXml = "<p:StopService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"

strResponse = objSession.Invoke(strMethodName, strResourceURI, strInputXml)

call DisplayOutput(strResponse)
 
strMethodName = "StartService" 
strActionURI = strResourceURI & "/" & strMethodName  
strInputXml = "<p:StartService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"
strResponse = objSession.Invoke(strMethodName, _
    strResourceURI, strInputXml)

call DisplayOutput(strResponse)

 
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
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**工作階段**](session.md)
</dt> </dl>

 

