---
title: '列舉值物件 (WSManDisp) '
description: 表示從作業傳回的結果資料流程，例如提取作業。
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- 列舉值物件 Windows 遠端管理
- 列舉值物件 Windows 遠端管理，描述
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025414"
---
# <a name="enumerator-object"></a>Enumerator 物件

表示從作業傳回的結果資料流程，例如提取作業。 例如， [**Session 列舉**](session-enumerate.md) 方法會傳回多個結果。

## <a name="members"></a>成員

**列舉** 值物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**列舉** 值物件具有這些方法。



| 方法                                  | 描述                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ReadItem**](enumerator-readitem.md) | 從資源抓取專案，並傳回專案的 XML 表示。<br/> |



 

### <a name="properties"></a>屬性

**列舉** 值物件具有這些屬性。



| 屬性                                                     | 描述                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AtEndOfStream**](enumerator-atendofstream.md)<br/> | 取得布林值，指出集合中是否有更多專案。<br/> |
| [**錯誤**](enumerator-error.md)<br/>                 | 取得其他錯誤資訊的 XML 表示。<br/>                         |



 

## <a name="remarks"></a>備註

若要啟動列舉，請使用 [**Session. 列舉**](session-enumerate.md)。 若要執行 [*WS-列舉：*](windows-remote-management-glossary.md)繼續讀取列舉中專案的 [*提取*](windows-remote-management-glossary.md)作業，請使用 [**ReadItem**](enumerator-readitem.md)。

**列舉** 值物件會對應至 [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)介面。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會列舉 (servername.domain.com) 的完整功能變數名稱所指定的遠端電腦上的所有磁片。 DisplayOutput 副程式會以和 WinRM 工具相同的方式來格式化資料輸出。


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
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
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WinRM 腳本 API](winrm-scripting-api.md)
</dt> <dt>

[列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Windows 遠端管理中的腳本](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





