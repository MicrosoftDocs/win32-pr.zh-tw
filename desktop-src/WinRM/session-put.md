---
title: Session (WSManDisp) 的 Put 方法
description: 更新資源。
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Put 方法 Windows 遠端管理
- Put 方法 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Put 方法
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4c6fc6123470f6633b77a1c51234e751f3be04044c0ad100f0017849cb1ac42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898688"
---
# <a name="sessionput-method"></a>Session. Put 方法

更新資源。

## <a name="syntax"></a>語法


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*resourceUri* \[在\]
</dt> <dd>

要更新之資源的識別碼。

此參數可包含下列清單中包含的其中一個元素：

-   具有或不含 [*選取器*](windows-remote-management-glossary.md)的 URI。 當呼叫 **Put** 方法來取得 WMI 資源時，請使用物件的索引鍵屬性（property）或屬性（property）。 例如，在下列 Visual Basic 腳本撰寫版 (VBScript) 程式碼範例中，則是由指定索引鍵 `Win32_Service?Name=winmgmt` 。

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   可能包含選取器、[*片段*](windows-remote-management-glossary.md)或 [*選項*](windows-remote-management-glossary.md)的 [**ResourceLocator**](resourcelocator.md)物件。
-   [*Ws-addressing*](windows-remote-management-glossary.md) 端點參考，如 [WS-Management 通訊協定](ws-management-protocol.md) standard 所述。 如需 WS-Management 通訊協定之公用規格的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。

</dd> <dt>

*資源* \[在\]
</dt> <dd>

更新的資源內容。

</dd> <dt>

*旗標* \[在中，選擇性\]
</dt> <dd>

保留的。 必須設定為 0。

</dd> </dl>

## <a name="return-value"></a>傳回值

包含已更新資源內容的 XML。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會將資料寫入 [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) 物件。 您必須在 *資源* 參數的 XML 中包含物件的所有非陣列屬性。 屬性的順序並不重要。


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

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
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

 

