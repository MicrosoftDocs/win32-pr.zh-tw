---
title: 'AtEndOfStream 屬性 (WSManDisp .h) '
description: 取得布林值，指出集合中是否有其他專案。
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- AtEndOfStream 屬性 Windows 遠端管理
- AtEndOfStream 屬性 Windows 遠端管理，列舉值物件
- 列舉值物件 Windows 遠端管理，AtEndOfStream 屬性
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1077837f82d650b57dfea0316ef15094b18749eefdb6957e62e6afd92cfe672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113199"
---
# <a name="enumeratoratendofstream-property"></a>AtEndOfStream 屬性

取得布林值，指出集合中是否有其他專案。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a>屬性值

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**真**


</dt> <dd>

集合中不再有任何專案。

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**假**


</dt> <dd>

有更多專案可供使用。

</dd> </dl>

## <a name="remarks"></a>備註

如果您在取得所需的所有資料之後釋放 [**列舉**](enumerator.md) 值物件，則會移除任何暫止的列舉要求。 如需詳細資訊，請參閱 [列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)。

## <a name="examples"></a>範例

下列 VBScript 範例會列舉作業系統實例。 請注意，釋出列舉物件會清除任何暫止的列舉要求。 DisplayOutput 副程式會以和 WinRM 工具相同的方式來格式化資料輸出。


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

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

[**列舉值**](enumerator.md)
</dt> <dt>

[列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





