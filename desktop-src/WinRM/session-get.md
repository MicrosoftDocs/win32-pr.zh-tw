---
title: Session (WSManDisp) 的 Get 方法
description: 抓取 URI 所指定的資源，並傳回目前資源實例的 XML 標記法。
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Get 方法 Windows 遠端管理
- Get 方法 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Get 方法
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c983c5f95ddfa3acc88b85b383ec85ddf85f885293031fe9bc4e4e07c90850a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642558"
---
# <a name="sessionget-method"></a>Session. Get 方法

抓取 [*URI*](windows-remote-management-glossary.md) 所指定的資源，並傳回目前資源實例的 XML 標記法。

## <a name="syntax"></a>語法


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*resourceUri* \[在\]
</dt> <dd>

要抓取之資源的識別碼。

此參數可包含下列其中一項：

-   具有或不含 [*選取器*](windows-remote-management-glossary.md)的 URI。 使用選取器來呼叫 **Get** 方法以取得 WMI 資源時，請使用物件的索引鍵屬性或屬性。 例如，在下列 Visual Basic 腳本撰寫版 (VBScript) 程式碼範例中，則是由指定索引鍵 `Win32_Service?Name=winmgmt` 。 針對單一類別（例如 [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)），您無法使用選取器。

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   可能包含選取器、[*片段*](windows-remote-management-glossary.md)或 [*選項*](windows-remote-management-glossary.md)的 [**ResourceLocator**](resourcelocator.md)物件。
-   [*Ws-addressing*](windows-remote-management-glossary.md)端點參考，如 WS-Management 通訊協定標準中所述。 如需 [WS-Management 通訊協定](ws-management-protocol.md)公用規格的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。

</dd> <dt>

*旗標* \[在中，選擇性\]
</dt> <dd>

保留的。 必須設定為 0。

</dd> </dl>

## <a name="return-value"></a>傳回值

資源的 XML 表示。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會抓取代表本機電腦上 WMI Winmgmt 服務之 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 實例的 XML 標記法。


```VB

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub

```



下列 VBScript 程式碼範例會從遠端電腦抓取 WMI Winmgmt 服務實例。 遠端電腦是以完整功能變數名稱 (servername.domain.com) 來識別。 本機和遠端版本之間唯一的差異是 [**CreateSession**](wsman-createsession.md)呼叫中的遠端電腦規格。


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
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

 

