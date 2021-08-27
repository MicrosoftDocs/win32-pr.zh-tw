---
title: Session (WSManDisp) 的 Create 方法
description: 建立資源的新實例，並傳回新物件 (EPR) 的端點參考。
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- 建立方法 Windows 遠端管理
- Create method Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，Create 方法
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97adac133adc4c636de395f564927a5f0194b3c52d50685ac034142e6c15aadf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823260"
---
# <a name="sessioncreate-method"></a>Session. Create 方法

建立資源的新實例，並傳回新物件 [*(EPR) 的端點參考*](windows-remote-management-glossary.md) 。

## <a name="syntax"></a>語法


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*resourceUri* \[在\]
</dt> <dd>

要建立之資源的識別碼。

此參數可包含下列其中一項：

-   具有一或多個 [*選取器*](windows-remote-management-glossary.md)的 URI。 請注意， [*WMI 外掛程式*](windows-remote-management-glossary.md) 不支援建立 [WS-Management 通訊協定](ws-management-protocol.md) 接聽程式以外的任何資源。
-   可能包含選取器、[*片段*](windows-remote-management-glossary.md)或 [*選項*](windows-remote-management-glossary.md)的 [**ResourceLocator**](resourcelocator.md)物件。
-   [*Ws-addressing*](windows-remote-management-glossary.md) 端點參考，如 WS-Management 通訊協定標準中所述。 如需 WS-Management 通訊協定之公用規格的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。

</dd> <dt>

*資源* 
</dt> <dd>

包含資源內容的 XML。

</dd> <dt>

*旗標* \[在中，選擇性\]
</dt> <dd>

保留的。 必須設定為 0。

</dd> </dl>

## <a name="return-value"></a>傳回值

新資源的 EPR。

## <a name="remarks"></a>備註

**Session。 Create** 只能用來建立資源的新實例。 使用 [**Session. Put**](session-put.md) 方法來更新資源的現有實例。 取得新的資源 URI 之後，您就可以呼叫 [**Session。 Get**](session-get.md) 會取得新的物件。 新物件包含資源提供者在建立新物件時所指派的任何屬性。 例如，如果您建立新的 [*WS-Management 通訊協定*](windows-remote-management-glossary.md) 接聽程式，並使用 **Session** 取出接聽程式物件，則您也會取得 **Port**、 **Enabled** 和 **ListeningOn** 屬性。

請注意， [*WMI 外掛程式*](windows-remote-management-glossary.md) 不支援建立 WS-Management 通訊協定接聽程式以外的任何資源。

下列語法用來呼叫這個方法。


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a>範例

下列 VBScript 程式碼範例會呼叫 **Session** ，在本機電腦上建立接聽程式。


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
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
</dt> <dt>

[WS-Management 通訊協定](ws-management-protocol.md)
</dt> </dl>

 

