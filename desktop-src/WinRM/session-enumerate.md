---
title: Session (WSManDisp) 的列舉方法
description: 列舉資料表、資料收集或記錄資源。
ms.assetid: ed8ad3ad-d033-45cb-b681-995c5f73b12e
ms.tgt_platform: multiple
keywords:
- 列舉方法 Windows 遠端管理
- 列舉方法 Windows 遠端管理，會話物件
- Session 物件 Windows 遠端管理，列舉方法
topic_type:
- apiref
api_name:
- Session.Enumerate
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc40a45cc28179acd8e5dc9fff17df8b8accddd8dffda3ea299571e11d46564
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642628"
---
# <a name="sessionenumerate-method"></a>Session. 列舉方法

列舉資料表、資料收集或記錄資源。 若要建立查詢，請在列舉中包含 *篩選* 參數和 *方言* 參數。 您也可以使用 [**ResourceLocator**](resourcelocator.md) 物件來建立查詢。 如需詳細資訊，請參閱 [列舉或列出資源的所有實例](enumerating-or-listing-all-instances-of-a-resource.md)。

## <a name="syntax"></a>語法


```VB
Session.Enumerate( _
  ByVal resourceUri, _
  [ ByVal filter ], _
  [ ByVal dialect ], _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*resourceUri* \[在\]
</dt> <dd>

要抓取之資源的識別碼。

此參數可包含下列其中一項：

-   資源的 URI。

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service"
    ```

    

-   [**ResourceLocator**](resourcelocator.md)物件。
-   [*Ws-addressing*](windows-remote-management-glossary.md)端點參考，如 WS-Management 通訊協定標準中所述。 如需 [WS-Management 通訊協定](ws-management-protocol.md)公用規格的詳細資訊，請參閱 [管理規格索引頁面](/previous-versions/dotnet/articles/ms951267(v=msdn.10))。

</dd> <dt>

*篩選* \[在中，選擇性\]
</dt> <dd>

定義列舉傳回資源中專案的篩選準則。 列舉資源時，只會傳回符合篩選準則的專案。 在列舉中包含 *篩選* 參數和 *方言* 參數，會將列舉轉換成查詢。 如需範例，請參閱 [查詢資源的特定實例](querying-for-specific-instances-of-a-resource.md)。

如果您有 *resourceURI* 參數的 [**ResourceLocator**](resourcelocator.md)物件，則不應使用此參數。

</dd> <dt>

*方言* \[在中，選擇性\]
</dt> <dd>

篩選所使用的語言。 [WQL](/windows/desktop/WmiSdk/wql-sql-for-wmi)是 WMI 使用的 SQL 子集，是唯一支援的語言。

如果您有 *resourceURI* 參數的 [**ResourceLocator**](resourcelocator.md)物件，則不應使用此參數。

</dd> <dt>

*旗標* \[在中，選擇性\]
</dt> <dd>

必須在 **\_ \_ WSManEnumFlags** 列舉中包含旗標的參數。 如需詳細資訊，請參閱 [列舉常數](enumeration-constants.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

列舉 [**值物件，**](enumerator.md) 包含列舉的結果。

## <a name="remarks"></a>備註

如需有關在列舉期間限制網路呼叫的詳細資訊，請參閱 [**BatchItems**](session-batchitems.md) 屬性。

請注意，如果旗標包含 [**列舉常數**](enumeration-constants.md) **WSManFlagHierarchyDeepBasePropsOnly** 或 **WSManFlagHierarchyShallow** ，則 Windows 遠端管理服務會傳回 **\_ \_ \_ \_ 不支援** 的錯誤錯誤碼錯誤的 WSMAN 多型模式。

如果指定了篩選，則它必須是與資源架構相關的有效檔。 方言參數是選擇性的。 但是，如果篩選字串的開頭是 <，但不是 XML 片段，則請在 *旗標* 參數中包含 *方言* 參數或設定 **WSManFlagNonXmlText** 旗標。 如需詳細資訊，請參閱 [**列舉常數**](enumeration-constants.md)。

對應的 c + + 方法是 [**iwsmansession.invoke：：列舉**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate)。

## <a name="examples"></a>範例

下列 VBScript 程式碼範例會列舉完整功能變數名稱所指定的遠端電腦上的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 實例 (servername.domain.com) 。 請注意，釋出列舉物件會清除暫止的列舉要求。 DisplayOutput 副程式使用 Winrm 命令列工具 XML 轉換檔 (WsmTxt. xsl) 以表格格式輸出資料。


```VB
Const RemoteComputer = "servername.domain.com"
Set objWsman = CreateObject( "WSMan.Automation" )

Set objSession = objWsman.CreateSession( "https://" & REMOTECOMPUTER )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_LogicalDisk"

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

[**會話**](session.md)
</dt> <dt>

[查詢資源的特定實例](querying-for-specific-instances-of-a-resource.md)
</dt> <dt>

[**BatchItems**](session-batchitems.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

