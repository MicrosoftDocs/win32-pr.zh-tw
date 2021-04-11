---
title: 'ResourceLocator 物件 (WSManDisp) '
description: 提供資源的路徑。 您可以使用 ResourceLocator 物件，而不是會話物件作業中的資源 URI，例如 Session. Get、Session. Put 或 Session。列舉。
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- ResourceLocator 物件 Windows 遠端管理
- ResourceLocator 物件 Windows 遠端管理，說明
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094027"
---
# <a name="resourcelocator-object"></a>ResourceLocator 物件

提供資源路徑的物件。 您可以使用 **ResourceLocator** 物件，而不是 [**會話**](session.md)物件作業中的 [*資源 URI*](windows-remote-management-glossary.md) ，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。

此物件可讓您：

-   新增一或多個識別特定資源實例的 [*選取器*](windows-remote-management-glossary.md) 。 這與在使用金鑰的資源的資源 URI 中提供金鑰值相同。 如需詳細資訊，請參閱 [**ResourceLocator. AddSelector**](resourcelocator-addselector.md)。 您可以使用呼叫 [**Session. 列舉**](session-enumerate.md)中的 *filter* 參數來進行類似的作業。
-   指定 [*片段*](windows-remote-management-glossary.md) 路徑和方言，以只取得資源的一個屬性。 您也可以藉由提供陣列索引來指定陣列屬性的一個或所有元素。 如需詳細資訊，請參閱 [**ResourceLocator. FragmentPath**](resourcelocator-fragmentpath.md)。
-   加入一個或多個資料來源可能需要用來處理要求的 [*選項*](windows-remote-management-glossary.md) 。 如需詳細資訊，請參閱 [**ResourceLocator. AddOption**](resourcelocator-addoption.md)。

如需詳細資訊，請參閱 [查詢資源的特定實例](querying-for-specific-instances-of-a-resource.md)。

## <a name="members"></a>成員

**ResourceLocator** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ResourceLocator** 物件有這些方法。



| 方法                                                   | 描述                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**AddOption**](resourcelocator-addoption.md)           | 新增處理要求所需的其他資料。<br/>                                                                   |
| [**AddSelector**](resourcelocator-addselector.md)       | 將 [*選取器*](windows-remote-management-glossary.md) 加入至 **ResourceLocator** 物件。<br/>     |
| [**ClearOptions**](resourcelocator-clearoptions.md)     | 從 **ResourceLocator** 物件移除任何 [*選項*](windows-remote-management-glossary.md)。<br/> |
| [**ClearSelectors**](resourcelocator-clearselectors.md) | 從 **ResourceLocator** 物件移除所有選取器。<br/>                                                            |



 

### <a name="properties"></a>屬性

**ResourceLocator** 物件具有這些屬性。



| 屬性                                                                          | 存取類型           | Description                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FragmentDialect**](resourcelocator-fragmentdialect.md)<br/>             | 讀取/寫入<br/> | 取得或設定 [*資源*](windows-remote-management-glossary.md)[*片段*](windows-remote-management-glossary.md)的語言方言。<br/> |
| [**FragmentPath**](resourcelocator-fragmentpath.md)<br/>                   | 讀取/寫入<br/> | 取得或設定 [*資源*](windows-remote-management-glossary.md)[*片段*](windows-remote-management-glossary.md)或屬性的路徑。<br/> |
| [**MustUnderstandOptions**](resourcelocator-mustunderstandoptions.md)<br/> | 讀取/寫入<br/> | 取得或設定 **ResourceLocator** 物件的 **MustUnderstandOptions** 值。<br/>                                                                                                         |
| [**ResourceURI**](resourcelocator-resourceuri.md)<br/>                     | 讀取/寫入<br/> | 取得或設定 **ResourceLocator** 物件中的 [*資源 URI*](windows-remote-management-glossary.md) 。<br/>                                                          |



 

## <a name="remarks"></a>備註

**ResourceLocator** 物件會對應至 **IWSManResourceLocator** 介面。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會從特定的 [**Win32 \_ 處理器**](/windows/desktop/CIMWin32Prov/win32-processor)實例取得 **NumberOfLogicalProcessors** 和 **NumberOfCores** 屬性。


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

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
</dt> </dl>

 

